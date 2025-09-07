---
layout: post
title:  "Solving Poisson's Equation Numerically"
date:   2025-09-15 
author: defwin
tags: [physics, analysis, partial differential equation, numerical method]
---

## Introduction

푸아송 방정식은 다음 형태의 편미분방정식을 뜻합니다.

$$\displaystyle \nabla^2 \Phi(\vec{x}) = \rho(\vec{x})$$

푸아송 방정식은 여러 문제에서 자주 등장하게 됩니다. 특히 전자기학에서 굉장히 중요한 방정식인데, 대표적으로 가우스 법칙이 정확히 푸아송 방정식의 꼴을 가집니다. 자기장의 경우에도 전기장이 시간에 대해 불변인 상황을 가정하면 벡터 퍼텐셜의 라플라시안이 전류밀도에 비례하게 되어 푸아송 방정식 꼴이 됩니다. 뉴턴 중력 문제 역시 가우스의 법칙으로 생각할 수 있으므로 푸아송 방정식이라고 볼 수 있습니다. 푸아송 방정식은 확산 방정식에도 응용할 수 있는데, 확산 방정식은 우변이 위치에 대한 함수가 아니라 $\Phi$에 대한 시간 미분 꼴이 들어가는 방정식으로, 푸아송 방정식의 풀이에 약간의 변형을 가하면 풀 수 있습니다. 

푸아송 방정식은 또한 해가 존재하고 유일함이 보장되어 굉장히 '좋은' 방정식입니다.
