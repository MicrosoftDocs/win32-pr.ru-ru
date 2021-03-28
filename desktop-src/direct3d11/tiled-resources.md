---
title: Мозаичные ресурсы
description: Мозаичные ресурсы можно рассматривать как крупные логические ресурсы, использующие небольшие объемы физической памяти.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887784"
---
# <a name="tiled-resources"></a><span data-ttu-id="2e5d9-103">Мозаичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e5d9-103">Tiled resources</span></span>

<span data-ttu-id="2e5d9-104">Мозаичные ресурсы можно рассматривать как крупные логические ресурсы, использующие небольшие объемы физической памяти.</span><span class="sxs-lookup"><span data-stu-id="2e5d9-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="2e5d9-105">В этом разделе описывается, зачем требуются мозаичные ресурсы и как создаются и используются мозаичные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2e5d9-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e5d9-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2e5d9-106">In this section</span></span>



| <span data-ttu-id="2e5d9-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="2e5d9-107">Topic</span></span>                                                                                   | <span data-ttu-id="2e5d9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2e5d9-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e5d9-109">Зачем нужны мозаичные ресурсы?</span><span class="sxs-lookup"><span data-stu-id="2e5d9-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="2e5d9-110">Требуется выполнить мозаичное выделение ресурсов, так что память с графическим процессором не тратится на хранение областей поверхностей, к которым известно приложение, и оборудование может понять, как выполнять фильтрацию по смежным плиткам.</span><span class="sxs-lookup"><span data-stu-id="2e5d9-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="2e5d9-111">Создание мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="2e5d9-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="2e5d9-112">Ресурсы мозаичного заполнения создаются путем указания флага D3D11 ресурса с назначением [**\_ \_ \_ мозаики**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) при создании ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e5d9-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="2e5d9-113">API-интерфейсы мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="2e5d9-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="2e5d9-114">Интерфейсы API, описанные в этом разделе, работают с мозаичными ресурсами и пулом плиток.</span><span class="sxs-lookup"><span data-stu-id="2e5d9-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="2e5d9-115">Доступ конвейера к мозаичным ресурсам</span><span class="sxs-lookup"><span data-stu-id="2e5d9-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="2e5d9-116">Ресурсы мозаичного заполнения можно использовать в представлениях ресурсов шейдера (SRV), представлениях целевого объекта отрисовки (РТВ), представления трафарета глубины (DSV) и неупорядоченных представлениях доступа (UAV), а также в некоторых точках привязки, где не используются представления, например привязки буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="2e5d9-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="2e5d9-117">Мозаичные ресурсы. уровни компонентов</span><span class="sxs-lookup"><span data-stu-id="2e5d9-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="2e5d9-118">Direct3D 11,2 предоставляет поддержку мозаичных ресурсов на двух уровнях с использованием [**значений \_ \_ \_ уровня D3D11 мозаичных ресурсов**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="2e5d9-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="2e5d9-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2e5d9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e5d9-120">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e5d9-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





