---
description: Некоторые старые платы ускорения трехмерной графики не поддерживают наложение текстуры с помощью альфа-значения пикселя назначения.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Монохромные карты светлого цвета (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691976"
---
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="260ed-103">Монохромные карты светлого цвета (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="260ed-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="260ed-104">Некоторые старые платы ускорения трехмерной графики не поддерживают наложение текстуры с помощью альфа-значения пикселя назначения.</span><span class="sxs-lookup"><span data-stu-id="260ed-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="260ed-105">Дополнительные сведения см. в разделе [смешение текстур Alpha (Direct3D 9)](alpha-texture-blending.md) .</span><span class="sxs-lookup"><span data-stu-id="260ed-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="260ed-106">Эти адаптеры также обычно не поддерживают множественное наложение текстуры.</span><span class="sxs-lookup"><span data-stu-id="260ed-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="260ed-107">Если ваше приложение работает на подобном адаптере, оно может использовать многопроходное наложение текстуры для сопоставления монохромного освещения.</span><span class="sxs-lookup"><span data-stu-id="260ed-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="260ed-108">Для сопоставления монохромного освещения приложение сохраняет сведения об освещении в данных альфа-канала его текстур карты освещения.</span><span class="sxs-lookup"><span data-stu-id="260ed-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="260ed-109">Приложение использует возможности Direct3D по фильтрации текстур для сопоставления каждого пикселя в изображении примитива соответствующему текселю на карте освещения.</span><span class="sxs-lookup"><span data-stu-id="260ed-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="260ed-110">Это устанавливает коэффициент наложения источника равным альфа-значению соответствующего текселя.</span><span class="sxs-lookup"><span data-stu-id="260ed-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="260ed-111">В следующем примере показано, как приложение может использовать текстуру в качестве монохромной схемы освещения.</span><span class="sxs-lookup"><span data-stu-id="260ed-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



<span data-ttu-id="260ed-112">Так как адаптеры отображения, которые не поддерживают альфа-смешение назначения, обычно не поддерживают несколько смешений текстур, в этом примере в качестве первой текстуры устанавливается Текстурная карта, доступная на всех многотрехмерных картах ускорителя.</span><span class="sxs-lookup"><span data-stu-id="260ed-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="260ed-113">Образец кода задает цветовую операцию для этапа смешения текстур для смешения данных текстуры с существующим цветом примитива.</span><span class="sxs-lookup"><span data-stu-id="260ed-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="260ed-114">Затем в качестве входных данных выбирается первая текстура и существующий цвет примитива.</span><span class="sxs-lookup"><span data-stu-id="260ed-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="260ed-115">См. также</span><span class="sxs-lookup"><span data-stu-id="260ed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="260ed-116">Светлое сопоставление с текстурами</span><span class="sxs-lookup"><span data-stu-id="260ed-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



