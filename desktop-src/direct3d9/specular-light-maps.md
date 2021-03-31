---
description: При освещении светового источника «блестящие» объекты — те, которые используют самые отражающие материалы — это отраженные блики.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Карты отраженного освещения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894630"
---
# <a name="specular-light-maps-direct3d-9"></a><span data-ttu-id="c8347-103">Карты отраженного освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c8347-103">Specular Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="c8347-104">При освещении светового источника «блестящие» объекты — те, которые используют самые отражающие материалы — это отраженные блики.</span><span class="sxs-lookup"><span data-stu-id="c8347-104">When illuminated by a light source, shiny objects - those that use highly reflective materials - receive specular highlights.</span></span> <span data-ttu-id="c8347-105">В некоторых случаях отраженные света, созданные модулем освещения, неточны.</span><span class="sxs-lookup"><span data-stu-id="c8347-105">In some cases, the specular highlights produced by the lighting module is not accurate.</span></span> <span data-ttu-id="c8347-106">Чтобы получить более привлекательный цвет, многие приложения Direct3D применяют отраженные схемы к примитивам.</span><span class="sxs-lookup"><span data-stu-id="c8347-106">To produce a more appealing highlight, many Direct3D applications apply specular light maps to primitives.</span></span>

<span data-ttu-id="c8347-107">Для сопоставления отраженного света, добавьте карту отраженного света к текстуре примитива, затем смодулируйте (умножьте результат на) картой света RGB- цвета.</span><span class="sxs-lookup"><span data-stu-id="c8347-107">To perform specular light mapping, add the specular light map to the primitive's texture, then modulate (multiply the result by) the RGB light map.</span></span>

<span data-ttu-id="c8347-108">В следующем примере кода показан этот процесс в C++.</span><span class="sxs-lookup"><span data-stu-id="c8347-108">The following code example illustrates this process in C++.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a><span data-ttu-id="c8347-109">См. также</span><span class="sxs-lookup"><span data-stu-id="c8347-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8347-110">Светлое сопоставление с текстурами</span><span class="sxs-lookup"><span data-stu-id="c8347-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



