---
title: Команда MCI_INFO (Ммсистем. h)
description: Команда MCI \_ Information извлекает строковые данные с устройства.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137251"
---
# <a name="mci_info-command"></a><span data-ttu-id="30b6b-104">\_Команда сведений MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-104">MCI\_INFO command</span></span>

<span data-ttu-id="30b6b-105">Команда MCI \_ Information извлекает строковые данные с устройства.</span><span class="sxs-lookup"><span data-stu-id="30b6b-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="30b6b-106">Все устройства распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="30b6b-106">All devices recognize this command.</span></span> <span data-ttu-id="30b6b-107">Сведения возвращаются в элементе **лпстрретурн** структуры, определенной параметром *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="30b6b-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="30b6b-108">Элемент **двретсизе** указывает длину буфера для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="30b6b-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="30b6b-109">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="30b6b-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="30b6b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="30b6b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="30b6b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-112">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="30b6b-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="30b6b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-114">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="30b6b-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="30b6b-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="30b6b-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span><span class="sxs-lookup"><span data-stu-id="30b6b-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-117">Указатель на структуру [**\_ \_ пармс сведений MCI**](mci-info-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="30b6b-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="30b6b-118">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="30b6b-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b6b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30b6b-119">Return Value</span></span>

<span data-ttu-id="30b6b-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="30b6b-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b6b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30b6b-121">Remarks</span></span>

<span data-ttu-id="30b6b-122">Следующие дополнительные стандартные и специальные флаги применяются ко всем устройствам, поддерживающим \_ сведения о MCI:</span><span class="sxs-lookup"><span data-stu-id="30b6b-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_продукт сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-124">Получает описание оборудования, связанного с устройством.</span><span class="sxs-lookup"><span data-stu-id="30b6b-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="30b6b-125">Устройства должны предоставлять описание, которое определяет как драйвер, так и используемое оборудование.</span><span class="sxs-lookup"><span data-stu-id="30b6b-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="30b6b-126">Следующие дополнительные флаги применяются к типу устройства **кдаудио** :</span><span class="sxs-lookup"><span data-stu-id="30b6b-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_ \_ удостоверение носителя сведений MCI \_</span><span class="sxs-lookup"><span data-stu-id="30b6b-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-128">Создает уникальный идентификатор для аудио компакт-диска, который в данный момент загружен в запрашиваемый проигрыватель.</span><span class="sxs-lookup"><span data-stu-id="30b6b-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="30b6b-129">Этот флаг возвращает строку из 16 шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="30b6b-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>\_сведения о MCI \_ мультимедиа \_ UPC</span><span class="sxs-lookup"><span data-stu-id="30b6b-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-131">Создает универсальный код продукта (UPC), закодированный на аудио компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="30b6b-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="30b6b-132">UPC — это строка цифр.</span><span class="sxs-lookup"><span data-stu-id="30b6b-132">The UPC is a string of digits.</span></span> <span data-ttu-id="30b6b-133">Она может быть недоступна для всех компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="30b6b-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="30b6b-134">Следующие дополнительные флаги применяются к типу устройства **дигиталвидео** :</span><span class="sxs-lookup"><span data-stu-id="30b6b-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_ \_ информационный элемент MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="30b6b-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-136">Константа, указывающая требуемую информацию, включается в элемент **двитем** структуры, определенной параметром *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="30b6b-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="30b6b-137">Для устройств с цифровыми видео определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="30b6b-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>Потоковая подпрограмма MCI \_ ДГВ \_ info \_ \_</span><span class="sxs-lookup"><span data-stu-id="30b6b-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-139">Возвращает имя для текущего алгоритма сжатия звука.</span><span class="sxs-lookup"><span data-stu-id="30b6b-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>\_ \_ \_ качество звука MCI ДГВ \_ info</span><span class="sxs-lookup"><span data-stu-id="30b6b-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-141">Возвращает имя текущего дескриптора качества звука.</span><span class="sxs-lookup"><span data-stu-id="30b6b-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>\_сведения ДГВ \_ MCI \_ все еще работают \_</span><span class="sxs-lookup"><span data-stu-id="30b6b-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-143">Возвращает имя текущего алгоритма сжатия изображений.</span><span class="sxs-lookup"><span data-stu-id="30b6b-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>\_ \_ \_ по-прежнему качество информации ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-145">Возвращает имя текущего дескриптора качества изображения.</span><span class="sxs-lookup"><span data-stu-id="30b6b-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_ \_ сведения \_ об использовании MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="30b6b-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-147">Возвращает строку, описывающую ограничения использования, которые могут быть накладываются владельцем визуальных или звуковых данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="30b6b-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>\_устройство MCI ДГВ \_ сведения о \_ \_ видеоалгоритме</span><span class="sxs-lookup"><span data-stu-id="30b6b-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-149">Возвращает имя для текущего алгоритма сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="30b6b-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_ \_ \_ качество видео о ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-151">Возвращает имя текущего дескриптора качества видео.</span><span class="sxs-lookup"><span data-stu-id="30b6b-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_версия сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-153">Возвращает уровень выпуска драйвера и оборудования устройства.</span><span class="sxs-lookup"><span data-stu-id="30b6b-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="30b6b-154">Разработчики драйверов устройств должны документировать синтаксис возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="30b6b-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_ \_ информационный текст MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="30b6b-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-156">Получает заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="30b6b-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_файл сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-158">Получает путь и имя файла последнего файла, указанного с помощью команды [MCI \_ Open](mci-open.md) или [MCI \_ Load](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="30b6b-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="30b6b-159">Если файл не указан, устройство возвращает строку, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="30b6b-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="30b6b-160">Этот флаг поддерживается только устройствами, которые возвращают **значение true** параметру MCI \_ жетдевкапс \_ использует файлы, \_ флаг команды [MCI \_ жетдевкапс](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="30b6b-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="30b6b-161">Для устройств с цифровыми видео *lpInfo* указывает на структуру [**\_ \_ \_ пармс ДГВ info**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="30b6b-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="30b6b-162">Следующие дополнительные флаги применяются к типу устройства **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="30b6b-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_сведения \_ об авторских правах на MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-164">Получает уведомление об авторских правах на файл MIDI из мета события об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="30b6b-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_файл сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-166">Получает имя файла текущего файла.</span><span class="sxs-lookup"><span data-stu-id="30b6b-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="30b6b-167">Этот флаг поддерживается только устройствами, которые возвращают **значение true** при вызове команды [MCI \_ ЖЕТДЕВКАПС](mci-getdevcaps.md) с \_ флагом MCI жетдевкапс \_ использует \_ файлы.</span><span class="sxs-lookup"><span data-stu-id="30b6b-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>\_имя сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-169">Получает имя последовательности из мета-события Sequence/Track Name.</span><span class="sxs-lookup"><span data-stu-id="30b6b-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="30b6b-170">К типу устройства **видеомагнитофона** применяется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="30b6b-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_сведения о видеомагнитофоне MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="30b6b-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-172">Задает элемент **лпстрретурн** структуры [**\_ \_ пармс MCI**](mci-info-parms.md) , указывающий на номер версии.</span><span class="sxs-lookup"><span data-stu-id="30b6b-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="30b6b-173">Также задает элемент **двретсизе** , равный длине строки, на которую указывает.</span><span class="sxs-lookup"><span data-stu-id="30b6b-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="30b6b-174">Следующие дополнительные флаги применяются к типу устройства **наложения** .</span><span class="sxs-lookup"><span data-stu-id="30b6b-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_файл сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-176">Получает имя файла текущего файла.</span><span class="sxs-lookup"><span data-stu-id="30b6b-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="30b6b-177">Этот флаг поддерживается только устройствами, которые возвращают **значение true** параметру MCI \_ жетдевкапс \_ использует файлы, \_ флаг команды [MCI \_ жетдевкапс](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="30b6b-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_ \_ информационный текст MCI \_ овли</span><span class="sxs-lookup"><span data-stu-id="30b6b-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-179">Получает заголовок окна, связанного с устройством наложения видео.</span><span class="sxs-lookup"><span data-stu-id="30b6b-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="30b6b-180">Следующие дополнительные флаги применяются к типу устройства **вавеаудио** :</span><span class="sxs-lookup"><span data-stu-id="30b6b-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="30b6b-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_файл сведений \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-182">Получает имя файла текущего файла.</span><span class="sxs-lookup"><span data-stu-id="30b6b-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="30b6b-183">Этот флаг поддерживается устройствами, которые возвращают **значение true** при вызове команды [MCI \_ ЖЕТДЕВКАПС](mci-getdevcaps.md) с \_ флагом MCI жетдевкапс \_ использует \_ файлы.</span><span class="sxs-lookup"><span data-stu-id="30b6b-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_звуковые \_ входные данные MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-185">Получает имя продукта для текущих входных данных.</span><span class="sxs-lookup"><span data-stu-id="30b6b-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="30b6b-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_звуковые \_ выходные данные MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="30b6b-187">Получает имя продукта для текущего вывода, а его значение — для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="30b6b-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30b6b-188">Требования</span><span class="sxs-lookup"><span data-stu-id="30b6b-188">Requirements</span></span>



| <span data-ttu-id="30b6b-189">Требование</span><span class="sxs-lookup"><span data-stu-id="30b6b-189">Requirement</span></span> | <span data-ttu-id="30b6b-190">Значение</span><span class="sxs-lookup"><span data-stu-id="30b6b-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b6b-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30b6b-191">Minimum supported client</span></span><br/> | <span data-ttu-id="30b6b-192">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30b6b-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30b6b-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30b6b-193">Minimum supported server</span></span><br/> | <span data-ttu-id="30b6b-194">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30b6b-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="30b6b-195">Заголовок</span><span class="sxs-lookup"><span data-stu-id="30b6b-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b6b-196"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30b6b-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b6b-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30b6b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b6b-198">MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="30b6b-199">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="30b6b-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

