---
title: Коды ошибок маршрутизации и удаленного доступа
description: Следующие коды ошибок маршрутизации и удаленного доступа (RRAS) определены в расеррор. h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15966d009f0690a1db24c21460da5b9e08a38347
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071305"
---
# <a name="routing-and-remote-access-error-codes"></a><span data-ttu-id="90bd5-103">Коды ошибок маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="90bd5-103">Routing and Remote Access Error Codes</span></span>

<span data-ttu-id="90bd5-104">Следующие коды ошибок маршрутизации и удаленного доступа (RRAS) определены в расеррор. h.</span><span class="sxs-lookup"><span data-stu-id="90bd5-104">The following Routing and Remote Access (RRAS) API error codes are defined in raserror.h.</span></span> <span data-ttu-id="90bd5-105">Все коды ошибок поддерживаются в Windows 2000 или более поздних версиях Windows, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="90bd5-105">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90bd5-106">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="90bd5-106">Return code/value</span></span></th>
<th><span data-ttu-id="90bd5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="90bd5-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <span data-ttu-id="90bd5-108"><dt><strong>Ожидается</strong></dt> <dt>600</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-108"><dt><strong>PENDING</strong></dt> <dt>600</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-109">Операция находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="90bd5-109">An operation is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <span data-ttu-id="90bd5-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-111">Указан недопустимый маркер порта.</span><span class="sxs-lookup"><span data-stu-id="90bd5-111">The port handle supplied is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <span data-ttu-id="90bd5-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-113">Указанный порт уже открыт.</span><span class="sxs-lookup"><span data-stu-id="90bd5-113">The specified port is already open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <span data-ttu-id="90bd5-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-115">Указанный буфер слишком мал.</span><span class="sxs-lookup"><span data-stu-id="90bd5-115">The buffer supplied is too small.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <span data-ttu-id="90bd5-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-117">Указаны неправильные сведения о портах.</span><span class="sxs-lookup"><span data-stu-id="90bd5-117">The port information specified is incorrect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <span data-ttu-id="90bd5-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-119">Не удается задать указанные сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="90bd5-119">The port information specified cannot be set.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-120">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-120">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <span data-ttu-id="90bd5-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-122">Указанный порт не подключен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-122">The port specified is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <span data-ttu-id="90bd5-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-124">Обнаружено недопустимое событие.</span><span class="sxs-lookup"><span data-stu-id="90bd5-124">An event that is not valid was detected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-125">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-125">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <span data-ttu-id="90bd5-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-127">Указанное устройство не существует.</span><span class="sxs-lookup"><span data-stu-id="90bd5-127">The specified device does not exist.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <span data-ttu-id="90bd5-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-129">Указанный тип устройства не существует.</span><span class="sxs-lookup"><span data-stu-id="90bd5-129">The specified device type does not exist.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <span data-ttu-id="90bd5-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-131">Указан недопустимый буфер.</span><span class="sxs-lookup"><span data-stu-id="90bd5-131">The buffer supplied is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <span data-ttu-id="90bd5-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-133">Указан недоступный маршрут.</span><span class="sxs-lookup"><span data-stu-id="90bd5-133">A route was specified that is not available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-134">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-134">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <span data-ttu-id="90bd5-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-136">Указанный маршрут не выделен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-136">The specified route is not allocated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <span data-ttu-id="90bd5-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-138">Указано недопустимое сжатие.</span><span class="sxs-lookup"><span data-stu-id="90bd5-138">The specified compression is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-139">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-139">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <span data-ttu-id="90bd5-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-141">Недостаточно доступных буферов.</span><span class="sxs-lookup"><span data-stu-id="90bd5-141">There were insufficient buffers available.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <span data-ttu-id="90bd5-142"><dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-142"><dt><strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-143">Указанный порт не найден.</span><span class="sxs-lookup"><span data-stu-id="90bd5-143">The specified port was not found.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <span data-ttu-id="90bd5-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-145">Ожидается асинхронный запрос.</span><span class="sxs-lookup"><span data-stu-id="90bd5-145">An asynchronous request is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <span data-ttu-id="90bd5-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-147">Указанный порт или устройство уже отключены.</span><span class="sxs-lookup"><span data-stu-id="90bd5-147">The specified port or device is already disconnecting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <span data-ttu-id="90bd5-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-149">Указанный порт не открыт.</span><span class="sxs-lookup"><span data-stu-id="90bd5-149">The specified port is not open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <span data-ttu-id="90bd5-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-151">Указанный порт отключен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-151">The specified port is disconnected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <span data-ttu-id="90bd5-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-153">Не удалось определить конечные точки.</span><span class="sxs-lookup"><span data-stu-id="90bd5-153">No endpoints could be determined.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-154">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-154">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <span data-ttu-id="90bd5-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-156">Не удается открыть указанный файл телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="90bd5-156">Cannot open the specified phone book file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <span data-ttu-id="90bd5-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-158">Не удается загрузить указанный файл телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="90bd5-158">Cannot load the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <span data-ttu-id="90bd5-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-160">Не удается найти указанную запись телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="90bd5-160">Cannot find the specified phone book entry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <span data-ttu-id="90bd5-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-162">Не удается выполнить запись в указанный файл телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="90bd5-162">Cannot write to the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <span data-ttu-id="90bd5-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-164">В указанной телефонной книге обнаружена недопустимая информация.</span><span class="sxs-lookup"><span data-stu-id="90bd5-164">Information found in the specified phone book is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <span data-ttu-id="90bd5-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-166">Не удалось загрузить строку.</span><span class="sxs-lookup"><span data-stu-id="90bd5-166">A string could not be loaded.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-167">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-167">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <span data-ttu-id="90bd5-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-169">Не удается найти указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="90bd5-169">Cannot find the specified key.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <span data-ttu-id="90bd5-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-171">Указанный порт был отключен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-171">The specified port was disconnected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <span data-ttu-id="90bd5-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-173">Указанный порт был отключен удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-173">The specified port was disconnected by the remote computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <span data-ttu-id="90bd5-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-175">Указанный порт был отключен из-за сбоя оборудования.</span><span class="sxs-lookup"><span data-stu-id="90bd5-175">The specified port was disconnected due to hardware failure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <span data-ttu-id="90bd5-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-177">Указанный порт отключен пользователем.</span><span class="sxs-lookup"><span data-stu-id="90bd5-177">The specified port was disconnected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <span data-ttu-id="90bd5-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-179">Неверный размер структуры.</span><span class="sxs-lookup"><span data-stu-id="90bd5-179">Incorrect structure size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <span data-ttu-id="90bd5-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-181">Указанный порт уже используется или не настроен для удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-181">The specified port is already in use or is not configured for remote access dial-out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <span data-ttu-id="90bd5-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-183">Не удалось зарегистрировать компьютер в удаленной сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-183">Your computer could not be registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-184">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-184">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <span data-ttu-id="90bd5-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-186">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="90bd5-186">An unknown error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <span data-ttu-id="90bd5-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-188">К указанному порту подключено неправильное устройство.</span><span class="sxs-lookup"><span data-stu-id="90bd5-188">The wrong device is attached to the specified port.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <span data-ttu-id="90bd5-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-190">Обнаружена строка, которую не удалось преобразовать.</span><span class="sxs-lookup"><span data-stu-id="90bd5-190">A string was detected that could not be converted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-191">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-191">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <span data-ttu-id="90bd5-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-193">Истекло время ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="90bd5-193">The request has timed out.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <span data-ttu-id="90bd5-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-195">Нет доступной асинхронной сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-195">No asynchronous net is available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-196">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-196">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <span data-ttu-id="90bd5-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-198">Произошла ошибка при вовлечении NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-198">An error has occurred involving NetBIOS.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-199">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-199">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <span data-ttu-id="90bd5-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-201">сервер не может выделить ресурсы NetBIOS, необходимые для поддержки клиента.</span><span class="sxs-lookup"><span data-stu-id="90bd5-201">he server cannot allocate NetBIOS resources needed to support the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-202">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-202">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <span data-ttu-id="90bd5-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-204">Одно из NetBIOS-имен вашего компьютера уже зарегистрировано в удаленной сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-204">One of your computer's NetBIOS names is already registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-205">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-205">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <span data-ttu-id="90bd5-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-207">Сбой сетевого адаптера на сервере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-207">A network adapter at the server failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-208">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-208">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <span data-ttu-id="90bd5-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-210">Всплывающие окна сетевых сообщений не появятся.</span><span class="sxs-lookup"><span data-stu-id="90bd5-210">You will not receive network message popups.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-211">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-211">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <span data-ttu-id="90bd5-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-213">Произошла внутренняя ошибка проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="90bd5-213">An internal authentication error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <span data-ttu-id="90bd5-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-215">Для указанной учетной записи запрещено выполнять вход в это время суток.</span><span class="sxs-lookup"><span data-stu-id="90bd5-215">The specified account is not permitted to log in at this time of day.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <span data-ttu-id="90bd5-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-217">Учетная запись отключена.</span><span class="sxs-lookup"><span data-stu-id="90bd5-217">The specified account is disabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <span data-ttu-id="90bd5-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-219">Срок действия указанного пароля истек.</span><span class="sxs-lookup"><span data-stu-id="90bd5-219">The specified password has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <span data-ttu-id="90bd5-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-221">Указанная учетная запись не имеет разрешений на удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="90bd5-221">The specified account does not have remote access permissions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <span data-ttu-id="90bd5-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-223">Сервер удаленного доступа не отвечает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-223">The remote access server is not responding.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-224">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-224">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <span data-ttu-id="90bd5-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-226">Модем или другое устройство подключения сообщило об ошибке.</span><span class="sxs-lookup"><span data-stu-id="90bd5-226">Your modem or other connection device has reported an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <span data-ttu-id="90bd5-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-228">Устройство вернуло неопознанный ответ.</span><span class="sxs-lookup"><span data-stu-id="90bd5-228">An unrecognized response was returned by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <span data-ttu-id="90bd5-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-230">Макрос, требуемый для устройства, не найден на устройстве. Раздел INF-файла.</span><span class="sxs-lookup"><span data-stu-id="90bd5-230">A macro required by the device was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <span data-ttu-id="90bd5-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-232">Команда или ответ на устройстве. Раздел INF-файла ссылается на неопределенный макрос.</span><span class="sxs-lookup"><span data-stu-id="90bd5-232">A command or response in the device .INF file section refers to an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <span data-ttu-id="90bd5-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-234"><message>Макрос не найден на устройстве. Раздел INF-файла.</span><span class="sxs-lookup"><span data-stu-id="90bd5-234">The <message> macro was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <span data-ttu-id="90bd5-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-236"><defaultoff>Макрос на устройстве. Раздел INF-файла содержит неопределенный макрос.</span><span class="sxs-lookup"><span data-stu-id="90bd5-236">The <defaultoff> macro in the device .INF file section contains an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <span data-ttu-id="90bd5-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-238">Устройство. Не удалось открыть INF-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-238">The device .INF file could not be opened.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <span data-ttu-id="90bd5-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-240">Имя устройства на устройстве. INF-файл или носитель. Слишком длинный INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-240">The device name in the device .INF or media .INI file is too long.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <span data-ttu-id="90bd5-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-242">Носитель. INI-файл ссылается на неизвестное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="90bd5-242">The media .INI file refers to an unknown device name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <span data-ttu-id="90bd5-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-244">Устройство. INF-файл не содержит ответов для команды.</span><span class="sxs-lookup"><span data-stu-id="90bd5-244">The device .INF file contains no responses for the command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <span data-ttu-id="90bd5-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-246">Устройство. В INF-файле отсутствует команда.</span><span class="sxs-lookup"><span data-stu-id="90bd5-246">The device .INF file is missing a command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <span data-ttu-id="90bd5-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-248">Попытка задать макрос, не указанный в списке устройств. Раздел INF-файла.</span><span class="sxs-lookup"><span data-stu-id="90bd5-248">Attempted to set a macro not listed in device .INF file section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <span data-ttu-id="90bd5-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-250">Носитель. INI-файл ссылается на неизвестный тип устройства.</span><span class="sxs-lookup"><span data-stu-id="90bd5-250">The media .INI file refers to an unknown device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <span data-ttu-id="90bd5-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-252">Не удается выделить память.</span><span class="sxs-lookup"><span data-stu-id="90bd5-252">Cannot allocate memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <span data-ttu-id="90bd5-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-254">Порт не настроен для удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-254">The port is not configured for remote access.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <span data-ttu-id="90bd5-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-256">Ваш модем или другое устройство подключения не работает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-256">Your modem or other connection device is not functioning.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <span data-ttu-id="90bd5-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-258">Не удается прочитать носитель. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-258">Cannot read the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <span data-ttu-id="90bd5-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-260">Подключение отброшено.</span><span class="sxs-lookup"><span data-stu-id="90bd5-260">The connection was dropped.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <span data-ttu-id="90bd5-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-262">Недопустимый параметр использования в ini-файле носителя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-262">The usage parameter in the media .ini file is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <span data-ttu-id="90bd5-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-264">Не удается прочитать имя раздела с носителя. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-264">Cannot read the section name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <span data-ttu-id="90bd5-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-266">Не удается прочитать тип устройства с носителя. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-266">Cannot read the device type from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <span data-ttu-id="90bd5-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-268">Не удается прочитать имя устройства с носителя. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-268">Cannot read the device name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <span data-ttu-id="90bd5-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-270">Не удается прочитать сведения об использовании с носителя. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-270">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <span data-ttu-id="90bd5-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-272">Системе не удалось прочесть максимальную скорость подключения перевозчика с носителя. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-272">The system was unable to read the maximum carrier connection speed from the media .INI file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-273">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-273">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <span data-ttu-id="90bd5-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-275">Не удается прочитать сведения об использовании с носителя. INI-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-275">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <span data-ttu-id="90bd5-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-277">Линия занята.</span><span class="sxs-lookup"><span data-stu-id="90bd5-277">The line is busy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <span data-ttu-id="90bd5-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-279">Вместо модема ответил человек.</span><span class="sxs-lookup"><span data-stu-id="90bd5-279">A person answered instead of a modem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <span data-ttu-id="90bd5-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-281">Нет ответа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-281">There is no answer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <span data-ttu-id="90bd5-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-283">Не удается обнаружить сигнал несущей.</span><span class="sxs-lookup"><span data-stu-id="90bd5-283">Cannot detect a carrier signal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <span data-ttu-id="90bd5-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-285">Нет гудка в линии.</span><span class="sxs-lookup"><span data-stu-id="90bd5-285">There is no dial tone.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <span data-ttu-id="90bd5-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-287">Модем (или другое устройство для подключения) сообщил об общей ошибке.</span><span class="sxs-lookup"><span data-stu-id="90bd5-287">The modem (or other connecting device) reported a general error.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-288">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-288">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <span data-ttu-id="90bd5-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-290">Произошла ошибка при записи имени раздела.</span><span class="sxs-lookup"><span data-stu-id="90bd5-290">There was an error in writing the section name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <span data-ttu-id="90bd5-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-292">Произошла ошибка при записи типа устройства.</span><span class="sxs-lookup"><span data-stu-id="90bd5-292">There was an error in writing the device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <span data-ttu-id="90bd5-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-294">Произошла ошибка при записи имени устройства.</span><span class="sxs-lookup"><span data-stu-id="90bd5-294">There was an error in writing the device name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <span data-ttu-id="90bd5-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-296">Произошла ошибка при записи максимальной скорости подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-296">There was an error in writing the maximum connection speed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <span data-ttu-id="90bd5-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-298">Произошла ошибка при записи максимальной частоты несущей частоты.</span><span class="sxs-lookup"><span data-stu-id="90bd5-298">There was an error in writing the maximum carrier speed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <span data-ttu-id="90bd5-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-300">Произошла ошибка при записи сведений об использовании.</span><span class="sxs-lookup"><span data-stu-id="90bd5-300">There was an error in writing the usage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <span data-ttu-id="90bd5-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-302">Произошла ошибка при записи значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90bd5-302">There was an error in writing the default-off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <span data-ttu-id="90bd5-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span></span></dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <span data-ttu-id="90bd5-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-305">Носитель. INI-файл пуст.</span><span class="sxs-lookup"><span data-stu-id="90bd5-305">The media .INI file is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <span data-ttu-id="90bd5-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-307">Отказано в доступе, так как имя пользователя, пароль или оба значения недопустимы в домене.</span><span class="sxs-lookup"><span data-stu-id="90bd5-307">Access denied because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <span data-ttu-id="90bd5-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-309">В порте или подключенном устройстве произошла ошибка оборудования</span><span class="sxs-lookup"><span data-stu-id="90bd5-309">A hardware failure has occurred in the port or attached device</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <span data-ttu-id="90bd5-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-311">Макрос не является двоичным макросом.</span><span class="sxs-lookup"><span data-stu-id="90bd5-311">The macro is not a binary macro.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <span data-ttu-id="90bd5-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-313">Не найдена DCB.</span><span class="sxs-lookup"><span data-stu-id="90bd5-313">DCB not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <span data-ttu-id="90bd5-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-315">Конечный автомат не запущен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-315">State machines are not started.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <span data-ttu-id="90bd5-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-317">Конечный автомат уже запущен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-317">State machines are already started.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <span data-ttu-id="90bd5-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-319">Циклическая зависимость от частичного ответа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-319">Partial response looping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <span data-ttu-id="90bd5-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-321">Имя ключа ответа на устройстве. Неверный формат INF-файла.</span><span class="sxs-lookup"><span data-stu-id="90bd5-321">A response key name in the device .INF file is not in the expected format.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <span data-ttu-id="90bd5-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-323">Ответ устройства привел к переполнению буфера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-323">The device response caused a buffer overflow.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <span data-ttu-id="90bd5-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-325">Расширенная команда на устройстве. Слишком длинный INF-файл.</span><span class="sxs-lookup"><span data-stu-id="90bd5-325">The expanded command in the device .INF file is too long.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <span data-ttu-id="90bd5-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-327">Устройство перешло на скорость подключения, которая не поддерживается драйвером COM.</span><span class="sxs-lookup"><span data-stu-id="90bd5-327">The device moved to a connection speed that is not supported by the COM driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <span data-ttu-id="90bd5-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-329">Получен ответ устройства, если не ожидалось ни одного.</span><span class="sxs-lookup"><span data-stu-id="90bd5-329">Device response received when none expected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <span data-ttu-id="90bd5-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-331">Произошла ошибка, так как включен интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="90bd5-331">An error occurred because the interactive mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <span data-ttu-id="90bd5-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-333">Указан недопустимый номер обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="90bd5-333">A bad callback number was specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <span data-ttu-id="90bd5-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-335">Указано недопустимое состояние проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="90bd5-335">The specified authentication state is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <span data-ttu-id="90bd5-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-337">Произошла ошибка при записи начальной скорости подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-337">An error occurred when writing the initial connection speed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-338">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-338">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <span data-ttu-id="90bd5-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-340">Получено диагностическое уведомление X. 25.</span><span class="sxs-lookup"><span data-stu-id="90bd5-340">An X.25 diagnostic indication was received.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <span data-ttu-id="90bd5-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-342">Срок действия указанной учетной записи истек.</span><span class="sxs-lookup"><span data-stu-id="90bd5-342">The specified account has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <span data-ttu-id="90bd5-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-344">Произошла ошибка при попытке изменить пароль в домене.</span><span class="sxs-lookup"><span data-stu-id="90bd5-344">An error occurred while attempting to change the password on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <span data-ttu-id="90bd5-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-346">При обмене данными с вашим модемом обнаружены ошибки переполнения последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="90bd5-346">Serial overrun errors were detected while communicating with your modem.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <span data-ttu-id="90bd5-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-348">Сбой инициализации RasMan.</span><span class="sxs-lookup"><span data-stu-id="90bd5-348">RasMan initialization failure.</span></span> <span data-ttu-id="90bd5-349">Проверьте журнал событий.</span><span class="sxs-lookup"><span data-stu-id="90bd5-349">Check the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <span data-ttu-id="90bd5-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-351">Двусторонний порт инициализируется.</span><span class="sxs-lookup"><span data-stu-id="90bd5-351">The two-way port is initializing.</span></span> <span data-ttu-id="90bd5-352">Подождите несколько секунд и перезвоните.</span><span class="sxs-lookup"><span data-stu-id="90bd5-352">Wait a few seconds and redial.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-353">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-353">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <span data-ttu-id="90bd5-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-355">Нет доступных активных линий ISDN.</span><span class="sxs-lookup"><span data-stu-id="90bd5-355">No active ISDN lines are available.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <span data-ttu-id="90bd5-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-357">Нет доступных каналов ISDN для выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="90bd5-357">No ISDN channels are available to make the call.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-358">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-358">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <span data-ttu-id="90bd5-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-360">Возникло слишком много ошибок из-за низкого качества телефонной линии.</span><span class="sxs-lookup"><span data-stu-id="90bd5-360">Too many errors occurred because of poor phone line quality.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-361">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-361">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <span data-ttu-id="90bd5-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-363">IP-конфигурация удаленного доступа непригодна для использования.</span><span class="sxs-lookup"><span data-stu-id="90bd5-363">The remote access IP configuration is unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <span data-ttu-id="90bd5-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-365">В статическом пуле IP-адресов удаленного доступа нет доступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="90bd5-365">No IP addresses are available in the static pool of remote access IP addresses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <span data-ttu-id="90bd5-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-367">Истекло время ожидания PPP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-367">A PPP timeout occurred.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <span data-ttu-id="90bd5-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-369">Соединение было прервано удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-369">The connection was terminated by the remote computer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-370">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-370">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <span data-ttu-id="90bd5-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-372">Протоколы управления PPP не настроены.</span><span class="sxs-lookup"><span data-stu-id="90bd5-372">No PPP control protocols are configured.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <span data-ttu-id="90bd5-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-374">Удаленный узел PPP не отвечает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-374">The remote PPP peer is not responding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <span data-ttu-id="90bd5-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-376">Недопустимый пакет PPP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-376">The PPP packet is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <span data-ttu-id="90bd5-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-378">Номер телефона, включая префикс и суффикс, слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="90bd5-378">The phone number, including the prefix and suffix, is too long.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <span data-ttu-id="90bd5-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-380">Протоколу IPX не удается выполнить вызов через модем (или другое устройство для подключения), так как этот компьютер не настроен для исходящего вызова (это маршрутизатор IPX).</span><span class="sxs-lookup"><span data-stu-id="90bd5-380">The IPX protocol cannot dial out on the modem (or other connecting device) because this computer is not configured for dialing out (it is an IPX router).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-381">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-381">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <span data-ttu-id="90bd5-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-383">Протоколу IPX не удается выполнить вызов через модем (или другое устройство для подключения), так как этот компьютер не настроен для набора номера (маршрутизатор IPX не установлен).</span><span class="sxs-lookup"><span data-stu-id="90bd5-383">The IPX protocol cannot dial in on the modem (or other connecting device) because this computer is not configured for dialing in (the IPX router is not installed).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-384">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-384">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <span data-ttu-id="90bd5-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-386">Протокол IPX не может использоваться для удаленного доступа на нескольких портах за один раз.</span><span class="sxs-lookup"><span data-stu-id="90bd5-386">The IPX protocol cannot be used for dial-out on more than one port at a time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <span data-ttu-id="90bd5-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-388">Не удается получить доступ к TCPCFG.DLL.</span><span class="sxs-lookup"><span data-stu-id="90bd5-388">Cannot access TCPCFG.DLL.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-389">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-389">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <span data-ttu-id="90bd5-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-391">Не удается найти IP-адаптер, привязанный к удаленному доступу.</span><span class="sxs-lookup"><span data-stu-id="90bd5-391">Cannot find an IP adapter bound to remote access.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <span data-ttu-id="90bd5-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-393">Нельзя использовать SLIP, если не установлен протокол IP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-393">SLIP cannot be used unless the IP protocol is installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <span data-ttu-id="90bd5-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-395">Регистрация компьютера не завершена.</span><span class="sxs-lookup"><span data-stu-id="90bd5-395">Computer registration is not complete.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-396">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-396">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <span data-ttu-id="90bd5-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-398">Указанный протокол не настроен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-398">The specified protocol is not configured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <span data-ttu-id="90bd5-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-400">Согласование PPP не сходится.</span><span class="sxs-lookup"><span data-stu-id="90bd5-400">The PPP negotiation is not converging.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <span data-ttu-id="90bd5-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-402">Протокол управления PPP для указанного сетевого протокола недоступен на сервере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-402">the PPP control protocol for the specified network protocol is not available on the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <span data-ttu-id="90bd5-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-404">Протокол управления связью PPP был завершен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-404">The PPP link control protocol was terminated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <span data-ttu-id="90bd5-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-406">Запрошенный адрес был отклонен сервером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-406">The requested address was rejected by the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <span data-ttu-id="90bd5-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-408">Удаленный компьютер прервал протокол управления.</span><span class="sxs-lookup"><span data-stu-id="90bd5-408">The remote computer terminated the control protocol.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <span data-ttu-id="90bd5-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-410">Обнаружено замыкание на себя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-410">Loopback detected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <span data-ttu-id="90bd5-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-412">Сервер не назначил адрес.</span><span class="sxs-lookup"><span data-stu-id="90bd5-412">The server did not assign an address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <span data-ttu-id="90bd5-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-414">Удаленный сервер не может использовать зашифрованный пароль Windows NT.</span><span class="sxs-lookup"><span data-stu-id="90bd5-414">The remote server cannot use the Windows NT encrypted password.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <span data-ttu-id="90bd5-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-416">Не удалось инициализировать устройства TAPI, настроенные для удаленного доступа, или они установлены неправильно.</span><span class="sxs-lookup"><span data-stu-id="90bd5-416">The TAPI devices configured for remote access failed to initialize or were not installed correctly.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <span data-ttu-id="90bd5-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-418">Локальный компьютер не поддерживает шифрование.</span><span class="sxs-lookup"><span data-stu-id="90bd5-418">The local computer does not support encryption.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <span data-ttu-id="90bd5-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-420">Удаленный сервер не поддерживает шифрование.</span><span class="sxs-lookup"><span data-stu-id="90bd5-420">The remote server does not support encryption.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <span data-ttu-id="90bd5-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-422">Удаленный компьютер требует шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="90bd5-422">The remote computer requires data encryption.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-423">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-423">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <span data-ttu-id="90bd5-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-425">Система не может использовать номер сети IPX, назначенный удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-425">The system cannot use the IPX network number assigned by the remote computer.</span></span> <span data-ttu-id="90bd5-426">Дополнительные сведения содержатся в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="90bd5-426">Additional information is provided in the event log.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-427">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-427">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <span data-ttu-id="90bd5-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-429">Недопустимый модуль управления сеансами (SMM).</span><span class="sxs-lookup"><span data-stu-id="90bd5-429">The Session Management Module (SMM) is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-430">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-430">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <span data-ttu-id="90bd5-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-432">SMM не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="90bd5-432">The SMM is uninitialized.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-433">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-433">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <span data-ttu-id="90bd5-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-435">Отсутствует MAC для порта.</span><span class="sxs-lookup"><span data-stu-id="90bd5-435">No MAC for port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-436">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-436">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <span data-ttu-id="90bd5-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-438">Истекло время ожидания SMM.</span><span class="sxs-lookup"><span data-stu-id="90bd5-438">The SMM timed out.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-439">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-439">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <span data-ttu-id="90bd5-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-441">Указан недопустимый номер телефона.</span><span class="sxs-lookup"><span data-stu-id="90bd5-441">A bad phone number was specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <span data-ttu-id="90bd5-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-443">Указана неправильная SMM.</span><span class="sxs-lookup"><span data-stu-id="90bd5-443">The wrong SMM was specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-444">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-444">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <span data-ttu-id="90bd5-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-446">Номер обратного вызова содержит недопустимый символ.</span><span class="sxs-lookup"><span data-stu-id="90bd5-446">The callback number contains a character that is not valid.</span></span> <span data-ttu-id="90bd5-447">Допустимы только следующие 18 символов: от 0 до 9, T, P, W, (,),-, @ и пробел.</span><span class="sxs-lookup"><span data-stu-id="90bd5-447">Only the following 18 characters are allowed: 0 to 9, T, P, W, (, ), -, @, and space.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-448">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-448">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <span data-ttu-id="90bd5-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-450">При обработке скрипта обнаружена синтаксическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="90bd5-450">A syntax error was encountered while processing a script.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <span data-ttu-id="90bd5-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-452">Не удалось отключить подключение, так как оно было создано маршрутизатором с несколькими протоколами.</span><span class="sxs-lookup"><span data-stu-id="90bd5-452">The connection could not be disconnected because it was created by the multi-protocol router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <span data-ttu-id="90bd5-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-454">Системе не удалось найти многоканальный пакет.</span><span class="sxs-lookup"><span data-stu-id="90bd5-454">The system could not find the multi-link bundle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <span data-ttu-id="90bd5-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-456">Система не может выполнить автоматический вызов, так как для этого соединения указан пользовательский номеронабиратель.</span><span class="sxs-lookup"><span data-stu-id="90bd5-456">The system cannot perform automated dial because this connection has a custom dialer specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <span data-ttu-id="90bd5-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-458">Это подключение уже набирается.</span><span class="sxs-lookup"><span data-stu-id="90bd5-458">This connection is already being dialed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <span data-ttu-id="90bd5-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-460">Не удалось запустить службу RAS автоматически.</span><span class="sxs-lookup"><span data-stu-id="90bd5-460">RAS could not be started automatically.</span></span> <span data-ttu-id="90bd5-461">Дополнительные сведения содержатся в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="90bd5-461">Additional information is provided in the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <span data-ttu-id="90bd5-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-463">В подключении уже включен общий доступ к подключению к Интернету (ICS).</span><span class="sxs-lookup"><span data-stu-id="90bd5-463">Internet Connection Sharing (ICS) is already enabled on the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-464">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-464">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <span data-ttu-id="90bd5-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-466">Произошла ошибка при изменении параметров общего доступа к подключению Интернета.</span><span class="sxs-lookup"><span data-stu-id="90bd5-466">An error occurred while the existing Internet Connection Sharing settings were being changed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-467">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-467">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <span data-ttu-id="90bd5-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-469">При включении возможностей маршрутизации произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="90bd5-469">An error occurred while routing capabilities were being enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-470">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-470">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <span data-ttu-id="90bd5-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-472">При включении общего доступа к подключению к Интернету произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="90bd5-472">An error occurred while Internet Connection Sharing was being enabled for the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-473">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-473">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <span data-ttu-id="90bd5-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-475">При настройке локальной сети для совместного использования произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="90bd5-475">An error occurred while the local network was being configured for sharing.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-476">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-476">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <span data-ttu-id="90bd5-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-478">Не удается включить общий доступ к подключению к Интернету.</span><span class="sxs-lookup"><span data-stu-id="90bd5-478">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="90bd5-479">Существует несколько подключений локальной сети, Кроме подключения к общему подключению.</span><span class="sxs-lookup"><span data-stu-id="90bd5-479">There is more than one LAN connection other than the connection to be shared.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-480">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-480">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <span data-ttu-id="90bd5-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-482">Модуль чтения смарт-карт не установлен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-482">No smart card reader is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <span data-ttu-id="90bd5-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-484">Не удается включить общий доступ к подключению к Интернету.</span><span class="sxs-lookup"><span data-stu-id="90bd5-484">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="90bd5-485">Для подключения к локальной сети уже настроен IP-адрес, необходимый для автоматической IP-адресации.</span><span class="sxs-lookup"><span data-stu-id="90bd5-485">A LAN connection is already configured with the IP address that is required for automatic IP addressing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <span data-ttu-id="90bd5-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-487">Не удалось найти сертификат.</span><span class="sxs-lookup"><span data-stu-id="90bd5-487">A certificate could not be found.</span></span> <span data-ttu-id="90bd5-488">Для подключений, использующих протокол L2TP через IPSec, требуется установка сертификата компьютера, также называемого сертификатом компьютера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-488">Connections that use the L2TP protocol over IPSec require the installation of a machine certificate, also known as a computer certificate.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <span data-ttu-id="90bd5-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-490">Не удается включить общий доступ к подключению к Интернету.</span><span class="sxs-lookup"><span data-stu-id="90bd5-490">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="90bd5-491">Подключение локальной сети, выбранное в качестве частной сети, имеет несколько настроенных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="90bd5-491">The LAN connection selected as the private network has more than one IP address configured.</span></span> <span data-ttu-id="90bd5-492">Перед включением общего доступа к Интернету перенастройте подключение локальной сети с помощью одного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="90bd5-492">Please reconfigure the LAN connection with a single IP address before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <span data-ttu-id="90bd5-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-494">Попытка подключения не удалась из-за сбоя шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="90bd5-494">The connection attempt failed because of failure to encrypt data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <span data-ttu-id="90bd5-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-496">Указанное назначение недоступно.</span><span class="sxs-lookup"><span data-stu-id="90bd5-496">The specified destination is not reachable.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <span data-ttu-id="90bd5-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-498">Удаленный компьютер отклонил попытки подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-498">The remote computer rejected the connection attempt.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <span data-ttu-id="90bd5-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-500">Попытка подключения не удалась, так как сеть занята.</span><span class="sxs-lookup"><span data-stu-id="90bd5-500">The connection attempt failed because the network is busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <span data-ttu-id="90bd5-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-502">Сетевое оборудование удаленного компьютера несовместимо с типом запрошенного вызова.</span><span class="sxs-lookup"><span data-stu-id="90bd5-502">The remote computer's network hardware is incompatible with the type of call requested.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <span data-ttu-id="90bd5-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-504">Попытка подключения не удалась, так как номер назначения изменился.</span><span class="sxs-lookup"><span data-stu-id="90bd5-504">The connection attempt failed because the destination number has changed.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <span data-ttu-id="90bd5-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-506">Попытка подключения не удалась из-за временного сбоя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-506">The connection attempt failed because of a temporary failure.</span></span> <span data-ttu-id="90bd5-507">Повторите попытку подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-507">Try connecting again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <span data-ttu-id="90bd5-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-509">Вызов был заблокирован удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-509">The call was blocked by the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <span data-ttu-id="90bd5-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-511">Не удалось подключить вызов, так как удаленный компьютер вызвал функцию "не беспокоить".</span><span class="sxs-lookup"><span data-stu-id="90bd5-511">The call could not be connected because the remote computer has invoked the Do Not Disturb feature.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <span data-ttu-id="90bd5-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-513">Попытка подключения не удалась из-за неупорядоченного модема или другого устройства подключения на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-513">The connection attempt failed because the modem or other connection device on the remote computer is out of order.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <span data-ttu-id="90bd5-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-515">Не удалось проверить удостоверение сервера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-515">It was not possible to verify the identity of the server.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <span data-ttu-id="90bd5-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-517">Для исходящего вызова с помощью этого подключения необходимо использовать смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="90bd5-517">To dial out using this connection you must use a smart card.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-518">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-518">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <span data-ttu-id="90bd5-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-520">Предпринятая функция недопустима для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-520">An attempted function is not valid for this connection.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <span data-ttu-id="90bd5-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-522">Попытка шифрования не удалась, так как не найден допустимый сертификат.</span><span class="sxs-lookup"><span data-stu-id="90bd5-522">The encryption attempt failed because no valid certificate was found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-523">Не рекомендуется использовать в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-523">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <span data-ttu-id="90bd5-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-525">Общий доступ к подключению (NAT) установлен в качестве протокола маршрутизации и должен быть удален перед включением общего доступа к подключению к Интернету.</span><span class="sxs-lookup"><span data-stu-id="90bd5-525">Connection Sharing (NAT) is currently installed as a routing protocol, and must be removed before enabling Internet Connection Sharing.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <span data-ttu-id="90bd5-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-527">Не удается включить общий доступ к подключению к Интернету.</span><span class="sxs-lookup"><span data-stu-id="90bd5-527">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="90bd5-528">Подключение по локальной сети, выбранное в качестве частной, отсутствует или отключено от сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-528">The LAN connection selected as the private network is either not present, or is disconnected from the network.</span></span> <span data-ttu-id="90bd5-529">Убедитесь, что адаптер локальной сети подключен, прежде чем включать общий доступ к подключению к Интернету.</span><span class="sxs-lookup"><span data-stu-id="90bd5-529">Please ensure that the LAN adapter is connected before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <span data-ttu-id="90bd5-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-531">Нельзя использовать это подключение во время входа, так как оно настроено на использование имени пользователя, отличного от того, на котором установлена смарт-карта.</span><span class="sxs-lookup"><span data-stu-id="90bd5-531">You cannot dial using this connection at login time because it is configured to use a user name different than the one on the smart card.</span></span> <span data-ttu-id="90bd5-532">Если вы хотите использовать это подключение во время входа, необходимо настроить его для использования имени пользователя на смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="90bd5-532">If you want to use this connection at login time, you must configure it to use the user name on the smart card.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <span data-ttu-id="90bd5-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-534">Нельзя использовать это подключение во время входа, так как оно не настроено для использования смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="90bd5-534">You cannot dial using this connection at login time because it is not configured to use a smart card.</span></span> <span data-ttu-id="90bd5-535">Если вы хотите использовать его во время входа в систему, необходимо изменить свойства этого подключения так, чтобы оно использовало смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="90bd5-535">If you want to use it at login time, you must edit the properties of this connection so that it uses a smart card.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <span data-ttu-id="90bd5-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-537">Попытка L2TP-подключения не удалась, так как на компьютере нет действительного сертификата компьютера для проверки подлинности безопасности.</span><span class="sxs-lookup"><span data-stu-id="90bd5-537">The L2TP connection attempt failed because there is no valid machine certificate on your computer for security authentication.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <span data-ttu-id="90bd5-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-539">Попытка L2TP-подключения не удалась, так как уровень безопасности не смог проверить подлинность удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-539">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <span data-ttu-id="90bd5-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-541">Попытка подключения L2TP не удалась, так как уровень безопасности не смог согласовать совместимые параметры с удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-541">The L2TP connection attempt failed because the security layer could not negotiate compatible parameters with the remote computer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <span data-ttu-id="90bd5-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-543">Попытка L2TP-подключения не удалась, так как уровень безопасности обнаружил ошибку обработки во время первоначального согласования с удаленным компьютером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-543">The L2TP connection attempt failed because the security layer encountered a processing error during initial negotiations with the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <span data-ttu-id="90bd5-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-545">Сбой попытки подключения L2TP из-за сбоя проверки сертификата на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-545">The L2TP connection attempt failed because certificate validation on the remote computer failed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <span data-ttu-id="90bd5-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-547">Попытка подключения L2TP не удалась, так как не найдена политика безопасности для подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-547">The L2TP connection attempt failed because security policy for the connection was not found.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <span data-ttu-id="90bd5-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-549">Попытка подключения L2TP не удалась, так как истекло время согласования безопасности.</span><span class="sxs-lookup"><span data-stu-id="90bd5-549">The L2TP connection attempt failed because security negotiation timed out.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <span data-ttu-id="90bd5-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-551">Попытка L2TP-подключения не удалась, поскольку произошла ошибка при согласовании безопасности.</span><span class="sxs-lookup"><span data-stu-id="90bd5-551">The L2TP connection attempt failed because an error occurred while negotiating security.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <span data-ttu-id="90bd5-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-553">Атрибут РАДИУСа протокола Frame для этого пользователя не является PPP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-553">The Framed Protocol RADIUS attribute for this user is not PPP.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <span data-ttu-id="90bd5-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-555">Неверный атрибут RADIUS типа туннеля для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-555">The Tunnel Type RADIUS attribute for this user is not correct.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <span data-ttu-id="90bd5-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-557">Атрибут RADIUS типа службы для этого пользователя не является ни фреймом, ни обратным вызовом.</span><span class="sxs-lookup"><span data-stu-id="90bd5-557">The Service Type RADIUS attribute for this user is neither Framed nor Callback Framed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <span data-ttu-id="90bd5-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-559">Не удалось установить подключение к удаленному компьютеру, так как модем не найден или занят.</span><span class="sxs-lookup"><span data-stu-id="90bd5-559">A connection to the remote computer could not be established because the modem was not found or was busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <span data-ttu-id="90bd5-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-561">Не удалось найти сертификат, который можно использовать с протоколом EAP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-561">A certificate could not be found that can be used with the Extensible Authentication Protocol (EAP).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <span data-ttu-id="90bd5-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-563">Общий доступ к подключению к Интернету (ICS) не может быть включен из-за конфликта IP-адресов в сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-563">Internet Connection Sharing (ICS) cannot be enabled due to an IP address conflict on the network.</span></span> <span data-ttu-id="90bd5-564">Для ICS требуется, чтобы узел был настроен для использования <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="90bd5-564">ICS requires the host be configured to use <strong>192.168.0.1</strong>.</span></span> <span data-ttu-id="90bd5-565">Убедитесь, что никакой другой клиент в сети не настроен на использование <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="90bd5-565">Ensure that no other client on the network is configured to use <strong>192.168.0.1</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-566">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-566">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-567">Windows 7 и более поздние версии: узел должен быть настроен для использования <strong>192.168.137.1</strong>
</span><span class="sxs-lookup"><span data-stu-id="90bd5-567">Windows 7 and later: The host must be configured to use <strong>192.168.137.1</strong>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <span data-ttu-id="90bd5-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-569">Не удалось установить VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="90bd5-569">Unable to establish the VPN connection.</span></span> <span data-ttu-id="90bd5-570">VPN-сервер может быть недоступен, или параметры безопасности для этого подключения могут быть неправильно настроены.</span><span class="sxs-lookup"><span data-stu-id="90bd5-570">The VPN server may be unreachable, or security parameters may not be configured properly for this connection.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-571">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-571">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <span data-ttu-id="90bd5-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-573">Это подключение настроено для проверки подлинности сервера доступа, но Windows не может проверить цифровой сертификат, отправленный сервером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-573">This connection is configured to validate the identity of the access server, but Windows cannot verify the digital certificate sent by the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-574">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-574">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <span data-ttu-id="90bd5-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-576">Указанная карта не распознана.</span><span class="sxs-lookup"><span data-stu-id="90bd5-576">The card supplied was not recognized.</span></span> <span data-ttu-id="90bd5-577">Убедитесь, что карточка вставлена правильно и надежно подходит.</span><span class="sxs-lookup"><span data-stu-id="90bd5-577">Please check that the card is inserted correctly, and fits securely.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-578">Поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-578">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <span data-ttu-id="90bd5-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-580">Конфигурация PEAP, хранящаяся в файле cookie сеанса, не соответствует текущей конфигурации сеанса.</span><span class="sxs-lookup"><span data-stu-id="90bd5-580">The PEAP configuration stored in the session cookie does not match the current session configuration.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-581">Поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-581">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <span data-ttu-id="90bd5-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-583">Удостоверение PEAP, хранящееся в файле cookie сеанса, не соответствует текущему удостоверению.</span><span class="sxs-lookup"><span data-stu-id="90bd5-583">The PEAP identity stored in the session cookie does not match the current identity.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-584">Поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-584">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <span data-ttu-id="90bd5-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-586">Нельзя использовать это подключение во время входа, так как оно настроено для использования учетных данных пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="90bd5-586">You cannot dial using this connection at login time because it is configured to use the currently-logged-in user's credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-587">Поддерживается в Windows XP с пакетом обновления 1 (SP1) и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-587">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <span data-ttu-id="90bd5-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-589">Подключение между компьютером и VPN-сервером запущено, но VPN-подключение не может быть завершено.</span><span class="sxs-lookup"><span data-stu-id="90bd5-589">A connection between your computer and the VPN server has been started, but the VPN connection cannot be completed.</span></span> <span data-ttu-id="90bd5-590">Наиболее распространенной причиной этого является то, что хотя бы одно интернет-устройство (например, брандмауэр или маршрутизатор) между компьютером и VPN-сервером не настроено на разрешение пакетов протокола GRE.</span><span class="sxs-lookup"><span data-stu-id="90bd5-590">The most common cause for this is that at least one Internet device (for example, a firewall or a router) between your computer and the VPN server is not configured to allow Generic Routing Encapsulation (GRE) protocol packets.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-591">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-591">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <span data-ttu-id="90bd5-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-593">Сетевое подключение между компьютером и VPN-сервером было прервано.</span><span class="sxs-lookup"><span data-stu-id="90bd5-593">The network connection between your computer and the VPN server was interrupted.</span></span> <span data-ttu-id="90bd5-594">Это может быть вызвано проблемой в передаче данных через VPN и, как правило, результатом задержки в Интернете или просто тем, что VPN-сервер достиг емкости.</span><span class="sxs-lookup"><span data-stu-id="90bd5-594">This can be caused by a problem in the VPN transmission and is commonly the result of internet latency or simply that your VPN server has reached capacity.</span></span> <span data-ttu-id="90bd5-595">Попробуйте повторно подключиться к VPN-серверу.</span><span class="sxs-lookup"><span data-stu-id="90bd5-595">Try to reconnect to the VPN server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-596">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-596">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <span data-ttu-id="90bd5-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-598">Не удалось установить сетевое подключение между компьютером и VPN-сервером, так как удаленный сервер отклонил подключение.</span><span class="sxs-lookup"><span data-stu-id="90bd5-598">The network connection between your computer and the VPN server could not be established because the remote server refused the connection.</span></span> <span data-ttu-id="90bd5-599">Обычно это вызвано несоответствием конфигурации сервера и параметров подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-599">This is typically caused by a mismatch between the server's configuration and your connection settings.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-600">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-600">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <span data-ttu-id="90bd5-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-602">Не удалось установить сетевое подключение между компьютером и VPN-сервером, так как удаленный сервер не отвечает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-602">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="90bd5-603">Это может быть вызвано тем, что одно из сетевых устройств (например, брандмауэры, NAT, маршрутизаторы) между компьютером и удаленным сервером не настроено для разрешения VPN-подключений.</span><span class="sxs-lookup"><span data-stu-id="90bd5-603">This could be because one of the network devices (for example, firewalls, NAT, routers) between your computer and the remote server is not configured to allow VPN connections.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-604">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-604">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <span data-ttu-id="90bd5-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-606">Было запущено сетевое подключение между компьютером и VPN-сервером, но VPN-подключение не было завершено.</span><span class="sxs-lookup"><span data-stu-id="90bd5-606">A network connection between your computer and the VPN server was started, but the VPN connection was not completed.</span></span> <span data-ttu-id="90bd5-607">Обычно это вызвано использованием неправильного или просроченного сертификата для проверки подлинности между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-607">This is typically caused by the use of an incorrect or expired certificate for authentication between the client and the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-608">Поддерживается в Windows Vista и более поздних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="90bd5-608">Supported in Windows Vista and later versions of Windows</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <span data-ttu-id="90bd5-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-610">Не удалось установить сетевое подключение между компьютером и VPN-сервером, так как удаленный сервер не отвечает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-610">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="90bd5-611">Обычно это вызвано проблемой с общим ключом между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="90bd5-611">This is typically caused by a pre-shared key problem between the client and server.</span></span> <span data-ttu-id="90bd5-612">Общий ключ используется для гарантии того, что вы указали, что вы являетесь в цикле связи IP-безопасности (IPSec).</span><span class="sxs-lookup"><span data-stu-id="90bd5-612">A pre-shared key is used to guarantee you are who you say you are in an IP Security (IPSec) communication cycle.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-613">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-613">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <span data-ttu-id="90bd5-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-615">Подключение не выполнено из-за политики, заданной на вашем RAS/VPN сервере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-615">The connection was prevented because of a policy configured on your RAS/VPN server.</span></span> <span data-ttu-id="90bd5-616">В частности, метод проверки подлинности, используемый сервером для проверки имени пользователя и пароля, может не соответствовать методу проверки подлинности, настроенному в профиле подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-616">Specifically, the authentication method used by the server to verify your username and password may not match the authentication method configured in your connection profile.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-617">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-617">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <span data-ttu-id="90bd5-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-619">Предпринята попытка установить второе широкополосное подключение, в то время как предыдущее высокоскоростное подключение уже установлено с помощью того же устройства или порта.</span><span class="sxs-lookup"><span data-stu-id="90bd5-619">You have attempted to establish a second broadband connection while a previous broadband connection is already established using the same device or port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-620">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-620">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <span data-ttu-id="90bd5-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-622">Не найдено базовое подключение Ethernet, необходимое для широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-622">The underlying Ethernet connectivity required for the broadband connection was not found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-623">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-623">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <span data-ttu-id="90bd5-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-625">Не удалось установить широкополосное сетевое подключение на компьютере, так как удаленный сервер не отвечает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-625">The broadband network connection could not be established on your computer because the remote server is not responding.</span></span> <span data-ttu-id="90bd5-626">Это может быть вызвано недопустимым значением поля Service Name для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-626">This could be caused by a value that is not valid for the 'Service Name' field for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-627">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-627">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <span data-ttu-id="90bd5-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-629">Функция или параметр, которые вы попытались включить, больше не поддерживаются службой удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-629">A feature or setting you have tried to enable is no longer supported by the remote access service.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-630">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-630">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <span data-ttu-id="90bd5-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-632">Невозможно удалить подключение, пока оно подключено.</span><span class="sxs-lookup"><span data-stu-id="90bd5-632">Cannot delete a connection while it is connected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-633">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-633">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <span data-ttu-id="90bd5-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-635">Клиенту принудительной защиты доступа к сети (NAP) не удалось создать системные ресурсы для подключений удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-635">The Network Access Protection (NAP) enforcement client could not create system resources for remote access connections.</span></span> <span data-ttu-id="90bd5-636">Некоторые сетевые службы или ресурсы могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="90bd5-636">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-637">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-637">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <span data-ttu-id="90bd5-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-639">Служба агента защиты доступа к сети (агент NAP) была отключена или не установлена на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-639">The Network Access Protection Agent (NAP Agent) service has been disabled or is not installed on this computer.</span></span> <span data-ttu-id="90bd5-640">Некоторые сетевые службы или ресурсы могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="90bd5-640">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-641">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-641">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <span data-ttu-id="90bd5-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-643">Клиенту принудительной защиты доступа к сети (NAP) не удалось зарегистрироваться в службе агента защиты доступа к сети (агент NAP).</span><span class="sxs-lookup"><span data-stu-id="90bd5-643">The Network Access Protection (NAP) enforcement client failed to register with the Network Access Protection Agent (NAP Agent) service.</span></span> <span data-ttu-id="90bd5-644">Некоторые сетевые службы или ресурсы могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="90bd5-644">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-645">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-645">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <span data-ttu-id="90bd5-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-647">Клиенту принудительной защиты доступа к сети (NAP) не удалось обработать запрос, так как подключение удаленного доступа не существует.</span><span class="sxs-lookup"><span data-stu-id="90bd5-647">The Network Access Protection (NAP) enforcement client was unable to process the request because the remote access connection does not exist.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-648">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-648">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <span data-ttu-id="90bd5-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-650">Клиент принудительной защиты доступа к сети (NAP) не ответил.</span><span class="sxs-lookup"><span data-stu-id="90bd5-650">The Network Access Protection (NAP) enforcement client did not respond.</span></span> <span data-ttu-id="90bd5-651">Некоторые сетевые службы или ресурсы могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="90bd5-651">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-652">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-652">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <span data-ttu-id="90bd5-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-654">Получен недопустимый Crypto-Binding тип-длина (TLV).</span><span class="sxs-lookup"><span data-stu-id="90bd5-654">The Crypto-Binding type-length-value (TLV) received is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-655">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-655">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <span data-ttu-id="90bd5-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-657">Crypto-Bindingный TLV не получен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-657">Crypto-Binding TLV was not received.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-658">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-658">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <span data-ttu-id="90bd5-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-660">Туннельный протокол "точка — точка" (PPTP) несовместим с IPv6.</span><span class="sxs-lookup"><span data-stu-id="90bd5-660">Point-to-Point Tunneling Protocol (PPTP) is incompatible with IPv6.</span></span> <span data-ttu-id="90bd5-661">Измените тип виртуальной частной сети на протокол L2TP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-661">Change the type of virtual private network to Layer Two Tunneling Protocol (L2TP).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-662">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-662">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <span data-ttu-id="90bd5-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-664">Ошибка при проверке EAPTLS кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="90bd5-664">EAPTLS validation of the cached credentials failed.</span></span> <span data-ttu-id="90bd5-665">Удаление кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="90bd5-665">Discard cached credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-666">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-666">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <span data-ttu-id="90bd5-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-668">Не удается завершить подключение по протоколу L2TP и IPsec, так как служба модулей ключей IPSec для IKE и AuthIP и (или) служба модуля базовой фильтрации не запущена.</span><span class="sxs-lookup"><span data-stu-id="90bd5-668">The L2TP/IPsec connection cannot be completed because the IKE and AuthIP IPSec Keying Modules service and/or the Base Filtering Engine service is not running.</span></span> <span data-ttu-id="90bd5-669">Эти службы необходимы для установления подключения по протоколу L2TP/IPSec.</span><span class="sxs-lookup"><span data-stu-id="90bd5-669">These services are required to establish an L2TP/IPSec connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-670">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-670">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <span data-ttu-id="90bd5-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-672">Соединение было прервано из-за истечения времени ожидания простоя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-672">The connection was terminated because of idle timeout.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-673">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-673">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <span data-ttu-id="90bd5-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-675">Модем (или другое устройство подключения) был отключен из-за сбоя связи.</span><span class="sxs-lookup"><span data-stu-id="90bd5-675">The modem (or other connecting device) was disconnected due to link failure.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-676">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-676">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <span data-ttu-id="90bd5-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-678">Соединение было прервано, так как пользователь вышел из системы.</span><span class="sxs-lookup"><span data-stu-id="90bd5-678">The connection was terminated because user logged off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-679">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-679">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <span data-ttu-id="90bd5-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-681">Соединение было прервано, так как произошло переключение пользователя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-681">The connection was terminated because user switch happened.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-682">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-682">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <span data-ttu-id="90bd5-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-684">Соединение было прервано из-за гибернации.</span><span class="sxs-lookup"><span data-stu-id="90bd5-684">The connection was terminated because of hibernation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-685">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-685">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <span data-ttu-id="90bd5-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-687">Соединение было разорвано из-за приостановки системы.</span><span class="sxs-lookup"><span data-stu-id="90bd5-687">The connection was terminated because the system got suspended.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-688">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-688">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <span data-ttu-id="90bd5-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-690">Соединение прервано, так как диспетчер подключений удаленного доступа остановлен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-690">The connection was terminated because Remote Access Connection manager stopped.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-691">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-691">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <span data-ttu-id="90bd5-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-693">Попытка L2TP-подключения не удалась, так как уровень безопасности не смог проверить подлинность удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-693">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <span data-ttu-id="90bd5-694">Это может быть вызвано тем, что одно или несколько полей сертификата, представленного удаленным сервером, не могут быть проверены как принадлежащие целевому назначению.</span><span class="sxs-lookup"><span data-stu-id="90bd5-694">This could be because one or more fields of the certificate presented by the remote server could not be validated as belonging to the target destination.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-695">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-695">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <span data-ttu-id="90bd5-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-697">Компьютер не поддерживает защиту доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-697">The machine is not NAP capable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-698">Поддерживается в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-698">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <span data-ttu-id="90bd5-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-700">Недопустимый идентификатор туннеля.</span><span class="sxs-lookup"><span data-stu-id="90bd5-700">Invalid Tunnel ID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-701">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-701">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <span data-ttu-id="90bd5-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-703">Выполняется другой запрос на обновление соединения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-703">Another update connection request is in progress.</span></span> <span data-ttu-id="90bd5-704">Служба RAS допускает только один запрос на обновление подключения за раз.</span><span class="sxs-lookup"><span data-stu-id="90bd5-704">RAS allows only one update connection request at a time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-705">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-705">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <span data-ttu-id="90bd5-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-707">Согласование с помощью настроенного протокола отключено.</span><span class="sxs-lookup"><span data-stu-id="90bd5-707">Negotiating using configured protocol is disable.</span></span> <span data-ttu-id="90bd5-708">Измените свойства соединения и выберите другой протокол для согласования и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="90bd5-708">Edit connection properties and select different protocol for negotiation and try again.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-709">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-709">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <span data-ttu-id="90bd5-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-711">Сбой согласования внутреннего адреса.</span><span class="sxs-lookup"><span data-stu-id="90bd5-711">Internal address negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-712">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-712">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <span data-ttu-id="90bd5-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-714">Клиент должен запросить внутренний адрес IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="90bd5-714">Client has to request an Internal IPv4 or IPv6 address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-715">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-715">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <span data-ttu-id="90bd5-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-717">Сбой согласования селекторов трафика.</span><span class="sxs-lookup"><span data-stu-id="90bd5-717">Traffic Selectors negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-718">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-718">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <span data-ttu-id="90bd5-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-720">Мобильное подключение отключено для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-720">Mobility is disabled for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-721">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-721">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <span data-ttu-id="90bd5-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-723">Подключение VPN по-прежнему подключается или повторно проходит проверку подлинности из-за изменения состояния карантина.</span><span class="sxs-lookup"><span data-stu-id="90bd5-723">The VPN Connection is still connecting or re-authenticating because of Quarantine state change.</span></span> <span data-ttu-id="90bd5-724">Запускать мобильное обновление только в том случае, если состояние подключения — "Connected".</span><span class="sxs-lookup"><span data-stu-id="90bd5-724">Initiate mobile update only when connection state is 'Connected'.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-725">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-725">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <span data-ttu-id="90bd5-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-727">Сервер отклонил проверку подлинности клиента из-за непредвиденного значения TLV или несоответствия значений для TLV.</span><span class="sxs-lookup"><span data-stu-id="90bd5-727">Server rejected client authentication, due to unexpected TLV or value mismatch for a TLV.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-728">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-728">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <span data-ttu-id="90bd5-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-730">Параметры назначения VPN не выбраны пользователем или больше не являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="90bd5-730">Either VPN destination preference is not selected by the user or it is no longer valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-731">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-731">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <span data-ttu-id="90bd5-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-733">Кэшированные учетные данные смарт-карты недопустимы.</span><span class="sxs-lookup"><span data-stu-id="90bd5-733">Cached smart card credential is invalid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-734">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-734">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <span data-ttu-id="90bd5-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-736">Сбой попытки подключения VPN из-за внутренней ошибки при добавлении файлов cookie в протокол SSTP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-736">VPN connection attempt failed due to internal error occurred while adding cookies to the Secure Socket Tunneling Protocol (SSTP).</span></span> <span data-ttu-id="90bd5-737">Подробные сведения см. в журнале системных событий.</span><span class="sxs-lookup"><span data-stu-id="90bd5-737">Please see the System Event Log for the detailed information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <span data-ttu-id="90bd5-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-739">Атрибуты внутреннего метода PEAP, хранящиеся в файле cookie, являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="90bd5-739">The PEAP inner method attribute(s) stored in the cookie is/are invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <span data-ttu-id="90bd5-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-741">Тип протокола расширенной проверки подлинности, необходимый для проверки подлинности подключения удаленного доступа, не установлен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-741">The Extensible Authentication Protocol type required for authentication of the remote access connection is not installed on your computer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <span data-ttu-id="90bd5-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-743">Тип протокола расширяемой проверки подлинности, настроенный для подключения удаленного доступа, не поддерживает единый вход.</span><span class="sxs-lookup"><span data-stu-id="90bd5-743">The Extensible Authentication Protocol type configured on the remote access connection does not support single sign-on.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <span data-ttu-id="90bd5-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-745">Тип протокола расширяемой проверки подлинности, настроенный для подключения удаленного доступа, не поддерживает запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="90bd5-745">The Extensible Authentication Protocol type configured on the remote access connection does not support the requested operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <span data-ttu-id="90bd5-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-747">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как сертификат, проверяющий подлинность клиента на сервере, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="90bd5-747">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is not valid.</span></span> <span data-ttu-id="90bd5-748">Убедитесь, что сертификат, используемый для проверки подлинности, допустим.</span><span class="sxs-lookup"><span data-stu-id="90bd5-748">Ensure that the certificate used for authentication is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <span data-ttu-id="90bd5-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-750">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как истек срок действия сертификата, проверяющего подлинность клиента на сервере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-750">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is expired.</span></span> <span data-ttu-id="90bd5-751">Продлите сертификат.</span><span class="sxs-lookup"><span data-stu-id="90bd5-751">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <span data-ttu-id="90bd5-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-753">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как сертификат, проверяющий подлинность клиента на сервере, отозван.</span><span class="sxs-lookup"><span data-stu-id="90bd5-753">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is revoked.</span></span> <span data-ttu-id="90bd5-754">Используйте сертификат, который не был отозван.</span><span class="sxs-lookup"><span data-stu-id="90bd5-754">Use a certificate that has not been revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <span data-ttu-id="90bd5-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-756">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности из-за ошибки в сертификате, который выполняет проверку подлинности клиента на сервере.</span><span class="sxs-lookup"><span data-stu-id="90bd5-756">The remote access connection completed, but authentication failed because of an error in the certificate that authenticates the client to the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <span data-ttu-id="90bd5-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-758">Подключение удаленного доступа выполнено, но проверка подлинности не удалась, так как сертификат, используемый клиентом для проверки подлинности сервера, недопустим.</span><span class="sxs-lookup"><span data-stu-id="90bd5-758">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <span data-ttu-id="90bd5-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-760">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как истек срок действия сертификата, используемого клиентом для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-760">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <span data-ttu-id="90bd5-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-762">Подключение удаленного доступа выполнено, но проверка подлинности не удалась, так как сертификат, используемый клиентом для проверки подлинности сервера, отозван.</span><span class="sxs-lookup"><span data-stu-id="90bd5-762">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <span data-ttu-id="90bd5-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-764">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности из-за ошибки в сертификате, используемом клиентом для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-764">The remote access connection completed, but authentication failed because of an error in the certificate that the client uses to authenticate the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <span data-ttu-id="90bd5-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-766">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как доверенный корневой сертификат, проверяющий сертификат пользователя, не найден в хранилище сертификатов доверенных корневых центров сертификации.</span><span class="sxs-lookup"><span data-stu-id="90bd5-766">The remote access connection completed, but authentication failed because a trusted root certificate that validates the user certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <span data-ttu-id="90bd5-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-768">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как доверенный корневой сертификат, используемый для проверки сертификата пользователя, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="90bd5-768">The remote access connection completed, but authentication failed because the trusted root certificate that is used to validate the user certificate is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <span data-ttu-id="90bd5-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-770">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как истек срок действия сертификата в хранилище сертификатов доверенных корневых центров сертификации, проверяющего сертификат пользователя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-770">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that authenticates the user certificate is expired.</span></span> <span data-ttu-id="90bd5-771">Продлите сертификат.</span><span class="sxs-lookup"><span data-stu-id="90bd5-771">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <span data-ttu-id="90bd5-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-773">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как сертификат, проверяющий сертификат сервера, не найден в хранилище сертификатов доверенных корневых центров сертификации.</span><span class="sxs-lookup"><span data-stu-id="90bd5-773">The remote access connection completed, but authentication failed because a certificate that validates the server certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <span data-ttu-id="90bd5-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-775">Подключение удаленного доступа выполнено, но проверка подлинности не удалась, так как сертификат в хранилище сертификатов доверенных корневых центров сертификации, который проверяет сертификат сервера, недопустим.</span><span class="sxs-lookup"><span data-stu-id="90bd5-775">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that validates the server certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <span data-ttu-id="90bd5-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-777">Подключение удаленного доступа выполнено, но произошел сбой проверки подлинности, так как для сертификата на сервере не указано имя сервера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-777">The remote access connection completed, but authentication failed because the certificate on the server computer does not have a server name specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <span data-ttu-id="90bd5-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-779">Внешнее удостоверение PEAP не совпадает с внутренним удостоверением при отключении конфиденциальности удостоверений.</span><span class="sxs-lookup"><span data-stu-id="90bd5-779">The PEAP outer identity is not same as the inner identity when identity privacy is turned OFF.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <span data-ttu-id="90bd5-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-781">Удаленное соединение не было установлено, так как не удалось разрешить имя сервера удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-781">The remote connection was not made because the name of the remote access server did not resolve.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <span data-ttu-id="90bd5-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-783">Для сертификата указан недопустимый пароль.</span><span class="sxs-lookup"><span data-stu-id="90bd5-783">The password provided for the certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <span data-ttu-id="90bd5-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-785">Не удалось включить интерфейс, так как был создан более одного интерфейса с одним и тем же назначением с помощью метода проверки подлинности с общим ключом.</span><span class="sxs-lookup"><span data-stu-id="90bd5-785">The interface could not be enabled because more than one interface with the same destination has been created with the pre-shared key authentication method.</span></span> <span data-ttu-id="90bd5-786">Измените метод назначения или проверки подлинности и включите интерфейс.</span><span class="sxs-lookup"><span data-stu-id="90bd5-786">Change the destination/auth method and enable the interface.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="90bd5-787">Следующие коды ошибок маршрутизации и удаленного доступа (RRAS) определены в мпреррор. h.</span><span class="sxs-lookup"><span data-stu-id="90bd5-787">The following Routing and Remote Access (RRAS) API error codes are defined in mprerror.h.</span></span> <span data-ttu-id="90bd5-788">Все коды ошибок поддерживаются в Windows 2000 или более поздних версиях Windows, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="90bd5-788">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90bd5-789">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="90bd5-789">Return code/value</span></span></th>
<th><span data-ttu-id="90bd5-790">Описание</span><span class="sxs-lookup"><span data-stu-id="90bd5-790">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <span data-ttu-id="90bd5-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-792">Маршрутизатор не работает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-792">The router is not running.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <span data-ttu-id="90bd5-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-794">Интерфейс уже подключен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-794">The interface is already connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <span data-ttu-id="90bd5-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-796">Указанный идентификатор протокола неизвестен маршрутизатору.</span><span class="sxs-lookup"><span data-stu-id="90bd5-796">The specified protocol identifier is not known to the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <span data-ttu-id="90bd5-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-798">Диспетчер интерфейсов вызова по требованию (DDM) не работает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-798">The Demand-dial Interface Manager (DDM) is not running.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <span data-ttu-id="90bd5-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-800">Интерфейс с таким именем уже зарегистрирован на маршрутизаторе.</span><span class="sxs-lookup"><span data-stu-id="90bd5-800">An interface with this name is already registered with the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <span data-ttu-id="90bd5-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-802">Интерфейс с таким именем не зарегистрирован на маршрутизаторе.</span><span class="sxs-lookup"><span data-stu-id="90bd5-802">An interface with this name is not registered with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <span data-ttu-id="90bd5-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-804">Интерфейс не подключен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-804">The interface is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <span data-ttu-id="90bd5-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-806">Указанный протокол останавливается.</span><span class="sxs-lookup"><span data-stu-id="90bd5-806">The specified protocol is stopping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <span data-ttu-id="90bd5-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-808">Интерфейс подключен, и поэтому не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="90bd5-808">The interface is connected and hence cannot be deleted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <span data-ttu-id="90bd5-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-810">Не были заданы учетные данные интерфейса.</span><span class="sxs-lookup"><span data-stu-id="90bd5-810">The interface credentials have not been set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <span data-ttu-id="90bd5-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-812">Этот интерфейс уже находится в процессе подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-812">This interface is already in the process of connecting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <span data-ttu-id="90bd5-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-814">Обновление сведений о маршрутизации для этого интерфейса уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="90bd5-814">An update of routing information on this interface is already in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <span data-ttu-id="90bd5-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-816">Недопустимая конфигурации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="90bd5-816">The interface configration is not valid.</span></span> <span data-ttu-id="90bd5-817">Уже существует другой интерфейс, подключенный к тому же интерфейсу на удаленном маршрутизаторе.</span><span class="sxs-lookup"><span data-stu-id="90bd5-817">There is already another interface that is connected to the same interface on the remote router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <span data-ttu-id="90bd5-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-819">Клиент удаленного доступа попытался подключиться через порт, зарезервированный только для маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="90bd5-819">A Remote Access Client attempted to connect over a port that was reserved for routers only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <span data-ttu-id="90bd5-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-821">Маршрутизатор вызова по требованию попытался подключиться через порт, зарезервированный только для клиентов удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-821">A Demand Dial Router attempted to connect over a port that was reserved for Remote Access Clients only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <span data-ttu-id="90bd5-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-823">Клиентский интерфейс с таким именем уже существует и в настоящее время подключен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-823">The client interface with this name already exists and is currently connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <span data-ttu-id="90bd5-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-825">Интерфейс находится в отключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="90bd5-825">The interface is in a disabled state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <span data-ttu-id="90bd5-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-827">Протокол проверки подлинности был отклонен удаленным одноранговым узлом.</span><span class="sxs-lookup"><span data-stu-id="90bd5-827">The authentication protocol was rejected by the remote peer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <span data-ttu-id="90bd5-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-829">Нет доступных протоколов проверки подлинности для использования.</span><span class="sxs-lookup"><span data-stu-id="90bd5-829">There are no authentication protocols available for use.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <span data-ttu-id="90bd5-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-831">Не удалось установить подключение, так как протокол проверки подлинности, используемый сервером RAS/VPN для проверки имени пользователя и пароля, не удалось сопоставить с параметрами в профиле подключения.</span><span class="sxs-lookup"><span data-stu-id="90bd5-831">The connection could not be established because the authentication protocol used by the RAS/VPN server to verify your username and password could not be matched with the settings in your connection profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <span data-ttu-id="90bd5-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-833">Удаленная учетная запись не имеет разрешения на удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="90bd5-833">The remote account does not have Remote Access permission.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <span data-ttu-id="90bd5-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-835">Срок действия удаленной учетной записи истек.</span><span class="sxs-lookup"><span data-stu-id="90bd5-835">The remote account has expired.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <span data-ttu-id="90bd5-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-837">Удаленная учетная запись отключена.</span><span class="sxs-lookup"><span data-stu-id="90bd5-837">The remote account is disabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <span data-ttu-id="90bd5-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-839">Для удаленной учетной записи не разрешено выполнять вход в это время суток.</span><span class="sxs-lookup"><span data-stu-id="90bd5-839">The remote account is not permitted to logon at this time of day.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <span data-ttu-id="90bd5-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-841">Отказано в доступе к удаленному одноранговому узлу, так как имя пользователя, пароль или оба значения недопустимы в домене.</span><span class="sxs-lookup"><span data-stu-id="90bd5-841">Access was denied to the remote peer because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <span data-ttu-id="90bd5-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-843">Нет доступных портов с поддержкой маршрутизации для использования этим интерфейсом вызова по требованию.</span><span class="sxs-lookup"><span data-stu-id="90bd5-843">There are no routing enabled ports available for use by this demand dial interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <span data-ttu-id="90bd5-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-845">Порт был отключен из-за неактивности.</span><span class="sxs-lookup"><span data-stu-id="90bd5-845">The port has been disconnected due to inactivity.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <span data-ttu-id="90bd5-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-847">В данный момент интерфейс недоступен.</span><span class="sxs-lookup"><span data-stu-id="90bd5-847">The interface is not reachable at this time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <span data-ttu-id="90bd5-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-849">Служба вызова по требованию находится в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="90bd5-849">The Demand Dial service is in a paused state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <span data-ttu-id="90bd5-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-851">Интерфейс отключен администратором.</span><span class="sxs-lookup"><span data-stu-id="90bd5-851">The interface has been disconnected by the administrator.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <span data-ttu-id="90bd5-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-853">Сервер проверки подлинности не ответил на запросы проверки подлинности в течение отведенного времени.</span><span class="sxs-lookup"><span data-stu-id="90bd5-853">The authentication server did not respond to authentication requests in a timely fashion.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <span data-ttu-id="90bd5-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-855">Достигнуто максимально допустимое число портов для использования в многокомпонентном соединении.</span><span class="sxs-lookup"><span data-stu-id="90bd5-855">The maximum number of ports allowed for use in the multi-linked connection has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <span data-ttu-id="90bd5-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-857">Достигнуто предельное время подключения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="90bd5-857">The connection time limit for the user has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <span data-ttu-id="90bd5-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-859">Достигнуто максимальное число поддерживаемых интерфейсов локальной сети.</span><span class="sxs-lookup"><span data-stu-id="90bd5-859">The maximum limit on the number of LAN interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <span data-ttu-id="90bd5-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-861">Достигнуто предельное число поддерживаемых интерфейсов вызова по требованию.</span><span class="sxs-lookup"><span data-stu-id="90bd5-861">The maximum limit on the number of Demand Dial interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <span data-ttu-id="90bd5-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-863">Достигнуто максимальное число поддерживаемых клиентов удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="90bd5-863">The maximum limit on the number of Remote Access Clients supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <span data-ttu-id="90bd5-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-865">Порт был отключен из-за политики протокола распределения пропускной способности (BAP).</span><span class="sxs-lookup"><span data-stu-id="90bd5-865">The port has been disconnected due to the Bandwidth Allocation Protocol (BAP) policy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <span data-ttu-id="90bd5-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-867">Поскольку используется другое подключение типа, входящее подключение не может принять ваш запрос на подключение.</span><span class="sxs-lookup"><span data-stu-id="90bd5-867">Because another connection of your type is in use, the incoming connection cannot accept your connection request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <span data-ttu-id="90bd5-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-869">В сети не было найдено ни одного RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-869">No RADIUS servers were located on the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <span data-ttu-id="90bd5-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-871">От сервера проверки подлинности RADIUS получен недопустимый ответ.</span><span class="sxs-lookup"><span data-stu-id="90bd5-871">The response received from the RADIUS authentication server was not valid.</span></span> <span data-ttu-id="90bd5-872">Убедитесь, что секретный пароль с учетом регистра для сервера RADIUS установлен правильно.</span><span class="sxs-lookup"><span data-stu-id="90bd5-872">Make sure that the case sensitive secret password for the RADIUS server is set correctly.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <span data-ttu-id="90bd5-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-874">У вас нет разрешения на подключение в данный момент.</span><span class="sxs-lookup"><span data-stu-id="90bd5-874">You do not have permission to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <span data-ttu-id="90bd5-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-876">У вас нет разрешения на подключение с использованием текущего типа устройства.</span><span class="sxs-lookup"><span data-stu-id="90bd5-876">You do not have permission to connect using the current device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <span data-ttu-id="90bd5-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-878">Не удалось установить подключение, так как метод проверки подлинности, используемый в профиле подключения, не разрешен для использования политикой доступа, настроенной на сервере RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="90bd5-878">The connection could not be established because the authentication method used by your connection profile is not permitted for use by an access policy configured on the RAS/VPN server.</span></span> <span data-ttu-id="90bd5-879">В частности, это может быть вызвано различиями в конфигурации метода проверки подлинности, выбранного на сервере RAS/VPN, и политики доступа, настроенной для нее.</span><span class="sxs-lookup"><span data-stu-id="90bd5-879">Specifically, this could be due to configuration differences between the authentication method selected on the RAS/VPN server and the access policy configured for it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <span data-ttu-id="90bd5-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-881">Для этого пользователя требуется BAP.</span><span class="sxs-lookup"><span data-stu-id="90bd5-881">BAP is required for this user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <span data-ttu-id="90bd5-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-883">В данный момент интерфейс не может подключаться.</span><span class="sxs-lookup"><span data-stu-id="90bd5-883">The interface is not allowed to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <span data-ttu-id="90bd5-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-885">Сохраненная конфигурация маршрутизатора несовместима с текущим маршрутизатором.</span><span class="sxs-lookup"><span data-stu-id="90bd5-885">The saved router configuration is incompatible with the current router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <span data-ttu-id="90bd5-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-887">Удаленный доступ обнаружил устаревшие учетные записи пользователей в формате, которые не будут автоматически перенесены.</span><span class="sxs-lookup"><span data-stu-id="90bd5-887">Remote Access has detected older format user accounts that will not be migrated automatically.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <span data-ttu-id="90bd5-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-889">Транспорт уже установлен с маршрутизатором.</span><span class="sxs-lookup"><span data-stu-id="90bd5-889">The transport is already installed with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <span data-ttu-id="90bd5-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-891">Недопустимая длина подписи, полученная в пакете от сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-891">The signature length received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-892">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-892">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <span data-ttu-id="90bd5-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-894">Недопустимая подпись, полученная в пакете от сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-894">The signature received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-895">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-895">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <span data-ttu-id="90bd5-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-897">Не получал подпись и Еапмессаже от сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-897">Did not receive signature along with EAPMessage from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-898">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-898">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <span data-ttu-id="90bd5-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-900">Недопустимая длина или идентификатор, полученный в пакете от сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-900">The length or Id received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-901">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-901">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <span data-ttu-id="90bd5-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-903">Недопустимая длина, полученная в пакете с атрибутом от сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-903">The length received in a packet with attribute from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-904">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-904">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <span data-ttu-id="90bd5-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-906">Недопустимый пакет, полученный от сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="90bd5-906">The packet received from RADIUS server in not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-907">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-907">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <span data-ttu-id="90bd5-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-909">Средство проверки подлинности не совпадает в пакете от RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="90bd5-909">Authenticator does not match in packet from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-910">Поддерживается в Windows XP и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-910">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <span data-ttu-id="90bd5-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span><span class="sxs-lookup"><span data-stu-id="90bd5-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span></span></dl></td>
<td><span data-ttu-id="90bd5-912">Сервер маршрутизации и удаленного доступа либо не настроен, либо не работает.</span><span class="sxs-lookup"><span data-stu-id="90bd5-912">Routing and Remote access server is either not configured or not running.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90bd5-913">Поддерживается в Windows 7 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="90bd5-913">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="90bd5-914">Требования</span><span class="sxs-lookup"><span data-stu-id="90bd5-914">Requirements</span></span>



| <span data-ttu-id="90bd5-915">Требование</span><span class="sxs-lookup"><span data-stu-id="90bd5-915">Requirement</span></span> | <span data-ttu-id="90bd5-916">Значение</span><span class="sxs-lookup"><span data-stu-id="90bd5-916">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90bd5-917">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90bd5-917">Minimum supported client</span></span><br/> | <span data-ttu-id="90bd5-918">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="90bd5-918">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90bd5-919">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90bd5-919">Minimum supported server</span></span><br/> | <span data-ttu-id="90bd5-920">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="90bd5-920">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 





