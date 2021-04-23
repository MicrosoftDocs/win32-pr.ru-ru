---
description: Приложение обычно визуализирует трехмерные сцены более реалистично, если в нем используются цветные карты. Карта цветного света использует данные RGB на карте света для получения информации об освещении.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Карты цветового освещения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496134"
---
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="d93d2-104">Карты цветового освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d93d2-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="d93d2-105">Приложение обычно визуализирует трехмерные сцены более реалистично, если в нем используются цветные карты.</span><span class="sxs-lookup"><span data-stu-id="d93d2-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="d93d2-106">Карта цветного света использует данные RGB на карте света для получения информации об освещении.</span><span class="sxs-lookup"><span data-stu-id="d93d2-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="d93d2-107">В следующем примере кода C++ показано освещение с помощью цветовых данных RGB.</span><span class="sxs-lookup"><span data-stu-id="d93d2-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



<span data-ttu-id="d93d2-108">В этом примере в качестве первой текстуры устанавливается Текстурная схема.</span><span class="sxs-lookup"><span data-stu-id="d93d2-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="d93d2-109">Затем он устанавливает состояние первого этапа смешивания для модуляции входящих данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="d93d2-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="d93d2-110">В нем используется первая текстура и текущий цвет примитива в качестве аргументов для операции модуляции.</span><span class="sxs-lookup"><span data-stu-id="d93d2-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d93d2-111">См. также</span><span class="sxs-lookup"><span data-stu-id="d93d2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d93d2-112">Светлое сопоставление с текстурами</span><span class="sxs-lookup"><span data-stu-id="d93d2-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



