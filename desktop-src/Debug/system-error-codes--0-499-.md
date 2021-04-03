---
description: Описание кодов ошибок 0-499, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Коды системных ошибок (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895973"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="c043f-103">Коды системных ошибок (0-499)</span><span class="sxs-lookup"><span data-stu-id="c043f-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="c043f-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="c043f-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="c043f-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c043f-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="c043f-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки от 0 до 499).</span><span class="sxs-lookup"><span data-stu-id="c043f-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="c043f-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="c043f-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="c043f-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="c043f-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="c043f-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**Ошибка при \_ успешном выполнении**</span><span class="sxs-lookup"><span data-stu-id="c043f-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-110">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c043f-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-111">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c043f-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**Ошибка \_ Недопустимая \_ функция**</span><span class="sxs-lookup"><span data-stu-id="c043f-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c043f-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-114">Неверная функция.</span><span class="sxs-lookup"><span data-stu-id="c043f-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_файл ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="c043f-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-116">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="c043f-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-117">Системе не удается найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="c043f-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_путь к ошибке \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="c043f-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-119">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="c043f-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-120">Системе не удается найти указанный путь.</span><span class="sxs-lookup"><span data-stu-id="c043f-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**Ошибка \_ слишком \_ много \_ открытых \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="c043f-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-122">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="c043f-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-123">Системе не удается открыть файл.</span><span class="sxs-lookup"><span data-stu-id="c043f-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="c043f-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-126">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="c043f-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Ошибка \_ недопустимого \_ маркера**</span><span class="sxs-lookup"><span data-stu-id="c043f-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-128">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="c043f-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-129">Дескриптор недействителен.</span><span class="sxs-lookup"><span data-stu-id="c043f-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**некоторая ошибка в \_ \_ корзине**</span><span class="sxs-lookup"><span data-stu-id="c043f-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-131">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="c043f-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-132">Блоки управления хранилищем были уничтожены.</span><span class="sxs-lookup"><span data-stu-id="c043f-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="c043f-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-134">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="c043f-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-135">Недостаточно ресурсов памяти для обработки этой команды.</span><span class="sxs-lookup"><span data-stu-id="c043f-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**Ошибка \_ недопустимого \_ блока**</span><span class="sxs-lookup"><span data-stu-id="c043f-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-137">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="c043f-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-138">Недопустимый адрес управляющего блока хранения.</span><span class="sxs-lookup"><span data-stu-id="c043f-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**Ошибка \_ неправильной \_ среды**</span><span class="sxs-lookup"><span data-stu-id="c043f-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-140">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="c043f-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-141">Неверное окружение.</span><span class="sxs-lookup"><span data-stu-id="c043f-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**\_неправильный \_ Формат ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-143">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="c043f-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-144">Была сделана попытка загрузить программу, имеющую неверный формат.</span><span class="sxs-lookup"><span data-stu-id="c043f-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**Ошибка \_ доступа к недопустимым \_ данным**</span><span class="sxs-lookup"><span data-stu-id="c043f-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-146">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="c043f-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-147">Недопустимый код доступа.</span><span class="sxs-lookup"><span data-stu-id="c043f-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**Ошибка при \_ недопустимых \_ данных**</span><span class="sxs-lookup"><span data-stu-id="c043f-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-149">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="c043f-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-150">Недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="c043f-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**Ошибка \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="c043f-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-152">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="c043f-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-153">Недостаточно свободного места для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="c043f-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**Ошибка \_ недопустимого \_ диска**</span><span class="sxs-lookup"><span data-stu-id="c043f-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-155">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="c043f-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-156">Системе не удается найти указанный диск.</span><span class="sxs-lookup"><span data-stu-id="c043f-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**Ошибка в \_ текущем \_ каталоге**</span><span class="sxs-lookup"><span data-stu-id="c043f-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-158">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="c043f-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-159">Невозможно удалить каталог.</span><span class="sxs-lookup"><span data-stu-id="c043f-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**Ошибка \_ не на \_ том же \_ устройстве**</span><span class="sxs-lookup"><span data-stu-id="c043f-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-161">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="c043f-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-162">Системе не удается переместить файл на другой диск.</span><span class="sxs-lookup"><span data-stu-id="c043f-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Ошибка \_ больше \_ нет \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="c043f-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-164">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="c043f-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-165">Больше нет файлов.</span><span class="sxs-lookup"><span data-stu-id="c043f-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**Ошибка \_ записи для \_ защиты**</span><span class="sxs-lookup"><span data-stu-id="c043f-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-167">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="c043f-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-168">Носитель защищен от записи.</span><span class="sxs-lookup"><span data-stu-id="c043f-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**Ошибка \_ неправильной \_ единицы**</span><span class="sxs-lookup"><span data-stu-id="c043f-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-170">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="c043f-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-171">Системе не удается найти указанное устройство.</span><span class="sxs-lookup"><span data-stu-id="c043f-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**Ошибка \_ не \_ готова**</span><span class="sxs-lookup"><span data-stu-id="c043f-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-173">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="c043f-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-174">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="c043f-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**Ошибка \_ неправильной \_ команды**</span><span class="sxs-lookup"><span data-stu-id="c043f-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-176">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="c043f-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-177">Устройство не распознает команду.</span><span class="sxs-lookup"><span data-stu-id="c043f-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**CRC, ошибка \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-179">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="c043f-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-180">Ошибка данных (циклическая проверка избыточности).</span><span class="sxs-lookup"><span data-stu-id="c043f-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**Ошибка \_ неправильной \_ длины**</span><span class="sxs-lookup"><span data-stu-id="c043f-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-182">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="c043f-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-183">Программа выдала команду, но длина команды неверна.</span><span class="sxs-lookup"><span data-stu-id="c043f-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**\_Поиск ошибок**</span><span class="sxs-lookup"><span data-stu-id="c043f-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-185">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="c043f-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-186">Диску не удается найти определенную область или отслеживание на диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**Ошибка \_ при \_ отсутствии \_ диска DOS**</span><span class="sxs-lookup"><span data-stu-id="c043f-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-188">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="c043f-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-189">Не удается получить доступ к указанному диску или дискете.</span><span class="sxs-lookup"><span data-stu-id="c043f-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_сектор ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="c043f-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-191">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="c043f-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-192">Диску не удалось найти запрошенный сектор.</span><span class="sxs-lookup"><span data-stu-id="c043f-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**Ошибка \_ вне \_ \_ бумаги**</span><span class="sxs-lookup"><span data-stu-id="c043f-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-194">28 (0x1C)</span><span class="sxs-lookup"><span data-stu-id="c043f-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-195">В принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="c043f-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**Ошибка \_ записи \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-197">29 (0x1D)</span><span class="sxs-lookup"><span data-stu-id="c043f-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-198">Системе не удается выполнить запись на указанное устройство.</span><span class="sxs-lookup"><span data-stu-id="c043f-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**Ошибка при \_ чтении \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-200">30 (0x1E)</span><span class="sxs-lookup"><span data-stu-id="c043f-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-201">Системе не удается выполнить чтение с указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="c043f-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**Ошибка \_ \_ при Gen**</span><span class="sxs-lookup"><span data-stu-id="c043f-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-203">31 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="c043f-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-204">Устройство, подключенное к системе, не работает.</span><span class="sxs-lookup"><span data-stu-id="c043f-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_нарушение общего доступа к ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-206">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="c043f-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-207">The process cannot access the file because it is being used by another process.</span><span class="sxs-lookup"><span data-stu-id="c043f-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_нарушение блокировки \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-209">33 (0x21)</span><span class="sxs-lookup"><span data-stu-id="c043f-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-210">Процессу не удается получить доступ к файлу, так как другой процесс заблокировал часть этого файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**Ошибка \_ неправильного \_ диска**</span><span class="sxs-lookup"><span data-stu-id="c043f-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-212">34 (0x22)</span><span class="sxs-lookup"><span data-stu-id="c043f-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-213">В дисководе находится неверная дискета.</span><span class="sxs-lookup"><span data-stu-id="c043f-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="c043f-214">Вставьте %2 (серийный номер тома: %3) в диск %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**превышено общее количество ошибок в \_ общем \_ буфере \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-216">36 (0x24)</span><span class="sxs-lookup"><span data-stu-id="c043f-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-217">Слишком много файлов открыто для совместного использования.</span><span class="sxs-lookup"><span data-stu-id="c043f-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**Ошибка при \_ обработке \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="c043f-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-219">38 (0x26)</span><span class="sxs-lookup"><span data-stu-id="c043f-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-220">Достигнут конец файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**Ошибка при \_ обработке \_ диска \_ переполнена**</span><span class="sxs-lookup"><span data-stu-id="c043f-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-222">39 (0x27)</span><span class="sxs-lookup"><span data-stu-id="c043f-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-223">Диск полон.</span><span class="sxs-lookup"><span data-stu-id="c043f-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Ошибка \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-225">50 (0x32)</span><span class="sxs-lookup"><span data-stu-id="c043f-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-226">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c043f-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**Ошибка \_ REM \_ не \_ список**</span><span class="sxs-lookup"><span data-stu-id="c043f-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-228">51 (0x33)</span><span class="sxs-lookup"><span data-stu-id="c043f-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-229">Windows не удается найти сетевой путь.</span><span class="sxs-lookup"><span data-stu-id="c043f-229">Windows cannot find the network path.</span></span> <span data-ttu-id="c043f-230">Убедитесь, что сетевой путь указан правильно и конечный компьютер не занят или отключен.</span><span class="sxs-lookup"><span data-stu-id="c043f-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="c043f-231">Если Windows по-прежнему не удается найти сетевой путь, обратитесь к администратору сети.</span><span class="sxs-lookup"><span data-stu-id="c043f-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**Ошибка \_ DUP \_ имя**</span><span class="sxs-lookup"><span data-stu-id="c043f-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-233">52 (0x34)</span><span class="sxs-lookup"><span data-stu-id="c043f-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-234">Вы не подключены, так как в сети существует повторяющееся имя.</span><span class="sxs-lookup"><span data-stu-id="c043f-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="c043f-235">При присоединении к домену перейдите в раздел система на панели управления, чтобы изменить имя компьютера, и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="c043f-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="c043f-236">При присоединении к Рабочей группе Выберите другое имя рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="c043f-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**Ошибка \_ неправильного \_ нетпас**</span><span class="sxs-lookup"><span data-stu-id="c043f-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-238">53 (0x35)</span><span class="sxs-lookup"><span data-stu-id="c043f-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-239">Сетевой путь не найден".</span><span class="sxs-lookup"><span data-stu-id="c043f-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**Ошибка " \_ сеть \_ занята"**</span><span class="sxs-lookup"><span data-stu-id="c043f-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-241">54 (0x36)</span><span class="sxs-lookup"><span data-stu-id="c043f-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-242">Сеть занята.</span><span class="sxs-lookup"><span data-stu-id="c043f-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**Ошибка \_ dev \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="c043f-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-244">55 (0x37)</span><span class="sxs-lookup"><span data-stu-id="c043f-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-245">Указанный сетевой ресурс или устройство больше не доступны.</span><span class="sxs-lookup"><span data-stu-id="c043f-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**Ошибка \_ слишком \_ много \_ команд**</span><span class="sxs-lookup"><span data-stu-id="c043f-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-247">56 (0x38)</span><span class="sxs-lookup"><span data-stu-id="c043f-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-248">Достигнуто ограничение на количество команд в сети BIOS.</span><span class="sxs-lookup"><span data-stu-id="c043f-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**Ошибка \_ ADAP \_ ХДВ \_ Err**</span><span class="sxs-lookup"><span data-stu-id="c043f-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-250">57 (0x39)</span><span class="sxs-lookup"><span data-stu-id="c043f-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-251">Произошла аппаратная ошибка сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="c043f-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**Ошибка \_ неправильного \_ net \_ отв**</span><span class="sxs-lookup"><span data-stu-id="c043f-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-253">58 (0x3A)</span><span class="sxs-lookup"><span data-stu-id="c043f-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-254">Указанный сервер не может выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="c043f-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**Ошибка \_ унексп \_ net \_ Err**</span><span class="sxs-lookup"><span data-stu-id="c043f-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-256">59 (0x3B)</span><span class="sxs-lookup"><span data-stu-id="c043f-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-257">Произошла непредвиденная ошибка сети.</span><span class="sxs-lookup"><span data-stu-id="c043f-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ошибка с \_ плохой ошибкой \_ REM \_ ADAP**</span><span class="sxs-lookup"><span data-stu-id="c043f-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-259">60 (0x3C)</span><span class="sxs-lookup"><span data-stu-id="c043f-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-260">Удаленный адаптер несовместим.</span><span class="sxs-lookup"><span data-stu-id="c043f-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**Ошибка \_ принтк \_ Full**</span><span class="sxs-lookup"><span data-stu-id="c043f-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-262">61 (0x3D)</span><span class="sxs-lookup"><span data-stu-id="c043f-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-263">Очередь принтера заполнена.</span><span class="sxs-lookup"><span data-stu-id="c043f-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**Ошибка \_ без \_ \_ области очереди**</span><span class="sxs-lookup"><span data-stu-id="c043f-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-265">62 (0x3E)</span><span class="sxs-lookup"><span data-stu-id="c043f-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-266">Место для хранения файла, ожидающего печати, недоступно на сервере.</span><span class="sxs-lookup"><span data-stu-id="c043f-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**\_Печать ошибки \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="c043f-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-268">63 (0x3F)</span><span class="sxs-lookup"><span data-stu-id="c043f-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-269">Ваш файл, ожидающий печати, был удален.</span><span class="sxs-lookup"><span data-stu-id="c043f-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**Ошибка \_ NETNAME \_ удалена**</span><span class="sxs-lookup"><span data-stu-id="c043f-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-271">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="c043f-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-272">Указанное сетевое имя более недоступно.</span><span class="sxs-lookup"><span data-stu-id="c043f-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**Ошибка \_ \_ отказа в доступе к сети \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-274">65 (0x41 влево)</span><span class="sxs-lookup"><span data-stu-id="c043f-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-275">Отказано в доступе к сети.</span><span class="sxs-lookup"><span data-stu-id="c043f-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**Ошибка \_ неправильного \_ \_ типа dev**</span><span class="sxs-lookup"><span data-stu-id="c043f-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-277">66 (0x42)</span><span class="sxs-lookup"><span data-stu-id="c043f-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-278">Неверный тип сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c043f-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**Ошибка \_ неправильного \_ сетевого \_ имени**</span><span class="sxs-lookup"><span data-stu-id="c043f-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-280">67 (0x43)</span><span class="sxs-lookup"><span data-stu-id="c043f-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-281">Не найдено сетевое имя".</span><span class="sxs-lookup"><span data-stu-id="c043f-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**Ошибка \_ слишком \_ много \_ имен**</span><span class="sxs-lookup"><span data-stu-id="c043f-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-283">68 (0x44)</span><span class="sxs-lookup"><span data-stu-id="c043f-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-284">Превышено ограничение на число имен для сетевого адаптера локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="c043f-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**Ошибка \_ слишком \_ много \_ подряд**</span><span class="sxs-lookup"><span data-stu-id="c043f-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-286">69 (0x45)</span><span class="sxs-lookup"><span data-stu-id="c043f-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-287">Превышено ограничение на количество сеансов сетевой BIOS.</span><span class="sxs-lookup"><span data-stu-id="c043f-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**\_общий доступ к ошибкам \_ приостановлен**</span><span class="sxs-lookup"><span data-stu-id="c043f-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-289">70 (0x46)</span><span class="sxs-lookup"><span data-stu-id="c043f-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-290">Удаленный сервер приостановлен или находится в процессе запуска.</span><span class="sxs-lookup"><span data-stu-id="c043f-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**Ошибка \_ req \_ не \_ акцеп**</span><span class="sxs-lookup"><span data-stu-id="c043f-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-292">71 (0x47)</span><span class="sxs-lookup"><span data-stu-id="c043f-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-293">В настоящее время больше нет доступных подключений к этому удаленному компьютеру, так как количество подключений, которое может принять компьютер, уже установлено.</span><span class="sxs-lookup"><span data-stu-id="c043f-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**Ошибка \_ редир \_ приостановлена**</span><span class="sxs-lookup"><span data-stu-id="c043f-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-295">72 (0x48)</span><span class="sxs-lookup"><span data-stu-id="c043f-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-296">Указанный принтер или дисковое устройство приостановлены.</span><span class="sxs-lookup"><span data-stu-id="c043f-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**\_файл ошибок \_ существует**</span><span class="sxs-lookup"><span data-stu-id="c043f-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-298">80 (0x50)</span><span class="sxs-lookup"><span data-stu-id="c043f-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-299">Файл существует</span><span class="sxs-lookup"><span data-stu-id="c043f-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**Ошибка \_ не может \_ быть**</span><span class="sxs-lookup"><span data-stu-id="c043f-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-301">82 (0x52)</span><span class="sxs-lookup"><span data-stu-id="c043f-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-302">Не удается создать каталог или файл.</span><span class="sxs-lookup"><span data-stu-id="c043f-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**Ошибка при \_ сбое \_ I24**</span><span class="sxs-lookup"><span data-stu-id="c043f-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-304">83 (0x53)</span><span class="sxs-lookup"><span data-stu-id="c043f-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-305">Сбой на INT 24.</span><span class="sxs-lookup"><span data-stu-id="c043f-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**Ошибка \_ из \_ \_ структур**</span><span class="sxs-lookup"><span data-stu-id="c043f-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-307">84 (0x54)</span><span class="sxs-lookup"><span data-stu-id="c043f-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-308">Хранилище для обработки этого запроса недоступно.</span><span class="sxs-lookup"><span data-stu-id="c043f-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**Ошибка \_ уже \_ назначена**</span><span class="sxs-lookup"><span data-stu-id="c043f-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-310">85 (0x55)</span><span class="sxs-lookup"><span data-stu-id="c043f-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-311">Имя локального устройства уже используется.</span><span class="sxs-lookup"><span data-stu-id="c043f-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**Ошибка \_ неправильного \_ пароля**</span><span class="sxs-lookup"><span data-stu-id="c043f-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-313">86 (0x56)</span><span class="sxs-lookup"><span data-stu-id="c043f-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-314">Указан неверный сетевой пароль.</span><span class="sxs-lookup"><span data-stu-id="c043f-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="c043f-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-316">87 (0x57)</span><span class="sxs-lookup"><span data-stu-id="c043f-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-317">Неправильный параметр".</span><span class="sxs-lookup"><span data-stu-id="c043f-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**Ошибка \_ ошибки \_ записи в сеть \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-319">88 (0x58)</span><span class="sxs-lookup"><span data-stu-id="c043f-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-320">В сети произошла ошибка записи.</span><span class="sxs-lookup"><span data-stu-id="c043f-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**Ошибка \_ без \_ \_ слотов процедур**</span><span class="sxs-lookup"><span data-stu-id="c043f-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-322">89 (0x59)</span><span class="sxs-lookup"><span data-stu-id="c043f-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-323">В данный момент система не может запустить другой процесс.</span><span class="sxs-lookup"><span data-stu-id="c043f-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**Ошибка \_ слишком \_ большого числа \_ семафоров**</span><span class="sxs-lookup"><span data-stu-id="c043f-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-325">100 (0x64)</span><span class="sxs-lookup"><span data-stu-id="c043f-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-326">Невозможно создать другой системный семафор.</span><span class="sxs-lookup"><span data-stu-id="c043f-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**Ошибка \_ без \_ \_ уже существующего \_ владельца SEM**</span><span class="sxs-lookup"><span data-stu-id="c043f-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-328">101 (0x65)</span><span class="sxs-lookup"><span data-stu-id="c043f-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-329">Эксклюзивный семафор принадлежит другому процессу.</span><span class="sxs-lookup"><span data-stu-id="c043f-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**указана ошибка \_ SEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-331">102 (0x66)</span><span class="sxs-lookup"><span data-stu-id="c043f-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-332">Семафор установлен и не может быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="c043f-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**Ошибка \_ слишком \_ много \_ \_ запросов SEM**</span><span class="sxs-lookup"><span data-stu-id="c043f-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-334">103 (0x67)</span><span class="sxs-lookup"><span data-stu-id="c043f-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-335">Семафор не может быть установлен повторно.</span><span class="sxs-lookup"><span data-stu-id="c043f-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**Ошибка \_ недопустима \_ во \_ \_ время прерывания**</span><span class="sxs-lookup"><span data-stu-id="c043f-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-337">104 (0x68)</span><span class="sxs-lookup"><span data-stu-id="c043f-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-338">Не удается запросить эксклюзивные семафоры во время прерывания.</span><span class="sxs-lookup"><span data-stu-id="c043f-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**Ошибка \_ SEM \_ owner \_ умер**</span><span class="sxs-lookup"><span data-stu-id="c043f-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-340">105 (0x69)</span><span class="sxs-lookup"><span data-stu-id="c043f-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-341">Предыдущее владение этим семафором завершено.</span><span class="sxs-lookup"><span data-stu-id="c043f-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**Ошибка \_ в \_ \_ ограничении пользователя SEM**</span><span class="sxs-lookup"><span data-stu-id="c043f-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-343">106 (0x6A)</span><span class="sxs-lookup"><span data-stu-id="c043f-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-344">Вставьте дискету для диска %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**Ошибка \_ при \_ изменении диска**</span><span class="sxs-lookup"><span data-stu-id="c043f-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-346">107 (0x6B)</span><span class="sxs-lookup"><span data-stu-id="c043f-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-347">Программа остановлена, так как не вставлена дополнительная дискета.</span><span class="sxs-lookup"><span data-stu-id="c043f-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**Ошибка \_ \_ блокировки диска**</span><span class="sxs-lookup"><span data-stu-id="c043f-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-349">108 (0x6C)</span><span class="sxs-lookup"><span data-stu-id="c043f-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-350">Диск занят или заблокирован другим процессом.</span><span class="sxs-lookup"><span data-stu-id="c043f-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**Ошибка при \_ нарушении \_ канала**</span><span class="sxs-lookup"><span data-stu-id="c043f-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-352">109 (0x6D)</span><span class="sxs-lookup"><span data-stu-id="c043f-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-353">Канал завершен.</span><span class="sxs-lookup"><span data-stu-id="c043f-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**Ошибка \_ \_ при открытии**</span><span class="sxs-lookup"><span data-stu-id="c043f-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-355">110 (0x6E)</span><span class="sxs-lookup"><span data-stu-id="c043f-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-356">Системе не удается открыть указанное устройство или файл.</span><span class="sxs-lookup"><span data-stu-id="c043f-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_ \_ переполнение буфера ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-358">111 (0x6F)</span><span class="sxs-lookup"><span data-stu-id="c043f-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-359">Имя файла слишком длинное.</span><span class="sxs-lookup"><span data-stu-id="c043f-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**Ошибка \_ \_ переполнения диска**</span><span class="sxs-lookup"><span data-stu-id="c043f-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-361">112 (0x70)</span><span class="sxs-lookup"><span data-stu-id="c043f-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-362">Недостаточно места на диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**Ошибка \_ больше \_ нет \_ \_ дескрипторов поиска**</span><span class="sxs-lookup"><span data-stu-id="c043f-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-364">113 (0x71)</span><span class="sxs-lookup"><span data-stu-id="c043f-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-365">Больше нет доступных идентификаторов внутренних файлов.</span><span class="sxs-lookup"><span data-stu-id="c043f-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**Ошибка \_ недопустимого \_ целевого \_ маркера**</span><span class="sxs-lookup"><span data-stu-id="c043f-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-367">114 (0x72)</span><span class="sxs-lookup"><span data-stu-id="c043f-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-368">Неверный целевой внутренний идентификатор файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**Ошибка \_ недопустимой \_ категории**</span><span class="sxs-lookup"><span data-stu-id="c043f-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-370">117 (0x75)</span><span class="sxs-lookup"><span data-stu-id="c043f-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-371">Вызов IOCTL, сделанный программой приложения, неверен.</span><span class="sxs-lookup"><span data-stu-id="c043f-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**Ошибка \_ при \_ проверке недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="c043f-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-373">118 (0x76)</span><span class="sxs-lookup"><span data-stu-id="c043f-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-374">Неправильное значение параметра проверки-on-Write.</span><span class="sxs-lookup"><span data-stu-id="c043f-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ОШИБКА с \_ неправильным \_ \_ уровнем драйвера**</span><span class="sxs-lookup"><span data-stu-id="c043f-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-376">119 (0x77)</span><span class="sxs-lookup"><span data-stu-id="c043f-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-377">Система не поддерживает запрошенную команду.</span><span class="sxs-lookup"><span data-stu-id="c043f-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**\_вызов ошибки \_ не \_ реализован**</span><span class="sxs-lookup"><span data-stu-id="c043f-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-379">120 (0x78)</span><span class="sxs-lookup"><span data-stu-id="c043f-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-380">Эта функция не поддерживается в этой системе.</span><span class="sxs-lookup"><span data-stu-id="c043f-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**Ошибка \_ \_ времени ожидания SEM**</span><span class="sxs-lookup"><span data-stu-id="c043f-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-382">121 (0x79)</span><span class="sxs-lookup"><span data-stu-id="c043f-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-383">Истек период ожидания семафора.</span><span class="sxs-lookup"><span data-stu-id="c043f-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="c043f-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-385">122 (0x7A)</span><span class="sxs-lookup"><span data-stu-id="c043f-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-386">Область данных, переданная в системный вызов, слишком мала.</span><span class="sxs-lookup"><span data-stu-id="c043f-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**Ошибка \_ недопустимое \_ имя**</span><span class="sxs-lookup"><span data-stu-id="c043f-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-388">123 (0x7B)</span><span class="sxs-lookup"><span data-stu-id="c043f-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-389">Синтаксическая ошибка в имени файла, имени каталога или метке тома.</span><span class="sxs-lookup"><span data-stu-id="c043f-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**\_Недопустимый \_ уровень ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-391">124 (0x7C)</span><span class="sxs-lookup"><span data-stu-id="c043f-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-392">Неверный уровень системного вызова.</span><span class="sxs-lookup"><span data-stu-id="c043f-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**Ошибка \_ без \_ \_ метки тома**</span><span class="sxs-lookup"><span data-stu-id="c043f-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-394">125 (0x7D)</span><span class="sxs-lookup"><span data-stu-id="c043f-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-395">Диск не имеет метки тома.</span><span class="sxs-lookup"><span data-stu-id="c043f-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**Ошибка \_ Mod \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="c043f-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-397">126 (0x7E)</span><span class="sxs-lookup"><span data-stu-id="c043f-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-398">Не найден указанный модуль.</span><span class="sxs-lookup"><span data-stu-id="c043f-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**Ошибка \_ \_ не \_ найдена процедура**</span><span class="sxs-lookup"><span data-stu-id="c043f-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-400">127 (0x7F)</span><span class="sxs-lookup"><span data-stu-id="c043f-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-401">Не удалось найти указанную процедуру.</span><span class="sxs-lookup"><span data-stu-id="c043f-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**Ошибка \_ Ожидание \_ отсутствия \_ дочерних элементов**</span><span class="sxs-lookup"><span data-stu-id="c043f-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-403">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="c043f-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-404">Нет дочерних процессов для ожидания.</span><span class="sxs-lookup"><span data-stu-id="c043f-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**Ошибка \_ дочернего элемента \_ не \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="c043f-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-406">129 (0x81)</span><span class="sxs-lookup"><span data-stu-id="c043f-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-407">Приложение %1 не может быть запущено в режиме Win32.</span><span class="sxs-lookup"><span data-stu-id="c043f-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**Ошибка \_ прямого \_ доступа к \_ обработчику**</span><span class="sxs-lookup"><span data-stu-id="c043f-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-409">130 (0x82)</span><span class="sxs-lookup"><span data-stu-id="c043f-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-410">Попытка использовать маркер файла для открытого раздела диска для операции, отличной от операций ввода-вывода с необработанным диском.</span><span class="sxs-lookup"><span data-stu-id="c043f-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**Ошибка при \_ поиске отрицательных результатов \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-412">131 (0x83)</span><span class="sxs-lookup"><span data-stu-id="c043f-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-413">Предпринята попытка переместить указатель на файл перед началом файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**\_Поиск ошибок \_ на \_ устройстве**</span><span class="sxs-lookup"><span data-stu-id="c043f-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-415">132 (0x84)</span><span class="sxs-lookup"><span data-stu-id="c043f-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-416">Не удается задать указатель файла для указанного устройства или файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**Ошибка \_ : \_ Присоединение к \_ целевому объекту**</span><span class="sxs-lookup"><span data-stu-id="c043f-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-418">133 (0x85)</span><span class="sxs-lookup"><span data-stu-id="c043f-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-419">Команду JOIN или SUBST нельзя использовать для диска, который содержит ранее подключенные диски.</span><span class="sxs-lookup"><span data-stu-id="c043f-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**Ошибка \_ \_ присоединена**</span><span class="sxs-lookup"><span data-stu-id="c043f-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-421">134 (0x86)</span><span class="sxs-lookup"><span data-stu-id="c043f-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-422">Предпринята попытка использовать команду JOIN или SUBST на диске, который уже присоединен.</span><span class="sxs-lookup"><span data-stu-id="c043f-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**\_указана \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="c043f-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-424">135 (0x87)</span><span class="sxs-lookup"><span data-stu-id="c043f-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-425">Была предпринята попытка использовать команду JOIN или SUBST на диске, который уже был заменен.</span><span class="sxs-lookup"><span data-stu-id="c043f-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**Ошибка \_ не \_ присоединена**</span><span class="sxs-lookup"><span data-stu-id="c043f-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-427">136 (0x88)</span><span class="sxs-lookup"><span data-stu-id="c043f-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-428">Система попыталась удалить соединение диска, который не присоединен.</span><span class="sxs-lookup"><span data-stu-id="c043f-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**не удается отобразить ошибку \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-430">137 (0x89)</span><span class="sxs-lookup"><span data-stu-id="c043f-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-431">Система попыталась удалить подстановку незаменяемого диска.</span><span class="sxs-lookup"><span data-stu-id="c043f-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**Ошибка при \_ присоединении \_ к \_ соединению**</span><span class="sxs-lookup"><span data-stu-id="c043f-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-433">138 (0x8A)</span><span class="sxs-lookup"><span data-stu-id="c043f-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-434">Система попыталась присоединить диск к каталогу на присоединенном диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**Ошибка \_ subst \_ для \_ subst**</span><span class="sxs-lookup"><span data-stu-id="c043f-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-436">139 (0x8B)</span><span class="sxs-lookup"><span data-stu-id="c043f-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-437">Система попыталась заменить диск на каталог на подставляемом диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**Ошибка при \_ присоединении \_ к \_ subst**</span><span class="sxs-lookup"><span data-stu-id="c043f-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-439">140 (0x8C)</span><span class="sxs-lookup"><span data-stu-id="c043f-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-440">Система попыталась присоединить диск к каталогу на подставляемом диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**Ошибка \_ subst \_ для \_ Присоединение**</span><span class="sxs-lookup"><span data-stu-id="c043f-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-442">141 (0x8D)</span><span class="sxs-lookup"><span data-stu-id="c043f-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-443">Система попыталась отобразить диск в каталог на присоединенном диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**\_диск занят \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-445">142 (0x8E)</span><span class="sxs-lookup"><span data-stu-id="c043f-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-446">В настоящее время системе не удается выполнить соединение или SUBST.</span><span class="sxs-lookup"><span data-stu-id="c043f-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**Ошибка на \_ том же \_ диске**</span><span class="sxs-lookup"><span data-stu-id="c043f-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-448">143 (0x8F)</span><span class="sxs-lookup"><span data-stu-id="c043f-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-449">Система не может присоединить или заменить диск на каталог или для каталога на том же диске.</span><span class="sxs-lookup"><span data-stu-id="c043f-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**Ошибка \_ dir \_ не \_ корневая папка**</span><span class="sxs-lookup"><span data-stu-id="c043f-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-451">144 (0x90)</span><span class="sxs-lookup"><span data-stu-id="c043f-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-452">Каталог не является вложенным каталогом корневого каталога.</span><span class="sxs-lookup"><span data-stu-id="c043f-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**Ошибка \_ dir, \_ не \_ пустая**</span><span class="sxs-lookup"><span data-stu-id="c043f-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-454">145 (0x91)</span><span class="sxs-lookup"><span data-stu-id="c043f-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-455">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="c043f-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**Ошибка \_ — \_ \_ путь SUBST**</span><span class="sxs-lookup"><span data-stu-id="c043f-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-457">146 (0x92)</span><span class="sxs-lookup"><span data-stu-id="c043f-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-458">Указанный путь используется в подстановке.</span><span class="sxs-lookup"><span data-stu-id="c043f-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**Ошибка \_ — \_ путь к соединению \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-460">147 (0x93)</span><span class="sxs-lookup"><span data-stu-id="c043f-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-461">Недостаточно ресурсов для обработки этой команды.</span><span class="sxs-lookup"><span data-stu-id="c043f-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**\_путь к ошибке \_ занят**</span><span class="sxs-lookup"><span data-stu-id="c043f-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-463">148 (0x94)</span><span class="sxs-lookup"><span data-stu-id="c043f-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-464">Указанный путь не может быть использован в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="c043f-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**Ошибка \_ : \_ subst \_ Target**</span><span class="sxs-lookup"><span data-stu-id="c043f-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-466">149 (0x95)</span><span class="sxs-lookup"><span data-stu-id="c043f-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-467">Предпринята попытка присоединить или заменить диск, для которого каталог на диске является целью предыдущего замены.</span><span class="sxs-lookup"><span data-stu-id="c043f-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**Ошибка \_ \_ трассировки системы**</span><span class="sxs-lookup"><span data-stu-id="c043f-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-469">150 (0x96)</span><span class="sxs-lookup"><span data-stu-id="c043f-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-470">Данные трассировки системы не указаны в файле CONFIG.SYS, или трассировка запрещена.</span><span class="sxs-lookup"><span data-stu-id="c043f-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**Ошибка при \_ неправильном \_ \_ числе событий**</span><span class="sxs-lookup"><span data-stu-id="c043f-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-472">151 (0x97)</span><span class="sxs-lookup"><span data-stu-id="c043f-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-473">Указано неправильное число указанных событий семафора для Досмукссемваит.</span><span class="sxs-lookup"><span data-stu-id="c043f-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**Ошибка \_ слишком \_ много \_ муксваитерс**</span><span class="sxs-lookup"><span data-stu-id="c043f-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-475">152 (0x98)</span><span class="sxs-lookup"><span data-stu-id="c043f-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-476">Досмукссемваит не выполнен; уже задано слишком много семафоров.</span><span class="sxs-lookup"><span data-stu-id="c043f-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**Ошибка \_ недопустимого \_ \_ формата списка**</span><span class="sxs-lookup"><span data-stu-id="c043f-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-478">153 (0x99)</span><span class="sxs-lookup"><span data-stu-id="c043f-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-479">Недопустимый список Досмукссемваит.</span><span class="sxs-lookup"><span data-stu-id="c043f-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**\_ \_ слишком \_ ДЛИННая метка ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-481">154 (0x9A)</span><span class="sxs-lookup"><span data-stu-id="c043f-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-482">Введенная метка тома превышает ограничение на количество символов в целевой файловой системе.</span><span class="sxs-lookup"><span data-stu-id="c043f-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**Ошибка \_ слишком \_ много \_ ткбс**</span><span class="sxs-lookup"><span data-stu-id="c043f-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-484">155 (0x9B)</span><span class="sxs-lookup"><span data-stu-id="c043f-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-485">Не удается создать другой поток.</span><span class="sxs-lookup"><span data-stu-id="c043f-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**\_сигнал ошибки \_ отклонен**</span><span class="sxs-lookup"><span data-stu-id="c043f-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-487">156 (0x9C)</span><span class="sxs-lookup"><span data-stu-id="c043f-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-488">Процесс получателя отклонил сигнал.</span><span class="sxs-lookup"><span data-stu-id="c043f-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**Ошибка \_ отклонена**</span><span class="sxs-lookup"><span data-stu-id="c043f-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-490">157 (0x9D)</span><span class="sxs-lookup"><span data-stu-id="c043f-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-491">Сегмент уже удален и не может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c043f-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**Ошибка \_ не \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="c043f-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-493">158 (0x9E)</span><span class="sxs-lookup"><span data-stu-id="c043f-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-494">Сегмент уже разблокирован.</span><span class="sxs-lookup"><span data-stu-id="c043f-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ОШИБКА с \_ неверным \_ \_ адресом THREADID**</span><span class="sxs-lookup"><span data-stu-id="c043f-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-496">159 (0x9F)</span><span class="sxs-lookup"><span data-stu-id="c043f-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-497">Неправильный адрес для идентификатора потока.</span><span class="sxs-lookup"><span data-stu-id="c043f-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ошибочные \_ \_ аргументы**</span><span class="sxs-lookup"><span data-stu-id="c043f-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-499">160 (0X82)</span><span class="sxs-lookup"><span data-stu-id="c043f-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-500">Один или несколько аргументов неверны.</span><span class="sxs-lookup"><span data-stu-id="c043f-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ОШИБКА с \_ неверным \_ путем**</span><span class="sxs-lookup"><span data-stu-id="c043f-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-502">161 (0xA1)</span><span class="sxs-lookup"><span data-stu-id="c043f-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-503">Указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="c043f-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**\_сигнал ошибки \_ в ожидании**</span><span class="sxs-lookup"><span data-stu-id="c043f-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-505">162 (0xA2)</span><span class="sxs-lookup"><span data-stu-id="c043f-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-506">Сигнал уже находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="c043f-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**Ошибка \_ Max \_ СРДС \_ достигнуто**</span><span class="sxs-lookup"><span data-stu-id="c043f-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-508">164 (токенов 0xA4)</span><span class="sxs-lookup"><span data-stu-id="c043f-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-509">В системе больше нельзя создавать потоки.</span><span class="sxs-lookup"><span data-stu-id="c043f-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_сбой блокировки \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-511">167 (0xA7)</span><span class="sxs-lookup"><span data-stu-id="c043f-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-512">Не удалось заблокировать область файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**Ошибка \_ занята**</span><span class="sxs-lookup"><span data-stu-id="c043f-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-514">170 (0xAA)</span><span class="sxs-lookup"><span data-stu-id="c043f-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-515">Запрошенный ресурс уже используется.</span><span class="sxs-lookup"><span data-stu-id="c043f-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**Ошибка \_ \_ \_ в процессе поддержки \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="c043f-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-517">171 (0xAB)</span><span class="sxs-lookup"><span data-stu-id="c043f-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-518">Идет обнаружение поддержки команд устройства.</span><span class="sxs-lookup"><span data-stu-id="c043f-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**Ошибка \_ отмены \_ нарушения**</span><span class="sxs-lookup"><span data-stu-id="c043f-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-520">173 (0xAD)</span><span class="sxs-lookup"><span data-stu-id="c043f-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-521">Запрос блокировки не был выполнен для указанной региона отмены.</span><span class="sxs-lookup"><span data-stu-id="c043f-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ОШИБКИ \_ атомарных \_ блокировок \_ не \_ поддерживаются**</span><span class="sxs-lookup"><span data-stu-id="c043f-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-523">174 (0xAE)</span><span class="sxs-lookup"><span data-stu-id="c043f-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-524">Файловая система не поддерживает атомарные изменения типа блокировки.</span><span class="sxs-lookup"><span data-stu-id="c043f-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**Ошибка \_ недопустимого \_ \_ номера сегмента**</span><span class="sxs-lookup"><span data-stu-id="c043f-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-526">180 (0xB4)</span><span class="sxs-lookup"><span data-stu-id="c043f-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-527">Система обнаружила неверный номер сегмента.</span><span class="sxs-lookup"><span data-stu-id="c043f-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ОШИБКА с \_ недопустимым \_ порядковым номером**</span><span class="sxs-lookup"><span data-stu-id="c043f-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-529">182 (0xB6)</span><span class="sxs-lookup"><span data-stu-id="c043f-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-530">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**Ошибка \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="c043f-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-532">183 (0xB7)</span><span class="sxs-lookup"><span data-stu-id="c043f-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-533">невозможно создать файл, так как он уже существует.</span><span class="sxs-lookup"><span data-stu-id="c043f-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**Ошибка \_ недопустимого \_ номера флага \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-535">186 (0xBA)</span><span class="sxs-lookup"><span data-stu-id="c043f-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-536">Передан неверный флаг.</span><span class="sxs-lookup"><span data-stu-id="c043f-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**Ошибка \_ SEM \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="c043f-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-538">187 (0xBB)</span><span class="sxs-lookup"><span data-stu-id="c043f-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-539">Указанное имя системного семафора не найдено.</span><span class="sxs-lookup"><span data-stu-id="c043f-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**Ошибка \_ при \_ запуске \_ кодесег**</span><span class="sxs-lookup"><span data-stu-id="c043f-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-541">188 (0xBC)</span><span class="sxs-lookup"><span data-stu-id="c043f-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-542">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**Ошибка \_ недопустимого \_ стакксег**</span><span class="sxs-lookup"><span data-stu-id="c043f-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-544">189 (0xBD)</span><span class="sxs-lookup"><span data-stu-id="c043f-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-545">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**Ошибка \_ недопустимого \_ MODULETYPE**</span><span class="sxs-lookup"><span data-stu-id="c043f-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-547">190 (0xBE)</span><span class="sxs-lookup"><span data-stu-id="c043f-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-548">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**Ошибка \_ недопустимой \_ \_ подписи exe**</span><span class="sxs-lookup"><span data-stu-id="c043f-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-550">191 (0xBF)</span><span class="sxs-lookup"><span data-stu-id="c043f-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-551">Не удается выполнить %1 в режиме Win32.</span><span class="sxs-lookup"><span data-stu-id="c043f-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**Ошибка \_ exe \_ помечена как \_ Недопустимая**</span><span class="sxs-lookup"><span data-stu-id="c043f-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-553">192 (0xC0)</span><span class="sxs-lookup"><span data-stu-id="c043f-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-554">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**Ошибка в \_ неправильном \_ \_ формате exe**</span><span class="sxs-lookup"><span data-stu-id="c043f-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-556">193 (0xC1)</span><span class="sxs-lookup"><span data-stu-id="c043f-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-557">%1 не является допустимым приложением Win32.</span><span class="sxs-lookup"><span data-stu-id="c043f-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Данные об ошибках при \_ итерации \_ \_ превышают \_ 64 КБ**</span><span class="sxs-lookup"><span data-stu-id="c043f-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-559">194 (0xC2)</span><span class="sxs-lookup"><span data-stu-id="c043f-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-560">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**Ошибка \_ недопустимого \_ миналлоксизе**</span><span class="sxs-lookup"><span data-stu-id="c043f-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-562">195 (0xC3)</span><span class="sxs-lookup"><span data-stu-id="c043f-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-563">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**Ошибка \_ динлинк \_ из \_ недопустимого \_ кольца**</span><span class="sxs-lookup"><span data-stu-id="c043f-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-565">196 (0xC4)</span><span class="sxs-lookup"><span data-stu-id="c043f-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-566">Операционная система не может запустить эту программу приложения.</span><span class="sxs-lookup"><span data-stu-id="c043f-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**Ошибка \_ иопл \_ не \_ включена**</span><span class="sxs-lookup"><span data-stu-id="c043f-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-568">197 (0xC5)</span><span class="sxs-lookup"><span data-stu-id="c043f-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-569">Операционная система в настоящее время не настроена для запуска этого приложения.</span><span class="sxs-lookup"><span data-stu-id="c043f-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**Ошибка \_ недопустимого \_ сегдпл**</span><span class="sxs-lookup"><span data-stu-id="c043f-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-571">198 (0xC6)</span><span class="sxs-lookup"><span data-stu-id="c043f-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-572">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**Ошибка \_ аутодатасег \_ превышает \_ 64 КБ**</span><span class="sxs-lookup"><span data-stu-id="c043f-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-574">199 (0xC7)</span><span class="sxs-lookup"><span data-stu-id="c043f-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-575">Операционная система не может запустить эту программу приложения.</span><span class="sxs-lookup"><span data-stu-id="c043f-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**Ошибка \_ RING2SEG \_ должна \_ быть \_ перемещаемой**</span><span class="sxs-lookup"><span data-stu-id="c043f-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-577">200 (0xC8)</span><span class="sxs-lookup"><span data-stu-id="c043f-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-578">Сегмент кода не может быть больше или равен 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="c043f-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR \_ reloc \_ chain \_ ксидс \_ сеглим**</span><span class="sxs-lookup"><span data-stu-id="c043f-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-580">201 (0xC9)</span><span class="sxs-lookup"><span data-stu-id="c043f-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-581">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**Ошибка \_ инфлуп \_ в \_ \_ цепочке reloc**</span><span class="sxs-lookup"><span data-stu-id="c043f-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-583">202 (0xCA)</span><span class="sxs-lookup"><span data-stu-id="c043f-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-584">Операционная система не может выполнить %1.</span><span class="sxs-lookup"><span data-stu-id="c043f-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**Ошибка \_ ENVVAR \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="c043f-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-586">203 (0xCB)</span><span class="sxs-lookup"><span data-stu-id="c043f-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-587">Системе не удалось найти указанный параметр среды.</span><span class="sxs-lookup"><span data-stu-id="c043f-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**Ошибка \_ не \_ \_ отправлен сигнал**</span><span class="sxs-lookup"><span data-stu-id="c043f-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-589">205 (0xCD)</span><span class="sxs-lookup"><span data-stu-id="c043f-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-590">Ни один из процессов в поддереве команды не имеет обработчика сигналов.</span><span class="sxs-lookup"><span data-stu-id="c043f-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**Ошибка \_ имя файла \_ ексцед \_ Range**</span><span class="sxs-lookup"><span data-stu-id="c043f-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-592">206 (0xCE)</span><span class="sxs-lookup"><span data-stu-id="c043f-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-593">Слишком длинное имя файла или расширение.</span><span class="sxs-lookup"><span data-stu-id="c043f-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**Ошибка \_ \_ \_ при использовании стека RING2 \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-595">207 (0xCF)</span><span class="sxs-lookup"><span data-stu-id="c043f-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-596">Стек Ring 2 используется.</span><span class="sxs-lookup"><span data-stu-id="c043f-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**\_ \_ \_ слишком \_ длинное расширение мета для ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-598">208 (0xD0)</span><span class="sxs-lookup"><span data-stu-id="c043f-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-599">Символы глобального имени файла \* или? введены неправильно или указано слишком много символов глобального имени файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**Ошибка \_ недопустимого \_ \_ номера сигнала**</span><span class="sxs-lookup"><span data-stu-id="c043f-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-601">209 (0xD1)</span><span class="sxs-lookup"><span data-stu-id="c043f-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-602">Отправляемый сигнал неверен.</span><span class="sxs-lookup"><span data-stu-id="c043f-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**\_Поток ошибок \_ 1 \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="c043f-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-604">210 (0xD2)</span><span class="sxs-lookup"><span data-stu-id="c043f-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-605">Не удается установить обработчик сигналов.</span><span class="sxs-lookup"><span data-stu-id="c043f-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**Ошибка \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="c043f-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-607">212 (0xD4)</span><span class="sxs-lookup"><span data-stu-id="c043f-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-608">Сегмент заблокирован и не может быть выделен повторно.</span><span class="sxs-lookup"><span data-stu-id="c043f-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**Ошибка \_ слишком \_ много \_ модулей**</span><span class="sxs-lookup"><span data-stu-id="c043f-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-610">214 (0xD6)</span><span class="sxs-lookup"><span data-stu-id="c043f-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-611">К этой программе или модулю динамической компоновки подключено слишком много модулей динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="c043f-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_вложенность ошибок \_ \_ запрещена**</span><span class="sxs-lookup"><span data-stu-id="c043f-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-613">215 (0xD7)</span><span class="sxs-lookup"><span data-stu-id="c043f-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-614">Невозможно вложить вызовы в LoadModule.</span><span class="sxs-lookup"><span data-stu-id="c043f-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**Ошибка \_ exe \_ \_ \_ несоответствие типов компьютеров**</span><span class="sxs-lookup"><span data-stu-id="c043f-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-616">216 (0xD8)</span><span class="sxs-lookup"><span data-stu-id="c043f-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-617">Эта версия %1 несовместима с версией Windows, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="c043f-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="c043f-618">Проверьте сведения о системе компьютера, а затем обратитесь к издателю программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="c043f-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**Ошибка \_ exe \_ не \_ может \_ изменить \_ двоичный файл со знаком**</span><span class="sxs-lookup"><span data-stu-id="c043f-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-620">217 (0xD9)</span><span class="sxs-lookup"><span data-stu-id="c043f-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-621">Файл образа %1 подписан, его невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="c043f-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**Ошибка \_ exe \_ не \_ может \_ изменить \_ \_ двоичный файл со строгим знаком**</span><span class="sxs-lookup"><span data-stu-id="c043f-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-623">218 (0xDA)</span><span class="sxs-lookup"><span data-stu-id="c043f-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-624">Файл образа %1 имеет строгие подписи, его невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="c043f-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**файл с ОШИБКАми \_ \_ извлечен \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-626">220 (0xDC)</span><span class="sxs-lookup"><span data-stu-id="c043f-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-627">Этот файл извлечен или заблокирован для редактирования другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="c043f-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**\_требуется извлечение \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="c043f-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-629">221 (0xDD)</span><span class="sxs-lookup"><span data-stu-id="c043f-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-630">Перед сохранением изменений необходимо извлечь файл.</span><span class="sxs-lookup"><span data-stu-id="c043f-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**Ошибка \_ неправильного \_ \_ типа файла**</span><span class="sxs-lookup"><span data-stu-id="c043f-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-632">222 (0xDE)</span><span class="sxs-lookup"><span data-stu-id="c043f-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-633">Сохраняемый или извлекаемый тип файла заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c043f-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**\_файл ошибок \_ слишком \_ большой**</span><span class="sxs-lookup"><span data-stu-id="c043f-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-635">223 (0xDF)</span><span class="sxs-lookup"><span data-stu-id="c043f-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-636">Размер файла превышает допустимый предел и не может быть сохранен.</span><span class="sxs-lookup"><span data-stu-id="c043f-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_ \_ требуется проверка подлинности форм с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-638">224 (0xE0)</span><span class="sxs-lookup"><span data-stu-id="c043f-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-639">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="c043f-639">Access Denied.</span></span> <span data-ttu-id="c043f-640">Перед открытием файлов в этом расположении необходимо сначала добавить веб-сайт в список надежных сайтов, перейти на веб-сайт и выбрать параметр автоматического входа.</span><span class="sxs-lookup"><span data-stu-id="c043f-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ОШИБОЧный \_ вирус \_ заражен**</span><span class="sxs-lookup"><span data-stu-id="c043f-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-642">225 (0xE1)</span><span class="sxs-lookup"><span data-stu-id="c043f-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-643">Операция не была успешно завершена, так как файл содержит вирус или потенциально нежелательное программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="c043f-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**Ошибка \_ при \_ удалении вируса**</span><span class="sxs-lookup"><span data-stu-id="c043f-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-645">226 (0xE2)</span><span class="sxs-lookup"><span data-stu-id="c043f-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-646">Этот файл содержит вирус или потенциально нежелательное программное обеспечение и не может быть открыт.</span><span class="sxs-lookup"><span data-stu-id="c043f-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="c043f-647">Из-за природы этого вируса или потенциально нежелательного программного обеспечения файл был удален из этого расположения.</span><span class="sxs-lookup"><span data-stu-id="c043f-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**\_локальный канал \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="c043f-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-649">229 (0xE5)</span><span class="sxs-lookup"><span data-stu-id="c043f-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-650">Канал является локальным.</span><span class="sxs-lookup"><span data-stu-id="c043f-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**Ошибка \_ неверного \_ канала**</span><span class="sxs-lookup"><span data-stu-id="c043f-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-652">230 (0xE6)</span><span class="sxs-lookup"><span data-stu-id="c043f-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-653">Недопустимое состояние канала.</span><span class="sxs-lookup"><span data-stu-id="c043f-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**\_канал ошибки \_ занят**</span><span class="sxs-lookup"><span data-stu-id="c043f-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-655">231 (0xE7)</span><span class="sxs-lookup"><span data-stu-id="c043f-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-656">Все экземпляры канала заняты.</span><span class="sxs-lookup"><span data-stu-id="c043f-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**Ошибка \_ без \_ данных**</span><span class="sxs-lookup"><span data-stu-id="c043f-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-658">232 (0xE8)</span><span class="sxs-lookup"><span data-stu-id="c043f-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-659">Канал закрывается.</span><span class="sxs-lookup"><span data-stu-id="c043f-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**\_канал ошибки \_ не \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="c043f-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-661">233 (0xE9)</span><span class="sxs-lookup"><span data-stu-id="c043f-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-662">Процесс отсутствует на другом конце канала.</span><span class="sxs-lookup"><span data-stu-id="c043f-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Ошибка \_ дополнительных \_ данных**</span><span class="sxs-lookup"><span data-stu-id="c043f-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-664">234 (0xEA)</span><span class="sxs-lookup"><span data-stu-id="c043f-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-665">More data is available.</span><span class="sxs-lookup"><span data-stu-id="c043f-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**Ошибка \_ VC \_ DISCONNECTED**</span><span class="sxs-lookup"><span data-stu-id="c043f-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-667">240 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="c043f-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-668">Сеанс был отменен.</span><span class="sxs-lookup"><span data-stu-id="c043f-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**Ошибка \_ недопустимого \_ \_ имени EA**</span><span class="sxs-lookup"><span data-stu-id="c043f-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-670">254 (0xFE)</span><span class="sxs-lookup"><span data-stu-id="c043f-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-671">Указано недопустимое имя расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="c043f-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**\_несоответствие \_ списка EA с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-673">255 (0xFF)</span><span class="sxs-lookup"><span data-stu-id="c043f-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-674">Расширенные атрибуты непоследовательны.</span><span class="sxs-lookup"><span data-stu-id="c043f-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_время ожидания ожидания**</span><span class="sxs-lookup"><span data-stu-id="c043f-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-676">258 (0x102)</span><span class="sxs-lookup"><span data-stu-id="c043f-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-677">Время операции ожидания истекло.</span><span class="sxs-lookup"><span data-stu-id="c043f-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Ошибка \_ больше \_ нет \_ элементов**</span><span class="sxs-lookup"><span data-stu-id="c043f-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-679">259 (0x103)</span><span class="sxs-lookup"><span data-stu-id="c043f-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-680">Больше нет доступных данных.</span><span class="sxs-lookup"><span data-stu-id="c043f-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**Ошибка \_ при \_ копировании**</span><span class="sxs-lookup"><span data-stu-id="c043f-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="c043f-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-683">Функции копирования использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="c043f-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**\_Каталог ошибок**</span><span class="sxs-lookup"><span data-stu-id="c043f-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="c043f-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-686">Недопустимое имя каталога.</span><span class="sxs-lookup"><span data-stu-id="c043f-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**Ошибка \_ EAS \_ окончательный \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="c043f-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-689">Расширенные атрибуты не помещаются в буфер.</span><span class="sxs-lookup"><span data-stu-id="c043f-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**Ошибка \_ EA \_ File \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="c043f-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="c043f-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-692">Файл расширенного атрибута в подключенной файловой системе поврежден.</span><span class="sxs-lookup"><span data-stu-id="c043f-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**Ошибка \_ \_ таблицы EA \_ Full**</span><span class="sxs-lookup"><span data-stu-id="c043f-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="c043f-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-695">Файл расширенной таблицы атрибутов заполнен.</span><span class="sxs-lookup"><span data-stu-id="c043f-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера EA**</span><span class="sxs-lookup"><span data-stu-id="c043f-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="c043f-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-698">Указан недопустимый расширенный маркер атрибута.</span><span class="sxs-lookup"><span data-stu-id="c043f-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**Ошибка \_ EAS \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="c043f-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-701">Подключенная файловая система не поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="c043f-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ОШИБКА, \_ не \_ владелец**</span><span class="sxs-lookup"><span data-stu-id="c043f-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="c043f-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-704">Попытка освободить мьютекс, не принадлежащий вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="c043f-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**Ошибка \_ слишком \_ много \_ записей**</span><span class="sxs-lookup"><span data-stu-id="c043f-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="c043f-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-707">В семафоре создано слишком много записей.</span><span class="sxs-lookup"><span data-stu-id="c043f-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**Ошибка \_ частичной \_ копии**</span><span class="sxs-lookup"><span data-stu-id="c043f-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="c043f-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-710">Завершена только часть запроса Реадпроцессмемори или Вритепроцессмемори.</span><span class="sxs-lookup"><span data-stu-id="c043f-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**Ошибка " \_ нежесткая блокировка \_ не \_ предоставлена"**</span><span class="sxs-lookup"><span data-stu-id="c043f-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="c043f-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-713">Запрос на нежесткую блокировку отклоняется.</span><span class="sxs-lookup"><span data-stu-id="c043f-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**Ошибка \_ недопустимого \_ протокола нежесткой блокировки \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-715">301 (0x12D)</span><span class="sxs-lookup"><span data-stu-id="c043f-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-716">Система получила недопустимое подтверждение на нежесткую блокировку.</span><span class="sxs-lookup"><span data-stu-id="c043f-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**Ошибка \_ \_ слишком \_ фрагментации диска**</span><span class="sxs-lookup"><span data-stu-id="c043f-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="c043f-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-719">Том слишком фрагментирован для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="c043f-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**Ошибка \_ удаления \_ в ожидании**</span><span class="sxs-lookup"><span data-stu-id="c043f-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="c043f-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-722">Не удается открыть файл, так как он находится в процессе удаления.</span><span class="sxs-lookup"><span data-stu-id="c043f-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**Ошибка \_ несовместима \_ с \_ глобальным \_ \_ \_ параметром реестра Short Name \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="c043f-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-725">Параметры короткого имени не могут быть изменены на этом томе из-за параметра глобального реестра.</span><span class="sxs-lookup"><span data-stu-id="c043f-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_ \_ \_ \_ \_ в томе не включены короткие имена \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="c043f-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="c043f-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-728">Короткие имена не включены на этом томе.</span><span class="sxs-lookup"><span data-stu-id="c043f-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**\_несоответствие \_ потока \_ безопасности при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="c043f-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-731">Поток безопасности для данного тома находится в нестабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c043f-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="c043f-732">Запустите CHKDSK на томе.</span><span class="sxs-lookup"><span data-stu-id="c043f-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**Ошибка \_ недопустимого \_ \_ диапазона блокировки**</span><span class="sxs-lookup"><span data-stu-id="c043f-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="c043f-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-735">Запрошенная операция блокировки файла не может быть обработана из-за недопустимого диапазона байтов.</span><span class="sxs-lookup"><span data-stu-id="c043f-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_подсистема изображения ошибки \_ \_ отсутствует \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="c043f-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-738">Отсутствует подсистема, необходимая для поддержки типа образа.</span><span class="sxs-lookup"><span data-stu-id="c043f-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID уведомления об ОШИБКе \_ \_ \_ уже \_ определен**</span><span class="sxs-lookup"><span data-stu-id="c043f-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="c043f-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-741">С указанным файлом уже связан GUID уведомления.</span><span class="sxs-lookup"><span data-stu-id="c043f-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**Ошибка \_ недопустимого \_ \_ обработчика исключений**</span><span class="sxs-lookup"><span data-stu-id="c043f-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="c043f-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-744">Обнаружена недопустимая подсистема обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="c043f-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**Ошибка при \_ дублировании \_ привилегий**</span><span class="sxs-lookup"><span data-stu-id="c043f-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="c043f-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-747">Для токена указаны дублирующиеся привилегии.</span><span class="sxs-lookup"><span data-stu-id="c043f-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**Ошибка \_ не \_ \_ обработано диапазонов**</span><span class="sxs-lookup"><span data-stu-id="c043f-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="c043f-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-750">Не удалось обработать диапазоны для указанной операции.</span><span class="sxs-lookup"><span data-stu-id="c043f-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**Ошибка \_ не \_ разрешена \_ в \_ системном \_ файле**</span><span class="sxs-lookup"><span data-stu-id="c043f-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="c043f-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-753">Операция не разрешена для внутреннего файла файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c043f-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**\_дисковые ресурсы с ошибками \_ \_ исчерпаны**</span><span class="sxs-lookup"><span data-stu-id="c043f-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-755">314 (0x13A)</span><span class="sxs-lookup"><span data-stu-id="c043f-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-756">Физические ресурсы этого диска исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="c043f-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**Ошибка \_ недопустимого \_ токена**</span><span class="sxs-lookup"><span data-stu-id="c043f-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="c043f-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-759">Недопустимый токен, представляющий данные.</span><span class="sxs-lookup"><span data-stu-id="c043f-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**Функция устройства с ОШИБКАми \_ \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="c043f-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-762">Устройство не поддерживает функцию команды.</span><span class="sxs-lookup"><span data-stu-id="c043f-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**Ошибка \_ MR \_ \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="c043f-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="c043f-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-765">Системе не удается найти текст сообщения с номером 0x %1 в файле сообщений для %2.</span><span class="sxs-lookup"><span data-stu-id="c043f-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_область ошибок \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="c043f-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="c043f-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-768">Указанная область не найдена.</span><span class="sxs-lookup"><span data-stu-id="c043f-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**Ошибка \_ НЕопределенной \_ области**</span><span class="sxs-lookup"><span data-stu-id="c043f-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="c043f-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-771">Указанная Централизованная политика доступа не определена на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c043f-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**Ошибка \_ недопустимого \_ ограничения**</span><span class="sxs-lookup"><span data-stu-id="c043f-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-773">320 (0x140)</span><span class="sxs-lookup"><span data-stu-id="c043f-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-774">Централизованная политика доступа, полученная из Active Directory, недопустима.</span><span class="sxs-lookup"><span data-stu-id="c043f-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**устройство с ОШИБКАми \_ \_ недоступно**</span><span class="sxs-lookup"><span data-stu-id="c043f-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="c043f-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-777">Устройство недоступно.</span><span class="sxs-lookup"><span data-stu-id="c043f-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**устройство с ОШИБКАми — \_ \_ нет \_ ресурсов**</span><span class="sxs-lookup"><span data-stu-id="c043f-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="c043f-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-780">На целевом устройстве недостаточно ресурсов для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="c043f-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**Ошибка \_ \_ контрольной суммы данных об ошибках \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="c043f-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-783">Произошла ошибка контрольной суммы целостности данных.</span><span class="sxs-lookup"><span data-stu-id="c043f-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="c043f-784">Данные в файловом потоке повреждены.</span><span class="sxs-lookup"><span data-stu-id="c043f-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**Ошибка при \_ ВЗАИМОсмешанных \_ \_ \_ операциях ядра EA**</span><span class="sxs-lookup"><span data-stu-id="c043f-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-786">324 (0x144)</span><span class="sxs-lookup"><span data-stu-id="c043f-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-787">Была предпринята попытка изменить как ядро, так и нормальный Расширенный атрибут (EA) в одной операции.</span><span class="sxs-lookup"><span data-stu-id="c043f-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**Ошибка \_ \_ Trim на уровне файлов \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-789">326 (0x146)</span><span class="sxs-lookup"><span data-stu-id="c043f-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-790">Устройство не поддерживает УСЕЧЕНИЕ на уровне файлов.</span><span class="sxs-lookup"><span data-stu-id="c043f-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_ \_ нарушение выравнивания по СМЕЩЕНию ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="c043f-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-793">В команде указано смещение данных, которое не соответствует детализации или выравниванию устройства.</span><span class="sxs-lookup"><span data-stu-id="c043f-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**Ошибка \_ недопустимого \_ поля \_ в \_ \_ списке параметров**</span><span class="sxs-lookup"><span data-stu-id="c043f-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="c043f-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-796">В списке параметров команды указано недопустимое поле.</span><span class="sxs-lookup"><span data-stu-id="c043f-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**Ошибка \_ при выполнении операции \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-798">329 (0x149)</span><span class="sxs-lookup"><span data-stu-id="c043f-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-799">В настоящее время выполняется операция с устройством.</span><span class="sxs-lookup"><span data-stu-id="c043f-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**Ошибка \_ неправильного \_ \_ пути к устройству**</span><span class="sxs-lookup"><span data-stu-id="c043f-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-801">330 (0x14A)</span><span class="sxs-lookup"><span data-stu-id="c043f-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-802">Предпринята попытка отправить команду через недопустимый путь к целевому устройству.</span><span class="sxs-lookup"><span data-stu-id="c043f-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**Ошибка \_ слишком \_ большого числа \_ дескрипторов**</span><span class="sxs-lookup"><span data-stu-id="c043f-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-804">331 (0x14B)</span><span class="sxs-lookup"><span data-stu-id="c043f-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-805">В команде указано число дескрипторов, превышающих максимальное поддерживаемое устройством.</span><span class="sxs-lookup"><span data-stu-id="c043f-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**Ошибка \_ очистки \_ данных \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="c043f-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-807">332 (0x14C)</span><span class="sxs-lookup"><span data-stu-id="c043f-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-808">Очистка в указанном файле отключена.</span><span class="sxs-lookup"><span data-stu-id="c043f-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**Ошибка \_ не является \_ избыточным \_ хранилищем**</span><span class="sxs-lookup"><span data-stu-id="c043f-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-810">333 (0x14D)</span><span class="sxs-lookup"><span data-stu-id="c043f-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-811">Устройство хранения данных не обеспечивает избыточность.</span><span class="sxs-lookup"><span data-stu-id="c043f-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_резидентный \_ файл ошибок \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-813">334 (0x14E)</span><span class="sxs-lookup"><span data-stu-id="c043f-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-814">Операция не поддерживается для резидентных файлов.</span><span class="sxs-lookup"><span data-stu-id="c043f-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**сжатый файл с ОШИБКАми \_ \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-816">335 (0x14F)</span><span class="sxs-lookup"><span data-stu-id="c043f-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-817">Операция не поддерживается для сжатого файла.</span><span class="sxs-lookup"><span data-stu-id="c043f-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_Каталог ошибок \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c043f-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="c043f-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-820">Операция не поддерживается в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c043f-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**Ошибка \_ \_ чтения \_ из \_ копии**</span><span class="sxs-lookup"><span data-stu-id="c043f-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="c043f-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-823">Не удалось прочитать указанную копию запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="c043f-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**Ошибка \_ при \_ перезагрузке "Недействие" \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-825">350 (0x15E)</span><span class="sxs-lookup"><span data-stu-id="c043f-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-826">Не было предпринято никаких действий, так как требуется перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="c043f-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**Ошибка \_ при \_ завершении работы**</span><span class="sxs-lookup"><span data-stu-id="c043f-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-828">351 (0x15F)</span><span class="sxs-lookup"><span data-stu-id="c043f-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-829">Сбой операции завершения работы.</span><span class="sxs-lookup"><span data-stu-id="c043f-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**Ошибка \_ при \_ перезапуске**</span><span class="sxs-lookup"><span data-stu-id="c043f-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="c043f-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-832">Сбой операции перезапуска.</span><span class="sxs-lookup"><span data-stu-id="c043f-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ОШИБОК \_ \_ достигнуто максимальное число сеансов \_**</span><span class="sxs-lookup"><span data-stu-id="c043f-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="c043f-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-835">Достигнуто максимальное число сеансов.</span><span class="sxs-lookup"><span data-stu-id="c043f-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**\_режим потока \_ ошибок \_ уже является \_ фоновым**</span><span class="sxs-lookup"><span data-stu-id="c043f-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="c043f-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-838">Поток уже находится в режиме фоновой обработки.</span><span class="sxs-lookup"><span data-stu-id="c043f-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_режим потока \_ ошибок \_ не является \_ фоновым**</span><span class="sxs-lookup"><span data-stu-id="c043f-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="c043f-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-841">Поток не находится в режиме фоновой обработки.</span><span class="sxs-lookup"><span data-stu-id="c043f-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**\_режим обработки \_ ошибок \_ уже является \_ фоновым**</span><span class="sxs-lookup"><span data-stu-id="c043f-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-843">402 (0x192)</span><span class="sxs-lookup"><span data-stu-id="c043f-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-844">Процесс уже находится в режиме фоновой обработки.</span><span class="sxs-lookup"><span data-stu-id="c043f-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**\_режим обработки \_ ошибок \_ не является \_ фоновым**</span><span class="sxs-lookup"><span data-stu-id="c043f-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-846">403 (0x193)</span><span class="sxs-lookup"><span data-stu-id="c043f-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-847">Процесс не находится в режиме фоновой обработки.</span><span class="sxs-lookup"><span data-stu-id="c043f-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c043f-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Ошибка \_ недопустимого \_ адреса**</span><span class="sxs-lookup"><span data-stu-id="c043f-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c043f-849">487 (0x1E7)</span><span class="sxs-lookup"><span data-stu-id="c043f-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="c043f-850">Попытка доступа к недопустимому адресу.</span><span class="sxs-lookup"><span data-stu-id="c043f-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="c043f-851">Требования</span><span class="sxs-lookup"><span data-stu-id="c043f-851">Requirements</span></span>



| <span data-ttu-id="c043f-852">Требование</span><span class="sxs-lookup"><span data-stu-id="c043f-852">Requirement</span></span> | <span data-ttu-id="c043f-853">Значение</span><span class="sxs-lookup"><span data-stu-id="c043f-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c043f-854">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c043f-854">Minimum supported client</span></span><br/> | <span data-ttu-id="c043f-855">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c043f-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c043f-856">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c043f-856">Minimum supported server</span></span><br/> | <span data-ttu-id="c043f-857">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c043f-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c043f-858">Header</span><span class="sxs-lookup"><span data-stu-id="c043f-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="c043f-859"><dt>WinError. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c043f-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c043f-860">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c043f-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c043f-861">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="c043f-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




