---
description: Описание кодов ошибок 1000-1299, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Коды системных ошибок (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538939"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="54ba5-103">Коды системных ошибок (1000-1299)</span><span class="sxs-lookup"><span data-stu-id="54ba5-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="54ba5-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="54ba5-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="54ba5-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54ba5-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="54ba5-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 1000 – 1299.</span><span class="sxs-lookup"><span data-stu-id="54ba5-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="54ba5-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="54ba5-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="54ba5-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="54ba5-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="54ba5-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_переполнение стека ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-110">1001 (0x3E9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-111">Слишком глубокая рекурсия. стек переполняется.</span><span class="sxs-lookup"><span data-stu-id="54ba5-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**Ошибка \_ недопустимого \_ сообщения**</span><span class="sxs-lookup"><span data-stu-id="54ba5-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-113">1002 (0x3EA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-114">Окно не может работать с отправленным сообщением.</span><span class="sxs-lookup"><span data-stu-id="54ba5-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**Ошибка \_ не может быть \_ \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-116">1003 (0x3EB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-117">Не удается завершить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="54ba5-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**Ошибка \_ недопустимых \_ флагов**</span><span class="sxs-lookup"><span data-stu-id="54ba5-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-119">1004 (0x3EC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-120">Недопустимые флаги.</span><span class="sxs-lookup"><span data-stu-id="54ba5-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**Ошибка \_ НЕраспознанного \_ тома**</span><span class="sxs-lookup"><span data-stu-id="54ba5-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-122">1005 (0x3ED)</span><span class="sxs-lookup"><span data-stu-id="54ba5-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-123">Том не содержит распознанную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="54ba5-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="54ba5-124">Убедитесь, что загружены все необходимые драйверы файловой системы и что том не поврежден.</span><span class="sxs-lookup"><span data-stu-id="54ba5-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**\_Недопустимый файл ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-126">1006 (0x3EE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-127">Том для файла был изменен извне, поэтому открытый файл больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="54ba5-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**Ошибка \_ полноэкранного \_ режима**</span><span class="sxs-lookup"><span data-stu-id="54ba5-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-129">1007 (0x3EF)</span><span class="sxs-lookup"><span data-stu-id="54ba5-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-130">Не удается выполнить запрошенную операцию в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="54ba5-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**Ошибка \_ без \_ токена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-132">1008 (0x3F0)</span><span class="sxs-lookup"><span data-stu-id="54ba5-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-133">Предпринята попытка ссылки на несуществующий токен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**Ошибка \_ баддб**</span><span class="sxs-lookup"><span data-stu-id="54ba5-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-135">1009 (0x3F1)</span><span class="sxs-lookup"><span data-stu-id="54ba5-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-136">База данных реестра конфигурации повреждена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**Ошибка \_ бадкэй**</span><span class="sxs-lookup"><span data-stu-id="54ba5-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-138">1010 (0x3F2)</span><span class="sxs-lookup"><span data-stu-id="54ba5-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-139">Недопустимый раздел реестра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="54ba5-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**Ошибка \_ кантопен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-141">1011 (0x3F3)</span><span class="sxs-lookup"><span data-stu-id="54ba5-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-142">Не удалось открыть раздел реестра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="54ba5-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**Ошибка \_ кантреад**</span><span class="sxs-lookup"><span data-stu-id="54ba5-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-144">1012 (размер 0x3f4)</span><span class="sxs-lookup"><span data-stu-id="54ba5-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-145">Не удалось прочитать раздел реестра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="54ba5-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**Ошибка \_ кантврите**</span><span class="sxs-lookup"><span data-stu-id="54ba5-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-147">1013 (0x3F5)</span><span class="sxs-lookup"><span data-stu-id="54ba5-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-148">Не удалось записать раздел реестра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="54ba5-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**\_реестр ошибок \_ восстановлен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-150">1014 (0x3F6)</span><span class="sxs-lookup"><span data-stu-id="54ba5-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-151">Один из файлов в базе данных реестра был восстановлен с помощью журнала или альтернативной копии.</span><span class="sxs-lookup"><span data-stu-id="54ba5-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="54ba5-152">Восстановление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="54ba5-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**\_реестр ошибок \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="54ba5-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-154">1015 (0x3F7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-155">Реестр поврежден.</span><span class="sxs-lookup"><span data-stu-id="54ba5-155">The registry is corrupted.</span></span> <span data-ttu-id="54ba5-156">Структура одного из файлов, содержащих данные реестра, повреждена, либо поврежден образ памяти системы, либо не удалось восстановить файл, так как альтернативная копия или журнал отсутствовали или повреждены.</span><span class="sxs-lookup"><span data-stu-id="54ba5-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**Ошибка \_ \_ при вводе-выводе реестра \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-158">1016 (0x3F8)</span><span class="sxs-lookup"><span data-stu-id="54ba5-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-159">Не удалось восстановить операцию ввода-вывода, инициированную реестром.</span><span class="sxs-lookup"><span data-stu-id="54ba5-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="54ba5-160">Реестру не удалось прочесть, записать или очистить один из файлов, содержащих образ системы в реестре.</span><span class="sxs-lookup"><span data-stu-id="54ba5-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**Ошибка \_ не \_ \_ файл реестра**</span><span class="sxs-lookup"><span data-stu-id="54ba5-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-162">1017 (0x3F9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-163">Система попыталась загрузить или восстановить файл в реестр, но указанный файл не находится в формате файла реестра.</span><span class="sxs-lookup"><span data-stu-id="54ba5-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**\_ключ ошибки \_ удален**</span><span class="sxs-lookup"><span data-stu-id="54ba5-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-165">1018 (0x3FA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-166">Попытка выполнить недопустимую операцию для раздела реестра, помеченного для удаления.</span><span class="sxs-lookup"><span data-stu-id="54ba5-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**\_нет \_ пространства журнала \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-168">1019 (0x3FB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-169">Системе не удалось выделить необходимый объем в журнале реестра.</span><span class="sxs-lookup"><span data-stu-id="54ba5-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**\_ключ ошибки \_ имеет \_ дочерние элементы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-171">1020 (0x3FC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-172">Невозможно создать символьную ссылку в разделе реестра, который уже содержит подразделы или значения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**\_дочерний элемент error \_ должен \_ быть \_ временным**</span><span class="sxs-lookup"><span data-stu-id="54ba5-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-174">1021 (0x3FD)</span><span class="sxs-lookup"><span data-stu-id="54ba5-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-175">Невозможно создать стабильный подраздел с временным родительским ключом.</span><span class="sxs-lookup"><span data-stu-id="54ba5-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**уведомление об ОШИБКе \_ \_ Перечисление \_ dir**</span><span class="sxs-lookup"><span data-stu-id="54ba5-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-177">1022 (0x3FE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-178">Выполняется запрос на уведомление об изменении, и данные не возвращаются в буфере вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="54ba5-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="54ba5-179">Теперь вызывающий объект должен перечислить файлы для поиска изменений.</span><span class="sxs-lookup"><span data-stu-id="54ba5-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_службы, зависящие от ошибок, \_ \_ выполняются**</span><span class="sxs-lookup"><span data-stu-id="54ba5-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-181">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-182">Элемент управления "Отмена" был отправлен службе, от которой зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**Ошибка при \_ недопустимом \_ \_ управлении службой**</span><span class="sxs-lookup"><span data-stu-id="54ba5-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-184">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-185">Запрошенный элемент управления не является допустимым для этой службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_ \_ время ожидания запроса службы ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-187">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-188">Служба не ответила на запрос запуска или контроля за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="54ba5-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**\_Служба ошибок \_ нет \_ потока**</span><span class="sxs-lookup"><span data-stu-id="54ba5-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-190">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-191">Не удалось создать поток для службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**\_ \_ база данных службы ошибок \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="54ba5-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-193">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-194">База данных службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="54ba5-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**\_Служба ошибок \_ уже \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-196">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="54ba5-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-197">Экземпляр службы уже запущен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**Ошибка \_ недопустимой \_ \_ учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-199">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="54ba5-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-200">Имя учетной записи недопустимо или не существует, или пароль недопустим для указанного имени учетной записи.</span><span class="sxs-lookup"><span data-stu-id="54ba5-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**\_Служба ошибок \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-202">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="54ba5-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-203">Не удается запустить службу, так как она отключена или не имеет связанных с ней включенных устройств.</span><span class="sxs-lookup"><span data-stu-id="54ba5-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**Ошибка \_ циклической \_ зависимости**</span><span class="sxs-lookup"><span data-stu-id="54ba5-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-205">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="54ba5-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-206">Указана циклическая зависимость службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**\_Служба ошибок \_ \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="54ba5-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-208">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="54ba5-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-209">Указанная служба не существует в качестве установленной службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**\_Служба ошибок \_ не может \_ принять \_ CTRL**</span><span class="sxs-lookup"><span data-stu-id="54ba5-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-211">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="54ba5-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-212">В данный момент служба не может принимать управляющие сообщения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**\_Служба ошибок \_ \_ неактивна**</span><span class="sxs-lookup"><span data-stu-id="54ba5-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-214">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="54ba5-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-215">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**Ошибка \_ при \_ \_ подключении к контроллеру службы \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-217">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="54ba5-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-218">Процессу службы не удалось подключиться к контроллеру службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**Ошибка \_ исключения \_ в \_ службе**</span><span class="sxs-lookup"><span data-stu-id="54ba5-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-220">1064 (0x428)</span><span class="sxs-lookup"><span data-stu-id="54ba5-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-221">При обработке управляющего запроса возникло исключение в службе.</span><span class="sxs-lookup"><span data-stu-id="54ba5-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**\_база данных \_ ошибок \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="54ba5-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-223">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="54ba5-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-224">Указанная база данных не существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**Ошибка \_ , \_ специфическая для службы \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-226">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-227">Служба вернула код ошибки, зависящий от службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**\_Обработка ошибок \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="54ba5-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-229">1067 (0x42B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-230">Процесс был неожиданно завершен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**\_ \_ Сбой зависимости службы \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="54ba5-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-232">1068 (0x42C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-233">Не удалось запустить службу или группу зависимостей.</span><span class="sxs-lookup"><span data-stu-id="54ba5-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**Ошибка \_ \_ при входе в службу ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-235">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-236">Служба не запущена из-за ошибки входа в систему.</span><span class="sxs-lookup"><span data-stu-id="54ba5-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**Ошибка \_ при \_ запуске \_ службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-238">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-239">После запуска служба зависла в состоянии ожидания запуска.</span><span class="sxs-lookup"><span data-stu-id="54ba5-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**Ошибка при \_ неправильной \_ \_ блокировке службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-241">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-242">Указана недопустимая блокировка базы данных службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_Служба ошибок \_ помечена \_ для \_ удаления**</span><span class="sxs-lookup"><span data-stu-id="54ba5-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-244">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="54ba5-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-245">Указанная служба помечена для удаления.</span><span class="sxs-lookup"><span data-stu-id="54ba5-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**\_Служба ошибок \_ существует**</span><span class="sxs-lookup"><span data-stu-id="54ba5-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-247">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="54ba5-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-248">Указанная служба уже существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**Ошибка \_ уже \_ запущена \_ LKG**</span><span class="sxs-lookup"><span data-stu-id="54ba5-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-250">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="54ba5-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-251">В настоящее время система работает с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="54ba5-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**\_зависимость службы \_ ошибок \_ удалена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-253">1075 (0x433)</span><span class="sxs-lookup"><span data-stu-id="54ba5-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-254">Служба зависимостей не существует или помечена для удаления.</span><span class="sxs-lookup"><span data-stu-id="54ba5-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**Ошибка \_ загрузки \_ уже \_ принята**</span><span class="sxs-lookup"><span data-stu-id="54ba5-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-256">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="54ba5-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-257">Текущая загрузка уже принята для использования в качестве последнего известного набора элементов управления.</span><span class="sxs-lookup"><span data-stu-id="54ba5-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**\_Служба ошибок \_ никогда не \_ запустилась**</span><span class="sxs-lookup"><span data-stu-id="54ba5-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-259">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="54ba5-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-260">С момента последней загрузки попытки запуска службы не были выполнены.</span><span class="sxs-lookup"><span data-stu-id="54ba5-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**Ошибка при \_ дублировании \_ \_ имени службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-262">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="54ba5-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-263">Это имя уже используется как имя службы или отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**Ошибка \_ другой \_ \_ учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-265">1079 (0x437)</span><span class="sxs-lookup"><span data-stu-id="54ba5-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-266">Учетная запись, указанная для этой службы, отличается от учетной записи, указанной для других служб, работающих в том же процессе.</span><span class="sxs-lookup"><span data-stu-id="54ba5-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**Ошибка \_ не \_ может \_ обнаружить \_ сбой драйвера**</span><span class="sxs-lookup"><span data-stu-id="54ba5-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-268">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="54ba5-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-269">Действия при сбое могут быть заданы только для служб Win32, а не для драйверов.</span><span class="sxs-lookup"><span data-stu-id="54ba5-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**Ошибка \_ не \_ может \_ обнаружить \_ Прерывание процесса**</span><span class="sxs-lookup"><span data-stu-id="54ba5-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-271">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="54ba5-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-272">Эта служба выполняется в том же процессе, что и диспетчер управления службами.</span><span class="sxs-lookup"><span data-stu-id="54ba5-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="54ba5-273">Поэтому диспетчер управления службами не может предпринимать никаких действий в случае непредвиденного завершения процесса этой службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**Ошибка \_ без \_ \_ программы восстановления**</span><span class="sxs-lookup"><span data-stu-id="54ba5-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-275">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-276">Для этой службы не настроена программа восстановления.</span><span class="sxs-lookup"><span data-stu-id="54ba5-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**\_Служба ошибок \_ отсутствует \_ в \_ exe**</span><span class="sxs-lookup"><span data-stu-id="54ba5-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-278">1083 (0x43B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-279">Исполняемая программа, для запуска которой настроена эта служба, не реализует службу.</span><span class="sxs-lookup"><span data-stu-id="54ba5-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**Ошибка \_ не \_ SAFEBOOT \_ службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-281">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-282">Эта служба не может быть запущена в защищенном режиме.</span><span class="sxs-lookup"><span data-stu-id="54ba5-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**Ошибка при \_ завершении \_ \_ носителя**</span><span class="sxs-lookup"><span data-stu-id="54ba5-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-284">1100 (0x44C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-285">Достигнут физический конец ленты.</span><span class="sxs-lookup"><span data-stu-id="54ba5-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**\_ \_ обнаружена ошибка метка файла**</span><span class="sxs-lookup"><span data-stu-id="54ba5-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-287">1101 (0x44D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-288">Доступ к ленте достиг метка файла.</span><span class="sxs-lookup"><span data-stu-id="54ba5-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**Ошибка \_ начала \_ \_ носителя**</span><span class="sxs-lookup"><span data-stu-id="54ba5-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-290">1102 (0x44E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-291">Обнаружено начало ленты или раздела.</span><span class="sxs-lookup"><span data-stu-id="54ba5-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**\_ \_ обнаружена ошибка сетмарк**</span><span class="sxs-lookup"><span data-stu-id="54ba5-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-293">1103 (0x44F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-294">Доступ к ленте достиг конца набора файлов.</span><span class="sxs-lookup"><span data-stu-id="54ba5-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**Ошибка \_ не \_ \_ обнаружено данных**</span><span class="sxs-lookup"><span data-stu-id="54ba5-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-296">1104 (0x450)</span><span class="sxs-lookup"><span data-stu-id="54ba5-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-297">На ленте больше нет данных.</span><span class="sxs-lookup"><span data-stu-id="54ba5-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**Ошибка \_ секции \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="54ba5-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-299">1105 (0x451)</span><span class="sxs-lookup"><span data-stu-id="54ba5-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-300">Не удалось секционировать ленту.</span><span class="sxs-lookup"><span data-stu-id="54ba5-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**Ошибка \_ недопустимой \_ \_ длины блока**</span><span class="sxs-lookup"><span data-stu-id="54ba5-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-302">1106 (0x452)</span><span class="sxs-lookup"><span data-stu-id="54ba5-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-303">При доступе к новой ленте многодискового раздела текущий размер блока неверен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**устройство с ОШИБКАми \_ \_ не \_ секционировано**</span><span class="sxs-lookup"><span data-stu-id="54ba5-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-305">1107 (0x453)</span><span class="sxs-lookup"><span data-stu-id="54ba5-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-306">Не удалось найти сведения о разделах ленты при загрузке ленты.</span><span class="sxs-lookup"><span data-stu-id="54ba5-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**Ошибка \_ не \_ удалось \_ заблокировать \_ носитель**</span><span class="sxs-lookup"><span data-stu-id="54ba5-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-308">1108 (0x454)</span><span class="sxs-lookup"><span data-stu-id="54ba5-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-309">Не удалось заблокировать механизм извлечения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="54ba5-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**Ошибка \_ не \_ удалось \_ выгрузить \_ носитель**</span><span class="sxs-lookup"><span data-stu-id="54ba5-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-311">1109 (0x455)</span><span class="sxs-lookup"><span data-stu-id="54ba5-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-312">Не удалось выгрузить носитель.</span><span class="sxs-lookup"><span data-stu-id="54ba5-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**\_носитель ошибок \_ изменен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-314">1110 (0x456)</span><span class="sxs-lookup"><span data-stu-id="54ba5-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-315">Носитель в устройстве мог измениться.</span><span class="sxs-lookup"><span data-stu-id="54ba5-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**\_сброс шины с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-317">1111 (0x457)</span><span class="sxs-lookup"><span data-stu-id="54ba5-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-318">Шина ввода-вывода сброшена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**Ошибка \_ без \_ носителя \_ в \_ устройстве**</span><span class="sxs-lookup"><span data-stu-id="54ba5-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-320">1112 (0x458)</span><span class="sxs-lookup"><span data-stu-id="54ba5-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-321">Нет носителя в устройстве.</span><span class="sxs-lookup"><span data-stu-id="54ba5-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**Ошибка \_ без \_ преобразования в Юникод \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-323">1113 (0x459)</span><span class="sxs-lookup"><span data-stu-id="54ba5-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-324">В целевой многобайтовой кодовой странице не существует сопоставления для символа Юникода.</span><span class="sxs-lookup"><span data-stu-id="54ba5-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**Ошибка \_ \_ при инициализации библиотеки DLL \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-326">1114 (0x45A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-327">Не удалось выполнить подпрограммы инициализации библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="54ba5-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**\_выполняется завершение работы \_ с \_ ошибкой**</span><span class="sxs-lookup"><span data-stu-id="54ba5-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-329">1115 (0x45B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-330">Выполняется завершение работы системы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**Ошибка \_ \_ при завершении работы \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-332">1116 (0x45C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-333">Не удалось прервать завершение работы системы, так как не выполнялось завершение работы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**\_устройство ввода-вывода с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-335">1117 (0x45D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-336">Выполнить запрос невозможно из-за ошибки устройства ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="54ba5-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**\_последовательная ошибка \_ без \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="54ba5-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-338">1118 (0x45E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-339">Не удалось инициализировать последовательные устройства.</span><span class="sxs-lookup"><span data-stu-id="54ba5-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="54ba5-340">Последовательный драйвер будет выгружен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**\_IRQ ошибок \_ занятости**</span><span class="sxs-lookup"><span data-stu-id="54ba5-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-342">1119 (0x45F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-343">Не удалось открыть устройство, которое совместно использовало запрос на прерывание (IRQ) с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="54ba5-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="54ba5-344">По крайней мере одно другое устройство, использующее этот IRQ, уже открыто.</span><span class="sxs-lookup"><span data-stu-id="54ba5-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**Ошибка при дополнительных операциях \_ \_ записи**</span><span class="sxs-lookup"><span data-stu-id="54ba5-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-346">1120 (0x460)</span><span class="sxs-lookup"><span data-stu-id="54ba5-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-347">Операция последовательного ввода-вывода была выполнена другой записью в последовательный порт.</span><span class="sxs-lookup"><span data-stu-id="54ba5-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="54ba5-348">\_Счетчик последовательного XOFF-порта ioctl \_ \_ достиг нуля.)</span><span class="sxs-lookup"><span data-stu-id="54ba5-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_время ожидания счетчика ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-350">1121 (0x461)</span><span class="sxs-lookup"><span data-stu-id="54ba5-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-351">Операция последовательного ввода-вывода завершена из-за истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="54ba5-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="54ba5-352">\_Счетчик последовательного XOFF-порта ioctl \_ \_ не получил доступ к нулю.)</span><span class="sxs-lookup"><span data-stu-id="54ba5-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**Ошибка \_ \_ отметка идентификатора дискеты \_ \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-354">1122 (0x462)</span><span class="sxs-lookup"><span data-stu-id="54ba5-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-355">На гибком диске не найдена метка адреса идентификатора.</span><span class="sxs-lookup"><span data-stu-id="54ba5-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**Ошибка при \_ отформатировании \_ неправильного \_ цилиндра**</span><span class="sxs-lookup"><span data-stu-id="54ba5-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-357">1123 (0x463)</span><span class="sxs-lookup"><span data-stu-id="54ba5-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-358">Несоответствие между полем идентификатора сектора гибкого диска и адресом записи контроллера гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="54ba5-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**Ошибка \_ флоппи-дисковода \_ неизвестная \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="54ba5-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-360">1124 (0x464)</span><span class="sxs-lookup"><span data-stu-id="54ba5-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-361">В контроллере дисковода гибких дисков обнаружена ошибка, не распознанная драйвером гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="54ba5-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ошибочные \_ \_ неправильные \_ регистры диска**</span><span class="sxs-lookup"><span data-stu-id="54ba5-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-363">1125 (0x465)</span><span class="sxs-lookup"><span data-stu-id="54ba5-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-364">Контроллер гибкого диска вернул непоследовательные результаты в регистрах.</span><span class="sxs-lookup"><span data-stu-id="54ba5-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**Ошибка \_ при повторной \_ калибровке диска \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-366">1126 (0x466)</span><span class="sxs-lookup"><span data-stu-id="54ba5-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-367">При доступе к жесткому диску операция повторной калибровки завершилась сбоем даже после повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="54ba5-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**Ошибка \_ \_ при выполнении операции с диском \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-369">1127 (0x467)</span><span class="sxs-lookup"><span data-stu-id="54ba5-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-370">При доступе к жесткому диску операция с диском завершилась сбоем даже после повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="54ba5-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**Ошибка \_ \_ при сбросе диска \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-372">1128 (0x468)</span><span class="sxs-lookup"><span data-stu-id="54ba5-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-373">При доступе к жесткому диску требуется сброс контроллера диска, но даже сбой.</span><span class="sxs-lookup"><span data-stu-id="54ba5-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**Ошибка \_ ЕОМ \_ Overflow**</span><span class="sxs-lookup"><span data-stu-id="54ba5-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-375">1129 (0x469)</span><span class="sxs-lookup"><span data-stu-id="54ba5-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-376">Обнаружен физический конец ленты.</span><span class="sxs-lookup"><span data-stu-id="54ba5-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**Ошибка \_ \_ недостаточно \_ памяти сервера \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-378">1130 (0x46A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-379">"Недостаточно памяти сервера для обработки команды".</span><span class="sxs-lookup"><span data-stu-id="54ba5-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**\_возможна ошибка \_ взаимоблокировки**</span><span class="sxs-lookup"><span data-stu-id="54ba5-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-381">1131 (0x46B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-382">Обнаружена потенциальная ситуация взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="54ba5-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_Выравнивание по сопоставлению ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-384">1132 (0x46C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-385">Указанный базовый адрес или смещение файла не имеют правильного выравнивания.</span><span class="sxs-lookup"><span data-stu-id="54ba5-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**Ошибка \_ при \_ установке \_ запрета на состояние электропитания \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-387">1140 (0x474)</span><span class="sxs-lookup"><span data-stu-id="54ba5-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-388">Попытка изменить системное состояние питания была заблокирована другим приложением или драйвером.</span><span class="sxs-lookup"><span data-stu-id="54ba5-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**Ошибка \_ \_ при установке \_ состояния электропитания \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-390">1141 (0x475)</span><span class="sxs-lookup"><span data-stu-id="54ba5-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-391">BIOS системы не удалось изменить состояние электропитания системы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**Ошибка \_ слишком \_ много \_ ссылок**</span><span class="sxs-lookup"><span data-stu-id="54ba5-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-393">1142 (0x476)</span><span class="sxs-lookup"><span data-stu-id="54ba5-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-394">Была предпринята попытка создать больше ссылок на файл, чем поддерживает файловая система.</span><span class="sxs-lookup"><span data-stu-id="54ba5-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**Ошибка \_ старой \_ \_ версии Win**</span><span class="sxs-lookup"><span data-stu-id="54ba5-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-396">1150 (0x47E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-397">Для указанной программы требуется более новая версия Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba5-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**Ошибка в приложении, не \_ \_ соответствующем \_ ОС**</span><span class="sxs-lookup"><span data-stu-id="54ba5-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-399">1151 (0x47F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-400">Указанная программа не является программой Windows или MS–DOS.</span><span class="sxs-lookup"><span data-stu-id="54ba5-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**Ошибка \_ приложения с одним \_ экземпляром \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-402">1152 (0x480)</span><span class="sxs-lookup"><span data-stu-id="54ba5-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-403">Невозможно запустить более одного экземпляра указанной программы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**Ошибка \_ \_ приложения рмоде**</span><span class="sxs-lookup"><span data-stu-id="54ba5-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-405">1153 (0x481)</span><span class="sxs-lookup"><span data-stu-id="54ba5-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-406">Указанная программа была написана для более ранней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba5-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**Ошибка \_ недопустимой \_ библиотеки DLL**</span><span class="sxs-lookup"><span data-stu-id="54ba5-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-408">1154 (0x482)</span><span class="sxs-lookup"><span data-stu-id="54ba5-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-409">Один из файлов библиотеки, необходимых для запуска этого приложения, поврежден.</span><span class="sxs-lookup"><span data-stu-id="54ba5-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**Ошибка \_ без \_ связи**</span><span class="sxs-lookup"><span data-stu-id="54ba5-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-411">1155 (0x483)</span><span class="sxs-lookup"><span data-stu-id="54ba5-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-412">С указанным файлом для этой операции не связано ни одно приложение.</span><span class="sxs-lookup"><span data-stu-id="54ba5-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**Ошибка \_ DDE — \_ сбой**</span><span class="sxs-lookup"><span data-stu-id="54ba5-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-414">1156 (0x484)</span><span class="sxs-lookup"><span data-stu-id="54ba5-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-415">Произошла ошибка при отправке команды приложению.</span><span class="sxs-lookup"><span data-stu-id="54ba5-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_Библиотека DLL ошибок \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-417">1157 (0x485)</span><span class="sxs-lookup"><span data-stu-id="54ba5-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-418">Не удается найти один из файлов библиотеки, необходимых для запуска этого приложения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ОШИБКИ \_ больше \_ нет \_ \_ дескрипторов пользователей**</span><span class="sxs-lookup"><span data-stu-id="54ba5-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-420">1158 (0x486)</span><span class="sxs-lookup"><span data-stu-id="54ba5-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-421">Текущий процесс использовал все свои системные квоты дескрипторов объектов диспетчера окон.</span><span class="sxs-lookup"><span data-stu-id="54ba5-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ только синхронное сообщение об ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-423">1159 (0x487)</span><span class="sxs-lookup"><span data-stu-id="54ba5-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-424">Сообщение может использоваться только с синхронными операциями.</span><span class="sxs-lookup"><span data-stu-id="54ba5-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_элемент источника \_ ошибки \_ пуст**</span><span class="sxs-lookup"><span data-stu-id="54ba5-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-426">1160 (0x488)</span><span class="sxs-lookup"><span data-stu-id="54ba5-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-427">Указанный исходный элемент не имеет носителя.</span><span class="sxs-lookup"><span data-stu-id="54ba5-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**\_элемент назначения \_ ошибки \_ полон**</span><span class="sxs-lookup"><span data-stu-id="54ba5-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-429">1161 (0x489)</span><span class="sxs-lookup"><span data-stu-id="54ba5-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-430">Указанный элемент назначения уже содержит носитель.</span><span class="sxs-lookup"><span data-stu-id="54ba5-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**Ошибка \_ недопустимого \_ \_ адреса элемента**</span><span class="sxs-lookup"><span data-stu-id="54ba5-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-432">1162 (0x48A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-433">Указанный элемент не существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**\_журнал ошибок \_ отсутствует \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-435">1163 (0x48B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-436">Указанный элемент является частью отсутствующего журнала.</span><span class="sxs-lookup"><span data-stu-id="54ba5-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**Ошибка \_ при \_ повторной инициализации \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="54ba5-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-438">1164 (0x48C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-439">Указанное устройство требует повторной инициализации из-за ошибок оборудования.</span><span class="sxs-lookup"><span data-stu-id="54ba5-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**устройство с ошибкой \_ \_ требует \_ очистки**</span><span class="sxs-lookup"><span data-stu-id="54ba5-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-441">1165 (0x48D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-442">Устройство обозначало необходимость очистки перед дальнейшими операциями.</span><span class="sxs-lookup"><span data-stu-id="54ba5-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**\_ \_ открыта дверца устройства с ошибкой \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-444">1166 (0x48E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-445">Устройство сообщило, что его дверца открыта.</span><span class="sxs-lookup"><span data-stu-id="54ba5-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**устройство с ошибкой \_ \_ не \_ подключено**</span><span class="sxs-lookup"><span data-stu-id="54ba5-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-447">1167 (0x48F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-448">Устройство не подключено.</span><span class="sxs-lookup"><span data-stu-id="54ba5-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**Ошибка \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-450">1168 (0x490)</span><span class="sxs-lookup"><span data-stu-id="54ba5-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-451">Элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="54ba5-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**Ошибка \_ без \_ соответствия**</span><span class="sxs-lookup"><span data-stu-id="54ba5-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-453">1169 (0x491)</span><span class="sxs-lookup"><span data-stu-id="54ba5-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-454">Для указанного ключа в индексе не найдено совпадений.</span><span class="sxs-lookup"><span data-stu-id="54ba5-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ не \_ удалось найти набор ошибок**</span><span class="sxs-lookup"><span data-stu-id="54ba5-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-456">1170 (0x492)</span><span class="sxs-lookup"><span data-stu-id="54ba5-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-457">Указанный набор свойств не существует в объекте.</span><span class="sxs-lookup"><span data-stu-id="54ba5-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_точка ошибки \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-459">1171 (0x493)</span><span class="sxs-lookup"><span data-stu-id="54ba5-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-460">Точка, передаваемая в Жетмаусемовепоинтс, отсутствует в буфере.</span><span class="sxs-lookup"><span data-stu-id="54ba5-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**Ошибка \_ без \_ \_ службы отслеживания**</span><span class="sxs-lookup"><span data-stu-id="54ba5-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-462">1172 (0x494)</span><span class="sxs-lookup"><span data-stu-id="54ba5-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-463">Служба отслеживания (Рабочая станция) не запущена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**Ошибка \_ без \_ \_ идентификатора тома**</span><span class="sxs-lookup"><span data-stu-id="54ba5-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-465">1173 (0x495)</span><span class="sxs-lookup"><span data-stu-id="54ba5-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-466">Не удалось найти идентификатор тома.</span><span class="sxs-lookup"><span data-stu-id="54ba5-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**Ошибка \_ не \_ удалось \_ удалить \_ замененные**</span><span class="sxs-lookup"><span data-stu-id="54ba5-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-468">1175 (0x497)</span><span class="sxs-lookup"><span data-stu-id="54ba5-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-469">Не удалось удалить файл для замены.</span><span class="sxs-lookup"><span data-stu-id="54ba5-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**Ошибка \_ не \_ удалось \_ Переместить \_ замену**</span><span class="sxs-lookup"><span data-stu-id="54ba5-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-471">1176 (0x498)</span><span class="sxs-lookup"><span data-stu-id="54ba5-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-472">Не удалось переместить заменяющий файл в заменяемый файл.</span><span class="sxs-lookup"><span data-stu-id="54ba5-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="54ba5-473">Файл, который необходимо заменить, сохранил свое исходное имя.</span><span class="sxs-lookup"><span data-stu-id="54ba5-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**Ошибка \_ не \_ удалось \_ Переместить \_ замену \_ 2**</span><span class="sxs-lookup"><span data-stu-id="54ba5-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-475">1177 (0x499)</span><span class="sxs-lookup"><span data-stu-id="54ba5-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-476">Не удалось переместить заменяющий файл в заменяемый файл.</span><span class="sxs-lookup"><span data-stu-id="54ba5-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="54ba5-477">Файл, который требуется заменить, был переименован с использованием имени резервной копии.</span><span class="sxs-lookup"><span data-stu-id="54ba5-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ выполняется удаление журнала \_ ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-479">1178 (0x49A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-480">Удаляется журнал изменений тома.</span><span class="sxs-lookup"><span data-stu-id="54ba5-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**\_журнал ошибок \_ \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-482">1179 (0x49B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-483">Журнал изменений тома неактивен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**обнаружен ОШИБОЧный \_ \_ файл \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-485">1180 (0x49C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-486">Файл найден, но он может быть неправильным.</span><span class="sxs-lookup"><span data-stu-id="54ba5-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_запись журнала \_ ошибок \_ удалена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-488">1181 (0x49D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-489">Запись журнала была удалена из журнала.</span><span class="sxs-lookup"><span data-stu-id="54ba5-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**Ошибка \_ завершения \_ работы \_ запланирована**</span><span class="sxs-lookup"><span data-stu-id="54ba5-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-491">1190 (0x4A6)</span><span class="sxs-lookup"><span data-stu-id="54ba5-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-492">Завершение работы системы уже запланировано.</span><span class="sxs-lookup"><span data-stu-id="54ba5-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**Ошибка \_ при завершении работы \_ пользователей, \_ вошедших \_ в систему**</span><span class="sxs-lookup"><span data-stu-id="54ba5-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-494">1191 (0x4A7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-495">Не удается запустить завершение работы системы, так как на компьютере вошли другие пользователи.</span><span class="sxs-lookup"><span data-stu-id="54ba5-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**Ошибка \_ неправильного \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="54ba5-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-497">1200 (0x4B0)</span><span class="sxs-lookup"><span data-stu-id="54ba5-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-498">Указано недопустимое имя устройства.</span><span class="sxs-lookup"><span data-stu-id="54ba5-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**Ошибка \_ \_ несвободного подключения**</span><span class="sxs-lookup"><span data-stu-id="54ba5-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-500">1201 (0x4B1)</span><span class="sxs-lookup"><span data-stu-id="54ba5-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-501">Устройство в настоящее время не подключено, но это запоминаемое подключение.</span><span class="sxs-lookup"><span data-stu-id="54ba5-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**устройство с ОШИБКАми \_ \_ уже \_ сохранено**</span><span class="sxs-lookup"><span data-stu-id="54ba5-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-503">1202 (0x4B2)</span><span class="sxs-lookup"><span data-stu-id="54ba5-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-504">Локальное имя устройства имеет запоминаемое подключение к другому сетевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="54ba5-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**Ошибка \_ без \_ сетевого \_ или \_ неверного \_ пути**</span><span class="sxs-lookup"><span data-stu-id="54ba5-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-506">1203 (0x4B3)</span><span class="sxs-lookup"><span data-stu-id="54ba5-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-507">Сетевой путь был либо неправильно введен, не существует, либо поставщик сети в настоящее время недоступен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="54ba5-508">Попробуйте ввести путь заново или обратитесь к администратору сети.</span><span class="sxs-lookup"><span data-stu-id="54ba5-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**Ошибка \_ неверного \_ поставщика**</span><span class="sxs-lookup"><span data-stu-id="54ba5-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-510">1204 (0x4B4)</span><span class="sxs-lookup"><span data-stu-id="54ba5-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-511">Указано недопустимое имя поставщика сети.</span><span class="sxs-lookup"><span data-stu-id="54ba5-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**Ошибка \_ не может \_ открыть \_ профиль**</span><span class="sxs-lookup"><span data-stu-id="54ba5-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-513">1205 (0x4B5)</span><span class="sxs-lookup"><span data-stu-id="54ba5-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-514">Не удалось открыть профиль сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ОШИБКА с \_ неправильным \_ профилем**</span><span class="sxs-lookup"><span data-stu-id="54ba5-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-516">1206 (0x4B6)</span><span class="sxs-lookup"><span data-stu-id="54ba5-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-517">Профиль сетевого подключения поврежден.</span><span class="sxs-lookup"><span data-stu-id="54ba5-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**Ошибка \_ не является \_ контейнером**</span><span class="sxs-lookup"><span data-stu-id="54ba5-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-519">1207 (0x4B7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-520">Невозможно перечислить неконтейнер.</span><span class="sxs-lookup"><span data-stu-id="54ba5-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**Ошибка \_ расширенной \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="54ba5-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-522">1208 (0x4B8)</span><span class="sxs-lookup"><span data-stu-id="54ba5-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-523">Произошла Расширенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="54ba5-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**Ошибка \_ недопустимого \_ GROUPNAME**</span><span class="sxs-lookup"><span data-stu-id="54ba5-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-525">1209 (0x4B9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-526">Формат указанного имени группы недопустим.</span><span class="sxs-lookup"><span data-stu-id="54ba5-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**Ошибка \_ недопустимое \_ имя компьютера**</span><span class="sxs-lookup"><span data-stu-id="54ba5-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-528">1210 (0x4BA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-529">Недопустимый формат указанного имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="54ba5-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**Ошибка \_ Недопустимая \_ EVENTNAME**</span><span class="sxs-lookup"><span data-stu-id="54ba5-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-531">1211 (0x4BB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-532">Недопустимый формат указанного имени события.</span><span class="sxs-lookup"><span data-stu-id="54ba5-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**Ошибка \_ недопустимое \_ имя домена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-534">1212 (0x4BC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-535">Недопустимый формат указанного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="54ba5-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**Ошибка \_ недопустимого \_ ServiceName**</span><span class="sxs-lookup"><span data-stu-id="54ba5-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-537">1213 (0x4BD)</span><span class="sxs-lookup"><span data-stu-id="54ba5-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-538">Формат указанного имени службы недопустим.</span><span class="sxs-lookup"><span data-stu-id="54ba5-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**Ошибка \_ недопустимого \_ NETNAME**</span><span class="sxs-lookup"><span data-stu-id="54ba5-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-540">1214 (0x4BE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-541">Недопустимый формат указанного сетевого имени.</span><span class="sxs-lookup"><span data-stu-id="54ba5-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**Ошибка \_ недопустимое \_ SHARENAME**</span><span class="sxs-lookup"><span data-stu-id="54ba5-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-543">1215 (0x4BF)</span><span class="sxs-lookup"><span data-stu-id="54ba5-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-544">Недопустимый формат указанного имени общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="54ba5-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**Ошибка \_ недопустимого \_ пассворднаме**</span><span class="sxs-lookup"><span data-stu-id="54ba5-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-546">1216 (0x4C0)</span><span class="sxs-lookup"><span data-stu-id="54ba5-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-547">Недопустимый формат указанного пароля.</span><span class="sxs-lookup"><span data-stu-id="54ba5-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**Ошибка \_ недопустимого \_ мессаженаме**</span><span class="sxs-lookup"><span data-stu-id="54ba5-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-549">1217 (0x4C1)</span><span class="sxs-lookup"><span data-stu-id="54ba5-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-550">Недопустимый формат указанного имени сообщения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**Ошибка \_ недопустимого \_ мессажедест**</span><span class="sxs-lookup"><span data-stu-id="54ba5-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-552">1218 (0x4C2)</span><span class="sxs-lookup"><span data-stu-id="54ba5-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-553">Недопустимый формат указанного назначения сообщения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_ \_ конфликт учетных данных сеанса с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-555">1219 (0x4C3)</span><span class="sxs-lookup"><span data-stu-id="54ba5-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-556">Несколько подключений к серверу или общему ресурсу одного и того же пользователя не разрешено использовать несколько имен пользователей.</span><span class="sxs-lookup"><span data-stu-id="54ba5-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="54ba5-557">Отключите все предыдущие подключения к серверу или общему ресурсу и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="54ba5-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_ \_ \_ превышен предел удаленного сеанса \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-559">1220 (0x4C4)</span><span class="sxs-lookup"><span data-stu-id="54ba5-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-560">Была предпринята попытка установить сеанс на сетевом сервере, но уже установлено слишком много сеансов для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="54ba5-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**Ошибка \_ DUP \_ имя_домена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-562">1221 (0x4C5)</span><span class="sxs-lookup"><span data-stu-id="54ba5-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-563">Имя рабочей группы или домена уже используется другим компьютером в сети.</span><span class="sxs-lookup"><span data-stu-id="54ba5-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**Ошибка \_ нет \_ сети**</span><span class="sxs-lookup"><span data-stu-id="54ba5-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-565">1222 (0x4C6)</span><span class="sxs-lookup"><span data-stu-id="54ba5-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-566">Сеть отсутствует или не запущена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**Ошибка \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-568">1223 (0x4C7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-569">Операция отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="54ba5-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**Ошибка \_ \_ сопоставленного пользователем \_ файла**</span><span class="sxs-lookup"><span data-stu-id="54ba5-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-571">1224 (0x4C8)</span><span class="sxs-lookup"><span data-stu-id="54ba5-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-572">Невозможно выполнить запрошенную операцию над файлом с открытым сопоставленным пользователем разделом.</span><span class="sxs-lookup"><span data-stu-id="54ba5-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**Ошибка при \_ подключении \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-574">1225 (0x4C9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-575">Удаленный компьютер отклонил сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="54ba5-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**Ошибка при \_ мягком \_ отключении**</span><span class="sxs-lookup"><span data-stu-id="54ba5-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-577">1226 (0x4CA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-578">Сетевое подключение было корректно закрыто.</span><span class="sxs-lookup"><span data-stu-id="54ba5-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**\_адрес ошибки \_ уже \_ связан**</span><span class="sxs-lookup"><span data-stu-id="54ba5-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-580">1227 (0x4CB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-581">С конечной точкой сетевого транспорта уже связан адрес.</span><span class="sxs-lookup"><span data-stu-id="54ba5-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**\_адрес ошибки \_ не \_ связан**</span><span class="sxs-lookup"><span data-stu-id="54ba5-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-583">1228 (0x4CC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-584">С конечной точкой сети еще не связан адрес.</span><span class="sxs-lookup"><span data-stu-id="54ba5-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**\_недопустимое подключение к ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-586">1229 (0x4CD)</span><span class="sxs-lookup"><span data-stu-id="54ba5-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-587">Предпринята попытка выполнить операцию для несуществующего сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**\_Подключение к ошибке \_ активно**</span><span class="sxs-lookup"><span data-stu-id="54ba5-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-589">1230 (0x4CE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-590">Попытка выполнить недопустимую операцию для активного сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**Ошибка " \_ сеть \_ недоступна"**</span><span class="sxs-lookup"><span data-stu-id="54ba5-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-592">1231 (0x4CF)</span><span class="sxs-lookup"><span data-stu-id="54ba5-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-593">Не удается получить доступ к сетевому расположению.</span><span class="sxs-lookup"><span data-stu-id="54ba5-593">The network location cannot be reached.</span></span> <span data-ttu-id="54ba5-594">Сведения об устранении неполадок в сети см. в справке Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba5-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**\_узел ошибок \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-596">1232 (0x4D0)</span><span class="sxs-lookup"><span data-stu-id="54ba5-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-597">Не удается получить доступ к сетевому расположению.</span><span class="sxs-lookup"><span data-stu-id="54ba5-597">The network location cannot be reached.</span></span> <span data-ttu-id="54ba5-598">Сведения об устранении неполадок в сети см. в справке Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba5-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**\_протокол ошибки \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-600">1233 (0x4D1)</span><span class="sxs-lookup"><span data-stu-id="54ba5-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-601">Не удается получить доступ к сетевому расположению.</span><span class="sxs-lookup"><span data-stu-id="54ba5-601">The network location cannot be reached.</span></span> <span data-ttu-id="54ba5-602">Сведения об устранении неполадок в сети см. в справке Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba5-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**\_порт ошибки \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-604">1234 (0x4D2)</span><span class="sxs-lookup"><span data-stu-id="54ba5-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-605">В конечной точке сети назначения в удаленной системе не работает ни одна служба.</span><span class="sxs-lookup"><span data-stu-id="54ba5-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**запрос на ошибку \_ \_ прерван**</span><span class="sxs-lookup"><span data-stu-id="54ba5-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-607">1235 (0x4D3)</span><span class="sxs-lookup"><span data-stu-id="54ba5-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-608">Запрос был прерван.</span><span class="sxs-lookup"><span data-stu-id="54ba5-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**\_Подключение к ошибке \_ прервано**</span><span class="sxs-lookup"><span data-stu-id="54ba5-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-610">1236 (0x4D4)</span><span class="sxs-lookup"><span data-stu-id="54ba5-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-611">Сетевое подключение прервано локальной системой.</span><span class="sxs-lookup"><span data-stu-id="54ba5-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**Ошибка \_ повтора**</span><span class="sxs-lookup"><span data-stu-id="54ba5-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-613">1237 (0x4D5)</span><span class="sxs-lookup"><span data-stu-id="54ba5-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-614">Не удалось завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="54ba5-614">The operation could not be completed.</span></span> <span data-ttu-id="54ba5-615">Необходимо выполнить повторную попытку.</span><span class="sxs-lookup"><span data-stu-id="54ba5-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_ \_ ограничение числа подключений об ошибках \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-617">1238 (0x4D6)</span><span class="sxs-lookup"><span data-stu-id="54ba5-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-618">Не удалось установить соединение с сервером, так как достигнуто предельное число одновременных подключений для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="54ba5-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**\_ограничение времени входа в систему \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-620">1239 (0x4D7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-621">Попытка входа в систему в течение неавторизованного времени для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="54ba5-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**Ошибка \_ при \_ вкста \_ ограничения имени входа**</span><span class="sxs-lookup"><span data-stu-id="54ba5-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-623">1240 (0x4D8)</span><span class="sxs-lookup"><span data-stu-id="54ba5-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-624">Учетная запись не имеет права на вход с этой станции.</span><span class="sxs-lookup"><span data-stu-id="54ba5-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**Ошибка при \_ неправильном \_ адресе**</span><span class="sxs-lookup"><span data-stu-id="54ba5-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-626">1241 (0x4D9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-627">Не удалось использовать сетевой адрес для запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="54ba5-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**Ошибка \_ уже \_ зарегистрирована**</span><span class="sxs-lookup"><span data-stu-id="54ba5-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-629">1242 (0x4DA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-630">Служба уже зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="54ba5-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_Служба ошибок \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-632">1243 (0x4DB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-633">Указанная служба не существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**Ошибка \_ не \_ прошла проверку подлинности**</span><span class="sxs-lookup"><span data-stu-id="54ba5-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-635">1244 (0x4DC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-636">Запрошенная операция не была выполнена, так как пользователь не прошел проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="54ba5-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**Ошибка \_ не \_ зарегистрирована \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-638">1245 (0x4DD)</span><span class="sxs-lookup"><span data-stu-id="54ba5-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-639">Запрошенная операция не была выполнена, так как пользователь не выполнил вход в сеть.</span><span class="sxs-lookup"><span data-stu-id="54ba5-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="54ba5-640">Указанная служба не существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**Ошибка \_ продолжения**</span><span class="sxs-lookup"><span data-stu-id="54ba5-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-642">1246 (0x4DE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-643">Продолжите работу с выполняемой работой.</span><span class="sxs-lookup"><span data-stu-id="54ba5-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**Ошибка \_ уже \_ инициализирована**</span><span class="sxs-lookup"><span data-stu-id="54ba5-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-645">1247 (0x4DF)</span><span class="sxs-lookup"><span data-stu-id="54ba5-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-646">Предпринята попытка выполнить операцию инициализации, когда инициализация уже завершена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**Ошибка \_ больше \_ \_ устройств**</span><span class="sxs-lookup"><span data-stu-id="54ba5-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-648">1248 (0x4E0)</span><span class="sxs-lookup"><span data-stu-id="54ba5-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-649">Больше нет локальных устройств.</span><span class="sxs-lookup"><span data-stu-id="54ba5-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**Ошибка \_ нет \_ такого \_ сайта**</span><span class="sxs-lookup"><span data-stu-id="54ba5-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-651">1249 (0x4E1)</span><span class="sxs-lookup"><span data-stu-id="54ba5-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-652">Указанный сайт не существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**Ошибка \_ \_ контроллер домена \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-654">1250 (0x4E2)</span><span class="sxs-lookup"><span data-stu-id="54ba5-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-655">Контроллер домена с указанным именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**Ошибка \_ только \_ при \_ наличии подключения**</span><span class="sxs-lookup"><span data-stu-id="54ba5-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-657">1251 (0x4E3)</span><span class="sxs-lookup"><span data-stu-id="54ba5-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-658">Эта операция поддерживается только при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="54ba5-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**Ошибка \_ переопределения \_ неизмененных изменений**</span><span class="sxs-lookup"><span data-stu-id="54ba5-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-660">1252 (0x4E4)</span><span class="sxs-lookup"><span data-stu-id="54ba5-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-661">Платформа групповой политики должна вызывать расширение, даже если изменения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="54ba5-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**Ошибка \_ неверного \_ \_ профиля пользователя**</span><span class="sxs-lookup"><span data-stu-id="54ba5-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-663">1253 (0x4E5)</span><span class="sxs-lookup"><span data-stu-id="54ba5-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-664">Указанный пользователь не имеет допустимого профиля.</span><span class="sxs-lookup"><span data-stu-id="54ba5-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**Ошибка \_ не \_ поддерживается \_ в \_ SBS**</span><span class="sxs-lookup"><span data-stu-id="54ba5-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-666">1254 (0x4E6)</span><span class="sxs-lookup"><span data-stu-id="54ba5-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-667">Эта операция не поддерживается на компьютере под Windows Server 2003 для Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="54ba5-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**Ошибка \_ \_ завершения работы \_ сервера \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-669">1255 (0x4E7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-670">Компьютер сервера завершает работу.</span><span class="sxs-lookup"><span data-stu-id="54ba5-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**Ошибка \_ размещения узла \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-672">1256 (0x4E8)</span><span class="sxs-lookup"><span data-stu-id="54ba5-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-673">Удаленная система недоступна.</span><span class="sxs-lookup"><span data-stu-id="54ba5-673">The remote system is not available.</span></span> <span data-ttu-id="54ba5-674">Сведения об устранении неполадок в сети см. в справке Windows.</span><span class="sxs-lookup"><span data-stu-id="54ba5-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**Ошибка \_ без \_ учетной записи \_ безопасности**</span><span class="sxs-lookup"><span data-stu-id="54ba5-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-676">1257 (0x4E9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-677">Указанный идентификатор безопасности не относится к домену учетной записи.</span><span class="sxs-lookup"><span data-stu-id="54ba5-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**Ошибка \_ не \_ является \_ идентификатором безопасности домена**</span><span class="sxs-lookup"><span data-stu-id="54ba5-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-679">1258 (0x4EA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-680">Указанный идентификатор безопасности не содержит компонент домена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**Ошибка \_ APPHELP \_ блок**</span><span class="sxs-lookup"><span data-stu-id="54ba5-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-682">1259 (0x4EB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-683">AppHelp диалоговое окно отменено, поэтому запускать приложение не удается.</span><span class="sxs-lookup"><span data-stu-id="54ba5-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_доступ к ошибкам \_ отключен \_ \_ политикой**</span><span class="sxs-lookup"><span data-stu-id="54ba5-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-685">1260 (0x4EC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-686">Эта программа заблокирована групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="54ba5-686">This program is blocked by group policy.</span></span> <span data-ttu-id="54ba5-687">Для получения дополнительных сведений обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="54ba5-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**Ошибка \_ при \_ использовании NAT для регистрации ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-689">1261 (0x4ED)</span><span class="sxs-lookup"><span data-stu-id="54ba5-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-690">Программа пытается использовать недопустимое значение регистра.</span><span class="sxs-lookup"><span data-stu-id="54ba5-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="54ba5-691">Обычно это вызвано неинициализированной регистрацией.</span><span class="sxs-lookup"><span data-stu-id="54ba5-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="54ba5-692">Эта ошибка относится только к Itanium.</span><span class="sxs-lookup"><span data-stu-id="54ba5-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**Ошибка \_ кскшаре \_ offline**</span><span class="sxs-lookup"><span data-stu-id="54ba5-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-694">1262 (0x4EE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-695">Общая папка в данный момент отключена или не существует.</span><span class="sxs-lookup"><span data-stu-id="54ba5-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**Ошибка \_ PKINIT \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-697">1263 (0x4EF)</span><span class="sxs-lookup"><span data-stu-id="54ba5-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-698">В протоколе Kerberos произошла ошибка при проверке сертификата KDC во время входа в смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="54ba5-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="54ba5-699">Дополнительные сведения см. в журнале системных событий.</span><span class="sxs-lookup"><span data-stu-id="54ba5-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**Ошибка \_ подсистемы смарт-карты \_ \_ при ошибке**</span><span class="sxs-lookup"><span data-stu-id="54ba5-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-701">1264 (0x4F0)</span><span class="sxs-lookup"><span data-stu-id="54ba5-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-702">В протоколе Kerberos произошла ошибка при попытке использовать подсистему смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="54ba5-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**\_обнаружено понижение ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-704">1265 (0x4F1)</span><span class="sxs-lookup"><span data-stu-id="54ba5-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-705">Системе не удается связаться с контроллером домена для обслуживания запроса проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="54ba5-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="54ba5-706">Повторите попытку позже.</span><span class="sxs-lookup"><span data-stu-id="54ba5-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**Ошибка \_ \_ блокировки компьютера**</span><span class="sxs-lookup"><span data-stu-id="54ba5-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-708">1271 (0x4F7)</span><span class="sxs-lookup"><span data-stu-id="54ba5-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-709">Компьютер заблокирован и не может завершить работу без параметра Force.</span><span class="sxs-lookup"><span data-stu-id="54ba5-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**\_обратный вызов ошибки \_ указал \_ недопустимые \_ данные**</span><span class="sxs-lookup"><span data-stu-id="54ba5-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-711">1273 (0x4F9)</span><span class="sxs-lookup"><span data-stu-id="54ba5-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-712">Определяемый приложением обратный вызов предоставил недопустимые данные при вызове.</span><span class="sxs-lookup"><span data-stu-id="54ba5-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**\_ \_ требуется обновление переднего плана для синхронизации ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-714">1274 (0x4FA)</span><span class="sxs-lookup"><span data-stu-id="54ba5-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-715">Платформа групповой политики должна вызывать расширение в синхронном обновлении политики переднего плана.</span><span class="sxs-lookup"><span data-stu-id="54ba5-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**\_драйвер ошибки \_ заблокирован**</span><span class="sxs-lookup"><span data-stu-id="54ba5-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-717">1275 (0x4FB)</span><span class="sxs-lookup"><span data-stu-id="54ba5-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-718">Загрузка этого драйвера заблокирована.</span><span class="sxs-lookup"><span data-stu-id="54ba5-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**Ошибка \_ при \_ импорте недействительной \_ \_ \_ библиотеки DLL**</span><span class="sxs-lookup"><span data-stu-id="54ba5-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-720">1276 (0x4FC)</span><span class="sxs-lookup"><span data-stu-id="54ba5-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-721">Библиотека динамической компоновки (DLL) ссылается на модуль, который не является ни библиотекой DLL, ни исполняемым образом процесса.</span><span class="sxs-lookup"><span data-stu-id="54ba5-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**Ошибка \_ доступа к \_ колонке "отключено" \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-723">1277 (0x4FD)</span><span class="sxs-lookup"><span data-stu-id="54ba5-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-724">Windows не удается открыть эту программу, так как она отключена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**Ошибка \_ доступа к \_ запрещенным \_ ИЗМЕНЕНИЯм в колонке \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-726">1278 (0x4FE)</span><span class="sxs-lookup"><span data-stu-id="54ba5-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-727">Windows не удается открыть эту программу, так как система принудительного применения лицензий была незаконно изменена или повреждена.</span><span class="sxs-lookup"><span data-stu-id="54ba5-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**Ошибка \_ восстановления \_ при сбое**</span><span class="sxs-lookup"><span data-stu-id="54ba5-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-729">1279 (0x4FF)</span><span class="sxs-lookup"><span data-stu-id="54ba5-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-730">Не удалось восстановить транзакцию.</span><span class="sxs-lookup"><span data-stu-id="54ba5-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**Ошибка \_ уже \_ Fiber**</span><span class="sxs-lookup"><span data-stu-id="54ba5-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="54ba5-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-733">Текущий поток уже преобразован в волокно.</span><span class="sxs-lookup"><span data-stu-id="54ba5-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**Ошибка \_ уже является \_ потоком**</span><span class="sxs-lookup"><span data-stu-id="54ba5-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="54ba5-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-736">Текущий поток уже преобразован из волокон.</span><span class="sxs-lookup"><span data-stu-id="54ba5-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_ \_ переполнение буфера СТЕКа ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="54ba5-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-739">Система обнаружила переполнение буфера на основе стека в этом приложении.</span><span class="sxs-lookup"><span data-stu-id="54ba5-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="54ba5-740">Такое переполнение потенциально может позволить злоумышленнику получить контроль над этим приложением.</span><span class="sxs-lookup"><span data-stu-id="54ba5-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**\_ \_ превышена квота параметра ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="54ba5-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-743">Данные в одном из параметров больше, чем может работать функция.</span><span class="sxs-lookup"><span data-stu-id="54ba5-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**\_ОТЛАДЧИК ошибок \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="54ba5-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-746">Попытка выполнить операцию с объектом Debug завершилась сбоем, так как объект находится в процессе удаления.</span><span class="sxs-lookup"><span data-stu-id="54ba5-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**Ошибка \_ \_ при загрузке с задержкой \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-748">1285 (0x505)</span><span class="sxs-lookup"><span data-stu-id="54ba5-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-749">Сбой при задержке загрузки DLL-файла или получении адреса функции в загружаемой с задержке DLL-библиотеке.</span><span class="sxs-lookup"><span data-stu-id="54ba5-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**Ошибка \_ не \_ разрешена для VDM**</span><span class="sxs-lookup"><span data-stu-id="54ba5-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="54ba5-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-752">%1 является 16-разрядным приложением.</span><span class="sxs-lookup"><span data-stu-id="54ba5-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="54ba5-753">У вас нет разрешений на выполнение 16-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="54ba5-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="54ba5-754">Проверьте свои разрешения у системного администратора.</span><span class="sxs-lookup"><span data-stu-id="54ba5-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**Ошибка \_ НЕопознанной \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="54ba5-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="54ba5-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-757">Недостаточно сведений для выяснения причины сбоя.</span><span class="sxs-lookup"><span data-stu-id="54ba5-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**Ошибка \_ недопустимого \_ \_ параметра крунтиме**</span><span class="sxs-lookup"><span data-stu-id="54ba5-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="54ba5-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-760">Неверное значение параметра, переданного в функцию среды выполнения C.</span><span class="sxs-lookup"><span data-stu-id="54ba5-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**Ошибка \_ за пределами \_ ВДЛ**</span><span class="sxs-lookup"><span data-stu-id="54ba5-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="54ba5-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-763">Операция была выполнена за пределами допустимой длины данных файла.</span><span class="sxs-lookup"><span data-stu-id="54ba5-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**Ошибка \_ несовместимый \_ \_ тип SID \_ службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="54ba5-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-766">Не удалось запустить службу, так как одна или несколько служб в одном процессе имеют несовместимый параметр типа идентификатора безопасности службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="54ba5-767">Служба с ограниченным типом SID может сосуществовать только в том же процессе с другими службами с ограниченным типом SID.</span><span class="sxs-lookup"><span data-stu-id="54ba5-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="54ba5-768">Если для этой службы был только что настроен тип идентификатора безопасности службы, то для запуска этой службы необходимо перезапустить процесс размещения.</span><span class="sxs-lookup"><span data-stu-id="54ba5-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="54ba5-769">В Windows Server 2003 и Windows XP неограниченная служба не может сосуществовать в одном процессе с другими службами.</span><span class="sxs-lookup"><span data-stu-id="54ba5-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="54ba5-770">Чтобы запустить эту службу, служба с типом SID неограниченного доступа должна быть перемещена в принадлежащий процесс.</span><span class="sxs-lookup"><span data-stu-id="54ba5-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**\_процесс драйвера \_ ошибки \_ завершен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="54ba5-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-773">Процесс, в котором размещается драйвер для этого устройства, был завершен.</span><span class="sxs-lookup"><span data-stu-id="54ba5-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_ограничение реализации \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="54ba5-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="54ba5-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-776">Операция попыталась превысить предел, определенный реализацией.</span><span class="sxs-lookup"><span data-stu-id="54ba5-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**процесс с ОШИБКАми \_ \_ \_ защищен**</span><span class="sxs-lookup"><span data-stu-id="54ba5-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="54ba5-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-779">Целевой процесс или процесс, содержащий целевой поток, является защищенным процессом.</span><span class="sxs-lookup"><span data-stu-id="54ba5-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**\_Служба ошибок \_ уведомлять \_ клиента \_ задержкой**</span><span class="sxs-lookup"><span data-stu-id="54ba5-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="54ba5-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-782">Клиент уведомлений службы задержкой слишком далеко позади текущего состояния служб на компьютере.</span><span class="sxs-lookup"><span data-stu-id="54ba5-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**\_ \_ превышена квота диска \_**</span><span class="sxs-lookup"><span data-stu-id="54ba5-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="54ba5-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-785">Операция запрошенного файла завершилась сбоем из-за превышения квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="54ba5-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="54ba5-786">Чтобы освободить место на диске, переместите файлы в другое расположение или удалите ненужные файлы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="54ba5-787">Для получения дополнительных сведений обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="54ba5-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**\_содержимое ошибки \_ заблокировано**</span><span class="sxs-lookup"><span data-stu-id="54ba5-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="54ba5-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-790">Не удалось выполнить запрошенную операцию с файлом, так как политика хранилища блокирует этот тип файла.</span><span class="sxs-lookup"><span data-stu-id="54ba5-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="54ba5-791">Для получения дополнительных сведений обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="54ba5-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**Ошибка \_ несовместимой \_ \_ привилегии службы**</span><span class="sxs-lookup"><span data-stu-id="54ba5-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="54ba5-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-794">Привилегия, необходимая службе для правильной работы, не существует в конфигурации учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="54ba5-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="54ba5-795">Для просмотра конфигурации службы и конфигурации учетной записи можно использовать оснастку консоли управления (MMC) "службы" и оснастку MMC "Локальные параметры безопасности" (secpol. msc).</span><span class="sxs-lookup"><span data-stu-id="54ba5-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**Ошибка \_ при \_ зависании приложения**</span><span class="sxs-lookup"><span data-stu-id="54ba5-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="54ba5-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-798">Поток, вовлеченный в эту операцию, не отвечает.</span><span class="sxs-lookup"><span data-stu-id="54ba5-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54ba5-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**Ошибка \_ недопустимой \_ Метки**</span><span class="sxs-lookup"><span data-stu-id="54ba5-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ba5-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="54ba5-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="54ba5-801">Указывает, что определенный идентификатор безопасности не может быть назначен в качестве метки объекта.</span><span class="sxs-lookup"><span data-stu-id="54ba5-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="54ba5-802">Требования</span><span class="sxs-lookup"><span data-stu-id="54ba5-802">Requirements</span></span>



| <span data-ttu-id="54ba5-803">Требование</span><span class="sxs-lookup"><span data-stu-id="54ba5-803">Requirement</span></span> | <span data-ttu-id="54ba5-804">Значение</span><span class="sxs-lookup"><span data-stu-id="54ba5-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54ba5-805">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54ba5-805">Minimum supported client</span></span><br/> | <span data-ttu-id="54ba5-806">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="54ba5-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54ba5-807">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54ba5-807">Minimum supported server</span></span><br/> | <span data-ttu-id="54ba5-808">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54ba5-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54ba5-809">Header</span><span class="sxs-lookup"><span data-stu-id="54ba5-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="54ba5-810"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="54ba5-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ba5-811">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54ba5-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ba5-812">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="54ba5-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




