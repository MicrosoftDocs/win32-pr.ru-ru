---
description: Задает время окончания топологии относительно начала первой топологии в последовательности.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Атрибут MF_TOPOLOGY_PROJECTSTART (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898349"
---
# <a name="mf_topology_projectstart-attribute"></a><span data-ttu-id="582b1-103">\_ \_ Атрибут ПРОЖЕКТСТАРТ топологии MF</span><span class="sxs-lookup"><span data-stu-id="582b1-103">MF\_TOPOLOGY\_PROJECTSTART attribute</span></span>

<span data-ttu-id="582b1-104">Задает время окончания топологии относительно начала первой топологии в последовательности.</span><span class="sxs-lookup"><span data-stu-id="582b1-104">Specifies the stop time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="582b1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="582b1-105">Data type</span></span>

<span data-ttu-id="582b1-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="582b1-106">**UINT64**</span></span>

<span data-ttu-id="582b1-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="582b1-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="582b1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="582b1-108">Remarks</span></span>

<span data-ttu-id="582b1-109">Значение задается в единицах 100 наносекунд.</span><span class="sxs-lookup"><span data-stu-id="582b1-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="582b1-110">Если сеанс мультимедиа был создан с атрибутом [**\_ \_ глобального \_ времени сеанса MF**](mf-session-global-time-attribute.md) , равным **true**, все топологии должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстарт** .</span><span class="sxs-lookup"><span data-stu-id="582b1-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="582b1-111">В противном случае топологии не должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстарт** .</span><span class="sxs-lookup"><span data-stu-id="582b1-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="582b1-112">Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="582b1-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="582b1-113">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="582b1-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="582b1-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="582b1-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="582b1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="582b1-115">Requirements</span></span>



| <span data-ttu-id="582b1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="582b1-116">Requirement</span></span> | <span data-ttu-id="582b1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="582b1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="582b1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="582b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="582b1-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="582b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="582b1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="582b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="582b1-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="582b1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="582b1-122">Header</span><span class="sxs-lookup"><span data-stu-id="582b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="582b1-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="582b1-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="582b1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="582b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="582b1-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="582b1-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="582b1-126">Время представления последовательности</span><span class="sxs-lookup"><span data-stu-id="582b1-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="582b1-127">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="582b1-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="582b1-128">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="582b1-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="582b1-129">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="582b1-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="582b1-130">**\_прожектстоп топология MF \_**</span><span class="sxs-lookup"><span data-stu-id="582b1-130">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




