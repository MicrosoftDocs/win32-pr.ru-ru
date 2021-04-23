---
description: Указывает категорию устройств для устройства видеозаписи.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154631"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="df7c9-103">\_ \_ \_ \_ \_ Атрибут категории видкап типа источника \_ девсаурце MF</span><span class="sxs-lookup"><span data-stu-id="df7c9-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="df7c9-104">Указывает категорию устройств для устройства видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="df7c9-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="df7c9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="df7c9-105">Data type</span></span>

<span data-ttu-id="df7c9-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="df7c9-106">**GUID**</span></span>

<span data-ttu-id="df7c9-107">Определено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="df7c9-107">The following value is defined.</span></span>



| <span data-ttu-id="df7c9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="df7c9-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="df7c9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="df7c9-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="df7c9-110"><dt>**\_ВИДЕОИНПУТДЕВИЦЕКАТЕГОРИ CLSID**</dt></span><span class="sxs-lookup"><span data-stu-id="df7c9-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="df7c9-111">Устройство видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="df7c9-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="df7c9-112">Get/Set</span><span class="sxs-lookup"><span data-stu-id="df7c9-112">Get/set</span></span>

<span data-ttu-id="df7c9-113">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.</span><span class="sxs-lookup"><span data-stu-id="df7c9-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="df7c9-114">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="df7c9-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="df7c9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df7c9-115">Remarks</span></span>

<span data-ttu-id="df7c9-116">Используйте этот атрибут в качестве входных данных для функции [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) при перечислении устройств видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="df7c9-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="df7c9-117">Кроме того, этот атрибут задается для объектов активации, возвращаемых следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="df7c9-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="df7c9-118">**мфкреатедевицесаурцеактивате**</span><span class="sxs-lookup"><span data-stu-id="df7c9-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="df7c9-119">**мфенумдевицесаурцес**</span><span class="sxs-lookup"><span data-stu-id="df7c9-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="df7c9-120">Атрибут применяется только к устройствам записи видео.</span><span class="sxs-lookup"><span data-stu-id="df7c9-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="df7c9-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="df7c9-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="df7c9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="df7c9-122">Requirements</span></span>



| <span data-ttu-id="df7c9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="df7c9-123">Requirement</span></span> | <span data-ttu-id="df7c9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="df7c9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df7c9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df7c9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="df7c9-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="df7c9-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="df7c9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df7c9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="df7c9-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="df7c9-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="df7c9-129">Header</span><span class="sxs-lookup"><span data-stu-id="df7c9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="df7c9-130"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="df7c9-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df7c9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df7c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df7c9-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df7c9-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="df7c9-133">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="df7c9-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="df7c9-134">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="df7c9-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




