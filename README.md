# CSS Fade
FadeIn and FadeOut with animation and transition

## Transition

### Visible
~~~~ css
.box {
  visibility: visible;
  opacity: 1;
  transition: opacity 0.25s;
}
~~~~

### Hidden
~~~~ css
.box {
  visibility: hidden;
  opacity: 0;
  transition: visibility 0s 0.2s, opacity 0.2s;
}
~~~~

## Animation

### FadeIn
~~~~ css
.box {
  animation-name: fadeIn;
  animation-duration: 0.5s;
}

@keyframes fadeIn {
  1% {
    position: absolute;
    top: -9999px;
    visibility: hidden;
    opacity: 0;
  }
  1.01% {
    visibility: hidden;
    opacity: 0;
  }
  100% {
    visibility: visible;
    opacity: 1;
  }
}
~~~~ 

### FadeOut
~~~~ css
.box {
  animation-name: fadeOut;
  animation-fill-mode: forwards;
  animation-duration: 0.5s;
}

@keyframes fadeOut {
  1% {
    visibility: visible;
    opacity: 1;
  }
  99.99% {
    visibility: hidden;
    opacity: 0;
  }
  100% {
    position: absolute;
    top: -9999px;
    visibility: hidden;
    opacity: 0;
  }
}
~~~~
