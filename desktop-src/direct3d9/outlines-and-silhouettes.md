---
description: Буфер трафарета можно использовать и для более абстрактных эффектов, таких как создание структур и силуэтов.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Контуры и Силхауеттес (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805302"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a><span data-ttu-id="53c09-103">Контуры и Силхауеттес (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="53c09-103">Outlines and Silhouettes (Direct3D 9)</span></span>

<span data-ttu-id="53c09-104">Буфер трафарета можно использовать и для более абстрактных эффектов, таких как создание структур и силуэтов.</span><span class="sxs-lookup"><span data-stu-id="53c09-104">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="53c09-105">Если приложение применит к изображению примитива маску трафарета той же формы но чуть меньшего размера, то итоговое изображение будет содержать только контур примитива.</span><span class="sxs-lookup"><span data-stu-id="53c09-105">If your application applies a stencil mask to the image of a primitive that is the same shape but slightly smaller, the resulting image contains only the primitive's outline.</span></span> <span data-ttu-id="53c09-106">Затем приложение может заполнить замаскированную трафаретом область изображения сплошным цветом, создавая для примитива эффект приподнятости.</span><span class="sxs-lookup"><span data-stu-id="53c09-106">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="53c09-107">Если маска трафарета имеет те же размеры и форму, что и примитив, который вы отрисовываете, на полученном изображении на месте примитива будет отверстие.</span><span class="sxs-lookup"><span data-stu-id="53c09-107">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="53c09-108">Затем приложение может заполнить это отверстие черным, создавая силуэт примитива.</span><span class="sxs-lookup"><span data-stu-id="53c09-108">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53c09-109">См. также</span><span class="sxs-lookup"><span data-stu-id="53c09-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c09-110">Методы буфера шаблона</span><span class="sxs-lookup"><span data-stu-id="53c09-110">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



