---
description: В этом разделе показано, как добавить кадры и анимации в простой куб.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Добавление кадров и анимации (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710692"
---
# <a name="adding-frames-and-animations-direct3d-9"></a>Добавление кадров и анимации (Direct3D 9)

В этом разделе показано, как добавить кадры и анимации в простой куб.

## <a name="working-with-frames"></a>Работа с кадрами

Ожидается, что фрейм примет следующую структуру.


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



Поместите определенную сетку Куба внутрь фрейма с помощью преобразования Identity. Затем примените анимацию к этому кадру.


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a>Работа с анимациями

Анимация определяется набором ключей. Ключ — это значение времени, связанное с операцией масштабирования, ориентацией или позицией.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



Затем анимации группируются в Аниматионсетс:


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



Теперь возьмите куб с помощью анимации.


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



Дополнительные сведения см. в статье [](animation.md) шаблоны анимации [**и анимации.**](animationset.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[X-файлы (прежние версии)](x-files--legacy-.md)
</dt> </dl>

 

 



