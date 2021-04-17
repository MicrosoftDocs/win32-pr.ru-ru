---
title: Использование прямоугольников (Windows Media Player SDK)
description: Использование прямоугольников
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- визуализации, прямоугольники
- Пользовательские визуализации, прямоугольники
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- Функция Render, прямоугольники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105701015"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="0c60b-108">Использование прямоугольников (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="0c60b-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="0c60b-109">Прямоугольники используются для указания прямоугольных областей в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0c60b-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="0c60b-110">В окне можно создать множество прямоугольников, но проигрыватель Windows Media предоставляет значения одного прямоугольника с помощью функции [ивмпеффектс:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) .</span><span class="sxs-lookup"><span data-stu-id="0c60b-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="0c60b-111">Если подключаемый модуль визуализируется с помощью окна, прямоугольник является клиентской областью окна.</span><span class="sxs-lookup"><span data-stu-id="0c60b-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="0c60b-112">Это называется прямоугольником КНР и определяет прямоугольник, который проигрыватель Windows Media будет отображать для визуализации.</span><span class="sxs-lookup"><span data-stu-id="0c60b-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="0c60b-113">Часто используйте этот параметр, чтобы не выходить за пределы прямоугольника, предоставляемого проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c60b-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="0c60b-114">Прямоугольник имеет четыре значения, определяющие его.</span><span class="sxs-lookup"><span data-stu-id="0c60b-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="0c60b-115">Они отображаются слева, сверху, справа и снизу.</span><span class="sxs-lookup"><span data-stu-id="0c60b-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="0c60b-116">Верхний левый угол прямоугольника определяется левым и верхним, а нижний и правый угол прямоугольника определяется снизу и справа.</span><span class="sxs-lookup"><span data-stu-id="0c60b-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="0c60b-117">Используйте следующий код, чтобы получить экстенты рисования прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0c60b-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="0c60b-118">Это необходимо сделать, так как пользователь может изменить размер окна и вы хотите, чтобы вы всегда рисулись в той области, которую пользователь может видеть.</span><span class="sxs-lookup"><span data-stu-id="0c60b-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="0c60b-119">Например, для рисования слева направо в верхней части окна используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="0c60b-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="0c60b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0c60b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c60b-121">**Реализация отрисовки**</span><span class="sxs-lookup"><span data-stu-id="0c60b-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




