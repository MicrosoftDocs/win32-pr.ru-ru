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
# <a name="adding-frames-and-animations-direct3d-9"></a><span data-ttu-id="dbd33-103">Добавление кадров и анимации (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dbd33-103">Adding Frames and Animations (Direct3D 9)</span></span>

<span data-ttu-id="dbd33-104">В этом разделе показано, как добавить кадры и анимации в простой куб.</span><span class="sxs-lookup"><span data-stu-id="dbd33-104">This section shows how to add frames and animations to a simple cube.</span></span>

## <a name="working-with-frames"></a><span data-ttu-id="dbd33-105">Работа с кадрами</span><span class="sxs-lookup"><span data-stu-id="dbd33-105">Working with Frames</span></span>

<span data-ttu-id="dbd33-106">Ожидается, что фрейм примет следующую структуру.</span><span class="sxs-lookup"><span data-stu-id="dbd33-106">A frame is expected to take the following structure.</span></span>


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



<span data-ttu-id="dbd33-107">Поместите определенную сетку Куба внутрь фрейма с помощью преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="dbd33-107">Place the defined cube mesh inside a frame with an identity transform.</span></span> <span data-ttu-id="dbd33-108">Затем примените анимацию к этому кадру.</span><span class="sxs-lookup"><span data-stu-id="dbd33-108">Then apply an animation to this frame.</span></span>


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



## <a name="working-with-animations"></a><span data-ttu-id="dbd33-109">Работа с анимациями</span><span class="sxs-lookup"><span data-stu-id="dbd33-109">Working with Animations</span></span>

<span data-ttu-id="dbd33-110">Анимация определяется набором ключей.</span><span class="sxs-lookup"><span data-stu-id="dbd33-110">An animation is defined by a set of keys.</span></span> <span data-ttu-id="dbd33-111">Ключ — это значение времени, связанное с операцией масштабирования, ориентацией или позицией.</span><span class="sxs-lookup"><span data-stu-id="dbd33-111">A key is a time value associated with a scaling operation, an orientation, or a position.</span></span>


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



<span data-ttu-id="dbd33-112">Затем анимации группируются в Аниматионсетс:</span><span class="sxs-lookup"><span data-stu-id="dbd33-112">Animations are then grouped into AnimationSets:</span></span>


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



<span data-ttu-id="dbd33-113">Теперь возьмите куб с помощью анимации.</span><span class="sxs-lookup"><span data-stu-id="dbd33-113">Now take the cube through an animation.</span></span>


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



<span data-ttu-id="dbd33-114">Дополнительные сведения см. в статье [](animation.md) шаблоны анимации [**и анимации.**](animationset.md)</span><span class="sxs-lookup"><span data-stu-id="dbd33-114">For more information, see the [**Animation**](animation.md) and [**AnimationSet**](animationset.md) templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbd33-115">См. также</span><span class="sxs-lookup"><span data-stu-id="dbd33-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbd33-116">X-файлы (прежние версии)</span><span class="sxs-lookup"><span data-stu-id="dbd33-116">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



