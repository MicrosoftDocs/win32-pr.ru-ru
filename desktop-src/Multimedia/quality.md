---
title: Quality, команда
description: Команда Quality определяет пользовательский уровень качества звука, видео или по-прежнему для сжатия данных изображения. Устройство Digital-Video распознает эту команду.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- Команда Quality Windows мультимедиа
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661971"
---
# <a name="quality-command"></a><span data-ttu-id="8de78-105">Quality, команда</span><span class="sxs-lookup"><span data-stu-id="8de78-105">quality command</span></span>

<span data-ttu-id="8de78-106">Команда Quality определяет пользовательский уровень качества звука, видео или по-прежнему для сжатия данных изображения.</span><span class="sxs-lookup"><span data-stu-id="8de78-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="8de78-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="8de78-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8de78-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="8de78-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8de78-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8de78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de78-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="8de78-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8de78-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="8de78-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8de78-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="8de78-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8de78-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*лпсзкуалити*</span><span class="sxs-lookup"><span data-stu-id="8de78-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="8de78-114">Один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="8de78-114">One or more of the following flags.</span></span> <span data-ttu-id="8de78-115">(Должен присутствовать один из трех флагов «аудио», «по-прежнему» и «Video».)</span><span class="sxs-lookup"><span data-stu-id="8de78-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="8de78-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8de78-116">Value</span></span>                 | <span data-ttu-id="8de78-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8de78-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de78-118">*алгоритм* алгоритма</span><span class="sxs-lookup"><span data-stu-id="8de78-118">algorithm *algorithm*</span></span> | <span data-ttu-id="8de78-119">Связывает уровень качества с указанным *алгоритмом*.</span><span class="sxs-lookup"><span data-stu-id="8de78-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="8de78-120">Этот *алгоритм* должен поддерживаться устройством и быть совместимым с используемым флагом "Audio", "по прежнему" или "видео".</span><span class="sxs-lookup"><span data-stu-id="8de78-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="8de78-121">Если этот параметр опущен, используется текущий алгоритм.</span><span class="sxs-lookup"><span data-stu-id="8de78-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="8de78-122">*имя* аудио</span><span class="sxs-lookup"><span data-stu-id="8de78-122">audio *name*</span></span>          | <span data-ttu-id="8de78-123">Указывает, что эта команда задает уровень качества "звук", определенный с помощью *имени*.</span><span class="sxs-lookup"><span data-stu-id="8de78-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="8de78-124">диалог</span><span class="sxs-lookup"><span data-stu-id="8de78-124">dialog</span></span>                | <span data-ttu-id="8de78-125">Запрашивает, что устройство отображает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8de78-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="8de78-126">Это диалоговое окно содержит зависящие от алгоритма поля, которые используются на внутреннем устройстве для создания структуры, описывающей конкретный уровень качества.</span><span class="sxs-lookup"><span data-stu-id="8de78-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="8de78-127">маркер *обработчика*</span><span class="sxs-lookup"><span data-stu-id="8de78-127">handle *handle*</span></span>       | <span data-ttu-id="8de78-128">Задает *маркер* структуры, содержащей зависящие от алгоритма данные, описывающие конкретный уровень качества.</span><span class="sxs-lookup"><span data-stu-id="8de78-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="8de78-129">Структуры для данных, на которые ссылается этот обработчик, относятся к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="8de78-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="8de78-130">*имя* по-прежнему</span><span class="sxs-lookup"><span data-stu-id="8de78-130">still *name*</span></span>          | <span data-ttu-id="8de78-131">Указывает, что команда задает уровень качества "все еще", обозначенный *именем.*</span><span class="sxs-lookup"><span data-stu-id="8de78-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="8de78-132">*имя* видео</span><span class="sxs-lookup"><span data-stu-id="8de78-132">video *name*</span></span>          | <span data-ttu-id="8de78-133">Указывает, что команда задает уровень качества "видео", определенный с помощью *имени*.</span><span class="sxs-lookup"><span data-stu-id="8de78-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="8de78-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="8de78-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8de78-135">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="8de78-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="8de78-136">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8de78-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de78-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8de78-137">Return Value</span></span>

<span data-ttu-id="8de78-138">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8de78-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8de78-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8de78-139">Remarks</span></span>

<span data-ttu-id="8de78-140">Эта команда определяет строковое имя для уровня качества, которое затем можно использовать в команде [сетвидео](setvideo.md) "Quality", сетвидео "качество", или [сетаудио](setaudio.md) "качество", чтобы установить его как текущее видео, все еще или уровень качества сжатия звука.</span><span class="sxs-lookup"><span data-stu-id="8de78-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="8de78-141">Требования</span><span class="sxs-lookup"><span data-stu-id="8de78-141">Requirements</span></span>



| <span data-ttu-id="8de78-142">Требование</span><span class="sxs-lookup"><span data-stu-id="8de78-142">Requirement</span></span> | <span data-ttu-id="8de78-143">Значение</span><span class="sxs-lookup"><span data-stu-id="8de78-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8de78-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8de78-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8de78-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8de78-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8de78-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8de78-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8de78-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8de78-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8de78-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8de78-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de78-149">MCI</span><span class="sxs-lookup"><span data-stu-id="8de78-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8de78-150">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="8de78-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="8de78-151">сетаудио</span><span class="sxs-lookup"><span data-stu-id="8de78-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="8de78-152">сетвидео</span><span class="sxs-lookup"><span data-stu-id="8de78-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

