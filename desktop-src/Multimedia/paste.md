---
title: вставить команду
description: Команда Вставить копирует содержимое буфера обмена в рабочую область. Устройство Digital-Video распознает эту команду.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- Команда "вставить" мультимедиа Windows
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071310"
---
# <a name="paste-command"></a><span data-ttu-id="d2b9f-105">вставить команду</span><span class="sxs-lookup"><span data-stu-id="d2b9f-105">paste command</span></span>

<span data-ttu-id="d2b9f-106">Команда Вставить копирует содержимое буфера обмена в рабочую область.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="d2b9f-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d2b9f-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d2b9f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2b9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b9f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="d2b9f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d2b9f-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d2b9f-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d2b9f-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*лпсзитем*</span><span class="sxs-lookup"><span data-stu-id="d2b9f-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="d2b9f-114">Один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-114">One or more of the following flags.</span></span>



| <span data-ttu-id="d2b9f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d2b9f-115">Value</span></span>                 | <span data-ttu-id="d2b9f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d2b9f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b9f-117">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="d2b9f-117">at *rectangle*</span></span>        | <span data-ttu-id="d2b9f-118">Задает расположение в кадре, куда вставляются данные.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="d2b9f-119">Верхний левый угол *прямоугольника* соответствует левому верхнему углу добавленных данных.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="d2b9f-120">Если прямоугольник имеет ненулевой размер в X или Y, содержимое буфера обмена масштабируется в этих измерениях при их вставлении в кадр.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="d2b9f-121">Если этот параметр опущен, *прямоугольником* по умолчанию выделяется весь фрейм.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="d2b9f-122">Если этот флаг указан в режиме "вставить" (по умолчанию), то любой регион за пределами прямоугольника закрашивается сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="d2b9f-123">*поток* аудиопотока</span><span class="sxs-lookup"><span data-stu-id="d2b9f-123">audio stream *stream*</span></span> | <span data-ttu-id="d2b9f-124">Указывает аудиопоток в рабочей области, затронутой командой.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="d2b9f-125">Если в буфере обмена существует только один звуковой поток, звуковые данные вставляются в указанный *поток*.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="d2b9f-126">Если в буфере обмена существует более одного звукового потока, *поток* указывает начальное число для последовательностей потока.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d2b9f-127">Если вы используете этот флаг, а также хотите вставить видео, необходимо также использовать флаг "поток видео".</span><span class="sxs-lookup"><span data-stu-id="d2b9f-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="d2b9f-128">(Если ни один из флагов не указан, вставляются все аудио-и видеопотоки и сохраняются их исходные номера потоков.)</span><span class="sxs-lookup"><span data-stu-id="d2b9f-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="d2b9f-129">insert</span><span class="sxs-lookup"><span data-stu-id="d2b9f-129">insert</span></span>                | <span data-ttu-id="d2b9f-130">Указывает, что данные вставляются в рабочую область.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="d2b9f-131">Все данные после точки вставки перемещаются в рабочую область вперед, чтобы освободить место.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="d2b9f-132">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d2b9f-133">перезапись</span><span class="sxs-lookup"><span data-stu-id="d2b9f-133">overwrite</span></span>             | <span data-ttu-id="d2b9f-134">Указывает, что данные копируются в рабочую область путем записи всех существующих данных после точки вставки.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="d2b9f-135">Флаги "Insert" и "overwrite" влияют на то, будут ли во время операции вставки кадры уничтожены или перемещены, а не как данные вставляются в пределах каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="d2b9f-136">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="d2b9f-136">to *position*</span></span>         | <span data-ttu-id="d2b9f-137">Указывает позиции в рабочей области, в которую вставляются данные.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="d2b9f-138">Если этот параметр опущен, по умолчанию используется текущая заданная позицией.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d2b9f-139">*поток* видео поток</span><span class="sxs-lookup"><span data-stu-id="d2b9f-139">video stream *stream*</span></span> | <span data-ttu-id="d2b9f-140">Указывает поток видео в рабочей области, на который влияет команда.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="d2b9f-141">Если в буфере обмена существует только один видеопоток, данные видео вставляются в указанный *поток*.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="d2b9f-142">Если в буфере обмена существует более одного видеопотока, *поток* указывает начальное число для последовательностей потока.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d2b9f-143">Если вы используете этот флаг, а также хотите вставить звук, необходимо также использовать флаг "Audio Stream".</span><span class="sxs-lookup"><span data-stu-id="d2b9f-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="d2b9f-144">(Если ни один из флагов не указан, вставляются все аудио-и видеопотоки и сохраняются их исходные номера потоков.)</span><span class="sxs-lookup"><span data-stu-id="d2b9f-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="d2b9f-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="d2b9f-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d2b9f-146">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d2b9f-147">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d2b9f-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b9f-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2b9f-148">Return Value</span></span>

<span data-ttu-id="d2b9f-149">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2b9f-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2b9f-150">Remarks</span></span>

<span data-ttu-id="d2b9f-151">В данных, скопированных из буфера обмена, отсутствуют сигналы.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="d2b9f-152">Изменение становится постоянным только при явном сохранении данных. Однако воспроизведение действует так, как если бы данные были добавлены.</span><span class="sxs-lookup"><span data-stu-id="d2b9f-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b9f-153">Требования</span><span class="sxs-lookup"><span data-stu-id="d2b9f-153">Requirements</span></span>



| <span data-ttu-id="d2b9f-154">Требование</span><span class="sxs-lookup"><span data-stu-id="d2b9f-154">Requirement</span></span> | <span data-ttu-id="d2b9f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d2b9f-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2b9f-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2b9f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b9f-157">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2b9f-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2b9f-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2b9f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b9f-159">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2b9f-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d2b9f-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2b9f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b9f-161">MCI</span><span class="sxs-lookup"><span data-stu-id="d2b9f-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d2b9f-162">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="d2b9f-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

