---
description: Указывает максимальное число кадров, которые будут помещены в буфер источника видеозаписи видео.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682876"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="b097f-103">MF \_ девсаурце \_ \_ тип источника \_ атрибута \_ видкап \_ максимальный \_ Размер буфера в атрибуте</span><span class="sxs-lookup"><span data-stu-id="b097f-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="b097f-104">Указывает максимальное число кадров, которые будут помещены в буфер источника видеозаписи видео.</span><span class="sxs-lookup"><span data-stu-id="b097f-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b097f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b097f-105">Data type</span></span>

<span data-ttu-id="b097f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b097f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b097f-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="b097f-107">Get/set</span></span>

<span data-ttu-id="b097f-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b097f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b097f-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b097f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b097f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b097f-110">Remarks</span></span>

<span data-ttu-id="b097f-111">По умолчанию источник видеозаписи видео помещает в буфер не более одного кадра за раз.</span><span class="sxs-lookup"><span data-stu-id="b097f-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="b097f-112">Можно увеличить предельный размер буфера, задав этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="b097f-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="b097f-113">Правильный способ установки этого атрибута зависит от функции, используемой для создания источника мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="b097f-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="b097f-114">[**Мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Задайте атрибут с помощью параметра *паттрибутес* функции.</span><span class="sxs-lookup"><span data-stu-id="b097f-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="b097f-115">[**Мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Задайте атрибут с помощью параметра *паттрибутес* функции.</span><span class="sxs-lookup"><span data-stu-id="b097f-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="b097f-116">[**Мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Задайте атрибут для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемого функцией.</span><span class="sxs-lookup"><span data-stu-id="b097f-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="b097f-117">Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="b097f-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="b097f-118">Атрибут применяется только к устройствам записи видео.</span><span class="sxs-lookup"><span data-stu-id="b097f-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="b097f-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b097f-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b097f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b097f-120">Requirements</span></span>



| <span data-ttu-id="b097f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b097f-121">Requirement</span></span> | <span data-ttu-id="b097f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b097f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b097f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b097f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b097f-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b097f-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b097f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b097f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b097f-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b097f-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b097f-127">Header</span><span class="sxs-lookup"><span data-stu-id="b097f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b097f-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b097f-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b097f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b097f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b097f-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b097f-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b097f-131">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="b097f-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b097f-132">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="b097f-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




