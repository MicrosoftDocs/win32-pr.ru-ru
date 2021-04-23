---
description: Указывает тип устройств, например запись звука или запись видео.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701653"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="b70bf-103">\_ \_ \_ Атрибут типа источника атрибута MF девсаурце \_</span><span class="sxs-lookup"><span data-stu-id="b70bf-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="b70bf-104">Указывает тип устройства, например запись звука или запись видео.</span><span class="sxs-lookup"><span data-stu-id="b70bf-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="b70bf-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b70bf-105">Data type</span></span>

<span data-ttu-id="b70bf-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b70bf-106">**GUID**</span></span>

<span data-ttu-id="b70bf-107">Для этого атрибута определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b70bf-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="b70bf-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b70bf-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="b70bf-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b70bf-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="b70bf-110"><dt>**\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ аудкап \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="b70bf-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="b70bf-111">Устройство для записи звука.</span><span class="sxs-lookup"><span data-stu-id="b70bf-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="b70bf-112"><dt>**\_ \_ тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="b70bf-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="b70bf-113">Устройство видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="b70bf-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="b70bf-114">Get/Set</span><span class="sxs-lookup"><span data-stu-id="b70bf-114">Get/set</span></span>

<span data-ttu-id="b70bf-115">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.</span><span class="sxs-lookup"><span data-stu-id="b70bf-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="b70bf-116">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="b70bf-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="b70bf-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b70bf-117">Remarks</span></span>

<span data-ttu-id="b70bf-118">Используйте этот атрибут в качестве входных данных для следующих функций:</span><span class="sxs-lookup"><span data-stu-id="b70bf-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="b70bf-119">**мфкреатедевицесаурце**</span><span class="sxs-lookup"><span data-stu-id="b70bf-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="b70bf-120">**мфкреатедевицесаурцеактивате**</span><span class="sxs-lookup"><span data-stu-id="b70bf-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="b70bf-121">**мфенумдевицесаурцес**</span><span class="sxs-lookup"><span data-stu-id="b70bf-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="b70bf-122">Кроме того, этот атрибут задается для объектов активации, возвращаемых функцией [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="b70bf-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="b70bf-123">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b70bf-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70bf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b70bf-124">Requirements</span></span>



| <span data-ttu-id="b70bf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b70bf-125">Requirement</span></span> | <span data-ttu-id="b70bf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b70bf-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b70bf-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b70bf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b70bf-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b70bf-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b70bf-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b70bf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b70bf-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b70bf-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b70bf-131">Header</span><span class="sxs-lookup"><span data-stu-id="b70bf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b70bf-132"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b70bf-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b70bf-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b70bf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70bf-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b70bf-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b70bf-135">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="b70bf-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b70bf-136">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="b70bf-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




