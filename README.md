# CSSだけで任意のテキストにタイピングアニメーション
タイプライターのようなエフェクトを任意のテキストに与えます。  

[via : Typewriter animation pure CSS](https://codepen.io/thiagoteles/pen/ogoxLw "Typewriter animation pure CSS")

~~~CSS
.line-1{/*対象のテキスト*/
    position: relative;
    top: 50%;  
    width: 24em;
    margin: 0 auto;
    border-right: 2px solid rgba(255,255,255,.75);
    font-size: 180%;
    text-align: center;
    white-space: nowrap;
    overflow: hidden;
    transform: translateY(-50%);    
}


.anim-typewriter{/*アニメーションセッティング*/
  animation: typewriter 4s steps(44) 1s 1 normal both,
 blinkTextCursor 500ms steps(44) infinite normal;
}
@keyframes typewriter{/*タイプライターライクなアニメーション*/
  from{width: 0;}
  to{width: 24em;}
}
@keyframes blinkTextCursor{/*点滅するカーソルのアニメーション*/
  from{border-right-color: rgba(255,255,255,.75);}
  to{border-right-color: transparent;}
}
~~~
