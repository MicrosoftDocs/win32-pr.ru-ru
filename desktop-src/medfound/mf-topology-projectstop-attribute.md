---
description: Задает время начала для топологии относительно начала первой топологии в последовательности.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: Атрибут MF_TOPOLOGY_PROJECTSTOP (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544335"
---
# <a name="mf_topology_projectstop-attribute"></a><span data-ttu-id="89bea-103">\_ \_ Атрибут ПРОЖЕКТСТОП топологии MF</span><span class="sxs-lookup"><span data-stu-id="89bea-103">MF\_TOPOLOGY\_PROJECTSTOP attribute</span></span>

<span data-ttu-id="89bea-104">Задает время начала для топологии относительно начала первой топологии в последовательности.</span><span class="sxs-lookup"><span data-stu-id="89bea-104">Specifies the start time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="89bea-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="89bea-105">Data type</span></span>

<span data-ttu-id="89bea-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="89bea-106">**UINT64**</span></span>

<span data-ttu-id="89bea-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="89bea-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89bea-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89bea-108">Remarks</span></span>

<span data-ttu-id="89bea-109">Значение задается в единицах 100 наносекунд.</span><span class="sxs-lookup"><span data-stu-id="89bea-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="89bea-110">Если сеанс мультимедиа был создан с атрибутом [**\_ \_ глобального \_ времени сеанса MF**](mf-session-global-time-attribute.md) , равным **true**, все топологии должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстоп** .</span><span class="sxs-lookup"><span data-stu-id="89bea-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="89bea-111">В противном случае топологии не должны содержать атрибут **MF \_ TOPOLOGY \_ прожектстоп** .</span><span class="sxs-lookup"><span data-stu-id="89bea-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="89bea-112">Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="89bea-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="89bea-113">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="89bea-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="89bea-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="89bea-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="89bea-115">Требования</span><span class="sxs-lookup"><span data-stu-id="89bea-115">Requirements</span></span>



| <span data-ttu-id="89bea-116">Требование</span><span class="sxs-lookup"><span data-stu-id="89bea-116">Requirement</span></span> | <span data-ttu-id="89bea-117">Значение</span><span class="sxs-lookup"><span data-stu-id="89bea-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89bea-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89bea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89bea-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89bea-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="89bea-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89bea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89bea-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89bea-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89bea-122">Header</span><span class="sxs-lookup"><span data-stu-id="89bea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89bea-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="89bea-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89bea-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89bea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89bea-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89bea-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="89bea-126">Время представления последовательности</span><span class="sxs-lookup"><span data-stu-id="89bea-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="89bea-127">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="89bea-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="89bea-128">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="89bea-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="89bea-129">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="89bea-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="89bea-130">**\_прожектстарт топология MF \_**</span><span class="sxs-lookup"><span data-stu-id="89bea-130">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




