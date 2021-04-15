---
description: При освещении с помощью источника света для матовых поверхностей отображается рассеянный световой отражение.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: Рассеянные световые карты (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab6a85fb93bc1ebcc15735431c1d54be4482a1f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494910"
---
# <a name="diffuse-light-maps-direct3d-9"></a><span data-ttu-id="f5a56-103">Рассеянные световые карты (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f5a56-103">Diffuse Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="f5a56-104">При освещении с помощью источника света для матовых поверхностей отображается рассеянный световой отражение.</span><span class="sxs-lookup"><span data-stu-id="f5a56-104">When illuminated by a light source, matte surfaces display diffuse light reflection.</span></span> <span data-ttu-id="f5a56-105">Яркость рассеянного света зависит от расстояния до источника света и угла между нормалью поверхности и вектором направленности источника света.</span><span class="sxs-lookup"><span data-stu-id="f5a56-105">The brightness of diffuse light depends on the distance from the light source and the angle between the surface normal and the light source direction vector.</span></span> <span data-ttu-id="f5a56-106">Эффекты рассеянного света, моделируемые с помощью расчетов освещения, обеспечивают создание лишь общих эффектов.</span><span class="sxs-lookup"><span data-stu-id="f5a56-106">The diffuse lighting effects simulated by lighting calculations produce only general effects.</span></span>

<span data-ttu-id="f5a56-107">Ваше приложение может моделировать более сложный рассеянный свет с использованием карт освещения для текстур.</span><span class="sxs-lookup"><span data-stu-id="f5a56-107">Your application can simulate more complex diffuse lighting with texture light maps.</span></span> <span data-ttu-id="f5a56-108">Для этого добавьте карту рассеянного освещения в базовую текстуру, как показано в следующем примере кода C++.</span><span class="sxs-lookup"><span data-stu-id="f5a56-108">Do this by adding the diffuse light map to the base texture, as shown in the following C++ code example.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a><span data-ttu-id="f5a56-109">См. также</span><span class="sxs-lookup"><span data-stu-id="f5a56-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5a56-110">Светлое сопоставление с текстурами</span><span class="sxs-lookup"><span data-stu-id="f5a56-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



