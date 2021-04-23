---
description: 'При использовании IDirect3DDevice9:: Упдатесурфаце передайте прямоугольник на исходной поверхности или используйте значение NULL, чтобы указать всю поверхность.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Копирование на поверхности (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496632"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="3ff99-103">Копирование на поверхности (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3ff99-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="3ff99-104">При использовании [**IDirect3DDevice9:: упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)передайте прямоугольник на исходной поверхности или используйте **значение NULL** , чтобы указать всю поверхность.</span><span class="sxs-lookup"><span data-stu-id="3ff99-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="3ff99-105">Вы также передаете точку на целевую поверхность, в которую копируется верхняя левая точка прямоугольника в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="3ff99-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="3ff99-106">Этот метод не поддерживает отсечение.</span><span class="sxs-lookup"><span data-stu-id="3ff99-106">This method does not support clipping.</span></span> <span data-ttu-id="3ff99-107">Операция завершится ошибкой, если исходный прямоугольник и соответствующий конечный прямоугольник не полностью содержатся в исходных и целевых поверхностях.</span><span class="sxs-lookup"><span data-stu-id="3ff99-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="3ff99-108">Этот метод не поддерживает альфа-смешение, цветовые ключи и преобразование формата.</span><span class="sxs-lookup"><span data-stu-id="3ff99-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="3ff99-109">Обратите внимание, что целевые и исходные поверхности должны быть разными.</span><span class="sxs-lookup"><span data-stu-id="3ff99-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="3ff99-110">Другие ограничения при использовании Упдатесурфаце см. в разделе [**IDirect3DDevice9:: упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span><span class="sxs-lookup"><span data-stu-id="3ff99-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="3ff99-111">Следующие методы также доступны в C++/C для копирования изображений на поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3ff99-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="3ff99-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="3ff99-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="3ff99-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="3ff99-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="3ff99-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="3ff99-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="3ff99-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="3ff99-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="3ff99-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="3ff99-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="3ff99-117">**IDirect3DDevice9:: Упдатесурфаце**</span><span class="sxs-lookup"><span data-stu-id="3ff99-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="3ff99-118">Пример Упдатесурфаце</span><span class="sxs-lookup"><span data-stu-id="3ff99-118">UpdateSurface Example</span></span>

<span data-ttu-id="3ff99-119">В следующем примере два прямоугольника копируются из исходной поверхности в конечную поверхность.</span><span class="sxs-lookup"><span data-stu-id="3ff99-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="3ff99-120">Первый прямоугольник копируется из (0, 0, 50, 50) на исходную поверхность в то же место на поверхности назначения, а второй — из (50, 50, 100, 100) на исходной поверхности в область назначения (150, 150, 200, 200).</span><span class="sxs-lookup"><span data-stu-id="3ff99-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="3ff99-121">См. также</span><span class="sxs-lookup"><span data-stu-id="3ff99-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ff99-122">Поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="3ff99-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="3ff99-123">**IDirect3DDevice9:: Стретчрект**</span><span class="sxs-lookup"><span data-stu-id="3ff99-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
