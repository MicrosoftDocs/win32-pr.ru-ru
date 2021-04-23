---
description: Константы типа мультимедиа определены ниже.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Константы TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689224"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="23ca1-103">\_Константы тапимедиатипе</span><span class="sxs-lookup"><span data-stu-id="23ca1-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="23ca1-104">Определены следующие типы носителей:</span><span class="sxs-lookup"><span data-stu-id="23ca1-104">The following media types are defined:</span></span>



| <span data-ttu-id="23ca1-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="23ca1-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="23ca1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="23ca1-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="23ca1-107"><dt>**Тапимедиатипе \_ ЗВУКОВОЙ**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="23ca1-108">Поток звукового мультимедиа, который вводит или выходит из компьютера.</span><span class="sxs-lookup"><span data-stu-id="23ca1-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="23ca1-109">Входные потоки мультимедиа обычно воспроизводятся на динамиках или отправляются на устройство телефонной трубки, а поток, оставляемый, обычно захватывается с помощью микрофона или устройства телефонной трубки.</span><span class="sxs-lookup"><span data-stu-id="23ca1-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="23ca1-110"><dt>**Тапимедиатипе \_ ВИДЕО**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="23ca1-111">Поток мультимедиа, который вводит или выходит из компьютера.</span><span class="sxs-lookup"><span data-stu-id="23ca1-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="23ca1-112">Входный поток мультимедиа обычно отображается в видеоокне, а поток мультимедиа, в своюмся, обычно захватывается видеокамерой.</span><span class="sxs-lookup"><span data-stu-id="23ca1-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="23ca1-113"><dt>**Тапимедиатипе \_ МОДЕМ**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="23ca1-114">Поток мультимедиа данных, связанный с модемом данных.</span><span class="sxs-lookup"><span data-stu-id="23ca1-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="23ca1-115"><dt>**Тапимедиатипе \_ G3FAX**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="23ca1-116">Поток мультимедиа данных, связанный с протоколом G3.</span><span class="sxs-lookup"><span data-stu-id="23ca1-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="23ca1-117"><dt>**Тапимедиатипе \_ 0x10000 для многодорожкности**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="23ca1-118">Поток находится в терминале с многодорожкностью.</span><span class="sxs-lookup"><span data-stu-id="23ca1-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="23ca1-119"><dt>**\_ \_ Одиночный поток MEDIATYPE RTP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="23ca1-120">Этот идентификатор GUID используется между переданным приложением терминалом и потоком MSP.</span><span class="sxs-lookup"><span data-stu-id="23ca1-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="23ca1-121">Если ПИН-код терминала поддерживает этот тип мультимедиа, поток будет обмениваться данными RTP с терминалом.</span><span class="sxs-lookup"><span data-stu-id="23ca1-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="23ca1-122">Этот режим поддерживается только потоками видео на H323 MSP и Ипконф MSP для Windows 2000 с пакетом обновления 1 (SP1) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="23ca1-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="23ca1-123">**Заголовок:** Объявлено в ипмсп. h.</span><span class="sxs-lookup"><span data-stu-id="23ca1-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="23ca1-124">Заголовок ипмсп. h недоступен в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="23ca1-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="23ca1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="23ca1-125">Requirements</span></span>



| <span data-ttu-id="23ca1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="23ca1-126">Requirement</span></span> | <span data-ttu-id="23ca1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="23ca1-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23ca1-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="23ca1-128">TAPI version</span></span><br/> | <span data-ttu-id="23ca1-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="23ca1-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="23ca1-130">Header</span><span class="sxs-lookup"><span data-stu-id="23ca1-130">Header</span></span><br/>       | <dl> <span data-ttu-id="23ca1-131"><dt>Tapi3. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ca1-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ca1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23ca1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ca1-133">**Иткосевент:: Get \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="23ca1-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="23ca1-134">**Итаммедиаформат:: Get \_ медиаформат**</span><span class="sxs-lookup"><span data-stu-id="23ca1-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="23ca1-135">**Итаммедиаформат::p UT \_ медиаформат**</span><span class="sxs-lookup"><span data-stu-id="23ca1-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="23ca1-136">**Иткаллинфо:: Get \_ каллинфолонг**</span><span class="sxs-lookup"><span data-stu-id="23ca1-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="23ca1-137">**Итмедиасуппорт:: Get \_ медиатипес**</span><span class="sxs-lookup"><span data-stu-id="23ca1-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="23ca1-138">**Иттерминалсуппорт:: Креатетерминал**</span><span class="sxs-lookup"><span data-stu-id="23ca1-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

