---
title: Значения, возвращаемые BITS
description: Файл Битсмсг. h содержит следующие константы возвращаемого значения.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- БИТЫ ошибок
- БИТЫ ошибок, коды
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987756"
---
# <a name="bits-return-values"></a><span data-ttu-id="a50da-105">Значения, возвращаемые BITS</span><span class="sxs-lookup"><span data-stu-id="a50da-105">BITS Return Values</span></span>

<span data-ttu-id="a50da-106">Файл Битсмсг. h содержит следующие константы возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a50da-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="a50da-107">Константы представляют возвращаемые значения, создаваемые BITS, и возвращаемые значения HTTP, которые захватывают биты.</span><span class="sxs-lookup"><span data-stu-id="a50da-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="a50da-108">Все остальные возвращаемые значения — это COM, RPC или преобразованные возвращаемые значения Windows (BITS использует значение [HRESULT из макроса \_ \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) для преобразования возвращаемых значений Windows в значения HRESULT).</span><span class="sxs-lookup"><span data-stu-id="a50da-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="a50da-109">Обратите внимание, что файл Битсмсг. h содержит дополнительные возвращаемые значения, не указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="a50da-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="a50da-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Частично \_ завершено: BG (0x00200017)</span><span class="sxs-lookup"><span data-stu-id="a50da-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-111">Переданное подмножество файлов задания успешно передано до вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="a50da-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="a50da-112">Были удалены те, которые не были завершены.</span><span class="sxs-lookup"><span data-stu-id="a50da-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ не \_ удается \_ удалить \_ файлы (0x0020001A)</span><span class="sxs-lookup"><span data-stu-id="a50da-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-114">Не удалось удалить все временные файлы, связанные с заданием.</span><span class="sxs-lookup"><span data-stu-id="a50da-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ переопределяется \_ \_ политикой (0x00200055)</span><span class="sxs-lookup"><span data-stu-id="a50da-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-116">Настройка конфигурации успешно сохранена, но предпочтение не будет использоваться, так как настроенный параметр групповая политика переопределяет настройки.</span><span class="sxs-lookup"><span data-stu-id="a50da-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ не \_ найдено (0x80200001)</span><span class="sxs-lookup"><span data-stu-id="a50da-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-118">Запрошенное задание не найдено.</span><span class="sxs-lookup"><span data-stu-id="a50da-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_ \_ Недопустимое состояние BG E \_ (0x80200002)</span><span class="sxs-lookup"><span data-stu-id="a50da-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-120">Запрошенное действие запрещено в текущем состоянии задания.</span><span class="sxs-lookup"><span data-stu-id="a50da-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)</span><span class="sxs-lookup"><span data-stu-id="a50da-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-122">Задание должно содержать один или несколько файлов, прежде чем можно будет возобновить задание.</span><span class="sxs-lookup"><span data-stu-id="a50da-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_Файл BG \_ E \_ \_ недоступен (0x80200004)</span><span class="sxs-lookup"><span data-stu-id="a50da-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-124">Сведения о файле недоступны, так как ошибка не связана с локальным или удаленным файлом.</span><span class="sxs-lookup"><span data-stu-id="a50da-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Протокол BG \_ E \_ \_ недоступен (0x80200005)</span><span class="sxs-lookup"><span data-stu-id="a50da-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-126">Сведения о протоколе недоступны, так как ошибка не связана с указанным Протоколом перемещения.</span><span class="sxs-lookup"><span data-stu-id="a50da-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>\_ \_ Место назначения BG E \_ заблокировано (0x8020000D)</span><span class="sxs-lookup"><span data-stu-id="a50da-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-128">Целевой том файловой системы, указанный в имени локального файла, заблокирован.</span><span class="sxs-lookup"><span data-stu-id="a50da-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>\_ \_ Изменение тома BG E \_ (0x8020000E)</span><span class="sxs-lookup"><span data-stu-id="a50da-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-130">Изменился целевой том, указанный в имени локального файла.</span><span class="sxs-lookup"><span data-stu-id="a50da-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="a50da-131">Например, исходная дискета заменена на другой гибкий диск.</span><span class="sxs-lookup"><span data-stu-id="a50da-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_ \_ Недоступная информация об ошибке BG E \_ \_ (0x8020000F)</span><span class="sxs-lookup"><span data-stu-id="a50da-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-133">Сведения об ошибках доступны, только если состояние задания — \_ \_ Ошибка состояния задания BG \_ .</span><span class="sxs-lookup"><span data-stu-id="a50da-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="a50da-134">Сведения об ошибке недоступны после того, как служба BITS начнет передачу данных задания или завершает работу клиента.</span><span class="sxs-lookup"><span data-stu-id="a50da-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>\_Сеть BG \_ E \_ отключена (0x80200010)</span><span class="sxs-lookup"><span data-stu-id="a50da-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-136">Сетевой адаптер неактивен или отключен.</span><span class="sxs-lookup"><span data-stu-id="a50da-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="a50da-137">Все задания помещаются в \_ \_ \_ состояние промежуточной ошибки состояния задания BG \_ .</span><span class="sxs-lookup"><span data-stu-id="a50da-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ отсутствует \_ \_ Размер файла (0x80200011)</span><span class="sxs-lookup"><span data-stu-id="a50da-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-139">Сервер не возвратил размер файла.</span><span class="sxs-lookup"><span data-stu-id="a50da-139">The server did not return the file size.</span></span> <span data-ttu-id="a50da-140">Служба BITS передает только статическое содержимое и требует, чтобы HTTP-сервер возвращал заголовок Content-Length.</span><span class="sxs-lookup"><span data-stu-id="a50da-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="a50da-141">Запрос на перемещение завершается неудачей, если URL-адрес указывает на динамическое содержимое.</span><span class="sxs-lookup"><span data-stu-id="a50da-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ Недостаточная \_ Поддержка HTTP BG E \_ (0x80200012)</span><span class="sxs-lookup"><span data-stu-id="a50da-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-143">Сервер не поддерживает протокол HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="a50da-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_ \_ Недостаточная \_ Поддержка диапазона BG E \_ (0x80200013)</span><span class="sxs-lookup"><span data-stu-id="a50da-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-145">Сервер не поддерживает заголовок Content-Range.</span><span class="sxs-lookup"><span data-stu-id="a50da-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="a50da-146">Как правило, эта ошибка возникает при попытке загрузить динамическое содержимое.</span><span class="sxs-lookup"><span data-stu-id="a50da-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="a50da-147">Эту ошибку также можно получить, если промежуточный прокси-сервер удаляет заголовок Content-Range или Content-Length.</span><span class="sxs-lookup"><span data-stu-id="a50da-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>\_ \_ Удаленное \_ \_ неподдерживаемое "BG E" (0x80200014)</span><span class="sxs-lookup"><span data-stu-id="a50da-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-149">Удаленное использование BITS не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a50da-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="a50da-150">Дополнительные сведения см. в разделе [Пользователи и сетевые подключения](users-and-network-connections.md).</span><span class="sxs-lookup"><span data-stu-id="a50da-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="a50da-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ — \_ новое \_ \_ сопоставление различий \_ (0x80200015)</span><span class="sxs-lookup"><span data-stu-id="a50da-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-152">Сопоставление сетевых дисков для локального файла отличается от сопоставления для текущего владельца, чем для предыдущего владельца.</span><span class="sxs-lookup"><span data-stu-id="a50da-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ новый \_ владелец \_ нет \_ \_ доступа к файлам (0x80200016)</span><span class="sxs-lookup"><span data-stu-id="a50da-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-154">У нового владельца недостаточно разрешений для временных файлов заданий.</span><span class="sxs-lookup"><span data-stu-id="a50da-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Слишком большой список прокси-серверов BG E \_ \_ \_ (0x80200018)</span><span class="sxs-lookup"><span data-stu-id="a50da-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-156">Список прокси-серверов HTTP слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="a50da-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="a50da-157">Размер списка не должен превышать 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="a50da-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_ \_ Слишком большой список обхода прокси-сервера BG E \_ \_ \_ \_ (0x80200019)</span><span class="sxs-lookup"><span data-stu-id="a50da-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-159">Список обхода прокси-сервера HTTP слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="a50da-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="a50da-160">Размер списка не должен превышать 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="a50da-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>\_ \_ Слишком \_ много файлов BG E \_ (0x8020001C)</span><span class="sxs-lookup"><span data-stu-id="a50da-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-162">В задание отправки нельзя добавить более одного файла.</span><span class="sxs-lookup"><span data-stu-id="a50da-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_ \_ Изменение ЛОКАЛЬНОГО файла BG E \_ \_ (0x8020001D)</span><span class="sxs-lookup"><span data-stu-id="a50da-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-164">Содержимое локального файла изменилось после начала процесса перемещения.</span><span class="sxs-lookup"><span data-stu-id="a50da-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="a50da-165">Содержимое локального файла не может измениться после начала процесса передачи для задания отправки или отправки-ответа.</span><span class="sxs-lookup"><span data-stu-id="a50da-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>\_ \_ Слишком большой BG E \_ (0x80200020)</span><span class="sxs-lookup"><span data-stu-id="a50da-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-167">Размер файла отправки превышает максимально допустимый размер отправки, указанный на сервере.</span><span class="sxs-lookup"><span data-stu-id="a50da-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_ \_ \_ Слишком длинная строка BG E \_ (0x80200021)</span><span class="sxs-lookup"><span data-stu-id="a50da-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-169">Указана слишком длинная строка.</span><span class="sxs-lookup"><span data-stu-id="a50da-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_Несоответствие \_ протокола клиентского сервера BG E \_ \_ \_ (0x80200022)</span><span class="sxs-lookup"><span data-stu-id="a50da-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-171">Клиенту и серверу не удалось согласовать протокол, используемый для задания отправки.</span><span class="sxs-lookup"><span data-stu-id="a50da-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_Сервер BG E с \_ \_ \_ включенным выполнением (0x80200023)</span><span class="sxs-lookup"><span data-stu-id="a50da-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-173">В виртуальном каталоге IIS, связанном с заданием, включены разрешения на выполнение скриптов или выполнения.</span><span class="sxs-lookup"><span data-stu-id="a50da-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="a50da-174">Чтобы передать файлы в виртуальный каталог, отключите разрешения скрипта и выполнения для виртуального каталога.</span><span class="sxs-lookup"><span data-stu-id="a50da-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>\_ \_ Слишком большое имя пользователя BG E \_ \_ (0x80200025)</span><span class="sxs-lookup"><span data-stu-id="a50da-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-176">Длина имени пользователя не может превышать 300 символов.</span><span class="sxs-lookup"><span data-stu-id="a50da-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>\_ \_ Слишком большой пароль BG E \_ \_ (0x80200026)</span><span class="sxs-lookup"><span data-stu-id="a50da-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-178">Длина пароля не может превышать 65535 символов.</span><span class="sxs-lookup"><span data-stu-id="a50da-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>\_ \_ Недопустимый \_ целевой объект проверки подлинности BG E \_ (0x80200027)</span><span class="sxs-lookup"><span data-stu-id="a50da-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-180">Указан недопустимый целевой объект проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a50da-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>\_ \_ Недопустимый \_ Схема проверки подлинности BG E \_ (0x80200028)</span><span class="sxs-lookup"><span data-stu-id="a50da-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-182">Указана недопустимая схема проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a50da-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E \_ : недопустимый \_ диапазон (0x8020002B)</span><span class="sxs-lookup"><span data-stu-id="a50da-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-184">Указанный диапазон байтов недопустим.</span><span class="sxs-lookup"><span data-stu-id="a50da-184">The specified byte range is invalid.</span></span> <span data-ttu-id="a50da-185">Диапазон байтов должен существовать в указанном удаленном файле.</span><span class="sxs-lookup"><span data-stu-id="a50da-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_Перекрывающиеся \_ \_ диапазоны BG E (0x8020002C)</span><span class="sxs-lookup"><span data-stu-id="a50da-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-187">Список диапазонов байтов содержит перекрывающиеся или дублирующиеся диапазоны, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a50da-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ заблокировано \_ \_ политикой (0x8020003E)</span><span class="sxs-lookup"><span data-stu-id="a50da-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-189">Параметры групповая политика не позволяют выполнять фоновые задания в данный момент.</span><span class="sxs-lookup"><span data-stu-id="a50da-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="a50da-190">Дополнительные сведения см. в описании политики [максинтернетбандвидс](group-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="a50da-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E \_ недопустимые \_ \_ сведения о прокси (0x8020003F)</span><span class="sxs-lookup"><span data-stu-id="a50da-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-192">Ошибка времени выполнения, указывающая на список прокси-серверов или список обхода прокси-сервера, указанный с помощью метода [**использованием метода ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) , недопустим.</span><span class="sxs-lookup"><span data-stu-id="a50da-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ недопустимые \_ учетные данные (0x80200040)</span><span class="sxs-lookup"><span data-stu-id="a50da-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-194">Недопустимый формат предоставленных учетных данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="a50da-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_ \_ Удалена запись BG E \_ (0x80200042)</span><span class="sxs-lookup"><span data-stu-id="a50da-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-196">Запись кэша удалена.</span><span class="sxs-lookup"><span data-stu-id="a50da-196">The cache record has been deleted.</span></span> <span data-ttu-id="a50da-197">Попытка обновить ее была прервана.</span><span class="sxs-lookup"><span data-stu-id="a50da-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_ \_ Ошибка UPnP BG E \_ (0x80200045)</span><span class="sxs-lookup"><span data-stu-id="a50da-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-199">Произошла ошибка универсального самонастраивающийся (UPnP).</span><span class="sxs-lookup"><span data-stu-id="a50da-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="a50da-200">Проверьте устройство шлюза Интернета.</span><span class="sxs-lookup"><span data-stu-id="a50da-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>\_ \_ Недоступен одноранговый кэшированный BG E \_ (0x80200047)</span><span class="sxs-lookup"><span data-stu-id="a50da-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-202">Одноранговое кэширование отключено.</span><span class="sxs-lookup"><span data-stu-id="a50da-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ бусикачерекорд (0x80200048)</span><span class="sxs-lookup"><span data-stu-id="a50da-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-204">Запись кэша используется и не может быть изменена или удалена.</span><span class="sxs-lookup"><span data-stu-id="a50da-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="a50da-205">Повторите попытку через несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="a50da-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>\_ \_ Превышено \_ Максимальное количество \_ заданий \_ на \_ пользователя: BG (0x80200049)</span><span class="sxs-lookup"><span data-stu-id="a50da-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-207">Число заданий для пользователя превысило предел для задания на пользователя, заданный параметром групповая политика Maxjobspermachine.</span><span class="sxs-lookup"><span data-stu-id="a50da-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>\_ \_ \_ Максимальное количество \_ заданий \_ в одном \_ компьютере (0x80200050): BG</span><span class="sxs-lookup"><span data-stu-id="a50da-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-209">Число заданий на компьютере превысило предел для заданий на компьютер, заданный параметром групповая политика MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="a50da-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>\_ \_ Слишком \_ много \_ файлов \_ в \_ задании BG (0x80200051)</span><span class="sxs-lookup"><span data-stu-id="a50da-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-211">Число файлов для задания превысило ограничение на количество файлов заданий, заданное параметром групповая политика MaxFilesPerJob.</span><span class="sxs-lookup"><span data-stu-id="a50da-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>\_ \_ Слишком \_ много \_ диапазонов \_ в \_ файле (0x80200052) BG E</span><span class="sxs-lookup"><span data-stu-id="a50da-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-213">Число диапазонов для файла превысило предел для диапазона файлов, заданный параметром групповая политика MaxRangesPerFile.</span><span class="sxs-lookup"><span data-stu-id="a50da-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>\_ \_ Сбой проверки BG E \_ (0x80200053)</span><span class="sxs-lookup"><span data-stu-id="a50da-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-215">Приложение запросило данные с веб-сайта, но ответ был недопустимым.</span><span class="sxs-lookup"><span data-stu-id="a50da-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="a50da-216">Для получения дополнительных сведений используйте Просмотр событий для просмотра журнала приложений \\ Microsoft \\ Windows \\ BITS — \\ Журнал операций клиента.</span><span class="sxs-lookup"><span data-stu-id="a50da-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>\_ \_ Максдовнлоад \_ тайм-аута BG E (0x80200054)</span><span class="sxs-lookup"><span data-stu-id="a50da-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-218">Время ожидания BITS при скачивании задания.</span><span class="sxs-lookup"><span data-stu-id="a50da-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="a50da-219">Загрузка не была завершена в течение максимального времени загрузки, заданного для задания или параметра групповая политика Максдовнлоадтиме.</span><span class="sxs-lookup"><span data-stu-id="a50da-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 400 (0x80190190)</span><span class="sxs-lookup"><span data-stu-id="a50da-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-221">Серверу не удалось обработать запрос на перемещение из-за недопустимого синтаксиса имени удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="a50da-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 401 (0x80190191)</span><span class="sxs-lookup"><span data-stu-id="a50da-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-223">У пользователя нет разрешения на доступ к удаленному файлу.</span><span class="sxs-lookup"><span data-stu-id="a50da-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="a50da-224">Запрошенный ресурс требует проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="a50da-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 404 (0x80190194)</span><span class="sxs-lookup"><span data-stu-id="a50da-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-226">Запрошенный URL-адрес не существует на сервере.</span><span class="sxs-lookup"><span data-stu-id="a50da-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="a50da-227">В IIS 7 Эта ошибка может означать, что</span><span class="sxs-lookup"><span data-stu-id="a50da-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="a50da-228">Отправка BITS не включена в виртуальном каталоге (vdir) на сервере.</span><span class="sxs-lookup"><span data-stu-id="a50da-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="a50da-229">, Что размер передачи превышает максимальный предел загрузки (Дополнительные сведения см. в описании свойства расширения IIS [**битсмаксимумуплоадсизе**](bits-iis-extension-properties.md) ).</span><span class="sxs-lookup"><span data-stu-id="a50da-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="a50da-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 407 (0x80190197)</span><span class="sxs-lookup"><span data-stu-id="a50da-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-231">У пользователя нет разрешения на доступ к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="a50da-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="a50da-232">Прокси-сервер требует проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="a50da-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 414 (0x8019019E)</span><span class="sxs-lookup"><span data-stu-id="a50da-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-234">Серверу не удается обработать запрос на перемещение.</span><span class="sxs-lookup"><span data-stu-id="a50da-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="a50da-235">Длина универсального кода ресурса (URI) в имени удаленного файла превышает длину, которую может интерпретировать сервер.</span><span class="sxs-lookup"><span data-stu-id="a50da-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 501 (0x801901F5)</span><span class="sxs-lookup"><span data-stu-id="a50da-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-237">Сервер не поддерживает функции, необходимые для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="a50da-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="a50da-238">В IIS 6 Эта ошибка означает, что отправка BITS не включена в виртуальном каталоге (vdir) на сервере.</span><span class="sxs-lookup"><span data-stu-id="a50da-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 503 (0x801901F7)</span><span class="sxs-lookup"><span data-stu-id="a50da-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-240">Служба временно перегружена и не может обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="a50da-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="a50da-241">Возобновите задание позже.</span><span class="sxs-lookup"><span data-stu-id="a50da-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 504 (0x801901F8)</span><span class="sxs-lookup"><span data-stu-id="a50da-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-243">Истекло время ожидания запроса на перемещение при ожидании шлюза.</span><span class="sxs-lookup"><span data-stu-id="a50da-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="a50da-244">Возобновите задание позже.</span><span class="sxs-lookup"><span data-stu-id="a50da-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="a50da-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E \_ , \_ Ошибка HTTP \_ 505 (0x801901F9)</span><span class="sxs-lookup"><span data-stu-id="a50da-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="a50da-246">Сервер не поддерживает версию протокола HTTP, указанную в имени удаленного файла.</span><span class="sxs-lookup"><span data-stu-id="a50da-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="a50da-247">Файл заголовка Битсмсг. h содержит дополнительные возвращаемые значения HTTP, не указанные выше, которые используются службой BITS для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="a50da-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="a50da-248">Дополнительные сведения об этих и других возвращаемых значениях HTTP см. в спецификации RFC 2616, приведенной в статье о задачах веб-проектирования в [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .</span><span class="sxs-lookup"><span data-stu-id="a50da-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 