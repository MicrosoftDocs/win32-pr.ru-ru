---
title: Команда сеттунер
description: Команда сеттунер изменяет текущий тюнер или параметр канала текущего тюнера. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- Команда сеттунер мультимедиа Windows
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493260"
---
# <a name="settuner-command"></a><span data-ttu-id="6996f-105">Команда сеттунер</span><span class="sxs-lookup"><span data-stu-id="6996f-105">settuner command</span></span>

<span data-ttu-id="6996f-106">Команда сеттунер изменяет текущий тюнер или параметр канала текущего тюнера.</span><span class="sxs-lookup"><span data-stu-id="6996f-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="6996f-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="6996f-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="6996f-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6996f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6996f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6996f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6996f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="6996f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6996f-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="6996f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6996f-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="6996f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6996f-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*лпсзтунер*</span><span class="sxs-lookup"><span data-stu-id="6996f-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="6996f-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="6996f-114">One of the following flags.</span></span>



| <span data-ttu-id="6996f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6996f-115">Value</span></span>                            | <span data-ttu-id="6996f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6996f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6996f-117">*канал* канала</span><span class="sxs-lookup"><span data-stu-id="6996f-117">channel *channel*</span></span>                | <span data-ttu-id="6996f-118">Задает для тюнера значение *канал*.</span><span class="sxs-lookup"><span data-stu-id="6996f-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="6996f-119">Возможно, вы не сможете изменить канал во время записи, в зависимости от ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="6996f-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="6996f-120">Канал, превышающий максимальный, задает для тюнера максимальный канал.</span><span class="sxs-lookup"><span data-stu-id="6996f-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="6996f-121">Поиск канала с переходом по каналу</span><span class="sxs-lookup"><span data-stu-id="6996f-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="6996f-122">Выполняет поиск следующего канала с допустимым сигналом.</span><span class="sxs-lookup"><span data-stu-id="6996f-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="6996f-123">"Поиск" — увеличивает номер канала в поиске.</span><span class="sxs-lookup"><span data-stu-id="6996f-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="6996f-124">"Поиск вниз" уменьшает номер канала в поиске.</span><span class="sxs-lookup"><span data-stu-id="6996f-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="6996f-125">При превышении максимального номера канала тюнер переносится на канал 1.</span><span class="sxs-lookup"><span data-stu-id="6996f-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="6996f-126">Аналогичным образом, при поиске, тюнер переносится к максимальному каналу.</span><span class="sxs-lookup"><span data-stu-id="6996f-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="6996f-127">канал исключается канала</span><span class="sxs-lookup"><span data-stu-id="6996f-127">channel upchannel down</span></span>           | <span data-ttu-id="6996f-128">Увеличивает или уменьшает канал тюнера.</span><span class="sxs-lookup"><span data-stu-id="6996f-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="6996f-129">Возможно, вы не сможете изменить канал во время записи, в зависимости от ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="6996f-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="6996f-130">При превышении максимального номера канала тюнер переносится на канал 1.</span><span class="sxs-lookup"><span data-stu-id="6996f-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="6996f-131">Аналогичным образом, при поиске, тюнер переносится к максимальному каналу.</span><span class="sxs-lookup"><span data-stu-id="6996f-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="6996f-132">номер </span><span class="sxs-lookup"><span data-stu-id="6996f-132">number *number*</span></span>                  | <span data-ttu-id="6996f-133">Указывает тюнер, затронутый командой сеттунер.</span><span class="sxs-lookup"><span data-stu-id="6996f-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="6996f-134">Если аргумент *Number* не задан, то предполагается значение по умолчанию, равное 1.</span><span class="sxs-lookup"><span data-stu-id="6996f-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="6996f-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="6996f-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6996f-136">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="6996f-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6996f-137">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6996f-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6996f-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6996f-138">Return Value</span></span>

<span data-ttu-id="6996f-139">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6996f-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6996f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="6996f-140">Requirements</span></span>



| <span data-ttu-id="6996f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="6996f-141">Requirement</span></span> | <span data-ttu-id="6996f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="6996f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6996f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6996f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6996f-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6996f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6996f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6996f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6996f-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6996f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6996f-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6996f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6996f-148">MCI</span><span class="sxs-lookup"><span data-stu-id="6996f-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6996f-149">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="6996f-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

