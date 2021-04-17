---
description: Указывает формат выходных данных устройства.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693859"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="751a3-103">\_ \_ \_ Атрибут типа носителя для атрибута MF девсаурце \_</span><span class="sxs-lookup"><span data-stu-id="751a3-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="751a3-104">Указывает формат выходных данных устройства.</span><span class="sxs-lookup"><span data-stu-id="751a3-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="751a3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="751a3-105">Data type</span></span>

<span data-ttu-id="751a3-106">**[**MFT \_ \_ \_ Сведения о типе регистрации**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** хранятся в виде **байта \[ \]**</span><span class="sxs-lookup"><span data-stu-id="751a3-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="751a3-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="751a3-107">Get/set</span></span>

<span data-ttu-id="751a3-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="751a3-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="751a3-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="751a3-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="751a3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="751a3-110">Remarks</span></span>

<span data-ttu-id="751a3-111">Этот атрибут содержит пару идентификаторов GUID: основной тип и подтип.</span><span class="sxs-lookup"><span data-stu-id="751a3-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="751a3-112">Эти GUID описывают формат вывода по умолчанию для устройства.</span><span class="sxs-lookup"><span data-stu-id="751a3-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="751a3-113">Устройство может поддерживать дополнительные выходные форматы.</span><span class="sxs-lookup"><span data-stu-id="751a3-113">The device might support additional output formats.</span></span>

<span data-ttu-id="751a3-114">Например, если устройство видеозаписи видео выводит RGB-32 видео, значение этого атрибута равно `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .</span><span class="sxs-lookup"><span data-stu-id="751a3-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="751a3-115">Этот атрибут является указанием для приложения.</span><span class="sxs-lookup"><span data-stu-id="751a3-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="751a3-116">Чтобы получить точный формат вывода, создайте источник мультимедиа для устройства и получите дескриптор представления источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="751a3-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="751a3-117">Этот атрибут задается для объектов активации, возвращаемых следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="751a3-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="751a3-118">**мфкреатедевицесаурцеактивате**</span><span class="sxs-lookup"><span data-stu-id="751a3-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="751a3-119">**мфенумдевицесаурцес**</span><span class="sxs-lookup"><span data-stu-id="751a3-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="751a3-120">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="751a3-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="751a3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="751a3-121">Requirements</span></span>



| <span data-ttu-id="751a3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="751a3-122">Requirement</span></span> | <span data-ttu-id="751a3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="751a3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="751a3-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="751a3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="751a3-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="751a3-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="751a3-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="751a3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="751a3-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="751a3-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="751a3-128">Header</span><span class="sxs-lookup"><span data-stu-id="751a3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="751a3-129"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="751a3-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751a3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="751a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751a3-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="751a3-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="751a3-132">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="751a3-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="751a3-133">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="751a3-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




