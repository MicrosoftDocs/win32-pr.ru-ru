---
description: 'Состояния визуализации устройства влияют на поведение почти каждой части конвейера. Состояния отрисовки задаются путем вызова IDirect3DDevice9:: Сетрендерстате.'
ms.assetid: 8ed8a2c3-f88e-427a-9b92-dc244dd453c9
title: Состояния отрисовки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0531aacedd4029eb39eb29ef777c9c9b09767b7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494265"
---
# <a name="render-states-direct3d-9"></a><span data-ttu-id="05f65-104">Состояния отрисовки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-104">Render States (Direct3D 9)</span></span>

<span data-ttu-id="05f65-105">Состояния визуализации устройства влияют на поведение почти каждой части конвейера.</span><span class="sxs-lookup"><span data-stu-id="05f65-105">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="05f65-106">Состояния отрисовки задаются путем вызова [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="05f65-106">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="05f65-107">Дополнительные сведения содержатся в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="05f65-107">Additional information is contained in the following topics:</span></span>

-   [<span data-ttu-id="05f65-108">Альфа-смешение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-108">Alpha Blending State (Direct3D 9)</span></span>](alpha-blending-state.md)
-   [<span data-ttu-id="05f65-109">Состояние тестирования Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-109">Alpha Testing State (Direct3D 9)</span></span>](alpha-testing-state.md)
-   [<span data-ttu-id="05f65-110">Состояние окружающего освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-110">Ambient Lighting State (Direct3D 9)</span></span>](ambient-lighting-state.md)
-   [<span data-ttu-id="05f65-111">Состояние сглаживания (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-111">Antialiasing State (Direct3D 9)</span></span>](antialiasing-state.md)
-   [<span data-ttu-id="05f65-112">Состояние отбора (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-112">Culling State (Direct3D 9)</span></span>](culling-state.md)
-   [<span data-ttu-id="05f65-113">Состояние буферизации глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-113">Depth Buffering State (Direct3D 9)</span></span>](depth-buffering-state.md)
-   [<span data-ttu-id="05f65-114">Состояние тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-114">Fog State (Direct3D 9)</span></span>](fog-state.md)
-   [<span data-ttu-id="05f65-115">Состояние освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-115">Lighting State (Direct3D 9)</span></span>](lighting-state.md)
-   [<span data-ttu-id="05f65-116">Состояние структуры и заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-116">Outline and Fill State (Direct3D 9)</span></span>](outline-and-fill-state.md)
-   [<span data-ttu-id="05f65-117">Состояние цвета для вершины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-117">Per-Vertex Color State (Direct3D 9)</span></span>](per-vertex-color-state.md)
-   [<span data-ttu-id="05f65-118">Отсеченное состояние примитива (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-118">Primitive Clipping State (Direct3D 9)</span></span>](primitive-clipping-state.md)
-   [<span data-ttu-id="05f65-119">Состояние заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-119">Shading State (Direct3D 9)</span></span>](shading-state.md)
-   [<span data-ttu-id="05f65-120">Состояние буфера набора элементов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-120">Stencil Buffer State (Direct3D 9)</span></span>](stencil-buffer-state.md)
-   [<span data-ttu-id="05f65-121">Состояние переноса текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05f65-121">Texture Wrapping State (Direct3D 9)</span></span>](texture-wrapping-state.md)

## <a name="related-topics"></a><span data-ttu-id="05f65-122">См. также</span><span class="sxs-lookup"><span data-stu-id="05f65-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05f65-123">Состояния</span><span class="sxs-lookup"><span data-stu-id="05f65-123">States</span></span>](states.md)
</dt> </dl>

 

 
