---
description: Указывает, имеют ли топологии глобальное время начала и окончания.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Атрибут MF_SESSION_GLOBAL_TIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712323"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="3e769-103">\_ \_ Глобальный \_ атрибут времени сеанса MF</span><span class="sxs-lookup"><span data-stu-id="3e769-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="3e769-104">Указывает, имеют ли топологии глобальное время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="3e769-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e769-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3e769-105">Data type</span></span>

<span data-ttu-id="3e769-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3e769-106">**UINT32**</span></span>

<span data-ttu-id="3e769-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="3e769-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e769-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e769-108">Remarks</span></span>

<span data-ttu-id="3e769-109">Этот атрибут можно задать при создании сесисон мультимедиа с помощью параметра *пконфигуратион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="3e769-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="3e769-110">Если этот атрибут существует и имеет ненулевое значение, то все топологии, передаваемые в сеанс мультимедиа, должны иметь атрибуты [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) и [**MF \_ Topology \_ прожектстоп**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3e769-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="3e769-111">Эти атрибуты указывают время начала и окончания топологии относительно всей презентации.</span><span class="sxs-lookup"><span data-stu-id="3e769-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="3e769-112">Если этот атрибут отсутствует или **имеет значение false**, топологии не должны иметь атрибут [**MF \_ Topology \_ прожектстарт**](mf-topology-projectstart-attribute.md) или [**MF \_ Topology \_ прожектстоп**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3e769-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="3e769-113">Используйте этот атрибут для создания последовательностей редактирования.</span><span class="sxs-lookup"><span data-stu-id="3e769-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="3e769-114">Дополнительные сведения см. в разделе [время показа последовательностей](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="3e769-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="3e769-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3e769-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e769-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3e769-116">Requirements</span></span>



| <span data-ttu-id="3e769-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3e769-117">Requirement</span></span> | <span data-ttu-id="3e769-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3e769-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e769-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e769-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e769-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e769-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e769-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e769-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e769-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e769-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3e769-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e769-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e769-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e769-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e769-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e769-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e769-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e769-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e769-127">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3e769-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e769-128">Время представления последовательности</span><span class="sxs-lookup"><span data-stu-id="3e769-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="3e769-129">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="3e769-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3e769-130">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3e769-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3e769-131">**\_прожектстарт топология MF \_**</span><span class="sxs-lookup"><span data-stu-id="3e769-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="3e769-132">**\_прожектстоп топология MF \_**</span><span class="sxs-lookup"><span data-stu-id="3e769-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




