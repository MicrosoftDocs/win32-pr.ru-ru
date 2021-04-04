---
title: Команда "вырезать"
description: Команда Cut удаляет данные из рабочей области и копирует их в буфер обмена. Устройство Digital-Video распознает эту команду.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- Вырезание команды мультимедиа Windows
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989162"
---
# <a name="cut-command"></a><span data-ttu-id="ba052-105">Команда "вырезать"</span><span class="sxs-lookup"><span data-stu-id="ba052-105">cut command</span></span>

<span data-ttu-id="ba052-106">Команда Cut удаляет данные из рабочей области и копирует их в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="ba052-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="ba052-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="ba052-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ba052-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ba052-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ba052-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba052-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba052-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="ba052-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ba052-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="ba052-111">Identifier of an MCI device.</span></span> <span data-ttu-id="ba052-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="ba052-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ba052-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*лпсзитем*</span><span class="sxs-lookup"><span data-stu-id="ba052-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="ba052-114">Один из следующих флагов, определяющих элемент для вырезания.</span><span class="sxs-lookup"><span data-stu-id="ba052-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="ba052-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ba052-115">Value</span></span>                 | <span data-ttu-id="ba052-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ba052-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba052-117">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="ba052-117">at *rectangle*</span></span>        | <span data-ttu-id="ba052-118">Задает часть каждого кадра, которая вырезается.</span><span class="sxs-lookup"><span data-stu-id="ba052-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="ba052-119">Если этот параметр опущен, по умолчанию используется весь кадр.</span><span class="sxs-lookup"><span data-stu-id="ba052-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="ba052-120">Если этот элемент указан, рамки не удаляются.</span><span class="sxs-lookup"><span data-stu-id="ba052-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="ba052-121">Вместо этого область внутри прямоугольника становится черным.</span><span class="sxs-lookup"><span data-stu-id="ba052-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="ba052-122">*поток* аудиопотока</span><span class="sxs-lookup"><span data-stu-id="ba052-122">audio stream *stream*</span></span> | <span data-ttu-id="ba052-123">Указывает аудиопоток в рабочей области, затронутой командой.</span><span class="sxs-lookup"><span data-stu-id="ba052-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="ba052-124">Если вы используете этот флаг, а также хотите вырезать видео, необходимо также использовать флаг "поток видео".</span><span class="sxs-lookup"><span data-stu-id="ba052-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="ba052-125">(Если ни один из флагов не указан, все потоки аудио и видео будут обрезаны.)</span><span class="sxs-lookup"><span data-stu-id="ba052-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="ba052-126">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="ba052-126">from *position*</span></span>       | <span data-ttu-id="ba052-127">Указывает начало диапазона для вырезания.</span><span class="sxs-lookup"><span data-stu-id="ba052-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="ba052-128">Если этот параметр опущен, по умолчанию используется текущая заданная позицией.</span><span class="sxs-lookup"><span data-stu-id="ba052-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="ba052-129">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="ba052-129">to *position*</span></span>         | <span data-ttu-id="ba052-130">Задает конец диапазона для вырезания.</span><span class="sxs-lookup"><span data-stu-id="ba052-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="ba052-131">Данные аудио и видео выводятся исключительно из этой должности.</span><span class="sxs-lookup"><span data-stu-id="ba052-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="ba052-132">Если этот параметр опущен, по умолчанию используется конец рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ba052-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="ba052-133">*поток* видео поток</span><span class="sxs-lookup"><span data-stu-id="ba052-133">video stream *stream*</span></span> | <span data-ttu-id="ba052-134">Указывает поток видео в рабочей области, на который влияет команда.</span><span class="sxs-lookup"><span data-stu-id="ba052-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="ba052-135">Если вы используете этот флаг, а также хотите вырезать звук, необходимо также использовать флаг "Audio Stream".</span><span class="sxs-lookup"><span data-stu-id="ba052-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="ba052-136">(Если ни один из флагов не указан, все потоки аудио и видео будут обрезаны.)</span><span class="sxs-lookup"><span data-stu-id="ba052-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="ba052-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="ba052-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ba052-138">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="ba052-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="ba052-139">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ba052-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba052-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba052-140">Return Value</span></span>

<span data-ttu-id="ba052-141">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ba052-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba052-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba052-142">Remarks</span></span>

<span data-ttu-id="ba052-143">Изменение становится постоянным только при явном сохранении данных. Однако воспроизведение действует так, как если бы данные были удалены.</span><span class="sxs-lookup"><span data-stu-id="ba052-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba052-144">Требования</span><span class="sxs-lookup"><span data-stu-id="ba052-144">Requirements</span></span>



| <span data-ttu-id="ba052-145">Требование</span><span class="sxs-lookup"><span data-stu-id="ba052-145">Requirement</span></span> | <span data-ttu-id="ba052-146">Значение</span><span class="sxs-lookup"><span data-stu-id="ba052-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ba052-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba052-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ba052-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ba052-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ba052-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba052-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ba052-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ba052-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ba052-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba052-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba052-152">MCI</span><span class="sxs-lookup"><span data-stu-id="ba052-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ba052-153">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="ba052-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

