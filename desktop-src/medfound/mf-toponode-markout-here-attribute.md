---
description: Указывает, применяется ли к этому узлу отметка для конвейера. Отметка — это точка, в которой заканчивается презентация. Если компоненты конвейера формируют данные после точки отметки, данные не подготавливаются к просмотру.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Атрибут MF_TOPONODE_MARKOUT_HERE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711287"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="e2811-105">\_Атрибут MF топоноде \_ метка \_</span><span class="sxs-lookup"><span data-stu-id="e2811-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="e2811-106">Указывает, применяется ли к этому узлу отметка для конвейера.</span><span class="sxs-lookup"><span data-stu-id="e2811-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="e2811-107">Отметка — это точка, в которой заканчивается презентация.</span><span class="sxs-lookup"><span data-stu-id="e2811-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="e2811-108">Если компоненты конвейера формируют данные после точки отметки, данные не подготавливаются к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e2811-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2811-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e2811-109">Data type</span></span>

<span data-ttu-id="e2811-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e2811-110">**UINT32**</span></span>

<span data-ttu-id="e2811-111">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="e2811-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2811-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2811-112">Remarks</span></span>

<span data-ttu-id="e2811-113">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="e2811-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="e2811-114">Если этот атрибут имеет **значение true**, то конвейер Media Foundation обрезает выходные примеры из этого узла в соответствии со временем окончания презентации.</span><span class="sxs-lookup"><span data-stu-id="e2811-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="e2811-115">Загрузчик топологии задает этот атрибут при разрешении топологии.</span><span class="sxs-lookup"><span data-stu-id="e2811-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="e2811-116">Большинству приложений не требуется устанавливать или извлекать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="e2811-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="e2811-117">Рекомендуется, чтобы только один узел в каждой ветви топологии имел атрибут со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="e2811-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="e2811-118">Ветвь топологии определяется в качестве пути от исходного узла до выходного узла.</span><span class="sxs-lookup"><span data-stu-id="e2811-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="e2811-119">В ветви на \_ \_ \_ одном узле ветви должны быть установлены атрибуты MF топоноде и [MF \_ топоноде \_ Маркин \_ ](mf-toponode-markin-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e2811-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="e2811-120">Они не могут быть установлены на разных узлах в одной ветви.</span><span class="sxs-lookup"><span data-stu-id="e2811-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="e2811-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="e2811-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2811-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e2811-122">Requirements</span></span>



| <span data-ttu-id="e2811-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e2811-123">Requirement</span></span> | <span data-ttu-id="e2811-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e2811-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2811-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2811-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e2811-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2811-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2811-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2811-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e2811-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2811-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e2811-129">Header</span><span class="sxs-lookup"><span data-stu-id="e2811-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2811-130"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2811-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2811-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2811-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2811-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2811-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2811-133">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="e2811-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e2811-134">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e2811-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e2811-135">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="e2811-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e2811-136">**MF \_ топоноде \_ Маркин \_**</span><span class="sxs-lookup"><span data-stu-id="e2811-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="e2811-137">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="e2811-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




