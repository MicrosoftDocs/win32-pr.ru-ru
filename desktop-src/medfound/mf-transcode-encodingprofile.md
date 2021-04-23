---
description: Указывает профиль соответствия устройства для кодирования файлов формата ASF.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Атрибут MF_TRANSCODE_ENCODINGPROFILE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543234"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="15d57-103">\_Атрибут енкодингпрофиле для ПЕРЕКОДИРОВАНИЯ MF \_</span><span class="sxs-lookup"><span data-stu-id="15d57-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="15d57-104">Указывает профиль соответствия устройства для кодирования файлов формата ASF.</span><span class="sxs-lookup"><span data-stu-id="15d57-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="15d57-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="15d57-105">Data type</span></span>

<span data-ttu-id="15d57-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="15d57-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="15d57-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="15d57-107">Get/set</span></span>

<span data-ttu-id="15d57-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: жеталлокатедстринг**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span><span class="sxs-lookup"><span data-stu-id="15d57-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="15d57-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="15d57-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="15d57-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15d57-110">Remarks</span></span>

<span data-ttu-id="15d57-111">Используйте этот атрибут при перекодировании на устройство, которое поддерживает Windows Media.</span><span class="sxs-lookup"><span data-stu-id="15d57-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="15d57-112">Если этот атрибут задан, кодировщик будет использовать профиль согласования устройства или шаблон для кодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="15d57-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="15d57-113">Перед созданием топологии перекодировки задайте атрибут в профиле перекодировки.</span><span class="sxs-lookup"><span data-stu-id="15d57-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="15d57-114">Значением этого атрибута может быть любая из строк шаблона соответствия, перечисленных в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="15d57-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="15d57-115">Шаблоны соответствия аудио устройства</span><span class="sxs-lookup"><span data-stu-id="15d57-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="15d57-116">Шаблоны соответствия видеоустройств</span><span class="sxs-lookup"><span data-stu-id="15d57-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="15d57-117">Для кодирования видео Windows Media построитель топологии использует этот атрибут для задания свойства [**мфпкэй \_ декодеркомплекситирекуестед**](mfpkey-decodercomplexityrequestedproperty.md) в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="15d57-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="15d57-118">Кодировщик будет пытаться использовать указанный шаблон для кодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="15d57-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="15d57-119">Чтобы получить фактический шаблон, проведите обход узлов топологии перекодировки, чтобы получить указатель на узел кодировщика.</span><span class="sxs-lookup"><span data-stu-id="15d57-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="15d57-120">Затем получите значение свойства [**мфпкэй \_ декодеркомплекситипрофиле**](mfpkey-decodercomplexityprofileproperty.md) из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="15d57-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="15d57-121">Построитель топологии также использует значение этого атрибута для задания свойства "Девицеконформанцетемплате" в приемнике ASF Media.</span><span class="sxs-lookup"><span data-stu-id="15d57-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="15d57-122">Если этот атрибут задан, то объект метаданных ASF-файла всегда создается независимо от значения, указанного приложением, для атрибута [ \_ \_ \_ \_ пересылки метаданных пропуска MF](mf-transcode-skip-metadata-transfer.md) .</span><span class="sxs-lookup"><span data-stu-id="15d57-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="15d57-123">Ниже приведены типичные значения для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="15d57-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="15d57-124">Значение</span><span class="sxs-lookup"><span data-stu-id="15d57-124">Value</span></span>   | <span data-ttu-id="15d57-125">Описание</span><span class="sxs-lookup"><span data-stu-id="15d57-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="15d57-126">ПРОФИЛЯ</span><span class="sxs-lookup"><span data-stu-id="15d57-126">"AP"</span></span>    | <span data-ttu-id="15d57-127">Видео расширенного профиля</span><span class="sxs-lookup"><span data-stu-id="15d57-127">Advanced profile video</span></span>           |
| <span data-ttu-id="15d57-128">МВ</span><span class="sxs-lookup"><span data-stu-id="15d57-128">"MP"</span></span>    | <span data-ttu-id="15d57-129">Видео о основном профиле</span><span class="sxs-lookup"><span data-stu-id="15d57-129">Main profile video</span></span>               |
| <span data-ttu-id="15d57-130">ПОРТОВ</span><span class="sxs-lookup"><span data-stu-id="15d57-130">"SP"</span></span>    | <span data-ttu-id="15d57-131">Видео простого профиля</span><span class="sxs-lookup"><span data-stu-id="15d57-131">Simple profile video</span></span>             |
| <span data-ttu-id="15d57-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="15d57-132">"MP@LL"</span></span> | <span data-ttu-id="15d57-133">Основной профиль, видео среднего уровня</span><span class="sxs-lookup"><span data-stu-id="15d57-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="15d57-134">L2</span><span class="sxs-lookup"><span data-stu-id="15d57-134">"L2"</span></span>    | <span data-ttu-id="15d57-135">Профиль аудиоподсистемы, <= 160 кбит/с</span><span class="sxs-lookup"><span data-stu-id="15d57-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="15d57-136">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="15d57-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d57-137">Требования</span><span class="sxs-lookup"><span data-stu-id="15d57-137">Requirements</span></span>



| <span data-ttu-id="15d57-138">Требование</span><span class="sxs-lookup"><span data-stu-id="15d57-138">Requirement</span></span> | <span data-ttu-id="15d57-139">Значение</span><span class="sxs-lookup"><span data-stu-id="15d57-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15d57-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15d57-140">Minimum supported client</span></span><br/> | <span data-ttu-id="15d57-141">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="15d57-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="15d57-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15d57-142">Minimum supported server</span></span><br/> | <span data-ttu-id="15d57-143">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="15d57-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="15d57-144">Header</span><span class="sxs-lookup"><span data-stu-id="15d57-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="15d57-145"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d57-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d57-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15d57-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d57-147">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15d57-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15d57-148">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="15d57-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="15d57-149">**Имфтранскодепрофиле:: Жетаудиоаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="15d57-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="15d57-150">**Имфтранскодепрофиле:: Сетаудиоаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="15d57-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="15d57-151">**Имфтранскодепрофиле:: Сетвидеоаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="15d57-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="15d57-152">**Имфтранскодепрофиле:: Жетвидеоаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="15d57-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
