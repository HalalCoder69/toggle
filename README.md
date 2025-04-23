 * {

    margin: 0;
    padding: 0;

}

body {
    display: flex;
    justify-content: right;
    align-items: right;
    min-height: 100vh;
    background: #2b2b2b;
    overflow-x: hidden;
    overflow-y: hidden;
}

label {
    width: 30px;
    height: 90px;
    padding: 0;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
}
input{
    position: absolute;
    opacity: 0;
}
.sun{
    position: absolute;
    font-size: 2em;
    color: #666;
    filter: drop-shadow(0 0 2px rgba(0,0,0, .5));
    transform: scale(0);
    transition: .5s ease;
}
input:checked~.sun{
    transition-delay: .3s;
    transform:  scale(1) rotate(360deg);
}
.moon{
    font-size: 2em;
    color: #666;
    filter: drop-shadow(0 0 2px rgba(0,0,0, .5));
    transition: .5s ease;
    transition-delay: .3s;
}
input:checked~.moon{
    transition-delay: 0s;
    transform: rotate(360deg) scale(0);
}
.toggle {
    position:absolute;
    display: block;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    box-shadow:
    inset 0 8px 60px rgba(0,0,0, .1),
    inset 0 8px 60px rgba(0,0,0, .1),
    inset 0 8px 60px rgba(0,0,0, .1);
    z-index: -1;
    transition: 1s;
}
input:checked~.toggle {
    background: #f8f8f8;
}
.animateBg{
    position: absolute;
    width: 200%;
    height: 200%;
    background: #ffffff;
    z-index: -2;
    clip-path: circle(0% at 50% 50%);
    transition: 1.5s ease-out;
}

input:checked~.animateBg {
    clip-path: circle(150% at 50% 50%);
}

