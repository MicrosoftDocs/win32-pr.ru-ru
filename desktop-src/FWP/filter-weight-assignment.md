---
title: Назначение весов фильтрам
description: Каждый фильтр в платформе фильтрации Windows (WFP) имеет соответствующий вес, который используется во время арбитража фильтра.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/26/2020
ms.locfileid: "104412711"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="3dd44-103">Назначение весов фильтрам</span><span class="sxs-lookup"><span data-stu-id="3dd44-103">Filter Weight Assignment</span></span>

<span data-ttu-id="3dd44-104">Каждый фильтр в платформе фильтрации Windows (WFP) имеет соответствующий вес, который используется во время [арбитража фильтра](filter-arbitration.md).</span><span class="sxs-lookup"><span data-stu-id="3dd44-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="3dd44-105">Вес фильтра, используемый модулем базовой фильтрации (BFE), имеет тип [**\_ UINT64 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="3dd44-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="3dd44-106">При добавлении фильтров вызывающие объекты имеют три варианта.</span><span class="sxs-lookup"><span data-stu-id="3dd44-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="3dd44-107">Задайте вес в виде [**\_ UINT64 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="3dd44-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="3dd44-108">В BFE используется указанный весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="3dd44-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="3dd44-109">Задайте для параметра вес значение [**FWP \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="3dd44-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="3dd44-110">BFE автоматически создает вес в диапазоне от \[ 0 до 2 ⁶ ⁰).</span><span class="sxs-lookup"><span data-stu-id="3dd44-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="3dd44-111">Задайте вес [**FWP \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) в диапазоне от \[ 0 до 15 \] .</span><span class="sxs-lookup"><span data-stu-id="3dd44-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="3dd44-112">В BFE в качестве идентификатора диапазона веса используется указанный вес.</span><span class="sxs-lookup"><span data-stu-id="3dd44-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="3dd44-113">BFE автоматически создает младшие биты 60 (точно так же, как если бы весовой коэффициент был установлен в [**FWP \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), а затем использует предоставленное значение для установки 4 старших битов.</span><span class="sxs-lookup"><span data-stu-id="3dd44-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="3dd44-114">Это позволяет вызывающим объектам вручную разделить пространство веса на 16 диапазонов, при этом используя Автоматическое взвешивание в пределах диапазона.</span><span class="sxs-lookup"><span data-stu-id="3dd44-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="3dd44-115">Если в одном подуровне зарегистрировано несколько вызовов, могут возникнуть проблемы, если фильтрам назначен один и тот же вес.</span><span class="sxs-lookup"><span data-stu-id="3dd44-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="3dd44-116">Эту ошибку можно предотвратить, выполнив выноски, создав свой собственный подуровень с помощью [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span><span class="sxs-lookup"><span data-stu-id="3dd44-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3dd44-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3dd44-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd44-118">**Идентификаторы веса фильтра**</span><span class="sxs-lookup"><span data-stu-id="3dd44-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




