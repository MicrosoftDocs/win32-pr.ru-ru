---
description: Следующие идентификаторы GUID определяют расширения полезных данных для потоков ASF.
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: Идентификаторы GUID расширения полезных данных ASF (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539650"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="537b9-103">Идентификаторы GUID расширения полезных данных ASF</span><span class="sxs-lookup"><span data-stu-id="537b9-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="537b9-104">Следующие идентификаторы GUID определяют расширения полезных данных для потоков ASF.</span><span class="sxs-lookup"><span data-stu-id="537b9-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="537b9-105">Константа</span><span class="sxs-lookup"><span data-stu-id="537b9-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="537b9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="537b9-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="537b9-107"><dt>**Мфасфсампликстенсион \_ сампледуратион**</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="537b9-108">Данные указывают длительность (в миллисекундах) образца, содержащегося в объекте buffer.</span><span class="sxs-lookup"><span data-stu-id="537b9-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="537b9-109"><dt>**Мфасфсампликстенсион \_ аутпутклеанпоинт**</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="537b9-110">Данные указывают, является ли образец ключевым кадром.</span><span class="sxs-lookup"><span data-stu-id="537b9-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="537b9-111">Нулевое значение указывает, что образец не является ключевым кадром.</span><span class="sxs-lookup"><span data-stu-id="537b9-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="537b9-112">Ненулевое значение указывает, что это ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="537b9-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="537b9-113"><dt>**Мфасфсампликстенсион \_ SMPTE**</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="537b9-114">Данные представляют собой код времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="537b9-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="537b9-115"><dt>**\_Имя файла мфасфсампликстенсион**</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="537b9-116">Данные в примере расширения указывают имя файла, из которого было получено содержимое в образце.</span><span class="sxs-lookup"><span data-stu-id="537b9-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="537b9-117"><dt>**\_ContentType мфасфсампликстенсион**</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="537b9-118">Данные определяют тип содержимого, которое содержит образец.</span><span class="sxs-lookup"><span data-stu-id="537b9-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="537b9-119"><dt>**Мфасфсампликстенсион \_ пикселаспектратио**</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="537b9-120">Данные обозначают пропорцию содержимого в образце пикселя.</span><span class="sxs-lookup"><span data-stu-id="537b9-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="537b9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="537b9-121">Requirements</span></span>



| <span data-ttu-id="537b9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="537b9-122">Requirement</span></span> | <span data-ttu-id="537b9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="537b9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="537b9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="537b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="537b9-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="537b9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="537b9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="537b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="537b9-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="537b9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="537b9-128">Header</span><span class="sxs-lookup"><span data-stu-id="537b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="537b9-129"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="537b9-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="537b9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="537b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537b9-131">**Имфасфстреамконфиг:: Аддпайлоадекстенсион**</span><span class="sxs-lookup"><span data-stu-id="537b9-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="537b9-132">**Имфасфстреамконфиг:: Жетпайлоадекстенсион**</span><span class="sxs-lookup"><span data-stu-id="537b9-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="537b9-133">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="537b9-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




