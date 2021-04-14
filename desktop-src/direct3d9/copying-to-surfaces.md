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
# <a name="copying-to-surfaces-direct3d-9"></a>Копирование на поверхности (Direct3D 9)

При использовании [**IDirect3DDevice9:: упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)передайте прямоугольник на исходной поверхности или используйте **значение NULL** , чтобы указать всю поверхность. Вы также передаете точку на целевую поверхность, в которую копируется верхняя левая точка прямоугольника в исходном изображении. Этот метод не поддерживает отсечение. Операция завершится ошибкой, если исходный прямоугольник и соответствующий конечный прямоугольник не полностью содержатся в исходных и целевых поверхностях. Этот метод не поддерживает альфа-смешение, цветовые ключи и преобразование формата. Обратите внимание, что целевые и исходные поверхности должны быть разными.

Другие ограничения при использовании Упдатесурфаце см. в разделе [**IDirect3DDevice9:: упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

Следующие методы также доступны в C++/C для копирования изображений на поверхность Direct3D.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9:: Упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>Пример Упдатесурфаце

В следующем примере два прямоугольника копируются из исходной поверхности в конечную поверхность. Первый прямоугольник копируется из (0, 0, 50, 50) на исходную поверхность в то же место на поверхности назначения, а второй — из (50, 50, 100, 100) на исходной поверхности в область назначения (150, 150, 200, 200).


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Поверхности Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9:: Стретчрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
