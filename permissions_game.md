---
title: File Permissions Game
layout: default
previous: interactive_games
---

<!-- x_ -->

<script src="js/perms.min.js"></script>
<script>
    var field, guess, button, result, hint, everything;

    function generate() {
        var num = Math.floor(Math.random() * 4095)
        var oct = pad(num.toString(8));
        field.innerHTML = Perms.toString(oct);
    }

    function click() {
        var txt = guess.value;
        if (txt.length === 3) txt = '0' + txt;

        var s;
        if (Perms.toString(txt) === field.innerHTML) {
            s = 'Correct!';
        } else {
            s = 'Sorry, try again';
        }
        result.innerHTML = '<h3>' + s + '</h3>';
    }

    function givehint() {
        var s = field.innerHTML;
        var m = Perms.toMode(s);
        result.innerHTML = '<code>' + s + '</code> converted to octal is <code>' + m + '</code>';
    }

    function pad(s) {
      for (var i = s.length; i < 4; ++i) {
        s = '0' + s;
      }
      return s;
    }

    function vieweverything() {
        var s = '<ul>';
        for (var i = 0; i <= 4095; i++) {
            var j = pad(i.toString(8));
            s += '<li><code>' + j + '</code> :: <code>' + Perms.toString(j) + '</code></li>';
        }
        result.innerHTML = s;
    }

    function init() {
        field = document.getElementById('permissions-field');
        guess = document.getElementById('permissions-guess');
        button = document.getElementById('permissions-button');
        result = document.getElementById('permissions-result');
        refresh = document.getElementById('permissions-refresh');
        hint = document.getElementById('permissions-hint');
        everything = document.getElementById('permissions-everything');

        button.onclick = click;
        refresh.onclick = generate;
        hint.onclick = givehint;
        everything.onclick = vieweverything;
        field.onkeydown = function(e) { if (e.keyCode === 13) button.onclick(); };
        field.focus();
        generate();
    }

    window.onload = init;
</script>

Convert <code><span id="permissions-field"></span></code> to octal
<input type="text" id="permissions-guess"></input>
<button id="permissions-button">check</button>
<button id="permissions-hint">answer</button>
<button id="permissions-refresh">refresh</button>
<br />
<span id="permissions-result"></span>
<br /><br />
<button id="permissions-everything">view everything</button>
