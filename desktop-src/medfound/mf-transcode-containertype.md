---
description: Указывает тип контейнера закодированного файла.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: Атрибут MF_TRANSCODE_CONTAINERTYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692541"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="55132-103">\_Атрибут контаинертипе для ПЕРЕКОДИРОВАНИЯ MF \_</span><span class="sxs-lookup"><span data-stu-id="55132-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="55132-104">Указывает тип контейнера закодированного файла.</span><span class="sxs-lookup"><span data-stu-id="55132-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="55132-105">Типы контейнеров поддерживаются Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="55132-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="55132-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="55132-106">Data type</span></span>

<span data-ttu-id="55132-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="55132-107">**GUID**</span></span>

<span data-ttu-id="55132-108">Возможные значения для типов контейнеров, предоставляемых Media Foundation, описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55132-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="55132-109">Значение</span><span class="sxs-lookup"><span data-stu-id="55132-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="55132-110">Значение</span><span class="sxs-lookup"><span data-stu-id="55132-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="55132-111"><dt>**Мфтранскодеконтаинертипе \_ ASF**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="55132-112">Контейнер файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="55132-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="55132-113"><dt>**Мфтранскодеконтаинертипе \_ MPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="55132-114">Контейнер файла MP4.</span><span class="sxs-lookup"><span data-stu-id="55132-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="55132-115"><dt>**Мфтранскодеконтаинертипе \_ MP3**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="55132-116">Контейнер файлов MP3.</span><span class="sxs-lookup"><span data-stu-id="55132-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="55132-117"><dt>**Мфтранскодеконтаинертипе \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="55132-118">контейнер файлов 3GP.</span><span class="sxs-lookup"><span data-stu-id="55132-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="55132-119"><dt>**Мфтранскодеконтаинертипе \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="55132-120">Контейнер файлов AC3.</span><span class="sxs-lookup"><span data-stu-id="55132-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="55132-121"><dt>**Мфтранскодеконтаинертипе \_ ADTS**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="55132-122">Контейнер файлов ADTS.</span><span class="sxs-lookup"><span data-stu-id="55132-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="55132-123"><dt>**Мфтранскодеконтаинертипе \_ MPEG2**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="55132-124">Контейнер файлов MPEG2.</span><span class="sxs-lookup"><span data-stu-id="55132-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="55132-125"><dt>**Мфтранскодеконтаинертипе \_ FMPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="55132-126">Контейнер файлов FMPEG4.</span><span class="sxs-lookup"><span data-stu-id="55132-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="55132-127"><dt>**\_Волна мфтранскодеконтаинертипе**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="55132-128">Контейнер файла WAVE.</span><span class="sxs-lookup"><span data-stu-id="55132-128">WAVE file container.</span></span><br/> <span data-ttu-id="55132-129">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="55132-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="55132-130"><dt>**Мфтранскодеконтаинертипе \_ AVI**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="55132-131">Контейнер файла AVI.</span><span class="sxs-lookup"><span data-stu-id="55132-131">AVI file container.</span></span><br/> <span data-ttu-id="55132-132">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="55132-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="55132-133"><dt>**Мфтранскодеконтаинертипе \_ AMR**</dt></span><span class="sxs-lookup"><span data-stu-id="55132-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="55132-134">Контейнер файлов AMR.</span><span class="sxs-lookup"><span data-stu-id="55132-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="55132-135">Get/Set</span><span class="sxs-lookup"><span data-stu-id="55132-135">Get/set</span></span>

<span data-ttu-id="55132-136">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.</span><span class="sxs-lookup"><span data-stu-id="55132-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="55132-137">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="55132-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="55132-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55132-138">Remarks</span></span>

<span data-ttu-id="55132-139">Этот атрибут используется как для функции быстрого перекодирования, так и для объекта модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="55132-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="55132-140">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="55132-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="55132-141">Быстрый перекодированный</span><span class="sxs-lookup"><span data-stu-id="55132-141">Fast Transcode</span></span>

<span data-ttu-id="55132-142">Перед сборкой топологии перекодировки приложение должно установить атрибут контейнера в профиле перекодировки.</span><span class="sxs-lookup"><span data-stu-id="55132-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="55132-143">Построитель топологии анализирует этот атрибут и загружает в конвейере соответствующий приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="55132-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="55132-144">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="55132-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="55132-145">**Имфтранскодепрофиле:: Жетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="55132-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="55132-146">**Имфтранскодепрофиле:: Сетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="55132-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="55132-147">Модуль записи приемников</span><span class="sxs-lookup"><span data-stu-id="55132-147">Sink Writer</span></span>

<span data-ttu-id="55132-148">Этот атрибут можно использовать для настройки типа контейнера файлов для модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="55132-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="55132-149">Дополнительные сведения см. в разделе [атрибуты модуля записи приемника](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="55132-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55132-150">Требования</span><span class="sxs-lookup"><span data-stu-id="55132-150">Requirements</span></span>



| <span data-ttu-id="55132-151">Требование</span><span class="sxs-lookup"><span data-stu-id="55132-151">Requirement</span></span> | <span data-ttu-id="55132-152">Значение</span><span class="sxs-lookup"><span data-stu-id="55132-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55132-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55132-153">Minimum supported client</span></span><br/> | <span data-ttu-id="55132-154">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="55132-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55132-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55132-155">Minimum supported server</span></span><br/> | <span data-ttu-id="55132-156">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="55132-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="55132-157">Header</span><span class="sxs-lookup"><span data-stu-id="55132-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="55132-158"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="55132-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55132-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55132-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55132-160">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55132-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55132-161">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="55132-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




