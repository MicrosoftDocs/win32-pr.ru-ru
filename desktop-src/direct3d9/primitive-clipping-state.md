---
description: Примитивы, которые находятся частично внутри (или полностью вне) представления фрустум, можно обрезать таким образом, чтобы отображалась только видимая часть примитива.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Отсеченное состояние примитива (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423153"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="20db7-103">Отсеченное состояние примитива (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="20db7-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="20db7-104">Примитивы, которые находятся частично внутри (или полностью вне) [представления фрустум](viewports-and-clipping.md) , можно обрезать таким образом, чтобы отображалась только видимая часть примитива.</span><span class="sxs-lookup"><span data-stu-id="20db7-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="20db7-105">Обрезка сокращает объем работы, который выполняется только для тех примитивов или частей примитива, которые будут видимы.</span><span class="sxs-lookup"><span data-stu-id="20db7-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="20db7-106">Чтобы использовать конвейер для обрезки, установите для \_ состояния прорисовки D3DRS обрезки значение **true** (по умолчанию), чтобы включить обрезку, или **false** , чтобы отключить вырезание Direct3D.</span><span class="sxs-lookup"><span data-stu-id="20db7-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20db7-107">См. также</span><span class="sxs-lookup"><span data-stu-id="20db7-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20db7-108">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="20db7-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



