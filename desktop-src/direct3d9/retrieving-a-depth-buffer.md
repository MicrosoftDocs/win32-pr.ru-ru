---
description: 'В следующем примере кода показано, как использовать метод IDirect3DDevice9:: ЖетдепсстенЦилсурфаце для получения указателя на поверхность буфера глубины, принадлежащую устройству.'
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: Получение буфера глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae914b8506fd0c4169f0cfec0d78d7c3bd9b9d61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140418"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a><span data-ttu-id="f6ff2-103">Получение буфера глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f6ff2-103">Retrieving a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="f6ff2-104">В следующем примере кода показано, как использовать метод [**IDirect3DDevice9:: жетдепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) для получения указателя на поверхность буфера глубины, принадлежащую устройству.</span><span class="sxs-lookup"><span data-stu-id="f6ff2-104">The following code example shows how to use the [**IDirect3DDevice9::GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) method to retrieve a pointer to the depth-buffer surface owned by the device.</span></span>


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a><span data-ttu-id="f6ff2-105">См. также</span><span class="sxs-lookup"><span data-stu-id="f6ff2-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6ff2-106">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="f6ff2-106">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
