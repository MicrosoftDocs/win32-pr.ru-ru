---
title: Команда MCI_SETAUDIO (Ммсистем. h)
description: Команда MCI \_ сетаудио задает значения, связанные с воспроизведением и записью звука. Эта команда распознает устройства цифрового видео и ВИДЕОМАГНИТОФОНА.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262215"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="c828b-105">\_Команда MCI сетаудио</span><span class="sxs-lookup"><span data-stu-id="c828b-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="c828b-106">Команда MCI \_ сетаудио задает значения, связанные с воспроизведением и записью звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="c828b-107">Эта команда распознает устройства цифрового видео и ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="c828b-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="c828b-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c828b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="c828b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c828b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c828b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="c828b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c828b-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="c828b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c828b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c828b-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="c828b-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c828b-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c828b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c828b-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*лпсетаудио*</span><span class="sxs-lookup"><span data-stu-id="c828b-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="c828b-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c828b-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c828b-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="c828b-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c828b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c828b-118">Return Value</span></span>

<span data-ttu-id="c828b-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c828b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c828b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c828b-120">Remarks</span></span>

<span data-ttu-id="c828b-121">Следующие флаги применяются к типу устройства **дигиталвидео** :</span><span class="sxs-lookup"><span data-stu-id="c828b-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c828b-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ ДГВ \_ сетаудио \_ ALG</span><span class="sxs-lookup"><span data-stu-id="c828b-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="c828b-123">Элемент **лпстралгорисм** структуры, идентифицируемой *лпсетаудио* , содержит адрес буфера, содержащего имя алгоритма сжатия звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="c828b-124">Алгоритм сжатия используется последующими командами [ \_ резервирования MCI](mci-reserve.md) или [ \_ записи MCI](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="c828b-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="c828b-125">Доступные алгоритмы зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="c828b-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="c828b-126">Если алгоритм несовместим с текущим форматом файла, формат файла меняется на формат по умолчанию для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="c828b-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ ДГВ \_ сетаудио \_ клокктиме</span><span class="sxs-lookup"><span data-stu-id="c828b-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="c828b-128">Указанное время указывается в миллисекундах и является абсолютным временем при использовании MCI \_ ДГВ \_ сетаудио \_ .</span><span class="sxs-lookup"><span data-stu-id="c828b-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="c828b-129">(На этот раз это не пошаговое воспроизведение рабочей области.)</span><span class="sxs-lookup"><span data-stu-id="c828b-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="c828b-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_ \_ \_ входные данные сетаудио MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="c828b-131">Изменяет флаг басов, высоких частот или громкости, чтобы он влиял на входной сигнал и изменяет записываемые данные.</span><span class="sxs-lookup"><span data-stu-id="c828b-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="c828b-132">По возможности это значение по умолчанию при мониторинге входных данных.</span><span class="sxs-lookup"><span data-stu-id="c828b-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_ \_ элемент сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="c828b-134">Постоянная звуковая константа задается в элементе **двитем** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-135">Константа определяет заданное значение.</span><span class="sxs-lookup"><span data-stu-id="c828b-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="c828b-136">Определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="c828b-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="c828b-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ ДГВ \_ сетаудио \_ авгбитесперсек</span><span class="sxs-lookup"><span data-stu-id="c828b-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="c828b-138">Среднее число байтов указывается в элементе **дввалуе** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-139">Это значение задает среднее число байт в секунду для воспроизведения или записи в форматах PCM (модуляция импульсного кода) и ADPCM (адаптивный разностный код пульса).</span><span class="sxs-lookup"><span data-stu-id="c828b-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="c828b-140">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="c828b-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ ДГВ \_ сетаудио \_ НЧ</span><span class="sxs-lookup"><span data-stu-id="c828b-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="c828b-142">Уровень низкой частоты звука указывается как фактор в элементе **дввалуе** структуры, идентифицируемой *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ ДГВ \_ сетаудио \_ битсперсампле</span><span class="sxs-lookup"><span data-stu-id="c828b-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="c828b-144">Число битов на выборку указывается в элементе **дввалуе** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-145">Это значение задает число битов для каждого образца, которое воспроизводится или записывается в формате PCM.</span><span class="sxs-lookup"><span data-stu-id="c828b-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="c828b-146">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="c828b-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ ДГВ \_ сетаудио \_ блоккалигн</span><span class="sxs-lookup"><span data-stu-id="c828b-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="c828b-148">Выравнивание блока данных задается в элементе **дввалуе** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-149">Это значение задает выравнивание блоков данных относительно начала входных данных типа «волна».</span><span class="sxs-lookup"><span data-stu-id="c828b-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ ДГВ \_ сетаудио \_ самплесперсек</span><span class="sxs-lookup"><span data-stu-id="c828b-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="c828b-151">Частота выборки указывается в элементе **дввалуе** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-152">Это значение задает частоту выборки для воспроизведения и записи с помощью алгоритмов PCM и ADPCM.</span><span class="sxs-lookup"><span data-stu-id="c828b-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="c828b-153">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="c828b-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_ \_ источник сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="c828b-155">Константа, указывающая источник звукового ввода, включается в элемент **дввалуе** структуры, идентифицируемой *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-156">Для источников входных данных аудио определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="c828b-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="c828b-157">\_ \_ \_ среднее значение источника сетаудио MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="c828b-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="c828b-158">Среднее значение левого и правого звуковых каналов.</span><span class="sxs-lookup"><span data-stu-id="c828b-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="c828b-159">\_ \_ источник СЕТАУДИО ДГВ \_ MCI \_ слева</span><span class="sxs-lookup"><span data-stu-id="c828b-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="c828b-160">Левый канал звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-160">Left audio channel.</span></span>

<span data-ttu-id="c828b-161">\_источник сетаудио ДГВ MCI ( \_ \_ \_ справа)</span><span class="sxs-lookup"><span data-stu-id="c828b-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="c828b-162">Правый канал звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-162">Right audio channel.</span></span>

<span data-ttu-id="c828b-163">\_ \_ \_ источник стерео ДГВ сетаудио \_</span><span class="sxs-lookup"><span data-stu-id="c828b-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="c828b-164">Розетк.</span><span class="sxs-lookup"><span data-stu-id="c828b-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_ \_ поток сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="c828b-166">Звуковой поток указывается в элементе **дввалуе** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-167">Целочисленное значение указывает аудиопоток, воспроизводимый из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c828b-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="c828b-168">Если поток не указан, воспроизводится первый физически чередующийся аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="c828b-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ ДГВ \_ сетаудио \_ ВЧ</span><span class="sxs-lookup"><span data-stu-id="c828b-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="c828b-170">Уровень высокой частоты звука указывается как фактор в элементе **дввалуе** структуры, идентифицируемой *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_ \_ том сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="c828b-172">Уровень звука для одного или обоих звуковых каналов указывается как фактор в **дввалуе** члене структуры, идентифицируемой *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-173">Если для левого и правого томов заданы разные значения, то коэффициент слева направо будет примерно не изменен.</span><span class="sxs-lookup"><span data-stu-id="c828b-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_ДГВ MCI \_ сетаудио, \_ слева</span><span class="sxs-lookup"><span data-stu-id="c828b-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="c828b-175">Включает левый канал звука при использовании MCI со \_ значением \_ On.</span><span class="sxs-lookup"><span data-stu-id="c828b-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="c828b-176">Отключает левый канал звука при использовании с MCI, \_ установленным в \_ Off.</span><span class="sxs-lookup"><span data-stu-id="c828b-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="c828b-177">Если этот флаг используется вместе с сочетанием \_ \_ значения сетаудио MCI ДГВ \_ и MCI \_ ДГВ \_ сетаудио \_ Volume, он устанавливает громкость левого звукового канала.</span><span class="sxs-lookup"><span data-stu-id="c828b-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="c828b-178">Если этот флаг используется с \_ \_ источником ДГВ сетаудио MCI \_ , он указывает левый канал звука в качестве источника для входного дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="c828b-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ ДГВ \_ сетаудио \_</span><span class="sxs-lookup"><span data-stu-id="c828b-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="c828b-180">Параметр длины перехода включается в элемент **двовер** структуры, идентифицируемой *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-181">Значение length указывает время (в единицах текущего формата времени), которое должно быть необходимо для внесения изменений, использующих фактор.</span><span class="sxs-lookup"><span data-stu-id="c828b-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="c828b-182">Если этот флаг не используется, изменения происходят немедленно.</span><span class="sxs-lookup"><span data-stu-id="c828b-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_ \_ качество сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="c828b-184">Элемент **лпстркуалити** структуры, идентифицируемой *лпсетаудио* , содержит адрес буфера, определяющего качество звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="c828b-185">Текстовая строка в буфере определяет характеристики алгоритма сжатия звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="c828b-186">Для \_ \_ \_ выбора дескриптора качества для указанного алгоритма можно использовать флаг ДГВ сетаудио в MCI.</span><span class="sxs-lookup"><span data-stu-id="c828b-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="c828b-187">Если этот флаг опущен, используется текущий алгоритм.</span><span class="sxs-lookup"><span data-stu-id="c828b-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="c828b-188">Доступные имена алгоритмов и дескрипторов зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="c828b-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="c828b-189">Каждое устройство предоставляет документацию по доступным алгоритмам и описание применимых имен дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="c828b-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="c828b-190">Команда [ \_ качества MCI](mci-quality.md) может определять дополнительные имена дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="c828b-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_ \_ запись сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="c828b-192">Указывает, включает ли запись звуковые данные или исключает их.</span><span class="sxs-lookup"><span data-stu-id="c828b-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="c828b-193">Если в сочетании с MCI \_ задано значение \_ , звуковые данные записываются.</span><span class="sxs-lookup"><span data-stu-id="c828b-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="c828b-194">Если в сочетании с MCI \_ установлено значение \_ Off, звуковые данные исключаются.</span><span class="sxs-lookup"><span data-stu-id="c828b-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="c828b-195">По умолчанию используются звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="c828b-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ ДГВ \_ сетаудио \_ right</span><span class="sxs-lookup"><span data-stu-id="c828b-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="c828b-197">Включает правый канал звука при использовании MCI со \_ значением \_ On.</span><span class="sxs-lookup"><span data-stu-id="c828b-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="c828b-198">Отключает правый канал звука при использовании MCI со \_ значением \_ Off.</span><span class="sxs-lookup"><span data-stu-id="c828b-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="c828b-199">Если этот флаг используется вместе с сочетанием \_ \_ значения сетаудио MCI ДГВ \_ и MCI \_ ДГВ \_ сетаудио \_ Volume, он устанавливает громкость правильного звукового канала.</span><span class="sxs-lookup"><span data-stu-id="c828b-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_ \_ значение сетаудио MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="c828b-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="c828b-201">Значение задается в элементе **дввалуе** структуры, определенной параметром *лпсетаудио*.</span><span class="sxs-lookup"><span data-stu-id="c828b-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="c828b-202">Значение значения задается константой, определенной для \_ \_ флага элемента MCI ДГВ сетаудио \_ .</span><span class="sxs-lookup"><span data-stu-id="c828b-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="c828b-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="c828b-204">Отключает указанный канал звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="c828b-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="c828b-206">Включает указанный канал звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="c828b-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>\_ \_ выходные данные сетаудио MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="c828b-208">Изменяет флаг басов, высоких частот или громкости таким образом, чтобы он изменяет только Воспроизводимый сигнал, а не запись.</span><span class="sxs-lookup"><span data-stu-id="c828b-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="c828b-209">По возможности это значение по умолчанию при мониторинге входных данных.</span><span class="sxs-lookup"><span data-stu-id="c828b-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="c828b-210">Для устройств с цифровыми видео параметр *лпсетаудио* указывает на структуру [**MCI \_ ДГВ \_ сетаудио \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="c828b-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="c828b-211">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="c828b-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c828b-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_ \_ запись СЕТАУДИО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="c828b-213">Задает включение или выключение записи звука, которая используется в сочетании с одним из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="c828b-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="c828b-214">MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="c828b-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="c828b-215">Запись звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-215">Audio recording on.</span></span>

<span data-ttu-id="c828b-216">MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="c828b-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="c828b-217">Запись звука отключена.</span><span class="sxs-lookup"><span data-stu-id="c828b-217">Audio recording off.</span></span> <span data-ttu-id="c828b-218">Возможно, потребуется сначала отключить запись сборки (с помощью команды [MCI \_ ](mci-set.md) с установленным \_ \_ флагом сбора записей в НАБОРе видеомагнитофонов MCI, \_ \_ установленным в OFF), прежде чем запись звука будет отключена.</span><span class="sxs-lookup"><span data-stu-id="c828b-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="c828b-219">\_направление MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-219">MCI\_TRACK</span></span>

<span data-ttu-id="c828b-220">Элемент **двтракк** структуры, определяемой параметром *лпсетаудио* , указывает, на какую запись влияет команда.</span><span class="sxs-lookup"><span data-stu-id="c828b-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="c828b-221">\_ \_ источник СЕТАУДИО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="c828b-222">Задает источник звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-222">Sets the audio source.</span></span> <span data-ttu-id="c828b-223">Этот флаг должен использоваться с \_ \_ флагом, СЕТАУДИО видеомагнитофона MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c828b-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="c828b-224">\_ \_ монитор СЕТАУДИО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="c828b-225">Задает монитор источника звука.</span><span class="sxs-lookup"><span data-stu-id="c828b-225">Sets the audio source monitor.</span></span> <span data-ttu-id="c828b-226">Этот флаг должен использоваться с \_ \_ флагом, СЕТАУДИО видеомагнитофона MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c828b-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="c828b-227">\_сетаудио ВИДЕОМАГНИТОФОН \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="c828b-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="c828b-228">Элемент **двто** структуры, идентифицируемой *лпсетаудио* , содержит константу, описывающую тип входных данных или наблюдаемых входных данных.</span><span class="sxs-lookup"><span data-stu-id="c828b-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="c828b-229">Он должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="c828b-229">It must be one of the following:</span></span>

<span data-ttu-id="c828b-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="c828b-230"><dl> <dd></span></span>

<span data-ttu-id="c828b-231">средство \_ \_ \_ настройки типа src \_ видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="c828b-232">Тип — тюнер.</span><span class="sxs-lookup"><span data-stu-id="c828b-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="c828b-233">\_ \_ \_ Строка типа src видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="c828b-234">Тип — Line.</span><span class="sxs-lookup"><span data-stu-id="c828b-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="c828b-235">\_ \_ \_ дополнительный тип src видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="c828b-236">Тип — вспомогательный.</span><span class="sxs-lookup"><span data-stu-id="c828b-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="c828b-237">\_ \_ тип src видеомагнитофона MCI \_ типа \_ универсальный</span><span class="sxs-lookup"><span data-stu-id="c828b-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="c828b-238">Тип является универсальным.</span><span class="sxs-lookup"><span data-stu-id="c828b-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="c828b-239">\_выкл. \_ \_ тип src видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="c828b-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="c828b-240">Тип — выкл.</span><span class="sxs-lookup"><span data-stu-id="c828b-240">Type is mute.</span></span> <span data-ttu-id="c828b-241">Его можно использовать только с \_ \_ \_ флагом источника сетаудио видеомагнитофона MCI.</span><span class="sxs-lookup"><span data-stu-id="c828b-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="c828b-242">\_ \_ \_ выходные данные типа src видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="c828b-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="c828b-243">Тип — Output.</span><span class="sxs-lookup"><span data-stu-id="c828b-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="c828b-244">\_ \_ номер СЕТАУДИО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="c828b-245">Элемент Двнумбер структуры, идентифицируемой Лпсетаудио, содержит входной звук (для типа, указанного в элементе Двто) для использования.</span><span class="sxs-lookup"><span data-stu-id="c828b-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="c828b-246">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпсетаудио* указывает на структуру [**\_ видеомагнитофона MCI \_ сетаудио \_ пармс**](mci-vcr-setaudio-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c828b-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c828b-247">Требования</span><span class="sxs-lookup"><span data-stu-id="c828b-247">Requirements</span></span>



| <span data-ttu-id="c828b-248">Требование</span><span class="sxs-lookup"><span data-stu-id="c828b-248">Requirement</span></span> | <span data-ttu-id="c828b-249">Значение</span><span class="sxs-lookup"><span data-stu-id="c828b-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c828b-250">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c828b-250">Minimum supported client</span></span><br/> | <span data-ttu-id="c828b-251">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c828b-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c828b-252">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c828b-252">Minimum supported server</span></span><br/> | <span data-ttu-id="c828b-253">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c828b-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c828b-254">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c828b-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="c828b-255"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c828b-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c828b-256">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c828b-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c828b-257">MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c828b-258">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="c828b-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

