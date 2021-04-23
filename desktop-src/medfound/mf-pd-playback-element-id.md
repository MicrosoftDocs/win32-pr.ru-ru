---
description: Содержит идентификатор элемента списка воспроизведения в презентации.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Атрибут MF_PD_PLAYBACK_ELEMENT_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656703"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="1d7d0-103">\_ \_ \_ Атрибут идентификатора элемента воспроизведения MF PD \_</span><span class="sxs-lookup"><span data-stu-id="1d7d0-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="1d7d0-104">Содержит идентификатор элемента списка воспроизведения в презентации.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d7d0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1d7d0-105">Data type</span></span>

<span data-ttu-id="1d7d0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1d7d0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1d7d0-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="1d7d0-107">Get/set</span></span>

<span data-ttu-id="1d7d0-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1d7d0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1d7d0-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1d7d0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1d7d0-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="1d7d0-110">Applies to</span></span>

[<span data-ttu-id="1d7d0-111">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="1d7d0-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="1d7d0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d7d0-112">Remarks</span></span>

<span data-ttu-id="1d7d0-113">Источники мультимедиа, доставляющие списки воспроизведения, при необходимости могут устанавливать этот атрибут в дескрипторах презентации.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="1d7d0-114">Когда источник мультимедиа доставляет список воспроизведения, он отправляет событие [меневпресентатион](menewpresentation.md) для каждого элемента списка воспроизведения после первого.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="1d7d0-115">Это событие содержит дескриптор представления для нового элемента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="1d7d0-116">Источник мультимедиа может назначать идентификаторы элементам, устанавливая \_ \_ \_ атрибут идентификатора элемента для воспроизведения MF PD \_ для каждого дескриптора презентации, включая тот, который создан с помощью [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="1d7d0-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="1d7d0-117">Источник мультимедиа также может отправить событие [меневпресентатион](menewpresentation.md) из-за динамического коммутатора потока или изменения числа потоков.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="1d7d0-118">В такой ситуации значение \_ \_ идентификатора элемента воспроизведения MF PD \_ \_ должно оставаться одинаковым для обеих презентаций, чтобы указать, что обе презентации представляют один и тот же элемент списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="1d7d0-119">Если две последовательные презентации имеют одно и то же значение для этого атрибута, то конвейер Microsoft Media Foundation ожидает непрерывную отметку времени в рамках перехода.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="1d7d0-120">Поэтому при переходе к следующей презентации источник мультимедиа не должен использовать атрибут « [ \_ \_ \_ фактический \_ Запуск источника событий MF](mf-event-source-actual-start-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="1d7d0-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="1d7d0-121">Источники мультимедиа, реализующие [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , должны использовать атрибут [ \_ \_ \_ ELEMENTID топоноде Sequence](mf-toponode-sequence-elementid-attribute.md) , а не \_ \_ \_ атрибут идентификатора элемента воспроизведения MF PD \_ .</span><span class="sxs-lookup"><span data-stu-id="1d7d0-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="1d7d0-122">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="1d7d0-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d7d0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1d7d0-123">Requirements</span></span>



| <span data-ttu-id="1d7d0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1d7d0-124">Requirement</span></span> | <span data-ttu-id="1d7d0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1d7d0-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7d0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d7d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1d7d0-127">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="1d7d0-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1d7d0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d7d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1d7d0-129">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="1d7d0-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1d7d0-130">Header</span><span class="sxs-lookup"><span data-stu-id="1d7d0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d7d0-131"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d7d0-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d7d0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d7d0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7d0-133">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d7d0-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d7d0-134">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="1d7d0-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




