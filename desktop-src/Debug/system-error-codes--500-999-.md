---
description: Описание кодов ошибок 500-999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Коды системных ошибок (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262704"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="e2337-103">Коды системных ошибок (500-999)</span><span class="sxs-lookup"><span data-stu-id="e2337-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="e2337-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="e2337-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="e2337-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2337-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="e2337-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 500 – 999).</span><span class="sxs-lookup"><span data-stu-id="e2337-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="e2337-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="e2337-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="e2337-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="e2337-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="e2337-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**Ошибка \_ при \_ загрузке профиля пользователя \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-110">500 (0x1F4)</span><span class="sxs-lookup"><span data-stu-id="e2337-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-111">Не удается загрузить профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2337-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_арифметическое \_ переполнение при ошибке**</span><span class="sxs-lookup"><span data-stu-id="e2337-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-113">534 (0x216)</span><span class="sxs-lookup"><span data-stu-id="e2337-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-114">Арифметический результат превысил 32 бит.</span><span class="sxs-lookup"><span data-stu-id="e2337-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**\_канал ошибки \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="e2337-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-116">535 (0x217)</span><span class="sxs-lookup"><span data-stu-id="e2337-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-117">Существует процесс на другом конце канала.</span><span class="sxs-lookup"><span data-stu-id="e2337-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**Ошибка \_ при \_ прослушивании канала**</span><span class="sxs-lookup"><span data-stu-id="e2337-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-119">536 (0x218)</span><span class="sxs-lookup"><span data-stu-id="e2337-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-120">Ожидание открытия процессом другого конца канала.</span><span class="sxs-lookup"><span data-stu-id="e2337-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**Ошибка \_ средства проверки ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-122">537 (0x219)</span><span class="sxs-lookup"><span data-stu-id="e2337-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-123">Средство проверки приложений обнаружило ошибку в текущем процессе.</span><span class="sxs-lookup"><span data-stu-id="e2337-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**Ошибка \_ абиос \_ , ошибка**</span><span class="sxs-lookup"><span data-stu-id="e2337-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-125">538 (0x21A)</span><span class="sxs-lookup"><span data-stu-id="e2337-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-126">Произошла ошибка в подсистеме АБИОС.</span><span class="sxs-lookup"><span data-stu-id="e2337-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**Ошибка \_ WX86, \_ предупреждение**</span><span class="sxs-lookup"><span data-stu-id="e2337-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-128">539 (0x21B)</span><span class="sxs-lookup"><span data-stu-id="e2337-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-129">В подсистеме WX86 возникло предупреждение.</span><span class="sxs-lookup"><span data-stu-id="e2337-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Ошибка \_ WX86 \_ , ошибка**</span><span class="sxs-lookup"><span data-stu-id="e2337-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-131">540 (0x21C)</span><span class="sxs-lookup"><span data-stu-id="e2337-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-132">Произошла ошибка в подсистеме WX86.</span><span class="sxs-lookup"><span data-stu-id="e2337-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_таймер ошибок \_ не \_ отменен**</span><span class="sxs-lookup"><span data-stu-id="e2337-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-134">541 (0x21D)</span><span class="sxs-lookup"><span data-stu-id="e2337-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-135">Предпринята попытка отмены или установки таймера, имеющего связанный объект APC, а поток субъекта не является потоком, который изначально установил таймер с помощью связанной подпрограммы APC.</span><span class="sxs-lookup"><span data-stu-id="e2337-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**Ошибка \_ очистки**</span><span class="sxs-lookup"><span data-stu-id="e2337-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-137">542 (0x21E)</span><span class="sxs-lookup"><span data-stu-id="e2337-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-138">Код исключения очистки.</span><span class="sxs-lookup"><span data-stu-id="e2337-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ошибочный \_ \_ стек ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-140">543 (0x21F)</span><span class="sxs-lookup"><span data-stu-id="e2337-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-141">Во время операции очистки обнаружен недопустимый или несогласованный стек.</span><span class="sxs-lookup"><span data-stu-id="e2337-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**Ошибка \_ недопустимого \_ \_ целевого объекта очистки**</span><span class="sxs-lookup"><span data-stu-id="e2337-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-143">544 (0x220)</span><span class="sxs-lookup"><span data-stu-id="e2337-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-144">При выполнении операции завершения обнаружен недопустимый целевой объект очистки.</span><span class="sxs-lookup"><span data-stu-id="e2337-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**Ошибка \_ недопустимых \_ \_ атрибутов порта**</span><span class="sxs-lookup"><span data-stu-id="e2337-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-146">545 (0x221)</span><span class="sxs-lookup"><span data-stu-id="e2337-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-147">Указаны недопустимые атрибуты объекта для Нткреатепорт или для Нтконнектпорт указаны недопустимые атрибуты порта</span><span class="sxs-lookup"><span data-stu-id="e2337-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**\_ \_ \_ слишком \_ ДЛИННое сообщение порта ошибки**</span><span class="sxs-lookup"><span data-stu-id="e2337-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-149">546 (0x222)</span><span class="sxs-lookup"><span data-stu-id="e2337-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-150">Длина сообщения, переданного в Нтрекуестпорт или Нтрекуестваитреплипорт, превышает максимально допустимое для порта сообщение.</span><span class="sxs-lookup"><span data-stu-id="e2337-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**Ошибка \_ недопустимой \_ квоты \_ ниже**</span><span class="sxs-lookup"><span data-stu-id="e2337-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-152">547 (0x223)</span><span class="sxs-lookup"><span data-stu-id="e2337-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-153">Предпринята попытка снижения предельной квоты ниже текущего использования.</span><span class="sxs-lookup"><span data-stu-id="e2337-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**устройство с ошибкой \_ \_ уже \_ подключено**</span><span class="sxs-lookup"><span data-stu-id="e2337-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-155">548 (0x224)</span><span class="sxs-lookup"><span data-stu-id="e2337-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-156">Предпринята попытка присоединения к устройству, которое уже подключено к другому устройству.</span><span class="sxs-lookup"><span data-stu-id="e2337-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**Ошибка при неправильном \_ \_ выравнивании инструкции**</span><span class="sxs-lookup"><span data-stu-id="e2337-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-158">549 (0x225)</span><span class="sxs-lookup"><span data-stu-id="e2337-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-159">Предпринята попытка выполнить инструкцию по несогласованному адресу, а система узла не поддерживает ссылки на несогласованные инструкции.</span><span class="sxs-lookup"><span data-stu-id="e2337-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**\_ \_ не ЗАПУЩЕНо ПРОФИЛИРОВАНие ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-161">550 (0x226)</span><span class="sxs-lookup"><span data-stu-id="e2337-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-162">Профилирование не запущено.</span><span class="sxs-lookup"><span data-stu-id="e2337-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**\_ \_ не ОСТАНОВЛЕНо ПРОФИЛИРОВАНие ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-164">551 (0x227)</span><span class="sxs-lookup"><span data-stu-id="e2337-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-165">Профилирование не остановлено.</span><span class="sxs-lookup"><span data-stu-id="e2337-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**\_не удалось \_ \_ интерпретировать ошибку**</span><span class="sxs-lookup"><span data-stu-id="e2337-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-167">552 (0x228)</span><span class="sxs-lookup"><span data-stu-id="e2337-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-168">Переданный список ACL не содержал минимально необходимой информации.</span><span class="sxs-lookup"><span data-stu-id="e2337-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**Ошибка \_ профилирования \_ в \_ ограничении**</span><span class="sxs-lookup"><span data-stu-id="e2337-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-170">553 (0x229)</span><span class="sxs-lookup"><span data-stu-id="e2337-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-171">Число активных объектов профилирования достигло максимума и больше не может быть запущено.</span><span class="sxs-lookup"><span data-stu-id="e2337-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ОШИБКА не \_ удается \_ дождаться**</span><span class="sxs-lookup"><span data-stu-id="e2337-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-173">554 (0x22A)</span><span class="sxs-lookup"><span data-stu-id="e2337-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-174">Используется, чтобы указать, что операция не может продолжаться без блокировки операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e2337-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ОШИБКА не \_ удается \_ завершить \_ самостоятельно**</span><span class="sxs-lookup"><span data-stu-id="e2337-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-176">555 (0x22B)</span><span class="sxs-lookup"><span data-stu-id="e2337-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-177">Указывает, что поток попытался завершить себя по умолчанию (с именем Нттерминатесреад со **значением NULL**) и последним потоком в текущем процессе.</span><span class="sxs-lookup"><span data-stu-id="e2337-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**\_непредвиденная ошибка при \_ создании ошибки mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-179">556 (0x22C)</span><span class="sxs-lookup"><span data-stu-id="e2337-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-180">Если возвращается ошибка MM, которая не определена в стандартном фильтре Фсртл, она преобразуется в одну из следующих ошибок, которые гарантированно будут в фильтре.</span><span class="sxs-lookup"><span data-stu-id="e2337-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="e2337-181">В этом случае данные теряются, но фильтр правильно обрабатывает исключение.</span><span class="sxs-lookup"><span data-stu-id="e2337-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**Ошибка \_ непредвиденной \_ \_ ошибки в карте mm \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-183">557 (0x22D)</span><span class="sxs-lookup"><span data-stu-id="e2337-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-184">Если возвращается ошибка MM, которая не определена в стандартном фильтре Фсртл, она преобразуется в одну из следующих ошибок, которые гарантированно будут в фильтре.</span><span class="sxs-lookup"><span data-stu-id="e2337-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="e2337-185">В этом случае данные теряются, но фильтр правильно обрабатывает исключение.</span><span class="sxs-lookup"><span data-stu-id="e2337-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**\_непредвиденная ошибка при \_ расширении ошибки mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-187">558 (0x22E)</span><span class="sxs-lookup"><span data-stu-id="e2337-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-188">Если возвращается ошибка MM, которая не определена в стандартном фильтре Фсртл, она преобразуется в одну из следующих ошибок, которые гарантированно будут в фильтре.</span><span class="sxs-lookup"><span data-stu-id="e2337-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="e2337-189">В этом случае данные теряются, но фильтр правильно обрабатывает исключение.</span><span class="sxs-lookup"><span data-stu-id="e2337-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**Ошибка \_ неправильной \_ \_ таблицы функции**</span><span class="sxs-lookup"><span data-stu-id="e2337-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-191">559 (0x22F)</span><span class="sxs-lookup"><span data-stu-id="e2337-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-192">При выполнении операции завершения обнаружена неверно сформированная Таблица функций.</span><span class="sxs-lookup"><span data-stu-id="e2337-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**Ошибка \_ при \_ \_ преобразовании GUID**</span><span class="sxs-lookup"><span data-stu-id="e2337-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-194">560 (0X230)</span><span class="sxs-lookup"><span data-stu-id="e2337-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-195">Указывает, что была предпринята попытка присвоить защиту файлу или каталогу файловой системы, а один из идентификаторов безопасности из этого дескриптора не может быть преобразован в идентификатор GUID, который может храниться в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="e2337-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="e2337-196">Это вызывает сбой попытки защиты, что может привести к сбою при попытке создания файла.</span><span class="sxs-lookup"><span data-stu-id="e2337-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**Ошибка \_ недопустимого \_ размера локальной таблицы \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-198">561 (0x231)</span><span class="sxs-lookup"><span data-stu-id="e2337-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-199">Указывает, что была предпринята попытка расширить список описателей локальной таблицы, задав ее размер или размер которой не является четным числом селекторов.</span><span class="sxs-lookup"><span data-stu-id="e2337-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**Ошибка \_ недопустимого \_ смещения локальной таблицы \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-201">563 (0x233)</span><span class="sxs-lookup"><span data-stu-id="e2337-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-202">Указывает, что начальное значение сведений о локальной списке описателей не является целым числом, кратным размеру селектора.</span><span class="sxs-lookup"><span data-stu-id="e2337-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**Ошибка \_ недопустимого \_ \_ дескриптора локальной таблицы**</span><span class="sxs-lookup"><span data-stu-id="e2337-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-204">564 (0x234)</span><span class="sxs-lookup"><span data-stu-id="e2337-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-205">Указывает, что при попытке настройки описателей локальной таблицы пользователь указал недопустимый дескриптор.</span><span class="sxs-lookup"><span data-stu-id="e2337-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**Ошибка \_ слишком \_ много \_ потоков**</span><span class="sxs-lookup"><span data-stu-id="e2337-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-207">565 (0x235)</span><span class="sxs-lookup"><span data-stu-id="e2337-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-208">Указывает, что процесс имеет слишком много потоков для выполнения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="e2337-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="e2337-209">Например, назначение основного маркера может быть выполнено только в том случае, если процесс имеет ноль или один поток.</span><span class="sxs-lookup"><span data-stu-id="e2337-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**поток ошибок, \_ \_ не \_ \_ обрабатываемый процессом**</span><span class="sxs-lookup"><span data-stu-id="e2337-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-211">566 (0x236)</span><span class="sxs-lookup"><span data-stu-id="e2337-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-212">Предпринята попытка обработать поток в рамках определенного процесса, но указанный поток не находится в указанном процессе.</span><span class="sxs-lookup"><span data-stu-id="e2337-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**\_ \_ превышена квота файла подкачки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-214">567 (0x237)</span><span class="sxs-lookup"><span data-stu-id="e2337-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-215">Превышена квота файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="e2337-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**Ошибка \_ при \_ \_ конфликте сервера входа**</span><span class="sxs-lookup"><span data-stu-id="e2337-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-217">568 (0x238)</span><span class="sxs-lookup"><span data-stu-id="e2337-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-218">Не удается запустить службу Netlogon, так как другая служба Netlogon, работающая в домене, конфликтует с указанной ролью.</span><span class="sxs-lookup"><span data-stu-id="e2337-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**\_требуется синхронизация с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-220">569 (0x239)</span><span class="sxs-lookup"><span data-stu-id="e2337-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-221">База данных SAM на сервере Windows Server значительно не синхронизирована с копией на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="e2337-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="e2337-222">Требуется полная синхронизация.</span><span class="sxs-lookup"><span data-stu-id="e2337-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**Ошибка \_ net \_ Open \_ не удалось**</span><span class="sxs-lookup"><span data-stu-id="e2337-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-224">570 (0x23A)</span><span class="sxs-lookup"><span data-stu-id="e2337-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-225">Сбой API NtCreateFile.</span><span class="sxs-lookup"><span data-stu-id="e2337-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="e2337-226">Эта ошибка никогда не должна возвращаться в приложение. это заполнитель для перенаправителя диспетчера LAN Windows, который будет использоваться в внутренних подпрограммых сопоставления ошибок.</span><span class="sxs-lookup"><span data-stu-id="e2337-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**Ошибка \_ \_ при выполнении права ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-228">571 (0x23B)</span><span class="sxs-lookup"><span data-stu-id="e2337-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-229">{Привилегия не пройдена} Не удалось изменить разрешения ввода-вывода для процесса.</span><span class="sxs-lookup"><span data-stu-id="e2337-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**Управление ОШИБКАми \_ \_ C \_ выходом**</span><span class="sxs-lookup"><span data-stu-id="e2337-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-231">572 (0x23C)</span><span class="sxs-lookup"><span data-stu-id="e2337-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-232">{Выход из приложения по CTRL + C} Приложение прервано в результате нажатия клавиш CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="e2337-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**Ошибка при \_ отсутствии \_ системфиле**</span><span class="sxs-lookup"><span data-stu-id="e2337-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-234">573 (0x23D)</span><span class="sxs-lookup"><span data-stu-id="e2337-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-235">{Отсутствует системный файл} Необходимый системный файл% HS поврежден или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e2337-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**Ошибка \_ НЕобработанного \_ исключения**</span><span class="sxs-lookup"><span data-stu-id="e2337-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-237">574 (0x23E)</span><span class="sxs-lookup"><span data-stu-id="e2337-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-238">{Ошибка приложения} Исключение% s (0x% 08lx) произошло в приложении в расположении 0x% 08LX.</span><span class="sxs-lookup"><span data-stu-id="e2337-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**Ошибка \_ \_ инициализации приложения \_ при ошибке**</span><span class="sxs-lookup"><span data-stu-id="e2337-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-240">575 (0x23F)</span><span class="sxs-lookup"><span data-stu-id="e2337-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-241">{Ошибка приложения} Не удалось правильно запустить приложение (0x% LX).</span><span class="sxs-lookup"><span data-stu-id="e2337-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="e2337-242">Нажмите кнопку ОК, чтобы закрыть приложение.</span><span class="sxs-lookup"><span data-stu-id="e2337-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**\_сбой создания файла подкачки ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-244">576 (0x240)</span><span class="sxs-lookup"><span data-stu-id="e2337-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-245">{Не удается создать файл подкачки} Не удалось создать файл подкачки% HS (% LX).</span><span class="sxs-lookup"><span data-stu-id="e2337-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="e2337-246">Запрошенный размер% ld.</span><span class="sxs-lookup"><span data-stu-id="e2337-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**Ошибка \_ недопустимого \_ \_ хэша изображения**</span><span class="sxs-lookup"><span data-stu-id="e2337-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-248">577 (0x241)</span><span class="sxs-lookup"><span data-stu-id="e2337-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-249">Windows не удается проверить цифровую подпись для этого файла.</span><span class="sxs-lookup"><span data-stu-id="e2337-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="e2337-250">При недавнем изменении оборудования или программного обеспечения может быть установлен файл, который подписан неправильно или поврежден или может быть вредоносным программным обеспечением из неизвестного источника.</span><span class="sxs-lookup"><span data-stu-id="e2337-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**Ошибка \_ без \_ файла подкачки**</span><span class="sxs-lookup"><span data-stu-id="e2337-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-252">578 (0x242)</span><span class="sxs-lookup"><span data-stu-id="e2337-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-253">{Не указан файл подкачки} В конфигурации системы не указан файл подкачки.</span><span class="sxs-lookup"><span data-stu-id="e2337-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**Ошибка \_ недопустимого \_ \_ контекста float**</span><span class="sxs-lookup"><span data-stu-id="e2337-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-255">579 (0x243)</span><span class="sxs-lookup"><span data-stu-id="e2337-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-256">ОБ Приложение реального режима выпустило инструкцию с плавающей запятой и оборудование с плавающей запятой отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e2337-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**Ошибка \_ без \_ \_ пары событий**</span><span class="sxs-lookup"><span data-stu-id="e2337-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-258">580 (0x244)</span><span class="sxs-lookup"><span data-stu-id="e2337-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-259">Операция синхронизации пары событий была выполнена с помощью объекта пары событий клиент/сервер конкретного потока, но с потоком не связан ни один объект пары событий.</span><span class="sxs-lookup"><span data-stu-id="e2337-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**Ошибка \_ \_ настройки доменного \_ сочетания \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-261">581 (0x245)</span><span class="sxs-lookup"><span data-stu-id="e2337-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-262">Неверная конфигурация Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e2337-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**Ошибка \_ недопустимого \_ символа**</span><span class="sxs-lookup"><span data-stu-id="e2337-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-264">582 (0x246)</span><span class="sxs-lookup"><span data-stu-id="e2337-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-265">Обнаружен недопустимый знак.</span><span class="sxs-lookup"><span data-stu-id="e2337-265">An illegal character was encountered.</span></span> <span data-ttu-id="e2337-266">Для многобайтовой кодировки это включает старший байт без завершающего байта.</span><span class="sxs-lookup"><span data-stu-id="e2337-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="e2337-267">Для набора символов Юникода это включает символы 0xFFFF и 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="e2337-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**Ошибка \_ НЕопределенного \_ символа**</span><span class="sxs-lookup"><span data-stu-id="e2337-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-269">583 (0x247)</span><span class="sxs-lookup"><span data-stu-id="e2337-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-270">Символ Юникода не определен в наборе символов Юникода, установленном в системе.</span><span class="sxs-lookup"><span data-stu-id="e2337-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**Ошибка в \_ томе гибких дисков \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-272">584 (0x248)</span><span class="sxs-lookup"><span data-stu-id="e2337-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-273">Невозможно создать файл подкачки на дискете.</span><span class="sxs-lookup"><span data-stu-id="e2337-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**Ошибка \_ BIOS \_ при \_ \_ подключении \_ прерывания**</span><span class="sxs-lookup"><span data-stu-id="e2337-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-275">585 (0x249)</span><span class="sxs-lookup"><span data-stu-id="e2337-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-276">BIOS системы не удалось подключить системное прерывание к устройству или шине, к которой подключено устройство.</span><span class="sxs-lookup"><span data-stu-id="e2337-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**Ошибка \_ контроллера резервного копирования \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-278">586 (0x24A)</span><span class="sxs-lookup"><span data-stu-id="e2337-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-279">Эта операция разрешена только для основного контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="e2337-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_Превышено ограничение мутанта ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-281">587 (0x24B)</span><span class="sxs-lookup"><span data-stu-id="e2337-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-282">Предпринята попытка получить мутант, чтобы было превышено его максимальное число.</span><span class="sxs-lookup"><span data-stu-id="e2337-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**\_ \_ требуется драйвер FS \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-284">588 (0x24C)</span><span class="sxs-lookup"><span data-stu-id="e2337-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-285">Доступ к тому, для которого требуется драйвер файловой системы, еще не был загружен.</span><span class="sxs-lookup"><span data-stu-id="e2337-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**Ошибка \_ не \_ может \_ загрузить \_ файл реестра**</span><span class="sxs-lookup"><span data-stu-id="e2337-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-287">589 (0x24D)</span><span class="sxs-lookup"><span data-stu-id="e2337-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-288">{Ошибка в файле реестра} Реестр не может загрузить куст (файл):% HS или его журнал или альтернативный вариант.</span><span class="sxs-lookup"><span data-stu-id="e2337-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="e2337-289">Он поврежден, отсутствует или недоступен для записи.</span><span class="sxs-lookup"><span data-stu-id="e2337-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**Ошибка \_ \_ при присоединении отладки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-291">590 (0x24E)</span><span class="sxs-lookup"><span data-stu-id="e2337-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-292">{Непредвиденный сбой в [**дебугактивепроцесс**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} При обработке запроса API **дебугактивепроцесс** произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e2337-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="e2337-293">Вы можете нажать кнопку ОК, чтобы завершить процесс, или кнопку Отмена, чтобы пропустить ошибку.</span><span class="sxs-lookup"><span data-stu-id="e2337-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**Ошибка \_ системного \_ процесса \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="e2337-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-295">591 (0x24F)</span><span class="sxs-lookup"><span data-stu-id="e2337-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-296">{Неустранимая системная ошибка} Непредвиденное завершение системного процесса% HS с состоянием 0x% 08x (0x% 08x 0x% 08x).</span><span class="sxs-lookup"><span data-stu-id="e2337-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="e2337-297">Работа системы завершена.</span><span class="sxs-lookup"><span data-stu-id="e2337-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**данные об ОШИБКАх \_ \_ не \_ приняты**</span><span class="sxs-lookup"><span data-stu-id="e2337-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-299">592 (0x250)</span><span class="sxs-lookup"><span data-stu-id="e2337-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-300">{Данные не приняты} Клиенту TDI не удалось справиться с данными, полученными во время индикации.</span><span class="sxs-lookup"><span data-stu-id="e2337-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**Ошибка при возникновении \_ \_ жесткой \_ ошибки VDM**</span><span class="sxs-lookup"><span data-stu-id="e2337-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-302">593 (0x251)</span><span class="sxs-lookup"><span data-stu-id="e2337-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-303">В NTVDM произошла несложная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e2337-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**Ошибка \_ при \_ отмене \_ истечения срока действия драйвера**</span><span class="sxs-lookup"><span data-stu-id="e2337-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-305">594 (0x252)</span><span class="sxs-lookup"><span data-stu-id="e2337-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-306">{Отмена времени ожидания} Драйверу% HS не удалось завершить отмененный запрос ввода-вывода за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="e2337-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**\_несоответствие \_ сообщения об ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-308">595 (0x253)</span><span class="sxs-lookup"><span data-stu-id="e2337-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-309">{Несоответствие сообщения ответа} Предпринята попытка ответить на сообщение LPC, но поток, указанный ИДЕНТИФИКАТОРом клиента в сообщении, не ожидал этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2337-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**Ошибка \_ потери \_ \_ данных вритебехинд**</span><span class="sxs-lookup"><span data-stu-id="e2337-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-311">596 (0x254)</span><span class="sxs-lookup"><span data-stu-id="e2337-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-312">{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="e2337-313">Данные потеряны.</span><span class="sxs-lookup"><span data-stu-id="e2337-313">The data has been lost.</span></span> <span data-ttu-id="e2337-314">Эта ошибка может быть вызвана сбоем оборудования или сетевого подключения компьютера.</span><span class="sxs-lookup"><span data-stu-id="e2337-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="e2337-315">Попробуйте сохранить этот файл в другой части.</span><span class="sxs-lookup"><span data-stu-id="e2337-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**Ошибка \_ \_ \_ \_ недопустимых параметров сервера клиента**</span><span class="sxs-lookup"><span data-stu-id="e2337-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-317">597 (0x255)</span><span class="sxs-lookup"><span data-stu-id="e2337-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-318">На сервер в окне общей памяти клиента или сервера переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="e2337-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="e2337-319">В окне общей памяти может быть помещено слишком много данных.</span><span class="sxs-lookup"><span data-stu-id="e2337-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**Ошибка \_ не является \_ крошечным \_ потоком**</span><span class="sxs-lookup"><span data-stu-id="e2337-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-321">598 (0x256)</span><span class="sxs-lookup"><span data-stu-id="e2337-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-322">Поток не является немаленькими потоком.</span><span class="sxs-lookup"><span data-stu-id="e2337-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**\_ \_ Чтение переполнения СТЕКа ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-324">599 (0x257)</span><span class="sxs-lookup"><span data-stu-id="e2337-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-325">Запрос должен обрабатываться кодом переполнения стека.</span><span class="sxs-lookup"><span data-stu-id="e2337-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**Ошибка \_ преобразования \_ в \_ крупный**</span><span class="sxs-lookup"><span data-stu-id="e2337-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-327">600 (0x258)</span><span class="sxs-lookup"><span data-stu-id="e2337-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-328">Внутренние коды состояний OFS, указывающие, как обрабатывается операция выделения.</span><span class="sxs-lookup"><span data-stu-id="e2337-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="e2337-329">Либо предпринимается повторная попытка после перемещения содержащего оноде, либо поток экстента преобразуется в большой поток.</span><span class="sxs-lookup"><span data-stu-id="e2337-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**\_обнаружена \_ Ошибка \_ вне \_ области**</span><span class="sxs-lookup"><span data-stu-id="e2337-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-331">601 (0x259)</span><span class="sxs-lookup"><span data-stu-id="e2337-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-332">При попытке найти объект найден объект, совпадающий по ИДЕНТИФИКАТОРу на томе, но он выходит за пределы области действия маркера, используемого для операции.</span><span class="sxs-lookup"><span data-stu-id="e2337-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**Ошибка при \_ выделении \_ контейнера**</span><span class="sxs-lookup"><span data-stu-id="e2337-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-334">602 (0x25A)</span><span class="sxs-lookup"><span data-stu-id="e2337-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-335">Массив контейнеров должен быть увеличен.</span><span class="sxs-lookup"><span data-stu-id="e2337-335">The bucket array must be grown.</span></span> <span data-ttu-id="e2337-336">Повторите транзакцию после этого.</span><span class="sxs-lookup"><span data-stu-id="e2337-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**Ошибка \_ Маршалловы о \_ переполнении**</span><span class="sxs-lookup"><span data-stu-id="e2337-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-338">603 (0x25B)</span><span class="sxs-lookup"><span data-stu-id="e2337-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-339">Переполнение буфера упаковки пользователя или ядра.</span><span class="sxs-lookup"><span data-stu-id="e2337-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**Ошибка \_ недопустимого \_ варианта**</span><span class="sxs-lookup"><span data-stu-id="e2337-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-341">604 (0x25C)</span><span class="sxs-lookup"><span data-stu-id="e2337-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-342">Указанная структура Variant содержит недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="e2337-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**Ошибка \_ неправильного \_ \_ буфера сжатия**</span><span class="sxs-lookup"><span data-stu-id="e2337-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-344">605 (0x25D)</span><span class="sxs-lookup"><span data-stu-id="e2337-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-345">Указанный буфер содержит некорректные данные.</span><span class="sxs-lookup"><span data-stu-id="e2337-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**Ошибка \_ при аудите ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-347">606 (0x25E)</span><span class="sxs-lookup"><span data-stu-id="e2337-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-348">{Сбой аудита} Сбой при создании аудита безопасности.</span><span class="sxs-lookup"><span data-stu-id="e2337-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**\_ \_ \_ не \_ задано разрешение таймера ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-350">607 (0x25F)</span><span class="sxs-lookup"><span data-stu-id="e2337-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-351">Разрешение таймера не было ранее задано текущим процессом.</span><span class="sxs-lookup"><span data-stu-id="e2337-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**Ошибка при \_ нехватке \_ сведений для входа \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-353">608 (0x260)</span><span class="sxs-lookup"><span data-stu-id="e2337-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-354">Недостаточно сведений об учетной записи для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="e2337-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**Ошибка- \_ неправильная \_ \_ точка входа DLL**</span><span class="sxs-lookup"><span data-stu-id="e2337-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-356">609 (0x261)</span><span class="sxs-lookup"><span data-stu-id="e2337-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-357">{Недопустимая точка входа DLL} Библиотека динамической компоновки% HS записана неправильно.</span><span class="sxs-lookup"><span data-stu-id="e2337-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="e2337-358">Указатель стека остался в непротиворечивом состоянии.</span><span class="sxs-lookup"><span data-stu-id="e2337-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="e2337-359">Точка входа должна быть объявлена как WINAPI или STDCALL.</span><span class="sxs-lookup"><span data-stu-id="e2337-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="e2337-360">Выберите Да, чтобы не загружать DLL.</span><span class="sxs-lookup"><span data-stu-id="e2337-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="e2337-361">Выберите Нет, чтобы продолжить выполнение.</span><span class="sxs-lookup"><span data-stu-id="e2337-361">Select NO to continue execution.</span></span> <span data-ttu-id="e2337-362">Выбор параметра нет может привести к неправильной работе приложения.</span><span class="sxs-lookup"><span data-stu-id="e2337-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**Ошибка \_ ошибочной \_ \_ точки входа службы**</span><span class="sxs-lookup"><span data-stu-id="e2337-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-364">610 (0x262)</span><span class="sxs-lookup"><span data-stu-id="e2337-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-365">{Недопустимая точка входа обратного вызова службы} Служба% HS записана неправильно.</span><span class="sxs-lookup"><span data-stu-id="e2337-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="e2337-366">Указатель стека остался в непротиворечивом состоянии.</span><span class="sxs-lookup"><span data-stu-id="e2337-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="e2337-367">Точка входа обратного вызова должна быть объявлена как WINAPI или STDCALL.</span><span class="sxs-lookup"><span data-stu-id="e2337-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="e2337-368">При нажатии кнопки "ОК" служба будет продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="e2337-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="e2337-369">Однако процесс службы может выполняться неправильно.</span><span class="sxs-lookup"><span data-stu-id="e2337-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**Ошибка \_ IP- \_ адреса \_ CONFLICT1**</span><span class="sxs-lookup"><span data-stu-id="e2337-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-371">611 (0x263)</span><span class="sxs-lookup"><span data-stu-id="e2337-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-372">IP-адрес конфликтует с другой системой в сети.</span><span class="sxs-lookup"><span data-stu-id="e2337-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**Ошибка \_ IP- \_ адреса \_ CONFLICT2**</span><span class="sxs-lookup"><span data-stu-id="e2337-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-374">612 (0x264)</span><span class="sxs-lookup"><span data-stu-id="e2337-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-375">IP-адрес конфликтует с другой системой в сети.</span><span class="sxs-lookup"><span data-stu-id="e2337-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_ \_ ограничение квоты для реестра с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-377">613 (0x265)</span><span class="sxs-lookup"><span data-stu-id="e2337-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-378">{Недостаточно свободного пространства в реестре} Система достигла максимального размера, допустимого для системной части реестра.</span><span class="sxs-lookup"><span data-stu-id="e2337-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="e2337-379">Дополнительные запросы к хранилищу будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="e2337-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**Ошибка при \_ отсутствии \_ активного обратного вызова \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-381">614 (0x266)</span><span class="sxs-lookup"><span data-stu-id="e2337-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-382">Если обратный вызов не активен, то системная служба возврата обратного вызова не может быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="e2337-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**Ошибка \_ PWD \_ слишком \_ короткий**</span><span class="sxs-lookup"><span data-stu-id="e2337-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-384">615 (0x267)</span><span class="sxs-lookup"><span data-stu-id="e2337-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-385">Предоставленный пароль слишком короткий для соответствия политике учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2337-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="e2337-386">Выберите более длинный пароль.</span><span class="sxs-lookup"><span data-stu-id="e2337-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**\_недавняя ошибка PWD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-388">616 (0x268)</span><span class="sxs-lookup"><span data-stu-id="e2337-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-389">Политика учетной записи пользователя не позволяет изменять пароли слишком часто.</span><span class="sxs-lookup"><span data-stu-id="e2337-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="e2337-390">Это делается для того, чтобы предотвратить переход пользователей на знакомый, но потенциально обнаруженный пароль.</span><span class="sxs-lookup"><span data-stu-id="e2337-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="e2337-391">Если вы считаете, что ваш пароль был скомпрометирован, немедленно обратитесь к администратору, чтобы назначить новый.</span><span class="sxs-lookup"><span data-stu-id="e2337-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**Ошибка \_ при \_ \_ конфликте журнала PWD**</span><span class="sxs-lookup"><span data-stu-id="e2337-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-393">617 (0x269)</span><span class="sxs-lookup"><span data-stu-id="e2337-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-394">Вы попытались изменить пароль на тот, который использовался в прошлом.</span><span class="sxs-lookup"><span data-stu-id="e2337-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="e2337-395">Это не разрешено политикой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2337-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="e2337-396">Выберите пароль, который ранее не использовался.</span><span class="sxs-lookup"><span data-stu-id="e2337-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**Ошибка \_ НЕподдерживаемого \_ сжатия**</span><span class="sxs-lookup"><span data-stu-id="e2337-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-398">618 (0x26A)</span><span class="sxs-lookup"><span data-stu-id="e2337-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-399">Указанный формат сжатия не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2337-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**Ошибка \_ недопустимого \_ \_ профиля оборудования**</span><span class="sxs-lookup"><span data-stu-id="e2337-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-401">619 (0x26B)</span><span class="sxs-lookup"><span data-stu-id="e2337-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-402">Указана недопустимая конфигурация профиля оборудования.</span><span class="sxs-lookup"><span data-stu-id="e2337-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**Ошибка \_ недопустимого \_ \_ \_ пути к устройству плугплай**</span><span class="sxs-lookup"><span data-stu-id="e2337-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-404">620 (0x26C)</span><span class="sxs-lookup"><span data-stu-id="e2337-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-405">Указан недопустимый путь к устройству реестра самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="e2337-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**список квот на ошибки не \_ \_ \_ согласуется**</span><span class="sxs-lookup"><span data-stu-id="e2337-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-407">621 (0x26D)</span><span class="sxs-lookup"><span data-stu-id="e2337-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-408">Указанный список квот внутренне не соответствует его дескриптору.</span><span class="sxs-lookup"><span data-stu-id="e2337-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**\_ \_ срок действия оценки ошибки**</span><span class="sxs-lookup"><span data-stu-id="e2337-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-410">622 (0x26E)</span><span class="sxs-lookup"><span data-stu-id="e2337-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-411">{Уведомление Windows Evaluation} Период ознакомительного использования Windows истек.</span><span class="sxs-lookup"><span data-stu-id="e2337-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="e2337-412">Эта система завершит работу через 1 час.</span><span class="sxs-lookup"><span data-stu-id="e2337-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="e2337-413">Чтобы восстановить доступ к этой установке Windows, обновите эту установку с помощью лицензированного дистрибутива этого продукта.</span><span class="sxs-lookup"><span data-stu-id="e2337-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**Ошибка \_ недопустимого \_ \_ перемещения DLL**</span><span class="sxs-lookup"><span data-stu-id="e2337-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-415">623 (0x26F)</span><span class="sxs-lookup"><span data-stu-id="e2337-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-416">{Недопустимое перемещение системной библиотеки DLL} Системная библиотека DLL% HS была перемещена в память.</span><span class="sxs-lookup"><span data-stu-id="e2337-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="e2337-417">Приложение не будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="e2337-417">The application will not run properly.</span></span> <span data-ttu-id="e2337-418">Перемещение произошло, так как библиотека DLL% HS занята диапазоном адресов, зарезервированным для системных библиотек Windows.</span><span class="sxs-lookup"><span data-stu-id="e2337-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="e2337-419">Поставщик, предоставляющий библиотеку DLL, должен быть обращен к новой библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="e2337-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**Ошибка \_ \_ инициализации DLL \_ при неудачном \_ выходе**</span><span class="sxs-lookup"><span data-stu-id="e2337-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-421">624 (0x270)</span><span class="sxs-lookup"><span data-stu-id="e2337-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-422">{Ошибка при инициализации DLL} Не удалось инициализировать приложение, так как работа станции Windows завершается.</span><span class="sxs-lookup"><span data-stu-id="e2337-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**Ошибка при \_ проверке \_ продолжения**</span><span class="sxs-lookup"><span data-stu-id="e2337-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-424">625 (0x271)</span><span class="sxs-lookup"><span data-stu-id="e2337-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-425">Процесс проверки должен перейти к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="e2337-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**Ошибка \_ больше не найдено \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-427">626 (0x272)</span><span class="sxs-lookup"><span data-stu-id="e2337-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-428">Больше нет соответствий для текущего перечисления индекса.</span><span class="sxs-lookup"><span data-stu-id="e2337-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_конфликт списка диапазонов ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-430">627 (0x273)</span><span class="sxs-lookup"><span data-stu-id="e2337-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-431">Не удалось добавить диапазон в список диапазонов из-за конфликта.</span><span class="sxs-lookup"><span data-stu-id="e2337-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**\_несоответствие \_ идентификатора безопасности сервера ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-433">628 (0x274)</span><span class="sxs-lookup"><span data-stu-id="e2337-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-434">Серверный процесс выполняется с идентификатором безопасности, отличным от того, который требуется клиенту.</span><span class="sxs-lookup"><span data-stu-id="e2337-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**Ошибка \_ не \_ удается \_ включить \_ только Deny**</span><span class="sxs-lookup"><span data-stu-id="e2337-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-436">629 (0x275)</span><span class="sxs-lookup"><span data-stu-id="e2337-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-437">Группа, помеченная как "использовать только для запрета", не может быть включена.</span><span class="sxs-lookup"><span data-stu-id="e2337-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ОШИБКА с \_ плавающей запятой \_ нескольких \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-439">630 (0x276)</span><span class="sxs-lookup"><span data-stu-id="e2337-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-440">ОБ Множественные ошибки с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e2337-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ОШИБКА с \_ плавающей запятой \_ множественная \_ ловушка**</span><span class="sxs-lookup"><span data-stu-id="e2337-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-442">631 (0x277)</span><span class="sxs-lookup"><span data-stu-id="e2337-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-443">ОБ Несколько ловушек с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="e2337-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**Ошибка \_ НЕинтерфейса**</span><span class="sxs-lookup"><span data-stu-id="e2337-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-445">632 (0x278)</span><span class="sxs-lookup"><span data-stu-id="e2337-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-446">Запрошенный интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2337-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**\_сбой драйвера ошибки в \_ \_ спящем режиме**</span><span class="sxs-lookup"><span data-stu-id="e2337-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-448">633 (0x279)</span><span class="sxs-lookup"><span data-stu-id="e2337-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-449">{Сбой системы в ждущем режиме} Драйвер% HS не поддерживает режим ожидания.</span><span class="sxs-lookup"><span data-stu-id="e2337-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="e2337-450">Обновление этого драйвера может привести к переходу системы в режим ожидания.</span><span class="sxs-lookup"><span data-stu-id="e2337-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**Ошибка при \_ повреждении \_ системного \_ файла**</span><span class="sxs-lookup"><span data-stu-id="e2337-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-452">634 (0x27A)</span><span class="sxs-lookup"><span data-stu-id="e2337-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-453">Системный файл %1 оказался поврежденным и был заменен.</span><span class="sxs-lookup"><span data-stu-id="e2337-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_минимум обязательств по ошибкам \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-455">635 (0x27B)</span><span class="sxs-lookup"><span data-stu-id="e2337-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-456">{Слишком низкая виртуальная память} В системе недостаточно виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="e2337-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="e2337-457">Windows увеличивает размер файла подкачки виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="e2337-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="e2337-458">Во время этого процесса запросы памяти для некоторых приложений могут быть отклонены.</span><span class="sxs-lookup"><span data-stu-id="e2337-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="e2337-459">Дополнительные сведения см. в справке.</span><span class="sxs-lookup"><span data-stu-id="e2337-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**Ошибка \_ при \_ перечислении PnP при перезапуске \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-461">636 (0x27C)</span><span class="sxs-lookup"><span data-stu-id="e2337-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-462">Устройство было удалено, поэтому перечисление необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="e2337-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**\_ \_ \_ Неправильная подпись системного образа ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-464">637 (0x27D)</span><span class="sxs-lookup"><span data-stu-id="e2337-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-465">{Неустранимая системная ошибка} Образ системы% s не подписан должным образом.</span><span class="sxs-lookup"><span data-stu-id="e2337-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="e2337-466">Файл был заменен подписанным файлом.</span><span class="sxs-lookup"><span data-stu-id="e2337-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="e2337-467">Работа системы завершена.</span><span class="sxs-lookup"><span data-stu-id="e2337-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**Ошибка \_ при \_ перезагрузке PnP \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-469">638 (0x27E)</span><span class="sxs-lookup"><span data-stu-id="e2337-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-470">Устройство не будет запущено без перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="e2337-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**Ошибка " \_ недостаточно \_ энергии"**</span><span class="sxs-lookup"><span data-stu-id="e2337-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-472">639 (0x27F)</span><span class="sxs-lookup"><span data-stu-id="e2337-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-473">Недостаточно энергии для завершения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="e2337-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**Ошибка \_ множественного \_ \_ нарушения сбоя**</span><span class="sxs-lookup"><span data-stu-id="e2337-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-475">640 (0x280)</span><span class="sxs-lookup"><span data-stu-id="e2337-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-476">Ошибка \_ множественного \_ \_ нарушения сбоя</span><span class="sxs-lookup"><span data-stu-id="e2337-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**Ошибка \_ при \_ завершении работы системы**</span><span class="sxs-lookup"><span data-stu-id="e2337-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-478">641 (0x281)</span><span class="sxs-lookup"><span data-stu-id="e2337-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-479">Система находится в процессе завершения работы.</span><span class="sxs-lookup"><span data-stu-id="e2337-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_порт ошибки \_ не \_ задан**</span><span class="sxs-lookup"><span data-stu-id="e2337-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-481">642 (0x282)</span><span class="sxs-lookup"><span data-stu-id="e2337-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-482">Выполнена попытка удаления процессов Дебугпорт, но порт не был связан с процессом.</span><span class="sxs-lookup"><span data-stu-id="e2337-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**Ошибка \_ \_ \_ при проверке версии \_ DS**</span><span class="sxs-lookup"><span data-stu-id="e2337-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-484">643 (0x283)</span><span class="sxs-lookup"><span data-stu-id="e2337-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-485">Эта версия Windows несовместима с версией поведения леса каталога, домена или контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="e2337-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_диапазон ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="e2337-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-487">644 (0x284)</span><span class="sxs-lookup"><span data-stu-id="e2337-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-488">Указанный диапазон не найден в списке диапазонов.</span><span class="sxs-lookup"><span data-stu-id="e2337-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**Ошибка \_ \_ незащищенного \_ режима \_ драйвера**</span><span class="sxs-lookup"><span data-stu-id="e2337-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-490">646 (0x286)</span><span class="sxs-lookup"><span data-stu-id="e2337-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-491">Драйвер не был загружен, так как система загружается в безопасный режим.</span><span class="sxs-lookup"><span data-stu-id="e2337-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**Ошибка \_ при ошибке \_ \_ записи драйвера**</span><span class="sxs-lookup"><span data-stu-id="e2337-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-493">647 (0x287)</span><span class="sxs-lookup"><span data-stu-id="e2337-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-494">Драйвер не был загружен из-за сбоя вызова инициализации.</span><span class="sxs-lookup"><span data-stu-id="e2337-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**Ошибка \_ \_ перечисления устройств \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-496">648 (0x288)</span><span class="sxs-lookup"><span data-stu-id="e2337-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-497">"% HS" обнаружил ошибку при применении питания или чтении конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="e2337-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="e2337-498">Это может быть вызвано сбоем оборудования или неудачным подключением.</span><span class="sxs-lookup"><span data-stu-id="e2337-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**\_точка подключения \_ ошибок \_ не \_ разрешена**</span><span class="sxs-lookup"><span data-stu-id="e2337-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-500">649 (0x289)</span><span class="sxs-lookup"><span data-stu-id="e2337-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-501">Не удалось выполнить операцию создания, так как имя содержит по крайней мере одну точку подключения, которая разрешается в том, к которому не присоединен указанный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="e2337-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**Ошибка \_ недопустимого \_ \_ параметра объекта устройства \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-503">650 (0x28A)</span><span class="sxs-lookup"><span data-stu-id="e2337-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-504">Параметр объекта устройства либо не является допустимым объектом устройства, либо не подключен к тому, указанному в имени файла.</span><span class="sxs-lookup"><span data-stu-id="e2337-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**произошла ошибка \_ MCA \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-506">651 (0x28B)</span><span class="sxs-lookup"><span data-stu-id="e2337-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-507">Произошла ошибка проверки компьютера.</span><span class="sxs-lookup"><span data-stu-id="e2337-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="e2337-508">Дополнительные сведения см. в системном журнале событий.</span><span class="sxs-lookup"><span data-stu-id="e2337-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**Ошибка \_ \_ базы данных драйвера ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-510">652 (0x28C)</span><span class="sxs-lookup"><span data-stu-id="e2337-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-511">Произошла ошибка \[ %2 при \] обработке базы данных драйвера.</span><span class="sxs-lookup"><span data-stu-id="e2337-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**\_ \_ \_ слишком большой системный куст \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="e2337-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-513">653 (0x28D)</span><span class="sxs-lookup"><span data-stu-id="e2337-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-514">Размер системного куста превысил установленный предел.</span><span class="sxs-lookup"><span data-stu-id="e2337-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**Ошибка \_ драйвера \_ ошибки \_ предыдущей \_ выгрузки**</span><span class="sxs-lookup"><span data-stu-id="e2337-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-516">654 (0x28E)</span><span class="sxs-lookup"><span data-stu-id="e2337-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-517">Не удалось загрузить драйвер, поскольку предыдущая версия драйвера по-прежнему находится в памяти.</span><span class="sxs-lookup"><span data-stu-id="e2337-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**Ошибка \_ VOLSNAP \_ Подготовка \_ гибернации**</span><span class="sxs-lookup"><span data-stu-id="e2337-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-519">655 (0x28F)</span><span class="sxs-lookup"><span data-stu-id="e2337-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-520">{Служба теневого копирования томов} Дождитесь, пока служба теневого копирования томов подготовит том% HS для спящего режима.</span><span class="sxs-lookup"><span data-stu-id="e2337-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**Ошибка при переходе в \_ спящий режим \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-522">656 (0x290)</span><span class="sxs-lookup"><span data-stu-id="e2337-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-523">Системе не удалось перейти в режим гибернации (код ошибки% HS).</span><span class="sxs-lookup"><span data-stu-id="e2337-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="e2337-524">Режим гибернации будет отключен до перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="e2337-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**Ошибка \_ PWD \_ слишком \_ длинный**</span><span class="sxs-lookup"><span data-stu-id="e2337-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-526">657 (0x291)</span><span class="sxs-lookup"><span data-stu-id="e2337-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-527">Предоставленный пароль слишком длинный для соответствия политике учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="e2337-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="e2337-528">Выберите более короткий пароль.</span><span class="sxs-lookup"><span data-stu-id="e2337-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**Ошибка \_ \_ ограничения файловой системы \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-530">665 (0x299)</span><span class="sxs-lookup"><span data-stu-id="e2337-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-531">Запрошенная операция не может быть завершена из-за ограничения файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e2337-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**Ошибка \_ утверждения ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-533">668 (0x29C)</span><span class="sxs-lookup"><span data-stu-id="e2337-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-534">Произошла ошибка утверждения.</span><span class="sxs-lookup"><span data-stu-id="e2337-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**Ошибка \_ ACPI \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-536">669 (0x29D)</span><span class="sxs-lookup"><span data-stu-id="e2337-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-537">В подсистеме ACPI произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="e2337-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**\_утверждение ошибки WOW \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-539">670 (0x29E)</span><span class="sxs-lookup"><span data-stu-id="e2337-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-540">Ошибка утверждения WOW.</span><span class="sxs-lookup"><span data-stu-id="e2337-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**Ошибка \_ PnP — \_ неправильная \_ \_ Таблица MPS**</span><span class="sxs-lookup"><span data-stu-id="e2337-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-542">671 (0x29F)</span><span class="sxs-lookup"><span data-stu-id="e2337-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-543">В таблице MPS системного BIOS отсутствует устройство.</span><span class="sxs-lookup"><span data-stu-id="e2337-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="e2337-544">Это устройство не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="e2337-544">This device will not be used.</span></span> <span data-ttu-id="e2337-545">Обратитесь к поставщику системы за обновлением BIOS.</span><span class="sxs-lookup"><span data-stu-id="e2337-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**Ошибка \_ \_ перевода PnP \_ при ошибке**</span><span class="sxs-lookup"><span data-stu-id="e2337-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-547">672 (0x2A0)</span><span class="sxs-lookup"><span data-stu-id="e2337-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-548">Транслятору не удалось перевести ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e2337-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**Ошибка \_ \_ \_ при преобразовании PnP IRQ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-550">673 (0x2A1)</span><span class="sxs-lookup"><span data-stu-id="e2337-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-551">Транслятору IRQ не удалось перевести ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e2337-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**Ошибка \_ \_ Недопустимый \_ идентификатор PNP**</span><span class="sxs-lookup"><span data-stu-id="e2337-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-553">674 (0x2A2)</span><span class="sxs-lookup"><span data-stu-id="e2337-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-554">Драйвер %2 вернул недопустимый идентификатор для дочернего устройства (%3).</span><span class="sxs-lookup"><span data-stu-id="e2337-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**Ошибка \_ \_ отладчика системы пробуждения \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-556">675 (0x2A3)</span><span class="sxs-lookup"><span data-stu-id="e2337-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-557">{Запущен отладчик ядра}. Системный отладчик был вызван прерыванием.</span><span class="sxs-lookup"><span data-stu-id="e2337-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_дескрипторы ошибок \_ закрыты**</span><span class="sxs-lookup"><span data-stu-id="e2337-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-559">676 (0x2A4)</span><span class="sxs-lookup"><span data-stu-id="e2337-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-560">{Handles Closed} Дескрипторы объектов были автоматически закрыты в результате выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="e2337-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**Ошибка при возникновении \_ лишних \_ сведений**</span><span class="sxs-lookup"><span data-stu-id="e2337-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-562">677 (0x2A5)</span><span class="sxs-lookup"><span data-stu-id="e2337-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-563">{Слишком много сведений} Указанный список управления доступом (ACL) содержит больше сведений, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="e2337-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**Ошибка \_ рксакт, \_ необходимая для фиксации \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-565">678 (0x2A6)</span><span class="sxs-lookup"><span data-stu-id="e2337-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-566">Это состояние предупреждения указывает на то, что состояние транзакции уже существует для поддерева реестра, но фиксация транзакции была ранее прервана.</span><span class="sxs-lookup"><span data-stu-id="e2337-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="e2337-567">Фиксация не выполнена, но откат не выполнен (поэтому при необходимости его можно зафиксировать).</span><span class="sxs-lookup"><span data-stu-id="e2337-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_Проверка носителя с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-569">679 (0x2A7)</span><span class="sxs-lookup"><span data-stu-id="e2337-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-570">{Носитель изменен} Возможно, носитель был изменен.</span><span class="sxs-lookup"><span data-stu-id="e2337-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**\_ \_ выполнена подстановка GUID ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-572">680 (0x2A8)</span><span class="sxs-lookup"><span data-stu-id="e2337-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-573">{Подстановка GUID} Во время преобразования глобального идентификатора (GUID) в идентификатор безопасности Windows (SID) не найден префикс GUID, определенный администратором.</span><span class="sxs-lookup"><span data-stu-id="e2337-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="e2337-574">Использовался заменяющий префикс, который не повлечет за собой нарушение безопасности системы.</span><span class="sxs-lookup"><span data-stu-id="e2337-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="e2337-575">Однако это может обеспечить более четкий доступ, чем планировалось.</span><span class="sxs-lookup"><span data-stu-id="e2337-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**Ошибка \_ остановлена \_ в \_ символьную ссылку**</span><span class="sxs-lookup"><span data-stu-id="e2337-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-577">681 (0x2A9)</span><span class="sxs-lookup"><span data-stu-id="e2337-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-578">Операция создания остановлена после достижения символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="e2337-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**Ошибка \_ лонгжумп**</span><span class="sxs-lookup"><span data-stu-id="e2337-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-580">682 (0x2AA)</span><span class="sxs-lookup"><span data-stu-id="e2337-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-581">Выполнен длинный переход.</span><span class="sxs-lookup"><span data-stu-id="e2337-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**Ошибка \_ плугплай \_ запрос \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-583">683 (0x2AB)</span><span class="sxs-lookup"><span data-stu-id="e2337-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-584">Операция запроса самонастраивающийся не выполнена.</span><span class="sxs-lookup"><span data-stu-id="e2337-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**Ошибка \_ очистки \_ консолидации**</span><span class="sxs-lookup"><span data-stu-id="e2337-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-586">684 (0x2AC)</span><span class="sxs-lookup"><span data-stu-id="e2337-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-587">Выполнена консолидация кадров.</span><span class="sxs-lookup"><span data-stu-id="e2337-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_ \_ восстановлен КУСТ реестра \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-589">685 (0x2AD)</span><span class="sxs-lookup"><span data-stu-id="e2337-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-590">{Восстановленный куст реестра} Куст реестра (файл):% HS поврежден и восстановлен.</span><span class="sxs-lookup"><span data-stu-id="e2337-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="e2337-591">Некоторые данные могли быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="e2337-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**\_DLL-библиотека ошибок \_ может \_ быть \_ небезопасной**</span><span class="sxs-lookup"><span data-stu-id="e2337-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-593">686 (0x2AE)</span><span class="sxs-lookup"><span data-stu-id="e2337-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-594">Приложение пытается запустить исполняемый код из модуля% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="e2337-595">Это может быть небезопасным.</span><span class="sxs-lookup"><span data-stu-id="e2337-595">This may be insecure.</span></span> <span data-ttu-id="e2337-596">Доступен альтернативный вариант,% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="e2337-597">Должно ли приложение использовать защищенный модуль% HS?</span><span class="sxs-lookup"><span data-stu-id="e2337-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**\_DLL-библиотека ошибок \_ может \_ быть \_ несовместима**</span><span class="sxs-lookup"><span data-stu-id="e2337-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-599">687 (0x2AF)</span><span class="sxs-lookup"><span data-stu-id="e2337-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-600">Приложение загружает исполняемый код из модуля% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="e2337-601">Это безопасно, но может быть несовместимо с предыдущими выпусками операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e2337-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="e2337-602">Доступен альтернативный вариант,% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="e2337-603">Должно ли приложение использовать защищенный модуль% HS?</span><span class="sxs-lookup"><span data-stu-id="e2337-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**Ошибка \_ DBG, \_ исключение \_ не \_ обработано**</span><span class="sxs-lookup"><span data-stu-id="e2337-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-605">688 (0x2B0)</span><span class="sxs-lookup"><span data-stu-id="e2337-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-606">Отладчик не обработал исключение.</span><span class="sxs-lookup"><span data-stu-id="e2337-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**Ошибка \_ \_ ответа dbg \_ позже**</span><span class="sxs-lookup"><span data-stu-id="e2337-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-608">689 (0x2B1)</span><span class="sxs-lookup"><span data-stu-id="e2337-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-609">Отладчик ответит позже.</span><span class="sxs-lookup"><span data-stu-id="e2337-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**Ошибка \_ dbg \_ не \_ удалось \_ предоставить \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="e2337-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-611">690 (0x2B2)</span><span class="sxs-lookup"><span data-stu-id="e2337-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-612">Отладчик не может предоставить Handle.</span><span class="sxs-lookup"><span data-stu-id="e2337-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**Ошибка \_ \_ прерывания \_ потока dbg**</span><span class="sxs-lookup"><span data-stu-id="e2337-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-614">691 (0x2B3)</span><span class="sxs-lookup"><span data-stu-id="e2337-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-615">Отладчик завершил поток.</span><span class="sxs-lookup"><span data-stu-id="e2337-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**Ошибка \_ \_ завершения \_ процесса dbg**</span><span class="sxs-lookup"><span data-stu-id="e2337-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-617">692 (0x2B4)</span><span class="sxs-lookup"><span data-stu-id="e2337-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-618">Отладчик завершил процесс.</span><span class="sxs-lookup"><span data-stu-id="e2337-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**Ошибка \_ \_ элемента управления dbg \_ C**</span><span class="sxs-lookup"><span data-stu-id="e2337-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-620">693 (0x2B5)</span><span class="sxs-lookup"><span data-stu-id="e2337-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-621">Отладчик получил управление C.</span><span class="sxs-lookup"><span data-stu-id="e2337-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**Ошибка \_ dbg \_ PRINTEXCEPTION \_ C**</span><span class="sxs-lookup"><span data-stu-id="e2337-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-623">694 (0x2B6)</span><span class="sxs-lookup"><span data-stu-id="e2337-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-624">Отладчик выпечатал исключение для элемента управления C.</span><span class="sxs-lookup"><span data-stu-id="e2337-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**Ошибка \_ dbg \_ рипексцептион**</span><span class="sxs-lookup"><span data-stu-id="e2337-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-626">695 (0x2B7)</span><span class="sxs-lookup"><span data-stu-id="e2337-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-627">Отладчик получил исключение RIP.</span><span class="sxs-lookup"><span data-stu-id="e2337-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**Ошибка \_ при \_ разрыве элемента управления dbg \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-629">696 (0x2B8)</span><span class="sxs-lookup"><span data-stu-id="e2337-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-630">Отладчик получил прерывание управления.</span><span class="sxs-lookup"><span data-stu-id="e2337-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**Ошибка \_ при \_ \_ возникновении команды dbg**</span><span class="sxs-lookup"><span data-stu-id="e2337-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-632">697 (0x2B9)</span><span class="sxs-lookup"><span data-stu-id="e2337-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-633">Исключение при обмене данными команды отладчика.</span><span class="sxs-lookup"><span data-stu-id="e2337-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**\_имя объекта \_ ошибки \_ существует**</span><span class="sxs-lookup"><span data-stu-id="e2337-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-635">698 (0x2BA)</span><span class="sxs-lookup"><span data-stu-id="e2337-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-636">{Объект существует} Предпринята попытка создать объект, и уже существовало имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e2337-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**\_поток ошибок \_ был \_ приостановлен**</span><span class="sxs-lookup"><span data-stu-id="e2337-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-638">699 (0x2BB)</span><span class="sxs-lookup"><span data-stu-id="e2337-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-639">{Поток приостановлен} Прерывание потока произошло во время приостановки потока.</span><span class="sxs-lookup"><span data-stu-id="e2337-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="e2337-640">Поток возобновлен, и завершение завершено.</span><span class="sxs-lookup"><span data-stu-id="e2337-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_изображение ошибки \_ не \_ в \_ базовом**</span><span class="sxs-lookup"><span data-stu-id="e2337-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-642">700 (0x2BC)</span><span class="sxs-lookup"><span data-stu-id="e2337-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-643">{Перемещается образ} Не удалось сопоставить файл изображения по адресу, указанному в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="e2337-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="e2337-644">На этом образе должны быть выполнены локальные исправления.</span><span class="sxs-lookup"><span data-stu-id="e2337-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**Ошибка \_ при \_ создании состояния рксакт \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-646">701 (0x2BD)</span><span class="sxs-lookup"><span data-stu-id="e2337-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-647">Это состояние информационного уровня указывает на то, что указанное состояние транзакции поддерева реестра еще не существует и его пришлось создавать.</span><span class="sxs-lookup"><span data-stu-id="e2337-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_уведомление о сегменте ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-649">702 (0x2BE)</span><span class="sxs-lookup"><span data-stu-id="e2337-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-650">{Загрузка сегмента} Виртуальная машина DOS (VDM) загружает, выгружает или перемещает образ сегмента программы MS-DOS или Win16.</span><span class="sxs-lookup"><span data-stu-id="e2337-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="e2337-651">Исключение вызывается, чтобы отладчик мог загружать, выгружать или отлаживать символы и точки останова в этих 16-битных сегментах.</span><span class="sxs-lookup"><span data-stu-id="e2337-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**Ошибка при \_ неправильном \_ текущем \_ каталоге**</span><span class="sxs-lookup"><span data-stu-id="e2337-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-653">703 (0x2BF)</span><span class="sxs-lookup"><span data-stu-id="e2337-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-654">{Недопустимый текущий каталог} Процесс не может переключиться на текущий каталог запуска% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="e2337-655">Нажмите кнопку ОК, чтобы присвоить текущему каталогу значение% HS, или нажмите кнопку Отмена для выхода.</span><span class="sxs-lookup"><span data-stu-id="e2337-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**Ошибка \_ \_ чтения ft \_ Read \_ из \_ резервной копии**</span><span class="sxs-lookup"><span data-stu-id="e2337-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-657">704 (0x2C0)</span><span class="sxs-lookup"><span data-stu-id="e2337-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-658">{Избыточное чтение} Чтобы удовлетворить запрос на чтение, отказоустойчивая файловая система NT успешно прочитала запрошенные данные из избыточной копии.</span><span class="sxs-lookup"><span data-stu-id="e2337-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="e2337-659">Это было сделано из-за сбоя файловой системы на члене отказоустойчивого тома, но ему не удалось переназначить неисправный участок устройства.</span><span class="sxs-lookup"><span data-stu-id="e2337-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**Ошибка \_ при \_ \_ восстановлении записи ft**</span><span class="sxs-lookup"><span data-stu-id="e2337-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-661">705 (0x2C1)</span><span class="sxs-lookup"><span data-stu-id="e2337-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-662">{Избыточная запись} Для удовлетворения запроса на запись отказоустойчивая файловая система NT успешно написала избыточную копию информации.</span><span class="sxs-lookup"><span data-stu-id="e2337-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="e2337-663">Это было сделано из-за того, что в файловой системе произошла ошибка на члене отказоустойчивого тома, но ему не удалось переназначить неисправный участок устройства.</span><span class="sxs-lookup"><span data-stu-id="e2337-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**\_несоответствие \_ типов компьютеров с ИЗОБРАЖЕНИЕм ошибки \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-665">706 (0x2C2)</span><span class="sxs-lookup"><span data-stu-id="e2337-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-666">{Несоответствие типа компьютера} Файл образа% HS допустим, но относится к типу компьютера, отличного от текущего компьютера.</span><span class="sxs-lookup"><span data-stu-id="e2337-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="e2337-667">Нажмите кнопку ОК, чтобы продолжить, или кнопку Отмена, чтобы завершить загрузку библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="e2337-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**Ошибка при \_ получении \_ части**</span><span class="sxs-lookup"><span data-stu-id="e2337-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-669">707 (0x2C3)</span><span class="sxs-lookup"><span data-stu-id="e2337-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-670">{Получено частичных данных} Сетевой транспорт вернул частичные данные клиенту.</span><span class="sxs-lookup"><span data-stu-id="e2337-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="e2337-671">Остальные данные будут отправлены позже.</span><span class="sxs-lookup"><span data-stu-id="e2337-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**сообщение об ОШИБКе \_ Отправлено \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-673">708 (0x2C4)</span><span class="sxs-lookup"><span data-stu-id="e2337-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-674">{Получено срочных данных} Сетевой транспорт вернул данные клиенту, который был помечен как отправленный удаленной системой.</span><span class="sxs-lookup"><span data-stu-id="e2337-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**Ошибка при \_ получении частично отправленного сообщения \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-676">709 (0x2C5)</span><span class="sxs-lookup"><span data-stu-id="e2337-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-677">{Получено частично отправленных данных} Сетевой транспорт вернул частичные данные клиенту, и эти данные были помечены удаленной системой как отправленные.</span><span class="sxs-lookup"><span data-stu-id="e2337-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="e2337-678">Остальные данные будут отправлены позже.</span><span class="sxs-lookup"><span data-stu-id="e2337-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**\_событие ошибки \_ выполнено**</span><span class="sxs-lookup"><span data-stu-id="e2337-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-680">710 (0x2C6)</span><span class="sxs-lookup"><span data-stu-id="e2337-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-681">{Событие TDI завершено} Индикатор TDI успешно завершил работу.</span><span class="sxs-lookup"><span data-stu-id="e2337-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**\_ \_ ожидание события ошибки**</span><span class="sxs-lookup"><span data-stu-id="e2337-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-683">711 (0x2C7)</span><span class="sxs-lookup"><span data-stu-id="e2337-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-684">{Ожидается событие TDI} Индикатор TDI перешел в состояние ожидания.</span><span class="sxs-lookup"><span data-stu-id="e2337-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**Ошибка при \_ проверке \_ файловой \_ системы**</span><span class="sxs-lookup"><span data-stu-id="e2337-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-686">712 (0x2C8)</span><span class="sxs-lookup"><span data-stu-id="e2337-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-687">Проверка файловой системы на% wZ.</span><span class="sxs-lookup"><span data-stu-id="e2337-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**Ошибка при \_ неустранимом \_ \_ выходе из приложения**</span><span class="sxs-lookup"><span data-stu-id="e2337-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-689">713 (0x2C9)</span><span class="sxs-lookup"><span data-stu-id="e2337-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-690">{Неустранимый выход из приложения}% HS.</span><span class="sxs-lookup"><span data-stu-id="e2337-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**Ошибка \_ предопределенного \_ маркера**</span><span class="sxs-lookup"><span data-stu-id="e2337-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-692">714 (0x2CA)</span><span class="sxs-lookup"><span data-stu-id="e2337-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-693">На указанный раздел реестра ссылается Стандартный маркер.</span><span class="sxs-lookup"><span data-stu-id="e2337-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**Ошибка \_ была \_ разблокирована**</span><span class="sxs-lookup"><span data-stu-id="e2337-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-695">715 (0x2CB)</span><span class="sxs-lookup"><span data-stu-id="e2337-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-696">{Страница разблокирована} Защита страницы заблокированной страницы изменена на "нет доступа", и страница была разблокирована из памяти и из процесса.</span><span class="sxs-lookup"><span data-stu-id="e2337-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_Уведомление службы \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-698">716 (0x2CC)</span><span class="sxs-lookup"><span data-stu-id="e2337-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-699">% HS</span><span class="sxs-lookup"><span data-stu-id="e2337-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**Ошибка \_ \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="e2337-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-701">717 (0x2CD)</span><span class="sxs-lookup"><span data-stu-id="e2337-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-702">{Страница заблокирована} Одна из страниц для блокировки уже заблокирована.</span><span class="sxs-lookup"><span data-stu-id="e2337-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**Ошибка \_ журнала \_ ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-704">718 (0x2CE)</span><span class="sxs-lookup"><span data-stu-id="e2337-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-705">Всплывающее окно приложения: %1: %2</span><span class="sxs-lookup"><span data-stu-id="e2337-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**Ошибка \_ уже \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="e2337-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-707">719 (0x2CF)</span><span class="sxs-lookup"><span data-stu-id="e2337-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-708">Ошибка \_ уже \_ Win32</span><span class="sxs-lookup"><span data-stu-id="e2337-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**\_несоответствие типов компьютеров с изображением ошибки \_ \_ \_ \_ exe**</span><span class="sxs-lookup"><span data-stu-id="e2337-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-710">720 (0x2D0)</span><span class="sxs-lookup"><span data-stu-id="e2337-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-711">{Несоответствие типа компьютера} Файл образа% HS допустим, но относится к типу компьютера, отличного от текущего компьютера.</span><span class="sxs-lookup"><span data-stu-id="e2337-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**Ошибка \_ не \_ \_ выполнен**</span><span class="sxs-lookup"><span data-stu-id="e2337-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-713">721 (0x2D1)</span><span class="sxs-lookup"><span data-stu-id="e2337-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-714">Выполнен оператор yield, и нет доступных потоков для выполнения.</span><span class="sxs-lookup"><span data-stu-id="e2337-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**\_возобновление таймера ошибок \_ \_ проигнорировано**</span><span class="sxs-lookup"><span data-stu-id="e2337-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-716">722 (0x2D2)</span><span class="sxs-lookup"><span data-stu-id="e2337-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-717">Флаг возобновляемости для API таймера проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="e2337-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**\_НЕобработанное арбитраж ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-719">723 (0x2D3)</span><span class="sxs-lookup"><span data-stu-id="e2337-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-720">Арбитр имеет отложенное разрешение на эти ресурсы родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="e2337-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**Ошибка \_ CARDBUS \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="e2337-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-722">724 (0x2D4)</span><span class="sxs-lookup"><span data-stu-id="e2337-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-723">Не удается запустить вставленное устройство CardBus из-за ошибки конфигурации в "% HS".</span><span class="sxs-lookup"><span data-stu-id="e2337-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии процессора MP**</span><span class="sxs-lookup"><span data-stu-id="e2337-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-725">725 (0x2D5)</span><span class="sxs-lookup"><span data-stu-id="e2337-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-726">Процессоры в этой многопроцессорной системе имеют разные уровни редакции.</span><span class="sxs-lookup"><span data-stu-id="e2337-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="e2337-727">Чтобы использовать все процессоры, операционная система ограничена функциями минимально производительного процессора в системе.</span><span class="sxs-lookup"><span data-stu-id="e2337-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="e2337-728">При возникновении проблем с этой системой обратитесь к производителю ЦП, чтобы узнать, поддерживается ли этот сочетание процессоров.</span><span class="sxs-lookup"><span data-stu-id="e2337-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**Ошибка в \_ режиме гибернации**</span><span class="sxs-lookup"><span data-stu-id="e2337-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-730">726 (0x2D6)</span><span class="sxs-lookup"><span data-stu-id="e2337-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-731">Система переведена в режим гибернации.</span><span class="sxs-lookup"><span data-stu-id="e2337-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**Ошибка \_ возобновления \_ режима гибернации**</span><span class="sxs-lookup"><span data-stu-id="e2337-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-733">727 (0x2D7)</span><span class="sxs-lookup"><span data-stu-id="e2337-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-734">Система была восстановлена из режима гибернации.</span><span class="sxs-lookup"><span data-stu-id="e2337-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**\_встроенное по ошибки \_ Обновлено**</span><span class="sxs-lookup"><span data-stu-id="e2337-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-736">728 (0x2D8)</span><span class="sxs-lookup"><span data-stu-id="e2337-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-737">Windows обнаружила, что системное встроенное по (BIOS) обновило \[ предыдущую дату встроенного по (%2, текущая дата встроенного по "%3") \] .</span><span class="sxs-lookup"><span data-stu-id="e2337-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**драйверы с ОШИБКАми \_ \_ утечка \_ заблокированных \_ страниц**</span><span class="sxs-lookup"><span data-stu-id="e2337-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-739">729 (0x2D9)</span><span class="sxs-lookup"><span data-stu-id="e2337-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-740">Драйвер устройства вызывает утечку заблокированных страниц ввода-вывода, что приводит к снижению производительности системы.</span><span class="sxs-lookup"><span data-stu-id="e2337-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="e2337-741">Система автоматически включила код отслеживания, чтобы попытаться обнаружить причину.</span><span class="sxs-lookup"><span data-stu-id="e2337-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**\_Система пробуждения с ошибкой \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-743">730 (0x2DA)</span><span class="sxs-lookup"><span data-stu-id="e2337-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-744">Система имеет пробудится.</span><span class="sxs-lookup"><span data-stu-id="e2337-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**\_Ожидание ошибки \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e2337-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-746">731 (0x2DB)</span><span class="sxs-lookup"><span data-stu-id="e2337-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-747">\_Ожидание ошибки \_ 1</span><span class="sxs-lookup"><span data-stu-id="e2337-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**\_Ожидание ошибки \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e2337-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-749">732 (0x2DC)</span><span class="sxs-lookup"><span data-stu-id="e2337-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-750">\_Ожидание ошибки \_ 2</span><span class="sxs-lookup"><span data-stu-id="e2337-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**Ошибка \_ ожидания \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e2337-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-752">733 (0x2DD)</span><span class="sxs-lookup"><span data-stu-id="e2337-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-753">Ошибка \_ ожидания \_ 3</span><span class="sxs-lookup"><span data-stu-id="e2337-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**Ошибка \_ ожидания \_ 63**</span><span class="sxs-lookup"><span data-stu-id="e2337-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-755">734 (0x2DE)</span><span class="sxs-lookup"><span data-stu-id="e2337-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-756">Ошибка \_ ожидания \_ 63</span><span class="sxs-lookup"><span data-stu-id="e2337-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**Ошибка \_ прекращения \_ ожидания \_ 0**</span><span class="sxs-lookup"><span data-stu-id="e2337-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-758">735 (0x2DF)</span><span class="sxs-lookup"><span data-stu-id="e2337-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-759">Ошибка \_ прекращения \_ ожидания \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2337-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**Ошибка \_ прекращения \_ ожидания \_ 63**</span><span class="sxs-lookup"><span data-stu-id="e2337-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-761">736 (0x2E0)</span><span class="sxs-lookup"><span data-stu-id="e2337-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-762">Ошибка \_ прекращения \_ ожидания \_ 63</span><span class="sxs-lookup"><span data-stu-id="e2337-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**Ошибка \_ пользователь \_ APC**</span><span class="sxs-lookup"><span data-stu-id="e2337-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-764">737 (0x2E1)</span><span class="sxs-lookup"><span data-stu-id="e2337-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-765">Ошибка \_ пользователь \_ APC</span><span class="sxs-lookup"><span data-stu-id="e2337-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**Ошибка при \_ ядре \_ APC**</span><span class="sxs-lookup"><span data-stu-id="e2337-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-767">738 (0x2E2)</span><span class="sxs-lookup"><span data-stu-id="e2337-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-768">Ошибка при \_ ядре \_ APC</span><span class="sxs-lookup"><span data-stu-id="e2337-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**предупреждение об ОШИБКе \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-770">739 (0x2E3)</span><span class="sxs-lookup"><span data-stu-id="e2337-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-771">предупреждение об ОШИБКе \_</span><span class="sxs-lookup"><span data-stu-id="e2337-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**\_требуется повышение уровня ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-773">740 (0x2E4)</span><span class="sxs-lookup"><span data-stu-id="e2337-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-774">Запрошенная операция требует повышения прав.</span><span class="sxs-lookup"><span data-stu-id="e2337-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**Ошибка \_ при повторном анализе**</span><span class="sxs-lookup"><span data-stu-id="e2337-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-776">741 (0x2E5)</span><span class="sxs-lookup"><span data-stu-id="e2337-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-777">Диспетчер объектов должен выполнить повторное синтаксический анализ, так как имя файла привело к созданию символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="e2337-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**Ошибка \_ OPLOCK \_ break \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-779">742 (0x2E6)</span><span class="sxs-lookup"><span data-stu-id="e2337-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-780">Операция открытия или создания завершена во время разрыва оппортунистической блокировки.</span><span class="sxs-lookup"><span data-stu-id="e2337-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**Ошибка \_ \_ подключения тома**</span><span class="sxs-lookup"><span data-stu-id="e2337-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-782">743 (0x2E7)</span><span class="sxs-lookup"><span data-stu-id="e2337-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-783">Файловая система подключила новый том.</span><span class="sxs-lookup"><span data-stu-id="e2337-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**Ошибка \_ рксакт \_ COMMITTED**</span><span class="sxs-lookup"><span data-stu-id="e2337-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-785">744 (0x2E8)</span><span class="sxs-lookup"><span data-stu-id="e2337-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-786">Это состояние успешного выполнения указывает, что состояние транзакции уже существует для поддерева реестра, но фиксация транзакции была ранее прервана.</span><span class="sxs-lookup"><span data-stu-id="e2337-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="e2337-787">Фиксация завершена.</span><span class="sxs-lookup"><span data-stu-id="e2337-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**\_Очистка уведомления об ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-789">745 (0x2E9)</span><span class="sxs-lookup"><span data-stu-id="e2337-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-790">Это означает, что запрос на уведомление об изменении был завершен из-за закрытия маркера, который сделал запрос на уведомление об изменении.</span><span class="sxs-lookup"><span data-stu-id="e2337-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**Ошибка \_ основного \_ транспортного \_ подключения \_ не удалось**</span><span class="sxs-lookup"><span data-stu-id="e2337-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-792">746 (0x2EA)</span><span class="sxs-lookup"><span data-stu-id="e2337-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-793">{Сбой подключения к основному транспорту} Предпринята попытка подключения к удаленному серверу% HS на основном транспорте, но подключение не выполнено.</span><span class="sxs-lookup"><span data-stu-id="e2337-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="e2337-794">Компьютер смог подключиться к дополнительному транспорту.</span><span class="sxs-lookup"><span data-stu-id="e2337-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_Переход на \_ сбой \_ страницы ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-796">747 (0x2EB)</span><span class="sxs-lookup"><span data-stu-id="e2337-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-797">Ошибка страницы была вызвана ошибкой перехода.</span><span class="sxs-lookup"><span data-stu-id="e2337-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**\_ \_ \_ нулевое требование к ошибке страницы \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-799">748 (0x2EC)</span><span class="sxs-lookup"><span data-stu-id="e2337-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-800">Ошибка страницы была вызвана нулевой ошибкой спроса.</span><span class="sxs-lookup"><span data-stu-id="e2337-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**Ошибка \_ \_ \_ при копировании ошибки страницы \_ при \_ записи**</span><span class="sxs-lookup"><span data-stu-id="e2337-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-802">749 (0x2ED)</span><span class="sxs-lookup"><span data-stu-id="e2337-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-803">Ошибка страницы была вызвана нулевой ошибкой спроса.</span><span class="sxs-lookup"><span data-stu-id="e2337-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**\_Страница " \_ сбой страницы \_ защиты \_ страниц ошибок"**</span><span class="sxs-lookup"><span data-stu-id="e2337-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-805">750 (0x2EE)</span><span class="sxs-lookup"><span data-stu-id="e2337-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-806">Ошибка страницы была вызвана нулевой ошибкой спроса.</span><span class="sxs-lookup"><span data-stu-id="e2337-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_ \_ \_ файл подкачки ошибки страницы ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-808">751 (0x2EF)</span><span class="sxs-lookup"><span data-stu-id="e2337-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-809">Ошибка страницы была удовлетворена считыванием данных с дополнительного устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="e2337-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**\_ \_ Блокировка страницы кэша \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-811">752 (0x2F0)</span><span class="sxs-lookup"><span data-stu-id="e2337-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-812">Кэшированная страница заблокирована во время операции.</span><span class="sxs-lookup"><span data-stu-id="e2337-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**аварийный \_ \_ дамп ошибок**</span><span class="sxs-lookup"><span data-stu-id="e2337-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-814">753 (0x2F1)</span><span class="sxs-lookup"><span data-stu-id="e2337-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-815">Аварийный дамп существует в файле подкачки.</span><span class="sxs-lookup"><span data-stu-id="e2337-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**\_буферы ошибок \_ все \_ нули**</span><span class="sxs-lookup"><span data-stu-id="e2337-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-817">754 (0x2F2)</span><span class="sxs-lookup"><span data-stu-id="e2337-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-818">Указанный буфер содержит все нули.</span><span class="sxs-lookup"><span data-stu-id="e2337-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**Ошибка \_ при повторном анализе \_ объекта**</span><span class="sxs-lookup"><span data-stu-id="e2337-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-820">755 (0x2F3)</span><span class="sxs-lookup"><span data-stu-id="e2337-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-821">Диспетчер объектов должен выполнить повторное синтаксический анализ, так как имя файла привело к созданию символьной ссылки.</span><span class="sxs-lookup"><span data-stu-id="e2337-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**\_ \_ изменились требования к РЕСУРСУ об ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-823">756 (0x2F4)</span><span class="sxs-lookup"><span data-stu-id="e2337-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-824">Устройство успешно выполнило запрос на завершение и его требования к ресурсам изменились.</span><span class="sxs-lookup"><span data-stu-id="e2337-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**\_Преобразование ошибок \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="e2337-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-826">757 (0x2F5)</span><span class="sxs-lookup"><span data-stu-id="e2337-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-827">Переводчик преобразует эти ресурсы в глобальное пространство, и дальнейшие переводы не выполняются.</span><span class="sxs-lookup"><span data-stu-id="e2337-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_нет ошибок \_ для \_ завершения**</span><span class="sxs-lookup"><span data-stu-id="e2337-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-829">758 (0x2F6)</span><span class="sxs-lookup"><span data-stu-id="e2337-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-830">Завершение процесса не имеет потоков для завершения.</span><span class="sxs-lookup"><span data-stu-id="e2337-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**Ошибка \_ процесса, \_ не \_ в \_ задании**</span><span class="sxs-lookup"><span data-stu-id="e2337-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-832">759 (0x2F7)</span><span class="sxs-lookup"><span data-stu-id="e2337-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-833">Указанный процесс не является частью задания.</span><span class="sxs-lookup"><span data-stu-id="e2337-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**Ошибка \_ процесса \_ в \_ задании**</span><span class="sxs-lookup"><span data-stu-id="e2337-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-835">760 (0x2F8)</span><span class="sxs-lookup"><span data-stu-id="e2337-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-836">Указанный процесс является частью задания.</span><span class="sxs-lookup"><span data-stu-id="e2337-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**Ошибка \_ VOLSNAP \_ режим гибернации \_ готов**</span><span class="sxs-lookup"><span data-stu-id="e2337-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-838">761 (0x2F9)</span><span class="sxs-lookup"><span data-stu-id="e2337-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-839">{Служба теневого копирования томов} Теперь система готова к переходу в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="e2337-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**Ошибка \_ фсфилтер \_ операция \_ \_ успешно завершена**</span><span class="sxs-lookup"><span data-stu-id="e2337-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-841">762 (0x2FA)</span><span class="sxs-lookup"><span data-stu-id="e2337-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-842">Файловая система или драйвер фильтра файловой системы успешно завершили операцию Фсфилтер.</span><span class="sxs-lookup"><span data-stu-id="e2337-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**\_вектор прерываний ошибок \_ \_ уже \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="e2337-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-844">763 (0x2FB)</span><span class="sxs-lookup"><span data-stu-id="e2337-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-845">Указанный вектор прерывания уже подключен.</span><span class="sxs-lookup"><span data-stu-id="e2337-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**\_прерывание ошибки \_ по-прежнему \_ подключено**</span><span class="sxs-lookup"><span data-stu-id="e2337-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-847">764 (0x2FC)</span><span class="sxs-lookup"><span data-stu-id="e2337-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-848">Указанный вектор прерывания все еще подключен.</span><span class="sxs-lookup"><span data-stu-id="e2337-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**Ошибка при \_ ожидании \_ \_ жесткой блокировки**</span><span class="sxs-lookup"><span data-stu-id="e2337-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-850">765 (0x2FD)</span><span class="sxs-lookup"><span data-stu-id="e2337-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-851">Операция заблокирована в ожидании нежесткой блокировки.</span><span class="sxs-lookup"><span data-stu-id="e2337-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**Ошибка \_ \_ обработки исключения \_ dbg**</span><span class="sxs-lookup"><span data-stu-id="e2337-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-853">766 (0x2FE)</span><span class="sxs-lookup"><span data-stu-id="e2337-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-854">Отладчик обработал исключение.</span><span class="sxs-lookup"><span data-stu-id="e2337-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**Ошибка \_ dbg \_ Continue**</span><span class="sxs-lookup"><span data-stu-id="e2337-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-856">767 (0x2FF)</span><span class="sxs-lookup"><span data-stu-id="e2337-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-857">Продолжение работы отладчика.</span><span class="sxs-lookup"><span data-stu-id="e2337-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_стек POP обратного вызова ошибки \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-859">768 (0x300)</span><span class="sxs-lookup"><span data-stu-id="e2337-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-860">В обратном вызове пользовательского режима возникло исключение, и необходимо удалить кадр обратного вызова ядра.</span><span class="sxs-lookup"><span data-stu-id="e2337-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**\_Сжатие ошибок \_ отключено**</span><span class="sxs-lookup"><span data-stu-id="e2337-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-862">769 (0x301)</span><span class="sxs-lookup"><span data-stu-id="e2337-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-863">Сжатие для этого тома отключено.</span><span class="sxs-lookup"><span data-stu-id="e2337-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**Ошибка \_ кантфетчбакквардс**</span><span class="sxs-lookup"><span data-stu-id="e2337-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-865">770 (0x302)</span><span class="sxs-lookup"><span data-stu-id="e2337-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-866">Поставщик данных не может получить обратно через результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="e2337-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**Ошибка \_ кантскроллбакквардс**</span><span class="sxs-lookup"><span data-stu-id="e2337-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-868">771 (0x303)</span><span class="sxs-lookup"><span data-stu-id="e2337-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-869">Поставщик данных не может прокручиваться назад по результирующему набору.</span><span class="sxs-lookup"><span data-stu-id="e2337-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**Ошибка \_ ровснотрелеасед**</span><span class="sxs-lookup"><span data-stu-id="e2337-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-871">772 (0x304)</span><span class="sxs-lookup"><span data-stu-id="e2337-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-872">Поставщик данных требует, чтобы ранее выбранные данные были освобождены перед запросом на получение дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="e2337-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**Ошибка \_ неверных \_ \_ флагов доступа**</span><span class="sxs-lookup"><span data-stu-id="e2337-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-874">773 (0x305)</span><span class="sxs-lookup"><span data-stu-id="e2337-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-875">Поставщику данных не удалось интерпретировать флаги, заданные для привязки столбца в методе доступа.</span><span class="sxs-lookup"><span data-stu-id="e2337-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_ \_ обнаружены ошибки**</span><span class="sxs-lookup"><span data-stu-id="e2337-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-877">774 (0x306)</span><span class="sxs-lookup"><span data-stu-id="e2337-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-878">При обработке запроса произошла одна или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="e2337-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**Ошибка \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="e2337-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-880">775 (0x307)</span><span class="sxs-lookup"><span data-stu-id="e2337-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-881">Реализация не может выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="e2337-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**запрос об ОШИБКе \_ \_ вне \_ \_ последовательности**</span><span class="sxs-lookup"><span data-stu-id="e2337-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-883">776 (0x308)</span><span class="sxs-lookup"><span data-stu-id="e2337-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-884">Клиент компонента запросил операцию, которая не является допустимой для состояния экземпляра компонента.</span><span class="sxs-lookup"><span data-stu-id="e2337-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**Ошибка \_ \_ при синтаксическом АНАЛИЗЕ версии ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-886">777 (0x309)</span><span class="sxs-lookup"><span data-stu-id="e2337-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-887">Не удалось проанализировать номер версии.</span><span class="sxs-lookup"><span data-stu-id="e2337-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**Ошибка \_ бадстартпоситион**</span><span class="sxs-lookup"><span data-stu-id="e2337-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-889">778 (0x30A)</span><span class="sxs-lookup"><span data-stu-id="e2337-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-890">Недопустимая Начальная Расположение итератора.</span><span class="sxs-lookup"><span data-stu-id="e2337-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_аппаратная память с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-892">779 (0x30B)</span><span class="sxs-lookup"><span data-stu-id="e2337-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-893">Оборудование сообщило о неисправимой ошибке памяти.</span><span class="sxs-lookup"><span data-stu-id="e2337-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**Ошибка \_ \_ восстановления диска \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="e2337-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-895">780 (0x30C)</span><span class="sxs-lookup"><span data-stu-id="e2337-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-896">Запрошенная операция требует, чтобы была включена самовосстановление.</span><span class="sxs-lookup"><span data-stu-id="e2337-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ОШИБКА не \_ хватает \_ ресурсов \_ для \_ указанного \_ общего \_ \_ размера раздела**</span><span class="sxs-lookup"><span data-stu-id="e2337-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-898">781 (0x30D)</span><span class="sxs-lookup"><span data-stu-id="e2337-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-899">В куче рабочего стола произошла ошибка при выделении памяти для сеанса.</span><span class="sxs-lookup"><span data-stu-id="e2337-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="e2337-900">Дополнительные сведения см. в журнале системных событий.</span><span class="sxs-lookup"><span data-stu-id="e2337-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**Переход на нечувствительный к \_ системе ошибка \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-902">782 (0x30E)</span><span class="sxs-lookup"><span data-stu-id="e2337-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-903">Состояние питания системы переходит с %2 на %3.</span><span class="sxs-lookup"><span data-stu-id="e2337-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**\_ \_ \_ сложный переход от системы \_ с ошибками**</span><span class="sxs-lookup"><span data-stu-id="e2337-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-905">783 (0x30F)</span><span class="sxs-lookup"><span data-stu-id="e2337-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-906">Состояние питания системы переходит с %2 на %3, но может ввести %4.</span><span class="sxs-lookup"><span data-stu-id="e2337-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**Ошибка \_ MCA, \_ исключение**</span><span class="sxs-lookup"><span data-stu-id="e2337-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-908">784 (0x310)</span><span class="sxs-lookup"><span data-stu-id="e2337-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-909">Поток отправляется с ИСКЛЮЧЕНИЕм MCA из-за MCA.</span><span class="sxs-lookup"><span data-stu-id="e2337-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**Ошибка \_ доступа к \_ аудиту \_ с помощью \_ политики**</span><span class="sxs-lookup"><span data-stu-id="e2337-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-911">785 (0x311)</span><span class="sxs-lookup"><span data-stu-id="e2337-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-912">Доступ к %1 отслеживается правилом политики %2.</span><span class="sxs-lookup"><span data-stu-id="e2337-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**\_доступ к ошибкам \_ \_ не отключен \_ безопасный \_ Пользовательский интерфейс \_ с помощью \_ политики**</span><span class="sxs-lookup"><span data-stu-id="e2337-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-914">786 (0x312)</span><span class="sxs-lookup"><span data-stu-id="e2337-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-915">Доступ к %1 ограничен администратором с помощью правила политики %2.</span><span class="sxs-lookup"><span data-stu-id="e2337-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**Ошибка при отмене \_ \_ хиберфиле**</span><span class="sxs-lookup"><span data-stu-id="e2337-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-917">787 (0x313)</span><span class="sxs-lookup"><span data-stu-id="e2337-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-918">Допустимый файл гибернации стал недействительным и должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="e2337-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**Ошибка при потере связи с \_ \_ вритебехинд \_ данных \_ сети \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-920">788 (0x314)</span><span class="sxs-lookup"><span data-stu-id="e2337-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-921">{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS; данные потеряны.</span><span class="sxs-lookup"><span data-stu-id="e2337-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="e2337-922">Эта ошибка может быть вызвана проблемами с сетевым подключением.</span><span class="sxs-lookup"><span data-stu-id="e2337-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="e2337-923">Попробуйте сохранить этот файл в другой части.</span><span class="sxs-lookup"><span data-stu-id="e2337-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**произошла ошибка при \_ утере \_ \_ \_ сетевого \_ сервера данных вритебехинд \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-925">789 (0x315)</span><span class="sxs-lookup"><span data-stu-id="e2337-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-926">{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS; данные потеряны.</span><span class="sxs-lookup"><span data-stu-id="e2337-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="e2337-927">Эта ошибка была возвращена сервером, на котором существует файл.</span><span class="sxs-lookup"><span data-stu-id="e2337-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="e2337-928">Попробуйте сохранить этот файл в другой части.</span><span class="sxs-lookup"><span data-stu-id="e2337-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**Ошибка \_ потери \_ \_ данных о \_ локальном \_ диске \_ вритебехинд**</span><span class="sxs-lookup"><span data-stu-id="e2337-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-930">790 (0x316)</span><span class="sxs-lookup"><span data-stu-id="e2337-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-931">{Сбой отложенной записи} Windows не удалось сохранить все данные для файла% HS; данные потеряны.</span><span class="sxs-lookup"><span data-stu-id="e2337-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="e2337-932">Эта ошибка может возникать, если устройство было удалено или носитель защищен от записи.</span><span class="sxs-lookup"><span data-stu-id="e2337-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**Ошибка \_ неправильной \_ \_ таблицы мкфг**</span><span class="sxs-lookup"><span data-stu-id="e2337-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-934">791 (0x317)</span><span class="sxs-lookup"><span data-stu-id="e2337-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-935">Ресурсы, необходимые для этого устройства, конфликтуют с таблицей МКФГ.</span><span class="sxs-lookup"><span data-stu-id="e2337-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**Ошибка \_ \_ восстановления диска \_ перенаправлено**</span><span class="sxs-lookup"><span data-stu-id="e2337-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-937">792 (0x318)</span><span class="sxs-lookup"><span data-stu-id="e2337-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-938">Не удалось выполнить восстановление тома, пока оно находится в сети.</span><span class="sxs-lookup"><span data-stu-id="e2337-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="e2337-939">Запланируйте отключение тома в автономном режиме, чтобы его можно было восстановить.</span><span class="sxs-lookup"><span data-stu-id="e2337-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**Ошибка \_ при \_ восстановлении диска \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-941">793 (0x319)</span><span class="sxs-lookup"><span data-stu-id="e2337-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-942">Восстановление тома не выполнено.</span><span class="sxs-lookup"><span data-stu-id="e2337-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**Ошибка \_ повреждения \_ \_ переполнения журнала**</span><span class="sxs-lookup"><span data-stu-id="e2337-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-944">794 (0x31A)</span><span class="sxs-lookup"><span data-stu-id="e2337-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-945">Один из журналов повреждений тома полон.</span><span class="sxs-lookup"><span data-stu-id="e2337-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="e2337-946">Последующие повреждения, которые могут быть обнаружены, не регистрируются.</span><span class="sxs-lookup"><span data-stu-id="e2337-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**Ошибка \_ поврежденного \_ журнала \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-948">795 (0x31B)</span><span class="sxs-lookup"><span data-stu-id="e2337-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-949">Один из журналов повреждений тома внутренне поврежден и должен быть создан повторно.</span><span class="sxs-lookup"><span data-stu-id="e2337-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="e2337-950">Том может содержать необнаруженные повреждения и должен быть проверен.</span><span class="sxs-lookup"><span data-stu-id="e2337-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**Ошибка \_ повреждения \_ журнала \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="e2337-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-952">796 (0x31C)</span><span class="sxs-lookup"><span data-stu-id="e2337-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-953">Один из журналов повреждений тома недоступен для работы.</span><span class="sxs-lookup"><span data-stu-id="e2337-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**Ошибка \_ при \_ \_ полном удалении \_ журнала**</span><span class="sxs-lookup"><span data-stu-id="e2337-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-955">797 (0x31D)</span><span class="sxs-lookup"><span data-stu-id="e2337-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-956">Один из журналов повреждений тома был удален, и в нем остались записи о повреждениях.</span><span class="sxs-lookup"><span data-stu-id="e2337-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="e2337-957">Том содержит обнаруженные повреждения и должен быть проверен.</span><span class="sxs-lookup"><span data-stu-id="e2337-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**Ошибка \_ — \_ Очистка журнала повреждена \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-959">798 (0x31E)</span><span class="sxs-lookup"><span data-stu-id="e2337-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-960">Один из журналов повреждений тома был удален программой chkdsk и больше не содержит реальных повреждений.</span><span class="sxs-lookup"><span data-stu-id="e2337-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**Ошибка \_ потерянного \_ имени \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-962">799 (0x31F)</span><span class="sxs-lookup"><span data-stu-id="e2337-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-963">Потерянные файлы существуют на томе, но их не удалось восстановить, так как в каталоге восстановления не удалось создать новые имена.</span><span class="sxs-lookup"><span data-stu-id="e2337-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="e2337-964">Файлы должны быть перемещены из каталога восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2337-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**Ошибка \_ жесткой блокировки при \_ переключении \_ на \_ новый \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="e2337-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-966">800 (0x320)</span><span class="sxs-lookup"><span data-stu-id="e2337-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-967">Жесткая блокировка, связанная с этим маркером, теперь связана с другим маркером.</span><span class="sxs-lookup"><span data-stu-id="e2337-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**Ошибка \_ не может \_ предоставить \_ запрошенную \_ нежесткую блокировку**</span><span class="sxs-lookup"><span data-stu-id="e2337-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-969">801 (0x321)</span><span class="sxs-lookup"><span data-stu-id="e2337-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-970">Невозможно предоставить нежесткую блокировку запрошенного уровня.</span><span class="sxs-lookup"><span data-stu-id="e2337-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="e2337-971">Может быть доступна нежесткая блокировка нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="e2337-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**Ошибка \_ не может привести к \_ нарушению \_ оппортунистической блокировки**</span><span class="sxs-lookup"><span data-stu-id="e2337-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-973">802 (0x322)</span><span class="sxs-lookup"><span data-stu-id="e2337-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-974">Операция не была успешно завершена, поскольку это привело бы к нарушению оппортунистической блокировки.</span><span class="sxs-lookup"><span data-stu-id="e2337-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="e2337-975">Вызывающий объект запросил, чтобы существующие операционные блокировки не были разорваны.</span><span class="sxs-lookup"><span data-stu-id="e2337-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**Ошибка \_ \_ закрытого маркера блокировки ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-977">803 (0x323)</span><span class="sxs-lookup"><span data-stu-id="e2337-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-978">Маркер, с которым связана эта жесткая блокировка, закрыт.</span><span class="sxs-lookup"><span data-stu-id="e2337-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="e2337-979">Нежесткая блокировка теперь разорвана.</span><span class="sxs-lookup"><span data-stu-id="e2337-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**Ошибка \_ без \_ \_ условия ACE**</span><span class="sxs-lookup"><span data-stu-id="e2337-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-981">804 (0x324)</span><span class="sxs-lookup"><span data-stu-id="e2337-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-982">Указанная запись управления доступом (ACE) не содержит условие.</span><span class="sxs-lookup"><span data-stu-id="e2337-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**Ошибка \_ недопустимого \_ \_ условия ACE**</span><span class="sxs-lookup"><span data-stu-id="e2337-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-984">805 (0x325)</span><span class="sxs-lookup"><span data-stu-id="e2337-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-985">Указанная запись управления доступом (ACE) содержит недопустимое условие.</span><span class="sxs-lookup"><span data-stu-id="e2337-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**Ошибка \_ при \_ отмене обработчика файла \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-987">806 (0x326)</span><span class="sxs-lookup"><span data-stu-id="e2337-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-988">Доступ к указанному обработчику файлов был отозван.</span><span class="sxs-lookup"><span data-stu-id="e2337-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_изображение ошибки \_ в \_ другой \_ базе**</span><span class="sxs-lookup"><span data-stu-id="e2337-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-990">807 (0x327)</span><span class="sxs-lookup"><span data-stu-id="e2337-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-991">Файл изображения был сопоставлен по адресу, отличному от адреса, указанного в файле изображения, но исправления по-прежнему будут автоматически выполняться на образе.</span><span class="sxs-lookup"><span data-stu-id="e2337-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**Ошибка \_ при \_ доступе EA \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-993">994 (0x3E2)</span><span class="sxs-lookup"><span data-stu-id="e2337-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-994">Отказано в доступе к расширенному атрибуту.</span><span class="sxs-lookup"><span data-stu-id="e2337-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**операция с ошибкой \_ \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="e2337-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-996">995 (0x3E3)</span><span class="sxs-lookup"><span data-stu-id="e2337-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-997">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="e2337-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**Ошибка ввода-вывода при ошибке \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-999">996 (0x3E4)</span><span class="sxs-lookup"><span data-stu-id="e2337-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-1000">Перекрытое событие ввода-вывода не находится в сигнальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="e2337-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**\_Ожидание ввода-вывода при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="e2337-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-1002">997 (0x3E5)</span><span class="sxs-lookup"><span data-stu-id="e2337-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-1003">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e2337-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**Ошибка \_ НЕдоступности**</span><span class="sxs-lookup"><span data-stu-id="e2337-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-1005">998 (0x3E6)</span><span class="sxs-lookup"><span data-stu-id="e2337-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-1006">Недопустимый доступ к расположению в памяти.</span><span class="sxs-lookup"><span data-stu-id="e2337-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2337-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**Ошибка \_ сваперрор**</span><span class="sxs-lookup"><span data-stu-id="e2337-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2337-1008">999 (0x3E7)</span><span class="sxs-lookup"><span data-stu-id="e2337-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="e2337-1009">Ошибка при выполнении операции со страницей.</span><span class="sxs-lookup"><span data-stu-id="e2337-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="e2337-1010">Требования</span><span class="sxs-lookup"><span data-stu-id="e2337-1010">Requirements</span></span>



| <span data-ttu-id="e2337-1011">Требование</span><span class="sxs-lookup"><span data-stu-id="e2337-1011">Requirement</span></span> | <span data-ttu-id="e2337-1012">Значение</span><span class="sxs-lookup"><span data-stu-id="e2337-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2337-1013">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2337-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="e2337-1014">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2337-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2337-1015">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2337-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="e2337-1016">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2337-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2337-1017">Header</span><span class="sxs-lookup"><span data-stu-id="e2337-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2337-1018"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2337-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2337-1019">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2337-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2337-1020">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="e2337-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
