---
title: Поведение средства программной прорисовки с несопоставленными плитками
description: В этом разделе описывается поведение растеризации несопоставленных плиток.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996774"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="f48b7-103">Поведение средства программной прорисовки с несопоставленными плитками</span><span class="sxs-lookup"><span data-stu-id="f48b7-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="f48b7-104">В этом разделе описывается поведение растеризации несопоставленных плиток.</span><span class="sxs-lookup"><span data-stu-id="f48b7-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="f48b7-105">DepthStencilView</span><span class="sxs-lookup"><span data-stu-id="f48b7-105">DepthStencilView</span></span>

<span data-ttu-id="f48b7-106">Поведение операций чтения и записи представления трафарета глубины (DSV) зависит от уровня поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="f48b7-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="f48b7-107">Сведения о разбиении требований см. в разделе Общее поведение операций чтения и записи для [мозаичных ресурсов](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="f48b7-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="f48b7-108">Ниже описывается идеальное поведение.</span><span class="sxs-lookup"><span data-stu-id="f48b7-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="f48b7-109">Если плитка не сопоставлена в представлении DepthStencilView, возвращаемое значение чтения глубины (0) передается любым операциям, настроенным для чтения значения глубины.</span><span class="sxs-lookup"><span data-stu-id="f48b7-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="f48b7-110">Операции записи в плитку с отсутствующей глубиной отклоняются.</span><span class="sxs-lookup"><span data-stu-id="f48b7-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="f48b7-111">Такое идеальное определение обработки записи не требуется для [второго уровня](tier-2.md). Операции записи в несопоставленные плитки могут оказаться в кэше, откуда данные могут взять последующие операции чтения.</span><span class="sxs-lookup"><span data-stu-id="f48b7-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="f48b7-112">RenderTargetView</span><span class="sxs-lookup"><span data-stu-id="f48b7-112">RenderTargetView</span></span>

<span data-ttu-id="f48b7-113">Поведение операций чтения и записи представления целевого объекта отрисовки (RTV) зависит от уровня поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="f48b7-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="f48b7-114">Сведения о разбиении требований см. в разделе Общее поведение операций чтения и записи для [мозаичных ресурсов](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="f48b7-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="f48b7-115">Во всех реализациях различные представления RTV (и DSV), привязанные одновременно, могут содержать разные сопоставленные или несопоставленные области и могут использовать различные форматы поверхностей (т. е. разные формы плиток).</span><span class="sxs-lookup"><span data-stu-id="f48b7-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="f48b7-116">Ниже описывается идеальное поведение.</span><span class="sxs-lookup"><span data-stu-id="f48b7-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="f48b7-117">Операции чтения из RTV возвращают значение 0 для отсутствующих плиток, а операции записи отклоняются.</span><span class="sxs-lookup"><span data-stu-id="f48b7-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="f48b7-118">Такое идеальное определение обработки записи не требуется для [второго уровня](tier-2.md). Операции записи в несопоставленные плитки могут оказаться в кэше, откуда данные могут взять последующие операции чтения.</span><span class="sxs-lookup"><span data-stu-id="f48b7-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f48b7-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f48b7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f48b7-120">Доступ конвейера к мозаичным ресурсам</span><span class="sxs-lookup"><span data-stu-id="f48b7-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




