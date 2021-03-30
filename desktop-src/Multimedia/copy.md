---
title: команда copy
description: Команда Copy копирует данные в буфер обмена. Устройство Digital-Video распознает эту команду.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- копирование команд мультимедиа Windows
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801523"
---
# <a name="copy-command"></a><span data-ttu-id="0fde2-105">команда copy</span><span class="sxs-lookup"><span data-stu-id="0fde2-105">copy command</span></span>

<span data-ttu-id="0fde2-106">Команда Copy копирует данные в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="0fde2-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="0fde2-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="0fde2-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="0fde2-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0fde2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0fde2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fde2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fde2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="0fde2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0fde2-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="0fde2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0fde2-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="0fde2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0fde2-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*лпсзитем*</span><span class="sxs-lookup"><span data-stu-id="0fde2-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="0fde2-114">Один из следующих флагов, определяющих копируемый элемент.</span><span class="sxs-lookup"><span data-stu-id="0fde2-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="0fde2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0fde2-115">Value</span></span>                 | <span data-ttu-id="0fde2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0fde2-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fde2-117">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="0fde2-117">at *rectangle*</span></span>        | <span data-ttu-id="0fde2-118">Указывает часть каждого кадра, который будет скопирован.</span><span class="sxs-lookup"><span data-stu-id="0fde2-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="0fde2-119">Если этот параметр опущен, по умолчанию используется весь фрейм.</span><span class="sxs-lookup"><span data-stu-id="0fde2-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="0fde2-120">*поток* аудиопотока</span><span class="sxs-lookup"><span data-stu-id="0fde2-120">audio stream *stream*</span></span> | <span data-ttu-id="0fde2-121">Указывает аудиопоток в рабочей области, затронутой командой.</span><span class="sxs-lookup"><span data-stu-id="0fde2-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="0fde2-122">Если вы используете этот флаг, а также хотите скопировать видео, необходимо также использовать флаг "поток видео".</span><span class="sxs-lookup"><span data-stu-id="0fde2-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="0fde2-123">(Если ни один из флагов не указан, копируются все потоки аудио и видео.)</span><span class="sxs-lookup"><span data-stu-id="0fde2-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="0fde2-124">от *расположения*</span><span class="sxs-lookup"><span data-stu-id="0fde2-124">from *position*</span></span>       | <span data-ttu-id="0fde2-125">Задает начало копируемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="0fde2-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="0fde2-126">Если этот параметр опущен, то значение по умолчанию равно текущему положению.</span><span class="sxs-lookup"><span data-stu-id="0fde2-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="0fde2-127">в *Расположение*</span><span class="sxs-lookup"><span data-stu-id="0fde2-127">to *position*</span></span>         | <span data-ttu-id="0fde2-128">Задает конец копируемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="0fde2-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="0fde2-129">Скопированные аудио и видео данные являются исключительно этой позицией.</span><span class="sxs-lookup"><span data-stu-id="0fde2-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="0fde2-130">Если этот параметр опущен, то значение по умолчанию — конец рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0fde2-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="0fde2-131">*поток* видео поток</span><span class="sxs-lookup"><span data-stu-id="0fde2-131">video stream *stream*</span></span> | <span data-ttu-id="0fde2-132">Указывает поток видео в рабочей области, на который влияет команда.</span><span class="sxs-lookup"><span data-stu-id="0fde2-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="0fde2-133">Если вы используете этот флаг, а также хотите скопировать аудио, необходимо также использовать флаг "Audio Stream".</span><span class="sxs-lookup"><span data-stu-id="0fde2-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="0fde2-134">(Если ни один из флагов не указан, копируются все потоки аудио и видео.)</span><span class="sxs-lookup"><span data-stu-id="0fde2-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="0fde2-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="0fde2-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0fde2-136">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="0fde2-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="0fde2-137">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0fde2-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fde2-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fde2-138">Return Value</span></span>

<span data-ttu-id="0fde2-139">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0fde2-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fde2-140">Требования</span><span class="sxs-lookup"><span data-stu-id="0fde2-140">Requirements</span></span>



| <span data-ttu-id="0fde2-141">Требование</span><span class="sxs-lookup"><span data-stu-id="0fde2-141">Requirement</span></span> | <span data-ttu-id="0fde2-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0fde2-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0fde2-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fde2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0fde2-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0fde2-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0fde2-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fde2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0fde2-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0fde2-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0fde2-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fde2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fde2-148">MCI</span><span class="sxs-lookup"><span data-stu-id="0fde2-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0fde2-149">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="0fde2-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

