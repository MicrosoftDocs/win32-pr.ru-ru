---
title: Команда MCI_SET (Ммсистем. h)
description: Команда MCI \_ Set задает сведения об устройстве. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск, наложение видео и аудио-файлы.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "105674511"
---
# <a name="mci_set-command"></a><span data-ttu-id="56ce0-105">\_Команда MCI Set</span><span class="sxs-lookup"><span data-stu-id="56ce0-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="56ce0-106">Обмен данными без смещения — Корпорация Майкрософт поддерживает различные и включенные среды.</span><span class="sxs-lookup"><span data-stu-id="56ce0-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="56ce0-107">В этом документе есть ссылки на слово "Slave".</span><span class="sxs-lookup"><span data-stu-id="56ce0-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="56ce0-108">В соответствии с руководством корпорации Майкрософт в [стиле Bias-Freeного обмена данными](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) это слово является исключаемым.</span><span class="sxs-lookup"><span data-stu-id="56ce0-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="56ce0-109">Это слово используется в том виде, в котором оно используется в командах.</span><span class="sxs-lookup"><span data-stu-id="56ce0-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="56ce0-110">Для обеспечения согласованности этот документ содержит это слово.</span><span class="sxs-lookup"><span data-stu-id="56ce0-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="56ce0-111">При изменении этого слова в командах будет исправлен этот документ в выравнивании.</span><span class="sxs-lookup"><span data-stu-id="56ce0-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="56ce0-112">Команда MCI \_ Set задает сведения об устройстве.</span><span class="sxs-lookup"><span data-stu-id="56ce0-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="56ce0-113">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск, наложение видео и аудио-файлы.</span><span class="sxs-lookup"><span data-stu-id="56ce0-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="56ce0-114">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="56ce0-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="56ce0-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="56ce0-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="56ce0-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-117">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="56ce0-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="56ce0-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-119">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="56ce0-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="56ce0-120">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="56ce0-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*лпсет*</span><span class="sxs-lookup"><span data-stu-id="56ce0-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-122">Указатель на структуру [**\_ \_ пармс набора MCI**](mci-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="56ce0-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="56ce0-123">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="56ce0-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ce0-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56ce0-124">Return Value</span></span>

<span data-ttu-id="56ce0-125">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="56ce0-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="56ce0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56ce0-126">Remarks</span></span>

<span data-ttu-id="56ce0-127">Следующие дополнительные флаги применяются ко всем устройствам, поддерживающим MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="56ce0-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>\_Установка \_ звука MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-129">Номер звукового канала включен в элемент Дваудио структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-130">Этот флаг следует использовать с параметром MCI \_ Set \_ On или \_ MCI \_ Off.</span><span class="sxs-lookup"><span data-stu-id="56ce0-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="56ce0-131">Чтобы указать номер канала, используйте одну из следующих констант:</span><span class="sxs-lookup"><span data-stu-id="56ce0-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ Set \_ Audio \_ ALL</span><span class="sxs-lookup"><span data-stu-id="56ce0-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-133">Все звуковые каналы.</span><span class="sxs-lookup"><span data-stu-id="56ce0-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>\_левая установка \_ звука \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-135">Левый канал.</span><span class="sxs-lookup"><span data-stu-id="56ce0-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>\_элемент MCI Set \_ Audio \_ right</span><span class="sxs-lookup"><span data-stu-id="56ce0-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-137">Правый канал.</span><span class="sxs-lookup"><span data-stu-id="56ce0-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>\_ \_ закрывается дверца набора MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-139">Закрывает медиа-обложку (если она есть).</span><span class="sxs-lookup"><span data-stu-id="56ce0-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>\_ \_ открыта дверца набора MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-141">Открывает мультимедийную обложку (если она есть).</span><span class="sxs-lookup"><span data-stu-id="56ce0-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-143">Отключает указанный видео или звуковой канал.</span><span class="sxs-lookup"><span data-stu-id="56ce0-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="56ce0-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-145">Включает указанный видео или звуковой канал.</span><span class="sxs-lookup"><span data-stu-id="56ce0-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_Формат времени, заданный MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-147">Параметр формата времени включается в элемент **двтимеформат** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-148">С этим флагом используются следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="56ce0-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_ \_ байты формата MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-150">В формате данных PCM (модуляции импульсного кода) изменяет описание элемента времени на bytes для ввода или вывода.</span><span class="sxs-lookup"><span data-stu-id="56ce0-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="56ce0-151">Распознается типом устройства **вавеаудио** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_кадры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-153">Последующие команды будут использовать фреймы.</span><span class="sxs-lookup"><span data-stu-id="56ce0-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="56ce0-154">Распознаются типами устройств **дигиталвидео**, **видеомагнитофона** и **видеодиск** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_Формат MCI \_ ХМс</span><span class="sxs-lookup"><span data-stu-id="56ce0-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-156">Изменяет формат времени на часы, минуты и секунды.</span><span class="sxs-lookup"><span data-stu-id="56ce0-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="56ce0-157">Распознаются типами устройств **видеомагнитофона** и **видеодиск** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>\_ \_ миллисекунды формата MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-159">Изменяет формат времени на миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="56ce0-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="56ce0-160">Распознается всеми типами устройств.</span><span class="sxs-lookup"><span data-stu-id="56ce0-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>формат MCI, \_ \_ MSF</span><span class="sxs-lookup"><span data-stu-id="56ce0-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-162">Изменяет формат времени на минуты, секунды и кадры.</span><span class="sxs-lookup"><span data-stu-id="56ce0-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="56ce0-163">Распознаются типами устройств **кдаудио** и **видеомагнитофона** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_примеры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-165">Изменяет формат времени на образцы для ввода или вывода.</span><span class="sxs-lookup"><span data-stu-id="56ce0-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="56ce0-166">Распознается типом устройства **вавеаудио** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Формат MCI \_ SMPTE \_ 24, \_ Формат MCI \_ SMPTE \_ 25 и формат MCI \_ \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="56ce0-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-168">Устанавливает формат времени: 24, 25 и 30 кадров SMPTE (обществом инженеров Motion и телевидения) соответственно.</span><span class="sxs-lookup"><span data-stu-id="56ce0-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="56ce0-169">Распознаются типами устройств **Sequencer** и **видеомагнитофона** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Формат MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="56ce0-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-171">Устанавливает формат времени равным 30 кадрам SMPTE.</span><span class="sxs-lookup"><span data-stu-id="56ce0-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="56ce0-172">Распознаются типами устройств **Sequencer** и **видеомагнитофона** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_Формат MCI \_ тмсф</span><span class="sxs-lookup"><span data-stu-id="56ce0-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-174">Изменяет формат времени на записи, минуты, секунды и кадры.</span><span class="sxs-lookup"><span data-stu-id="56ce0-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="56ce0-175">(MCI использует номера непрерывной записи.) Распознаются типами устройств **кдаудио** и **видеомагнитофона** .</span><span class="sxs-lookup"><span data-stu-id="56ce0-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>видеозапись MCI \_ Set \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-177">Устанавливает или отключает видеосигнал.</span><span class="sxs-lookup"><span data-stu-id="56ce0-177">Sets the video signal on or off.</span></span> <span data-ttu-id="56ce0-178">Этот флаг следует использовать с параметром MCI \_ Set \_ On или MCI \_ \_ Off.</span><span class="sxs-lookup"><span data-stu-id="56ce0-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="56ce0-179">Устройства, не имеющие видео, возвращают МЦИЕРР \_ НЕподдерживаемую \_ функцию.</span><span class="sxs-lookup"><span data-stu-id="56ce0-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="56ce0-180">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="56ce0-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ ДГВ \_ Set \_ FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="56ce0-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-182">Параметр формата файла включен в элемент **двфилеформат** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-183">Для устройств с цифровыми видео формат файла используется для сохранения или записи команд.</span><span class="sxs-lookup"><span data-stu-id="56ce0-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="56ce0-184">Если этот параметр опущен, то по умолчанию может быть задан формат драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="56ce0-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="56ce0-185">Если указанный формат файла конфликтует с текущим выбранным алгоритмом и качеством, то они будут заменены на значения по умолчанию для формата файла.</span><span class="sxs-lookup"><span data-stu-id="56ce0-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="56ce0-186">Определены следующие константы формата файла:</span><span class="sxs-lookup"><span data-stu-id="56ce0-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ ДГВ \_ FF \_ AVI</span><span class="sxs-lookup"><span data-stu-id="56ce0-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-188">Формат AVI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ ДГВ \_ FF \_ авсс</span><span class="sxs-lookup"><span data-stu-id="56ce0-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-190">Формат АВСС.</span><span class="sxs-lookup"><span data-stu-id="56ce0-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ ДГВ \_ FF \_ DIB</span><span class="sxs-lookup"><span data-stu-id="56ce0-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-192">Формат DIB.</span><span class="sxs-lookup"><span data-stu-id="56ce0-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ ДГВ \_ FF \_ JFIF</span><span class="sxs-lookup"><span data-stu-id="56ce0-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-194">Формат JFIF.</span><span class="sxs-lookup"><span data-stu-id="56ce0-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ ДГВ \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="56ce0-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-196">Формат JPEG.</span><span class="sxs-lookup"><span data-stu-id="56ce0-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ ДГВ \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="56ce0-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-198">Формат MPEG.</span><span class="sxs-lookup"><span data-stu-id="56ce0-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ ДГВ \_ FF \_ рдиб</span><span class="sxs-lookup"><span data-stu-id="56ce0-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-200">RLE DIB Format.</span><span class="sxs-lookup"><span data-stu-id="56ce0-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ ДГВ \_ FF \_ ржпег</span><span class="sxs-lookup"><span data-stu-id="56ce0-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-202">Формат РЖПЕГ.</span><span class="sxs-lookup"><span data-stu-id="56ce0-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>\_ДГВ MCI \_ Set \_ Поиск в \_ точности</span><span class="sxs-lookup"><span data-stu-id="56ce0-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-204">Задает формат, используемый для позиционирования.</span><span class="sxs-lookup"><span data-stu-id="56ce0-204">Sets the format used for positioning.</span></span> <span data-ttu-id="56ce0-205">Этот флаг следует использовать с параметром MCI \_ Set \_ On или \_ MCI \_ Off.</span><span class="sxs-lookup"><span data-stu-id="56ce0-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="56ce0-206">Если \_ для MCI задано значение \_ On, то воспроизведение или запись точно обращается к кадру, указанному с помощью MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="56ce0-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="56ce0-207">Это может добавить дополнительную задержку, если запрошенный кадр не является ключевым.</span><span class="sxs-lookup"><span data-stu-id="56ce0-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="56ce0-208">Если указан параметр MCI \_ \_ Off, устройство будет выполнять поиск по кадру, предшествующему запрошенному кадру.</span><span class="sxs-lookup"><span data-stu-id="56ce0-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="56ce0-209">Для некоторых файлов и устройств это может быть первый кадр файла.</span><span class="sxs-lookup"><span data-stu-id="56ce0-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="56ce0-210">Значение по умолчанию для этого флага зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="56ce0-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_ \_ скорость установки MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="56ce0-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-212">Параметр Speed включается в элемент **двспид** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-213">Скорость указывается как отношение между номинальной частотой кадров и требуемой частотой кадров, где Номинальная частота кадров определяется как 1000.</span><span class="sxs-lookup"><span data-stu-id="56ce0-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="56ce0-214">Половина скорости — 500, а двойная скорость — 2000.</span><span class="sxs-lookup"><span data-stu-id="56ce0-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="56ce0-215">Допустимый диапазон скорости зависит от устройства и, возможно, от файла.</span><span class="sxs-lookup"><span data-stu-id="56ce0-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_набор ДГВ \_ MCI \_ все еще</span><span class="sxs-lookup"><span data-stu-id="56ce0-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-217">При использовании с MCI \_ ДГВ \_ Set \_ FILEFORMAT набор MCI \_ устанавливает формат файла, используемый для команд записи.</span><span class="sxs-lookup"><span data-stu-id="56ce0-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="56ce0-218">Для устройств с цифровыми видео параметр *лпсет* указывает на структуру [**MCI \_ ДГВ \_ Set \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .</span><span class="sxs-lookup"><span data-stu-id="56ce0-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="56ce0-219">Для типа устройства **Sequencer** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="56ce0-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI \_ Seq \_ Формат \_ сонгптр</span><span class="sxs-lookup"><span data-stu-id="56ce0-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-221">Задает формат времени для единиц указателя песни.</span><span class="sxs-lookup"><span data-stu-id="56ce0-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_ \_ Мастер установки MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="56ce0-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-223">Задает секвенсор в качестве источника данных синхронизации и указывает, что тип синхронизации указан в элементе **двмастер** структуры, определенной параметром *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-224">МЦИСЕК возвращает МЦИЕРР \_ НЕподдерживаемую \_ функцию.</span><span class="sxs-lookup"><span data-stu-id="56ce0-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="56ce0-225">Для типа синхронизации определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="56ce0-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="56ce0-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-227">Программа Sequencer будет отсылать данные синхронизации формата MIDI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="56ce0-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-229">Программа Sequencer будет передавать данные синхронизации формата SMPTE.</span><span class="sxs-lookup"><span data-stu-id="56ce0-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ нет</span><span class="sxs-lookup"><span data-stu-id="56ce0-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-231">Программа Sequencer не будет передавать данные синхронизации.</span><span class="sxs-lookup"><span data-stu-id="56ce0-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>\_ \_ смещение набора MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="56ce0-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-233">Изменяет смещение SMPTE последовательности, заданную элементом **двоффсет** структуры, определенной параметром *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-234">Это влияет только на последовательности с типом деления SMPTE.</span><span class="sxs-lookup"><span data-stu-id="56ce0-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI \_ Seq \_ Set \_ Port</span><span class="sxs-lookup"><span data-stu-id="56ce0-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-236">Задает в качестве выходного порта MIDI последовательности, заданной идентификатором устройства MIDI, в элементе **двпорт** структуры, определенной параметром *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-237">Устройство закрывает предыдущий порт (если он есть) и пытается открыть и использовать новый порт.</span><span class="sxs-lookup"><span data-stu-id="56ce0-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="56ce0-238">В случае сбоя он возвращает ошибку и повторно открывает ранее использовавшийся порт (если он есть).</span><span class="sxs-lookup"><span data-stu-id="56ce0-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="56ce0-239">Для портов определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="56ce0-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ нет</span><span class="sxs-lookup"><span data-stu-id="56ce0-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-241">Закрывает ранее использовавшийся порт (если он есть).</span><span class="sxs-lookup"><span data-stu-id="56ce0-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="56ce0-242">Программа Sequencer работает точно так же, как если бы порт был открыт, за исключением того, что сообщение MIDI не отправляется.</span><span class="sxs-lookup"><span data-stu-id="56ce0-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_СОПОСТАВИТЕЛЬ MIDI</span><span class="sxs-lookup"><span data-stu-id="56ce0-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-244">Задает порт, Открытый для сопоставителя MIDI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ Set \_ Slave</span><span class="sxs-lookup"><span data-stu-id="56ce0-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-246">Задает Sequencer для получения данных синхронизации и указывает, что тип синхронизации указан в элементе **двславе** структуры, определенной параметром *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-247">МЦИСЕК возвращает МЦИЕРР \_ НЕподдерживаемую \_ функцию.</span><span class="sxs-lookup"><span data-stu-id="56ce0-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="56ce0-248">Для типа синхронизации определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="56ce0-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_файл MCI Seq \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-250">Задает секвенсор для получения данных синхронизации, содержащихся в файле MIDI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="56ce0-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-252">Задает секвенсор для получения данных синхронизации MIDI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ нет</span><span class="sxs-lookup"><span data-stu-id="56ce0-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-254">Задает для программы Sequencer игнорирование данных синхронизации в потоке MIDI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="56ce0-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-256">Задает Sequencer для получения данных синхронизации SMPTE.</span><span class="sxs-lookup"><span data-stu-id="56ce0-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ Seq \_ Set \_ темп</span><span class="sxs-lookup"><span data-stu-id="56ce0-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-258">Изменяет темп последовательности MIDI на, указанную элементом **двтемпо** структуры, на которую указывает *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="56ce0-259">Для последовательностей с типом деления ППКН, темп указывается в ритме в минуту; для последовательностей с типом деления SMPTE, темп указывается в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="56ce0-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="56ce0-260">Для устройств Sequencer параметр *лпсет* указывает на структуру [**MCI \_ Seq \_ Set \_ пармс**](mci-seq-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="56ce0-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="56ce0-261">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="56ce0-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_ \_ \_ запись сбора данных для видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-263">Задает устройство для записи в режимах сборки или вставки (если сборка отключена, вставка включена и наоборот).</span><span class="sxs-lookup"><span data-stu-id="56ce0-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="56ce0-264">Используйте с одним из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="56ce0-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="56ce0-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-266">Задает запись сборки в и отключает запись вставки.</span><span class="sxs-lookup"><span data-stu-id="56ce0-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="56ce0-267">Записывает все видео, аудио и временные дорожки.</span><span class="sxs-lookup"><span data-stu-id="56ce0-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-269">Задает отключение записи и включает вставку записи в.</span><span class="sxs-lookup"><span data-stu-id="56ce0-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="56ce0-270">Если запись сборки отключена, для записи можно выбрать отдельные дорожки видео, звука и времени.</span><span class="sxs-lookup"><span data-stu-id="56ce0-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_ \_ Установка часов видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-272">Элемент **двклокк** структуры, идентифицируемой *лпсет* , содержит новое время.</span><span class="sxs-lookup"><span data-stu-id="56ce0-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>\_ \_ \_ предварительное определение счетчика для видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-274">Элемент **двкаунтерформат** структуры, идентифицируемой *лпсет* , содержит константу, указывающую новый формат времени счетчика, который будет использоваться счетчиком состояния.</span><span class="sxs-lookup"><span data-stu-id="56ce0-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="56ce0-275">Список допустимых констант см \_ \_ . в разделе Формат времени MCI Set \_ в списке дополнительных флагов для этой команды.</span><span class="sxs-lookup"><span data-stu-id="56ce0-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_ \_ \_ значение счетчика "Установка видеомагнитофона MCI" \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-277">Элемент **двкаунтервалуе** структуры, идентифицируемой *лпсет* , содержит новое значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="56ce0-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_ \_ индекс набора видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-279">Элемент **двиндекс** структуры, идентифицируемой *лпсет* , содержит константу, указывающую на содержимое экрана на экране, и должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="56ce0-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_ \_ Счетчик индекса видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-281">Отображает счетчик.</span><span class="sxs-lookup"><span data-stu-id="56ce0-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_ \_ Дата индекса видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-283">Отображает дату.</span><span class="sxs-lookup"><span data-stu-id="56ce0-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_ \_ время индекса видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-285">Отображает время.</span><span class="sxs-lookup"><span data-stu-id="56ce0-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_временной код \_ индекса \_ видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-287">Отображает код времени.</span><span class="sxs-lookup"><span data-stu-id="56ce0-287">Displays timecode.</span></span>

<span data-ttu-id="56ce0-288">Дополнительные сведения см. в описании команды [MCI \_ index](mci-index.md) .</span><span class="sxs-lookup"><span data-stu-id="56ce0-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_ \_ \_ время ожидания приостановки установки видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-290">Элемент **двпаусетимеаут** структуры, идентифицируемой *лпсет* , содержит максимальную продолжительность команды Pause в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="56ce0-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>\_ \_ \_ длительность интервала перехода установки видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-292">Элемент **двпостроллдуратион** структуры, идентифицируемой *лпсет* , содержит длину видеокассеты (в текущем формате времени), необходимую для переноса данных в транспорт видеомагнитофона при выполнении команды остановки или приостановки.</span><span class="sxs-lookup"><span data-stu-id="56ce0-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_ \_ Установка питания видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-294">Задает включение или выключение питания.</span><span class="sxs-lookup"><span data-stu-id="56ce0-294">Sets the power on or off.</span></span> <span data-ttu-id="56ce0-295">Должен использоваться с одним из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="56ce0-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-297">Выключает питание.</span><span class="sxs-lookup"><span data-stu-id="56ce0-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="56ce0-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-299">Включает питание.</span><span class="sxs-lookup"><span data-stu-id="56ce0-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_ \_ Длительность предустановки видеомагнитофона видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-301">Элемент **двпрероллдуратион** структуры, идентифицируемой *лпсет* , содержит длину видеокассеты в текущем формате времени, необходимую для стабилизации выходных данных видеомагнитофона.</span><span class="sxs-lookup"><span data-stu-id="56ce0-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_ \_ Формат записи для набора видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-303">Элемент **дврекордформат** структуры, идентифицируемой *лпсет* , содержит константу, описывающую скорость записи, которая должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="56ce0-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_Формат видеомагнитофона MCI ( \_ \_ EP)</span><span class="sxs-lookup"><span data-stu-id="56ce0-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-305">Записи с медленным ускорением.</span><span class="sxs-lookup"><span data-stu-id="56ce0-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_Формат видеомагнитофона MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="56ce0-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-307">Записи со средней и медленной скоростью.</span><span class="sxs-lookup"><span data-stu-id="56ce0-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_Формат видеомагнитофона MCI \_ \_ SP</span><span class="sxs-lookup"><span data-stu-id="56ce0-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-309">Записи со стандартной скоростью.</span><span class="sxs-lookup"><span data-stu-id="56ce0-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_ \_ скорость установки видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-311">Элемент **двспид** структуры, идентифицируемой *лпсет* , содержит новое значение скорости, где 1000 — нормальная скорость, 2000 — двойная скорость, а 500 — половина скорости и т. д.</span><span class="sxs-lookup"><span data-stu-id="56ce0-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_ \_ Установка \_ длины ленты для видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-313">Элемент **двтапеленгс** структуры, идентифицируемой *лпсет* , содержит новую длину ленты при условии, что длина ленты не может быть обнаружена.</span><span class="sxs-lookup"><span data-stu-id="56ce0-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>видеомагнитофон для MCI \_ \_ задается \_ \_ режим времени</span><span class="sxs-lookup"><span data-stu-id="56ce0-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-315">Элемент **двтимемоде** структуры, идентифицируемой *лпсет* , содержит константу, указывающую на новый режим позиционирования времени.</span><span class="sxs-lookup"><span data-stu-id="56ce0-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="56ce0-316">Допустимы следующие константы:</span><span class="sxs-lookup"><span data-stu-id="56ce0-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_ \_ Счетчик времени видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-318">Заставляет устройство использовать только счетчик.</span><span class="sxs-lookup"><span data-stu-id="56ce0-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_ \_ Обнаружение времени видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-320">При каждом добавлении новой ленты в устройство или при изменении режима с не готового к работе устройство должно пытаться определить, доступен ли код времени на ленте.</span><span class="sxs-lookup"><span data-stu-id="56ce0-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="56ce0-321">Если доступен код времени, используйте код времени во всех последующих командах, задающих позиции.</span><span class="sxs-lookup"><span data-stu-id="56ce0-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="56ce0-322">В противном случае используйте счетчик.</span><span class="sxs-lookup"><span data-stu-id="56ce0-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>временной код \_ видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-324">Заставляет устройство использовать только код времени.</span><span class="sxs-lookup"><span data-stu-id="56ce0-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_ \_ Отслеживание набора видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-326">Настройка скорости транспортировки ленты ВИДЕОМАГНИТОФОНА с тонкой настройкой и должна использоваться с одним из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="56ce0-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_видеомагнитофон, \_ плюс</span><span class="sxs-lookup"><span data-stu-id="56ce0-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-328">Увеличивает скорость транспортировки на ленту.</span><span class="sxs-lookup"><span data-stu-id="56ce0-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>видеомагнитофон MCI \_ \_ минус</span><span class="sxs-lookup"><span data-stu-id="56ce0-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-330">Уменьшает скорость транспортировки на ленту.</span><span class="sxs-lookup"><span data-stu-id="56ce0-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_Сброс ВИДЕОМАГНИТОФОНА \_ MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-332">Возвращает настройку отслеживания в ноль.</span><span class="sxs-lookup"><span data-stu-id="56ce0-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="56ce0-333">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпсет* указывает на структуру [**\_ \_ \_ пармс набора видеомагнитофона MCI**](mci-vcr-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="56ce0-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="56ce0-334">С типом устройства **видеодиск** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="56ce0-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_ \_ запись формата MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="56ce0-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-336">Изменяет формат времени для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="56ce0-336">Changes the time format to tracks.</span></span> <span data-ttu-id="56ce0-337">MCI использует номера непрерывной записи.</span><span class="sxs-lookup"><span data-stu-id="56ce0-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="56ce0-338">С типом устройства **вавеаудио** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="56ce0-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="56ce0-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_звуковые \_ входные данные MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-340">Задает входные данные, используемые для записи в элемент **винпут** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_звуковые \_ выходные данные MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-342">Задает выходные данные, используемые для воспроизведения в элемент **ваутпут** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>\_анинпут, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-344">Для записи можно использовать любой звуковой ввод, совместимый с текущим форматом.</span><span class="sxs-lookup"><span data-stu-id="56ce0-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>\_анйоутпут, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-346">Для воспроизведения можно использовать любые выходные данные, совместимые с текущим форматом.</span><span class="sxs-lookup"><span data-stu-id="56ce0-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>\_авгбитесперсек, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-348">Задает байты в секунду, используемые для воспроизведения, записи и сохранения, в элемент **навгбитесперсек** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>\_битсперсампле, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-350">Задает бит на выборку, используемую для воспроизведения, записи и сохранения, в элемент **нбитсперсампле** формата данных PCM, идентифицируемого *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>\_блоккалигн, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-352">Задает выравнивание блока, используемого для воспроизведения, записи и сохранения, в элемент **нблоккалигн** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>каналы звукозаписи MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-354">Число каналов указывается в элементе **нчаннелс** структуры, определенной параметром *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>\_форматтаг, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-356">Задает тип формата, используемого для воспроизведения, записи и сохранения, в элемент **вформаттаг** структуры, идентифицируемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="56ce0-357">Указание формата ВОЛНового \_ \_ PCM меняет формат на PCM.</span><span class="sxs-lookup"><span data-stu-id="56ce0-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="56ce0-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>\_самплесперсек, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="56ce0-359">Задает выборку в секунду, используемую для воспроизведения, записи и сохранения, в элемент **нсамплесперсек** структуры, определяемой *лпсет*.</span><span class="sxs-lookup"><span data-stu-id="56ce0-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="56ce0-360">Для устройств с аудио-волнами параметр *лпсет* указывает на структуру [**\_ \_ \_ пармс набора**](mci-wave-set-parms.md) звукозаписи MCI.</span><span class="sxs-lookup"><span data-stu-id="56ce0-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="56ce0-361">При создании файла для хранения данных определяются некоторые свойства аудио-данных с волнами.</span><span class="sxs-lookup"><span data-stu-id="56ce0-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="56ce0-362">Эти свойства описывают, как данные структурированы в файле и не могут быть изменены после начала записи.</span><span class="sxs-lookup"><span data-stu-id="56ce0-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="56ce0-363">Эти свойства определяются в следующем списке флагов:</span><span class="sxs-lookup"><span data-stu-id="56ce0-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="56ce0-364">\_авгбитесперсек, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="56ce0-365">\_битсперсампле, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="56ce0-366">\_блоккалигн, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="56ce0-367">каналы звукозаписи MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="56ce0-368">\_форматтаг, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="56ce0-369">\_самплесперсек, \_ набор ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="56ce0-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="56ce0-370">Требования</span><span class="sxs-lookup"><span data-stu-id="56ce0-370">Requirements</span></span>



| <span data-ttu-id="56ce0-371">Требование</span><span class="sxs-lookup"><span data-stu-id="56ce0-371">Requirement</span></span> | <span data-ttu-id="56ce0-372">Значение</span><span class="sxs-lookup"><span data-stu-id="56ce0-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ce0-373">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56ce0-373">Minimum supported client</span></span><br/> | <span data-ttu-id="56ce0-374">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56ce0-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56ce0-375">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56ce0-375">Minimum supported server</span></span><br/> | <span data-ttu-id="56ce0-376">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56ce0-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56ce0-377">Заголовок</span><span class="sxs-lookup"><span data-stu-id="56ce0-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ce0-378"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56ce0-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ce0-379">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56ce0-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ce0-380">MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="56ce0-381">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="56ce0-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

