---
title: Game Physics
layout: post
date: '2022-05-11 22:40:00 +0000'
background: /post_img/gamephysics/title.jpg
subtitle: Game physics implementation and tutorial
artist: artstation.com
---

![](https://img.shields.io/github/watchers/orangelie/orangelie.github.io.svg) ![](https://img.shields.io/badge/WritingInProgress-YES-green.svg)

**안녕하세요.**  
우리가 실제 현실세상이 아니더라도, 3d를 2d그래픽에 투영한 게임이든 일반적인 2d기반의 게임이든간에 대부분의 게임들은 각자만의 방식으로 구현된 물리법칙에 따라 오브젝트들의 위치를 실시간으로 계산합니다.  
  
우리는 이러한 게임속의 물리원리들을 간략하게 이해해보고, 이론을 위주로 구현하는방식을 통해 해당 튜토리얼을 진행할 생각입니다.  
  
시작하기 앞서서, 글쓴이는 해당 글을 정리하고 직접 레포지토리와 함께 개설했습니다.  
만약에 잘못된 정보나 고칠점이 존재한다고 생각하신다면 **gamedeveloppp@gmail.com**으로 연락부탁드립니다 !  
  <br>
> 사전에 알아두면 좋은 렌더링 기술: **DirectX9 DirectX11 DirectX12 Unity3D**

<br>
## 🎮 목차    
   
<span style='background-color: #fff5b1'>  
<a  href="#target1"> 충돌처리와 충돌반응 </a>  
  
<a  href="#target2">  질점 </a>   
</span>  
  <br>  
<a  name="target1">  </a>  
## ♣️ 충돌처리와 충돌반응  
만약에 우리가 아래와 같이 두개의 원이 있다고 가정할때, 두 원이 겹치는 조건은 어떻게 계산할 수 있을까요?  
절대로 복잡하게 계산하는것이아니며, 또한 계산량이 많아서도 안됩니다.  
![circle_collision](/post_img/gamephysics/circle_collision.png)  

절대로 복잡하게 계산하는것이아니며, 또한 계산량이 많아서도 안됩니다. 
$$
f(x)=ax^2+bx+c\\ (테스트용수식)
g(x)=Ax^4
$$

<a  name="target2">  </a>
## ♣️ 질점
