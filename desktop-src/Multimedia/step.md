---
title: Команда Step
description: Команда Step выполняет шаги по воспроизведению одного или нескольких кадров вперед или назад. Действие по умолчанию — шаг вперед одного кадра. Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- Пошаговая команда мультимедиа Windows
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490476"
---
# <a name="step-command"></a><span data-ttu-id="e03e9-106">Команда Step</span><span class="sxs-lookup"><span data-stu-id="e03e9-106">step command</span></span>

<span data-ttu-id="e03e9-107">Команда Step выполняет шаги по воспроизведению одного или нескольких кадров вперед или назад.</span><span class="sxs-lookup"><span data-stu-id="e03e9-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="e03e9-108">Действие по умолчанию — шаг вперед одного кадра.</span><span class="sxs-lookup"><span data-stu-id="e03e9-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="e03e9-109">Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.</span><span class="sxs-lookup"><span data-stu-id="e03e9-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="e03e9-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e03e9-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e03e9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e03e9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e03e9-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="e03e9-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e03e9-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="e03e9-113">Identifier of an MCI device.</span></span> <span data-ttu-id="e03e9-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="e03e9-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e03e9-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*лпсзстепфлагс*</span><span class="sxs-lookup"><span data-stu-id="e03e9-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e03e9-116">Один или оба следующих флага.</span><span class="sxs-lookup"><span data-stu-id="e03e9-116">One or both of the following flags.</span></span>



| <span data-ttu-id="e03e9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e03e9-117">Value</span></span>       | <span data-ttu-id="e03e9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e03e9-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03e9-119">по *кадрам*</span><span class="sxs-lookup"><span data-stu-id="e03e9-119">by *frames*</span></span> | <span data-ttu-id="e03e9-120">Указывает число кадров для шага.</span><span class="sxs-lookup"><span data-stu-id="e03e9-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="e03e9-121">Если указано отрицательное значение *frames* , нельзя указать флаг "Reverse".</span><span class="sxs-lookup"><span data-stu-id="e03e9-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="e03e9-122">reverse</span><span class="sxs-lookup"><span data-stu-id="e03e9-122">reverse</span></span>     | <span data-ttu-id="e03e9-123">Шаг между кадрами в обратную.</span><span class="sxs-lookup"><span data-stu-id="e03e9-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="e03e9-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="e03e9-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e03e9-125">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="e03e9-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e03e9-126">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="e03e9-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="e03e9-127">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e03e9-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e03e9-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e03e9-128">Return Value</span></span>

<span data-ttu-id="e03e9-129">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e03e9-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e03e9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e03e9-130">Requirements</span></span>



| <span data-ttu-id="e03e9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e03e9-131">Requirement</span></span> | <span data-ttu-id="e03e9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e03e9-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e03e9-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e03e9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e03e9-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e03e9-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e03e9-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e03e9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e03e9-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e03e9-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e03e9-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e03e9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03e9-138">MCI</span><span class="sxs-lookup"><span data-stu-id="e03e9-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e03e9-139">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="e03e9-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

