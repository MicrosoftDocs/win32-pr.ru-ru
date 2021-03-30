---
description: Содержит указатель на диспетчер устройств Microsoft Direct3D для модуля чтения исходного кода.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Атрибут MF_SOURCE_READER_D3D_MANAGER (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910196"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="52426-103">\_ \_ \_ Атрибут диспетчера D3D чтения источника MF \_</span><span class="sxs-lookup"><span data-stu-id="52426-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="52426-104">Содержит указатель на [Диспетчер устройств Microsoft Direct3D](direct3d-device-manager.md) для [модуля чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="52426-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="52426-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="52426-105">Data type</span></span>

<span data-ttu-id="52426-106">**IDirect3DDeviceManager9 \* или имфдксгидевицеманажер \*** хранятся как \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="52426-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="52426-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="52426-107">Get/set</span></span>

<span data-ttu-id="52426-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="52426-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="52426-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="52426-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="52426-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52426-110">Remarks</span></span>

<span data-ttu-id="52426-111">Значение этого атрибута может быть указателем на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) или [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span><span class="sxs-lookup"><span data-stu-id="52426-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="52426-112">Используйте этот атрибут, чтобы предоставить устройство Direct3D для видеодекодеров, загруженных модулем чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="52426-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="52426-113">Если установить этот атрибут и декодер поддерживает ускорение видео Microsoft DirectX (ДКСВА), модуль чтения исходного кода использует устройство Direct3D для выделения буферов видео.</span><span class="sxs-lookup"><span data-stu-id="52426-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="52426-114">Эти буферы совместимы с обработчиком видео ДКСВА 2.</span><span class="sxs-lookup"><span data-stu-id="52426-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="52426-115">(См. раздел [Обработка видео дксва](dxva-video-processing.md).)</span><span class="sxs-lookup"><span data-stu-id="52426-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="52426-116">Используйте этот атрибут со следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="52426-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="52426-117">**мфкреатесаурцереадерфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="52426-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="52426-118">**мфкреатесаурцереадерфроммедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="52426-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="52426-119">**мфкреатесаурцереадерфромурл**</span><span class="sxs-lookup"><span data-stu-id="52426-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="52426-120">Обычно этот атрибут задается, если вы используете модуль чтения исходного кода для получения раскодированных видеокадров и используете Direct3D для вывода кадров.</span><span class="sxs-lookup"><span data-stu-id="52426-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="52426-121">Установка этого атрибута позволяет декодеру использовать ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="52426-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="52426-122">Этот атрибут не задается, если:</span><span class="sxs-lookup"><span data-stu-id="52426-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="52426-123">Модуль чтения исходного кода используется только для обработки аудио и не видео.</span><span class="sxs-lookup"><span data-stu-id="52426-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="52426-124">Вы получаете сжатое видео из модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="52426-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="52426-125">В этом случае модуль чтения исходного кода не создает декодер.</span><span class="sxs-lookup"><span data-stu-id="52426-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="52426-126">Требования</span><span class="sxs-lookup"><span data-stu-id="52426-126">Requirements</span></span>



| <span data-ttu-id="52426-127">Требование</span><span class="sxs-lookup"><span data-stu-id="52426-127">Requirement</span></span> | <span data-ttu-id="52426-128">Значение</span><span class="sxs-lookup"><span data-stu-id="52426-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52426-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52426-129">Minimum supported client</span></span><br/> | <span data-ttu-id="52426-130">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="52426-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="52426-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52426-131">Minimum supported server</span></span><br/> | <span data-ttu-id="52426-132">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="52426-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="52426-133">Header</span><span class="sxs-lookup"><span data-stu-id="52426-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="52426-134"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="52426-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52426-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52426-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52426-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52426-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52426-137">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="52426-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="52426-138">Атрибуты модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="52426-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




