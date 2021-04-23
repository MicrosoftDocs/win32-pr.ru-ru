---
title: Мозаичные ресурсы. уровни компонентов
description: Direct3D 11,2 предоставляет поддержку мозаичных ресурсов на двух уровнях с использованием \_ значений уровня D3D11 мозаичных \_ ресурсов \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986230"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="56ff4-103">Мозаичные ресурсы. уровни компонентов</span><span class="sxs-lookup"><span data-stu-id="56ff4-103">Tiled resources features tiers</span></span>

<span data-ttu-id="56ff4-104">Direct3D 11,2 предоставляет поддержку мозаичных ресурсов на двух уровнях с использованием [**значений \_ \_ \_ уровня D3D11 мозаичных ресурсов**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="56ff4-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="56ff4-105">Чтобы запросить, поддерживает ли оборудование и драйвер мозаичное заполнение ресурсов и уровень уровня, передайте значение [**D3D11 \_ функции \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) параметру *Feature функции* [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="56ff4-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="56ff4-106">Кроме того, передайте указатель на [**структуру \_ D3D11 \_ данных \_ функции D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) в параметр *пфеатуресуппортдата* и передайте размер D3D11 **функции D3D11 \_ \_ \_ \_ OPTIONS1** структуры в параметр *феатуресуппортдатасизе* .</span><span class="sxs-lookup"><span data-stu-id="56ff4-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="56ff4-107">**Чеккфеатуресуппорт** возвращает уровень уровня в качестве значения [**\_ \_ \_ уровня ресурсов D3D11 мозаичного**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) элемента **тиледресаурцестиер** в **D3D11 \_ функции \_ \_ D3D11 \_ OPTIONS1**.</span><span class="sxs-lookup"><span data-stu-id="56ff4-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="56ff4-108">В этом разделе описываются эти два уровня.</span><span class="sxs-lookup"><span data-stu-id="56ff4-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="56ff4-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="56ff4-109">In this section</span></span>



| <span data-ttu-id="56ff4-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="56ff4-110">Topic</span></span>                           | <span data-ttu-id="56ff4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="56ff4-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="56ff4-112">Уровень 1</span><span class="sxs-lookup"><span data-stu-id="56ff4-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="56ff4-113">В этом разделе описывается поддержка 1-го уровня.</span><span class="sxs-lookup"><span data-stu-id="56ff4-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="56ff4-114">Уровень 2</span><span class="sxs-lookup"><span data-stu-id="56ff4-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="56ff4-115">В этом разделе описывается поддержка уровня 2.</span><span class="sxs-lookup"><span data-stu-id="56ff4-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="56ff4-116">См. также</span><span class="sxs-lookup"><span data-stu-id="56ff4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56ff4-117">Мозаичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56ff4-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





