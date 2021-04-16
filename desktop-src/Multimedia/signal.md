---
title: сигнал, команда
description: Команда сигнала определяет указанную точку в рабочей области путем отправки приложения в \_ сообщение МЦИСИГНАЛ mm. Устройство Digital-Video распознает эту команду. МЦИАВИ поддерживает только один активный сигнал за раз.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- сигнал команды "мультимедиа Windows"
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672704"
---
# <a name="signal-command"></a><span data-ttu-id="61468-106">сигнал, команда</span><span class="sxs-lookup"><span data-stu-id="61468-106">signal command</span></span>

<span data-ttu-id="61468-107">Команда сигнала определяет указанную точку в рабочей области путем отправки приложения в сообщение [ \_ мЦисигнал mm](mm-mcisignal.md) .</span><span class="sxs-lookup"><span data-stu-id="61468-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="61468-108">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="61468-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="61468-109">МЦИАВИ поддерживает только один активный сигнал за раз.</span><span class="sxs-lookup"><span data-stu-id="61468-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="61468-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="61468-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="61468-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="61468-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61468-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="61468-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="61468-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="61468-113">Identifier of an MCI device.</span></span> <span data-ttu-id="61468-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="61468-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="61468-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*лпсзсигналфлагс*</span><span class="sxs-lookup"><span data-stu-id="61468-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="61468-116">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="61468-116">One of the following flags.</span></span>



| <span data-ttu-id="61468-117">Значение</span><span class="sxs-lookup"><span data-stu-id="61468-117">Value</span></span>            | <span data-ttu-id="61468-118">Значение</span><span class="sxs-lookup"><span data-stu-id="61468-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61468-119">в позиции</span><span class="sxs-lookup"><span data-stu-id="61468-119">at position</span></span>      | <span data-ttu-id="61468-120">Указывает кадр для вызова сигнала.</span><span class="sxs-lookup"><span data-stu-id="61468-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="61468-121">cancel</span><span class="sxs-lookup"><span data-stu-id="61468-121">cancel</span></span>           | <span data-ttu-id="61468-122">Удаляет сигналы из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="61468-122">Removes signals from the workspace.</span></span> <span data-ttu-id="61468-123">Отдельный сигнал задается с помощью флага "усервалуе".</span><span class="sxs-lookup"><span data-stu-id="61468-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="61468-124">Если флаг "усервалуе" не указан с помощью команды "Отмена", устройство отменяет все сигналы.</span><span class="sxs-lookup"><span data-stu-id="61468-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="61468-125">Флаг "Cancel" несовместим с флагами "at", "ALL" и "return позиции".</span><span class="sxs-lookup"><span data-stu-id="61468-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="61468-126">Каждый *интервал*</span><span class="sxs-lookup"><span data-stu-id="61468-126">every *interval*</span></span> | <span data-ttu-id="61468-127">Задает период сигналов.</span><span class="sxs-lookup"><span data-stu-id="61468-127">Specifies the period of the signals.</span></span> <span data-ttu-id="61468-128">Значение *интервала* указывается в текущем формате времени. При использовании с *положением*"at" сигналы помещаются по всей рабочей области с одной сигнальной меткой, размещенной в *позиции*.</span><span class="sxs-lookup"><span data-stu-id="61468-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="61468-129">Без флага "at" сигналы помещаются по всей рабочей области с одним сигналом в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="61468-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="61468-130">Если этот флаг опущен, помечается только расположение, обозначенное флагом "at".</span><span class="sxs-lookup"><span data-stu-id="61468-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="61468-131">Если значение *интервала* меньше минимальной частоты, поддерживаемой устройством, оно будет использовать его минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="61468-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="61468-132">возвращаемое расположение</span><span class="sxs-lookup"><span data-stu-id="61468-132">return position</span></span>  | <span data-ttu-id="61468-133">Указывает, что устройство должно отправить значение расположения вместо идентификатора "усервалуе" в сигнальном сообщении.</span><span class="sxs-lookup"><span data-stu-id="61468-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="61468-134">Идентификатор "усервалуе" по-прежнему можно использовать для отмены или переопределения сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="61468-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="61468-135">*идентификатор* усервалуе</span><span class="sxs-lookup"><span data-stu-id="61468-135">uservalue *id*</span></span>   | <span data-ttu-id="61468-136">Указывает идентификатор, который передается обратно сигнальным сообщением.</span><span class="sxs-lookup"><span data-stu-id="61468-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="61468-137">Этот идентификатор выступает в качестве идентификатора, который можно использовать с другими командами **сигналов** для ссылки на этот параметр **сигнала** .</span><span class="sxs-lookup"><span data-stu-id="61468-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="61468-138">Если этот параметр опущен, значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="61468-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="61468-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="61468-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="61468-140">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="61468-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="61468-141">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="61468-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61468-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61468-142">Return Value</span></span>

<span data-ttu-id="61468-143">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="61468-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="61468-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61468-144">Remarks</span></span>

<span data-ttu-id="61468-145">Дескриптор окна, используемый для уведомления о сообщениях о завершении работы команды, также используется для сигнализации.</span><span class="sxs-lookup"><span data-stu-id="61468-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="61468-146">Требования</span><span class="sxs-lookup"><span data-stu-id="61468-146">Requirements</span></span>



| <span data-ttu-id="61468-147">Требование</span><span class="sxs-lookup"><span data-stu-id="61468-147">Requirement</span></span> | <span data-ttu-id="61468-148">Значение</span><span class="sxs-lookup"><span data-stu-id="61468-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="61468-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61468-149">Minimum supported client</span></span><br/> | <span data-ttu-id="61468-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61468-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="61468-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61468-151">Minimum supported server</span></span><br/> | <span data-ttu-id="61468-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61468-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="61468-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61468-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61468-154">MCI</span><span class="sxs-lookup"><span data-stu-id="61468-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="61468-155">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="61468-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="61468-156">\_МЦИСИГНАЛ мм</span><span class="sxs-lookup"><span data-stu-id="61468-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 

