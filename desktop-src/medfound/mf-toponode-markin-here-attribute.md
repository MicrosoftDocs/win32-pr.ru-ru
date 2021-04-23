---
description: Указывает, применяет ли конвейер отметку на этом узле.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Атрибут MF_TOPONODE_MARKIN_HERE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711290"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="47038-103">\_Атрибут MF топоноде \_ Маркин \_ здесь</span><span class="sxs-lookup"><span data-stu-id="47038-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="47038-104">Указывает, применяет ли конвейер отметку на этом узле.</span><span class="sxs-lookup"><span data-stu-id="47038-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="47038-105">Пометка — это точка, с которой начинается презентация.</span><span class="sxs-lookup"><span data-stu-id="47038-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="47038-106">Если компоненты конвейера формируют данные перед точкой отметки, данные не подготавливаются к просмотру.</span><span class="sxs-lookup"><span data-stu-id="47038-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="47038-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="47038-107">Data type</span></span>

<span data-ttu-id="47038-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="47038-108">**UINT32**</span></span>

<span data-ttu-id="47038-109">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="47038-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47038-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47038-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="47038-111">Большинству приложений не требуется использовать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="47038-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="47038-112">[Сеанс мультимедиа](media-session.md) автоматически задает этот атрибут при необходимости.</span><span class="sxs-lookup"><span data-stu-id="47038-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="47038-113">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="47038-113">This attribute applies to all node types.</span></span> <span data-ttu-id="47038-114">Если атрибут имеет **значение true**, то конвейер Media Foundation обрезает выходные примеры из этого узла в соответствии со временем начала презентации.</span><span class="sxs-lookup"><span data-stu-id="47038-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="47038-115">Загрузчик топологии задает этот атрибут при разрешении топологии.</span><span class="sxs-lookup"><span data-stu-id="47038-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="47038-116">Рекомендуется, чтобы только один узел в каждой ветви топологии имел атрибут со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="47038-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="47038-117">Ветвь топологии определяется в качестве пути от исходного узла до выходного узла.</span><span class="sxs-lookup"><span data-stu-id="47038-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="47038-118">В ветви на [ \_ \_ \_ ](mf-toponode-markout-here-attribute.md) \_ \_ \_ одном узле ветви должны быть установлены атрибуты MF топоноде и MF топоноде Маркин.</span><span class="sxs-lookup"><span data-stu-id="47038-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="47038-119">Они не могут быть установлены на разных узлах в одной ветви.</span><span class="sxs-lookup"><span data-stu-id="47038-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="47038-120">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="47038-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="47038-121">Требования</span><span class="sxs-lookup"><span data-stu-id="47038-121">Requirements</span></span>



| <span data-ttu-id="47038-122">Требование</span><span class="sxs-lookup"><span data-stu-id="47038-122">Requirement</span></span> | <span data-ttu-id="47038-123">Значение</span><span class="sxs-lookup"><span data-stu-id="47038-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47038-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47038-124">Minimum supported client</span></span><br/> | <span data-ttu-id="47038-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47038-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47038-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47038-126">Minimum supported server</span></span><br/> | <span data-ttu-id="47038-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47038-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="47038-128">Header</span><span class="sxs-lookup"><span data-stu-id="47038-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="47038-129"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="47038-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47038-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47038-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47038-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47038-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="47038-132">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="47038-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="47038-133">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="47038-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="47038-134">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="47038-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="47038-135">**Разметка MF \_ топоноде \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47038-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="47038-136">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="47038-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




