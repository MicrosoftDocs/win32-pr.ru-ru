---
title: Сообщения об ошибках (WinInet. h)
description: Функции WinINet возвращают коды ошибок там, где это уместно. Следующие ошибки относятся к функциям WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137751"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="cf37d-104">Сообщения об ошибках (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="cf37d-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="cf37d-105">Функции WinINet возвращают коды ошибок там, где это уместно.</span><span class="sxs-lookup"><span data-stu-id="cf37d-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="cf37d-106">Следующие ошибки относятся к функциям WinINet.</span><span class="sxs-lookup"><span data-stu-id="cf37d-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="cf37d-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**Ошибка \_ при \_ удалении FTP**</span><span class="sxs-lookup"><span data-stu-id="cf37d-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-108">12111</span><span class="sxs-lookup"><span data-stu-id="cf37d-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-109">Операция FTP не была завершена из-за прерывания сеанса.</span><span class="sxs-lookup"><span data-stu-id="cf37d-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**Ошибка \_ FTP \_ без \_ пассивного \_ режима**</span><span class="sxs-lookup"><span data-stu-id="cf37d-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-111">12112</span><span class="sxs-lookup"><span data-stu-id="cf37d-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-112">Пассивный режим недоступен на сервере.</span><span class="sxs-lookup"><span data-stu-id="cf37d-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**Ошибка \_ \_ \_ при выполнении FTP-перемещения \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-114">12110</span><span class="sxs-lookup"><span data-stu-id="cf37d-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-115">Невозможно выполнить запрошенную операцию над обработчиком сеанса FTP, так как операция уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf37d-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена атрибут Gopher**</span><span class="sxs-lookup"><span data-stu-id="cf37d-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-117">12137</span><span class="sxs-lookup"><span data-stu-id="cf37d-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-118">Не удалось найти запрошенный атрибут.</span><span class="sxs-lookup"><span data-stu-id="cf37d-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-119">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**Ошибка \_ в \_ данных \_ Gopher**</span><span class="sxs-lookup"><span data-stu-id="cf37d-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-121">12132</span><span class="sxs-lookup"><span data-stu-id="cf37d-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-122">При получении данных от сервера gopher обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="cf37d-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-123">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**Ошибка \_ \_ в конце \_ \_ данных Gopher**</span><span class="sxs-lookup"><span data-stu-id="cf37d-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-125">12133</span><span class="sxs-lookup"><span data-stu-id="cf37d-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-126">Достигнут конец данных.</span><span class="sxs-lookup"><span data-stu-id="cf37d-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-127">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**Ошибка \_ Gopher \_ неверный \_ \_ тип указателя**</span><span class="sxs-lookup"><span data-stu-id="cf37d-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-129">12135</span><span class="sxs-lookup"><span data-stu-id="cf37d-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-130">Недопустимый тип указателя для данной операции.</span><span class="sxs-lookup"><span data-stu-id="cf37d-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-131">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**Ошибка \_ Gopher, \_ Недопустимый \_ указатель**</span><span class="sxs-lookup"><span data-stu-id="cf37d-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-133">12134</span><span class="sxs-lookup"><span data-stu-id="cf37d-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-134">Указан недопустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="cf37d-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-135">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**Ошибка \_ Gopher \_ не \_ файл**</span><span class="sxs-lookup"><span data-stu-id="cf37d-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-137">12131</span><span class="sxs-lookup"><span data-stu-id="cf37d-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-138">Запрос должен быть выполнен для указателя файла.</span><span class="sxs-lookup"><span data-stu-id="cf37d-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-139">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**Ошибка \_ Gopher \_ , \_ а не Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-141">12136</span><span class="sxs-lookup"><span data-stu-id="cf37d-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-142">Запрошенная операция может быть выполнена только для сервера gopher + или с указателем, указывающим на операцию Gopher +.</span><span class="sxs-lookup"><span data-stu-id="cf37d-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-143">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**Ошибка \_ \_ протокола Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-145">12130</span><span class="sxs-lookup"><span data-stu-id="cf37d-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-146">При синтаксическом анализе данных, возвращенных с сервера gopher, обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="cf37d-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-147">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**Ошибка \_ Gopher \_ неизвестный \_ указатель**</span><span class="sxs-lookup"><span data-stu-id="cf37d-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-149">12138</span><span class="sxs-lookup"><span data-stu-id="cf37d-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-150">Неизвестный тип указателя.</span><span class="sxs-lookup"><span data-stu-id="cf37d-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-151">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="cf37d-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**Ошибка \_ cookie HTTP- \_ файла \_ отклонено**</span><span class="sxs-lookup"><span data-stu-id="cf37d-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-153">12162</span><span class="sxs-lookup"><span data-stu-id="cf37d-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-154">Файл cookie HTTP отклонен сервером.</span><span class="sxs-lookup"><span data-stu-id="cf37d-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**Ошибка \_ HTTP \_ cookie \_ требует \_ подтверждения**</span><span class="sxs-lookup"><span data-stu-id="cf37d-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-156">12161</span><span class="sxs-lookup"><span data-stu-id="cf37d-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-157">Для HTTP-файла cookie требуется подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cf37d-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-158">Windows Vista и Windows Server 2008 и более ранние версии.</span><span class="sxs-lookup"><span data-stu-id="cf37d-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**Ошибка \_ HTTP- \_ сервера нижнего уровня \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-160">12151</span><span class="sxs-lookup"><span data-stu-id="cf37d-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-161">Сервер не вернул заголовки.</span><span class="sxs-lookup"><span data-stu-id="cf37d-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**\_заголовок ошибки \_ HTTP \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="cf37d-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-163">12155</span><span class="sxs-lookup"><span data-stu-id="cf37d-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-164">Не удалось добавить заголовок, поскольку он уже существует.</span><span class="sxs-lookup"><span data-stu-id="cf37d-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_заголовок ошибки \_ HTTP \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="cf37d-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-166">12150</span><span class="sxs-lookup"><span data-stu-id="cf37d-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-167">Не удалось найти запрошенный заголовок.</span><span class="sxs-lookup"><span data-stu-id="cf37d-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**Ошибка \_ - \_ Недопустимый \_ заголовок HTTP**</span><span class="sxs-lookup"><span data-stu-id="cf37d-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-169">12153</span><span class="sxs-lookup"><span data-stu-id="cf37d-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-170">Указанный заголовок недопустим.</span><span class="sxs-lookup"><span data-stu-id="cf37d-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**Ошибка \_ - \_ Недопустимый \_ \_ запрос HTTP**</span><span class="sxs-lookup"><span data-stu-id="cf37d-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-172">12154</span><span class="sxs-lookup"><span data-stu-id="cf37d-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-173">Запрос, сделанный в [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) , является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="cf37d-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**Ошибка \_ HTTP — \_ Недопустимый \_ \_ ответ сервера**</span><span class="sxs-lookup"><span data-stu-id="cf37d-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-175">12152</span><span class="sxs-lookup"><span data-stu-id="cf37d-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-176">Не удалось проанализировать ответ сервера.</span><span class="sxs-lookup"><span data-stu-id="cf37d-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**Ошибка \_ HTTP \_ не \_ перенаправлена**</span><span class="sxs-lookup"><span data-stu-id="cf37d-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-178">12160</span><span class="sxs-lookup"><span data-stu-id="cf37d-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-179">Не удалось перенаправить HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="cf37d-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**Ошибка \_ \_ при перенаправлении HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-181">12156</span><span class="sxs-lookup"><span data-stu-id="cf37d-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-182">Перенаправление завершилось сбоем, так как схема изменилась (например, HTTP на FTP) или все попытки перенаправления завершились неудачей (по умолчанию пять попыток).</span><span class="sxs-lookup"><span data-stu-id="cf37d-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**Ошибка \_ при \_ перенаправлении HTTP, запрос на перенаправление \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-184">12168</span><span class="sxs-lookup"><span data-stu-id="cf37d-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-185">Перенаправление требует подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf37d-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**Ошибка \_ \_ \_ при выполнении асинхронного потока в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-187">12047</span><span class="sxs-lookup"><span data-stu-id="cf37d-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-188">Приложению не удалось запустить асинхронный поток.</span><span class="sxs-lookup"><span data-stu-id="cf37d-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**Ошибка \_ Интернет \_ \_ \_ - \_ скрипта автоматического прокси**</span><span class="sxs-lookup"><span data-stu-id="cf37d-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-190">12166</span><span class="sxs-lookup"><span data-stu-id="cf37d-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-191">Произошла ошибка в скрипте автоматической настройки прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf37d-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**Ошибка в \_ Интернете, \_ неправильная \_ \_ Длина параметра**</span><span class="sxs-lookup"><span data-stu-id="cf37d-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-193">12010</span><span class="sxs-lookup"><span data-stu-id="cf37d-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-194">Длина параметра, указанного в [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) или [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) , неверна для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="cf37d-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**Ошибка \_ Internet \_ Bad \_ \_ параметр реестра**</span><span class="sxs-lookup"><span data-stu-id="cf37d-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-196">12022</span><span class="sxs-lookup"><span data-stu-id="cf37d-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-197">Требуемое значение реестра найдено, но имеет неверный тип или имеет недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="cf37d-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**Ошибка \_ \_ \_ подключения к Интернету**</span><span class="sxs-lookup"><span data-stu-id="cf37d-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-199">12029</span><span class="sxs-lookup"><span data-stu-id="cf37d-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-200">Сбой при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="cf37d-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**Ошибка \_ Internet \_ чг \_ POST \_ не \_ является \_ безопасной**</span><span class="sxs-lookup"><span data-stu-id="cf37d-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-202">12042</span><span class="sxs-lookup"><span data-stu-id="cf37d-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-203">Приложение выполняет публикацию и пытается изменить несколько строк текста на небезопасном сервере.</span><span class="sxs-lookup"><span data-stu-id="cf37d-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**Ошибка \_ \_ \_ требуется сертификат проверки подлинности клиента Интернета \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-205">12044</span><span class="sxs-lookup"><span data-stu-id="cf37d-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-206">Сервер запрашивает проверку подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="cf37d-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**Ошибка \_ при \_ \_ настройке проверки подлинности клиента Интернета \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-208">12046</span><span class="sxs-lookup"><span data-stu-id="cf37d-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-209">На этом компьютере не настроена авторизация клиента.</span><span class="sxs-lookup"><span data-stu-id="cf37d-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**Ошибка \_ \_ прерванного подключения к Интернету \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-211">12030</span><span class="sxs-lookup"><span data-stu-id="cf37d-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-212">Подключение к серверу прервано.</span><span class="sxs-lookup"><span data-stu-id="cf37d-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**Ошибка \_ \_ сброса подключения к Интернету \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-214">12031</span><span class="sxs-lookup"><span data-stu-id="cf37d-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-215">Подключение к серверу было сброшено.</span><span class="sxs-lookup"><span data-stu-id="cf37d-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**Ошибка \_ \_ при декодировании в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-217">12175</span><span class="sxs-lookup"><span data-stu-id="cf37d-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-218">WinINet не смог выполнить декодирование содержимого в ответе.</span><span class="sxs-lookup"><span data-stu-id="cf37d-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="cf37d-219">Дополнительные сведения см. в разделе о [**кодировании содержимого**](content-encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="cf37d-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**Ошибка \_ \_ ожидания диалогового окна Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-221">12049</span><span class="sxs-lookup"><span data-stu-id="cf37d-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-222">В ходе выполнения другого потока появится диалоговое окно Password (пароль).</span><span class="sxs-lookup"><span data-stu-id="cf37d-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**Ошибка \_ подключения к Интернету \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-224">12163</span><span class="sxs-lookup"><span data-stu-id="cf37d-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-225">Потеряно подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="cf37d-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**Ошибка \_ \_ расширенной \_ ошибки Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-227">12003</span><span class="sxs-lookup"><span data-stu-id="cf37d-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-228">С сервера возвращена Расширенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="cf37d-228">An extended error was returned from the server.</span></span> <span data-ttu-id="cf37d-229">Обычно это строка или буфер, содержащий подробное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cf37d-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="cf37d-230">Вызовите [**интернетжетластреспонсеинфо**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) , чтобы получить текст ошибки.</span><span class="sxs-lookup"><span data-stu-id="cf37d-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**Ошибка \_ \_ при сбое в Интернете \_ дуетосекуритичекк**</span><span class="sxs-lookup"><span data-stu-id="cf37d-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-232">12171</span><span class="sxs-lookup"><span data-stu-id="cf37d-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-233">Сбой функции из-за проверки безопасности.</span><span class="sxs-lookup"><span data-stu-id="cf37d-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**Ошибка \_ при \_ попытке принудительного подключения к Интернету \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-235">12032</span><span class="sxs-lookup"><span data-stu-id="cf37d-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-236">Функции необходимо повторить запрос.</span><span class="sxs-lookup"><span data-stu-id="cf37d-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**Ошибка \_ при \_ \_ попытке входа в Интернет Fortezza \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-238">12054</span><span class="sxs-lookup"><span data-stu-id="cf37d-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-239">Запрошенный ресурс требует проверки подлинности Fortezza.</span><span class="sxs-lookup"><span data-stu-id="cf37d-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**Ошибка \_ в \_ наличии обработчика Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-241">12036</span><span class="sxs-lookup"><span data-stu-id="cf37d-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-242">Не удалось выполнить запрос, так как маркер уже существует.</span><span class="sxs-lookup"><span data-stu-id="cf37d-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**Ошибка \_ Интернет \_ -HTTP \_ для \_ HTTPS \_ в \_ редир**</span><span class="sxs-lookup"><span data-stu-id="cf37d-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-244">12039</span><span class="sxs-lookup"><span data-stu-id="cf37d-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-245">Приложение переходит с подключения не SSL к SSL-соединению из-за перенаправления.</span><span class="sxs-lookup"><span data-stu-id="cf37d-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**Ошибка \_ Интернет \_ \_ -отправки HTTP HTTPS \_ \_ редир**</span><span class="sxs-lookup"><span data-stu-id="cf37d-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-247">12052</span><span class="sxs-lookup"><span data-stu-id="cf37d-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-248">Данные, отправляемые в SSL-соединение, перенаправляются на подключение, не поддерживающее SSL.</span><span class="sxs-lookup"><span data-stu-id="cf37d-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**Ошибка \_ Интернет \_ \_ -HTTPS для \_ HTTP \_ в \_ редир**</span><span class="sxs-lookup"><span data-stu-id="cf37d-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-250">12040</span><span class="sxs-lookup"><span data-stu-id="cf37d-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-251">Приложение перемещается из SSL в подключение без SSL из-за перенаправления.</span><span class="sxs-lookup"><span data-stu-id="cf37d-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**Ошибка в \_ Интернете, \_ неправильный \_ Формат**</span><span class="sxs-lookup"><span data-stu-id="cf37d-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-253">12027</span><span class="sxs-lookup"><span data-stu-id="cf37d-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-254">Недопустимый формат запроса.</span><span class="sxs-lookup"><span data-stu-id="cf37d-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**Ошибка \_ при \_ неправильном \_ состоянии обработчика Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-256">12019</span><span class="sxs-lookup"><span data-stu-id="cf37d-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-257">Не удается выполнить запрошенную операцию, так как указанный обработчик находится в неправильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="cf37d-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**Ошибка \_ при \_ неправильном \_ типе обработчика Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-259">12018</span><span class="sxs-lookup"><span data-stu-id="cf37d-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-260">Для этой операции указан недопустимый тип обработчика.</span><span class="sxs-lookup"><span data-stu-id="cf37d-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**Ошибка в \_ Интернете \_ неверный \_ пароль**</span><span class="sxs-lookup"><span data-stu-id="cf37d-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-262">12014</span><span class="sxs-lookup"><span data-stu-id="cf37d-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-263">Не удалось выполнить запрос на подключение и вход на FTP-сервер, так как указанный пароль неверен.</span><span class="sxs-lookup"><span data-stu-id="cf37d-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**Ошибка в \_ Интернете \_ неправильное \_ \_ имя пользователя**</span><span class="sxs-lookup"><span data-stu-id="cf37d-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-265">12013</span><span class="sxs-lookup"><span data-stu-id="cf37d-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-266">Не удалось выполнить запрос на подключение и вход на FTP-сервер, так как указано неверное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf37d-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**Ошибка \_ при \_ вставке \_ компакт CDROM в Интернет**</span><span class="sxs-lookup"><span data-stu-id="cf37d-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-268">12053</span><span class="sxs-lookup"><span data-stu-id="cf37d-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-269">Для запроса требуется вставить компакт-диск на устройство чтения компакт-дисков, чтобы указать требуемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="cf37d-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-270">Windows Vista и Windows Server 2008 и более ранние версии.</span><span class="sxs-lookup"><span data-stu-id="cf37d-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**Ошибка \_ при \_ внутренней \_ ошибке Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-272">12004</span><span class="sxs-lookup"><span data-stu-id="cf37d-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-273">Произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="cf37d-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**Ошибка в \_ Интернете, \_ Недопустимый \_ ЦС**</span><span class="sxs-lookup"><span data-stu-id="cf37d-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-275">12045</span><span class="sxs-lookup"><span data-stu-id="cf37d-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-276">Функция не знакома с центром сертификации, создавшим сертификат сервера.</span><span class="sxs-lookup"><span data-stu-id="cf37d-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**Ошибка \_ при \_ выполнении недопустимой операции в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-278">12016</span><span class="sxs-lookup"><span data-stu-id="cf37d-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-279">Запрошенная операция недопустима.</span><span class="sxs-lookup"><span data-stu-id="cf37d-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**\_ \_ Недопустимый \_ параметр "ошибка в Интернете"**</span><span class="sxs-lookup"><span data-stu-id="cf37d-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-281">12009</span><span class="sxs-lookup"><span data-stu-id="cf37d-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-282">Запрос к [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) или [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) указал недопустимое значение параметра.</span><span class="sxs-lookup"><span data-stu-id="cf37d-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**Ошибка \_ \_ \_ запроса прокси-сервера в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-284">12033</span><span class="sxs-lookup"><span data-stu-id="cf37d-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-285">Недопустимый запрос к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="cf37d-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**Ошибка \_ \_ \_ URL-адреса, недопустимого в Интернете**</span><span class="sxs-lookup"><span data-stu-id="cf37d-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-287">12005</span><span class="sxs-lookup"><span data-stu-id="cf37d-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-288">Недопустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="cf37d-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена веб – элемент**</span><span class="sxs-lookup"><span data-stu-id="cf37d-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-290">12028</span><span class="sxs-lookup"><span data-stu-id="cf37d-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-291">Не удалось найти запрошенный элемент.</span><span class="sxs-lookup"><span data-stu-id="cf37d-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**Ошибка \_ \_ при входе в Интернет \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-293">12015</span><span class="sxs-lookup"><span data-stu-id="cf37d-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-294">Не удалось выполнить запрос на подключение к серверу FTP и его вход.</span><span class="sxs-lookup"><span data-stu-id="cf37d-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**Ошибка \_ при входе в Интернет. \_ \_ \_ Отображение \_ \_ тела сущности**</span><span class="sxs-lookup"><span data-stu-id="cf37d-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-296">12174</span><span class="sxs-lookup"><span data-stu-id="cf37d-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-297">С веб-сайта возвращен заголовок дайджеста MS-Logoff.</span><span class="sxs-lookup"><span data-stu-id="cf37d-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="cf37d-298">Этот заголовок специально указывает пакету дайджеста очистить учетные данные для связанной области.</span><span class="sxs-lookup"><span data-stu-id="cf37d-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="cf37d-299">Эта ошибка будет возвращена только в случае, если параметр "ошибка подключения к ошибке при входе в сеть" имеет значение " [ \_ \_ \_ \_ \_ отображать \_ \_ тело сущности](option-flags.md) ". в противном случае возвращается **Ошибка \_ \_ \_ входа в Интернет** .</span><span class="sxs-lookup"><span data-stu-id="cf37d-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**Ошибка \_ \_ смешанной \_ безопасности в Интернете**</span><span class="sxs-lookup"><span data-stu-id="cf37d-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-301">12041</span><span class="sxs-lookup"><span data-stu-id="cf37d-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-302">Содержимое не полностью защищено.</span><span class="sxs-lookup"><span data-stu-id="cf37d-302">The content is not entirely secure.</span></span> <span data-ttu-id="cf37d-303">Возможно, часть просматриваемого содержимого поступила с незащищенных серверов.</span><span class="sxs-lookup"><span data-stu-id="cf37d-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**Ошибка \_ " \_ имя Интернета \_ не \_ разрешено"**</span><span class="sxs-lookup"><span data-stu-id="cf37d-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-305">12007</span><span class="sxs-lookup"><span data-stu-id="cf37d-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-306">Не удалось разрешить имя сервера.</span><span class="sxs-lookup"><span data-stu-id="cf37d-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**Ошибка \_ Интернета — \_ требуется \_ MSN \_ SSPI \_ pkg**</span><span class="sxs-lookup"><span data-stu-id="cf37d-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-308">12173</span><span class="sxs-lookup"><span data-stu-id="cf37d-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-309">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="cf37d-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**Ошибка \_ в \_ \_ пользовательском интерфейсе для Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-311">12034</span><span class="sxs-lookup"><span data-stu-id="cf37d-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-312">Запрошен пользовательский интерфейс или другая операция блокировки.</span><span class="sxs-lookup"><span data-stu-id="cf37d-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-313">Windows Vista и Windows Server 2008 и более ранние версии.</span><span class="sxs-lookup"><span data-stu-id="cf37d-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**Ошибка \_ \_ \_ обратного вызова в Интернете**</span><span class="sxs-lookup"><span data-stu-id="cf37d-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-315">12025</span><span class="sxs-lookup"><span data-stu-id="cf37d-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-316">Не удалось выполнить асинхронный запрос, поскольку не задана функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="cf37d-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**Ошибка \_ Интернета \_ без \_ контекста**</span><span class="sxs-lookup"><span data-stu-id="cf37d-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-318">12024</span><span class="sxs-lookup"><span data-stu-id="cf37d-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-319">Не удалось выполнить асинхронный запрос, так как было указано нулевое значение контекста.</span><span class="sxs-lookup"><span data-stu-id="cf37d-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**Ошибка \_ " \_ нет \_ прямого \_ доступа к Интернету"**</span><span class="sxs-lookup"><span data-stu-id="cf37d-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-321">12023</span><span class="sxs-lookup"><span data-stu-id="cf37d-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-322">В настоящее время невозможно выполнить прямой доступ к сети.</span><span class="sxs-lookup"><span data-stu-id="cf37d-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**Ошибка " \_ сеть \_ не \_ инициализирована"**</span><span class="sxs-lookup"><span data-stu-id="cf37d-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-324">12172</span><span class="sxs-lookup"><span data-stu-id="cf37d-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-325">Инициализация API WinINet не выполнена.</span><span class="sxs-lookup"><span data-stu-id="cf37d-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="cf37d-326">Указывает, что функция более высокого уровня, например [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena), еще не была вызвана.</span><span class="sxs-lookup"><span data-stu-id="cf37d-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**Ошибка \_ \_ \_ запроса прокси-сервера в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-328">12020</span><span class="sxs-lookup"><span data-stu-id="cf37d-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-329">Запрос не может быть выполнен через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="cf37d-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**Ошибка \_ при \_ отмене операции в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-331">12017</span><span class="sxs-lookup"><span data-stu-id="cf37d-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-332">Операция была отменена, как правило, из-за того, что обработчик, на котором был запущен запрос, был закрыт до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="cf37d-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**\_ \_ параметр "Ошибка Интернета не может быть установлен" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-334">12011</span><span class="sxs-lookup"><span data-stu-id="cf37d-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-335">Невозможно задать запрошенный параметр, выполняется только запрос.</span><span class="sxs-lookup"><span data-stu-id="cf37d-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**Ошибка \_ Интернета \_ вне \_ \_ дескрипторов**</span><span class="sxs-lookup"><span data-stu-id="cf37d-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-337">12001</span><span class="sxs-lookup"><span data-stu-id="cf37d-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-338">В данный момент больше не удалось создать дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="cf37d-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**сообщение об ошибке " \_ Интернет \_ -Публикация не \_ \_ \_ защищена"**</span><span class="sxs-lookup"><span data-stu-id="cf37d-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-340">12043</span><span class="sxs-lookup"><span data-stu-id="cf37d-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-341">Приложение передает данные на сервер, который не является безопасным.</span><span class="sxs-lookup"><span data-stu-id="cf37d-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена протокол Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-343">12008</span><span class="sxs-lookup"><span data-stu-id="cf37d-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-344">Не удалось найти запрошенный протокол.</span><span class="sxs-lookup"><span data-stu-id="cf37d-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**Ошибка \_ \_ \_ недоступности прокси-сервера Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-346">12165</span><span class="sxs-lookup"><span data-stu-id="cf37d-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-347">Указанный прокси-сервер недоступен.</span><span class="sxs-lookup"><span data-stu-id="cf37d-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**Ошибка \_ при \_ \_ изменении схемы перенаправления Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-349">12048</span><span class="sxs-lookup"><span data-stu-id="cf37d-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-350">Функции не удалось выполнить перенаправление, поскольку схема изменилась (например, с HTTP на FTP).</span><span class="sxs-lookup"><span data-stu-id="cf37d-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**Ошибка \_ \_ \_ \_ не \_ найдена значение реестра Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-352">12021</span><span class="sxs-lookup"><span data-stu-id="cf37d-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-353">Не удалось найти требуемое значение реестра.</span><span class="sxs-lookup"><span data-stu-id="cf37d-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**Ошибка \_ \_ запроса \_ в Интернет**</span><span class="sxs-lookup"><span data-stu-id="cf37d-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-355">12026</span><span class="sxs-lookup"><span data-stu-id="cf37d-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-356">Не удалось выполнить требуемую операцию, так как ожидается один или несколько запросов.</span><span class="sxs-lookup"><span data-stu-id="cf37d-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**Ошибка \_ \_ диалогового окна повторного подключения к Интернету \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-358">12050</span><span class="sxs-lookup"><span data-stu-id="cf37d-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-359">Необходимо повторить попытку в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cf37d-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**Ошибка \_ \_ \_ \_ недопустимое общее имя сертификата Internet sec \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-361">12038</span><span class="sxs-lookup"><span data-stu-id="cf37d-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-362">Неверное общее имя SSL-сертификата (поле имени узла), например, если вы указали www.server.com, а общее имя сертификата — www.different.com.</span><span class="sxs-lookup"><span data-stu-id="cf37d-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**Ошибка \_ при \_ обращении к Интернету с \_ \_ \_ недопустимым сертификатом**</span><span class="sxs-lookup"><span data-stu-id="cf37d-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-364">12037</span><span class="sxs-lookup"><span data-stu-id="cf37d-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-365">Дата SSL-сертификата, полученная с сервера, является неправильной.</span><span class="sxs-lookup"><span data-stu-id="cf37d-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="cf37d-366">Срок действия сертификата истек.</span><span class="sxs-lookup"><span data-stu-id="cf37d-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ошибки при ошибках \_ сертификатов Интернета ( \_ сек) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-368">12055</span><span class="sxs-lookup"><span data-stu-id="cf37d-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-369">SSL-сертификат содержит ошибки.</span><span class="sxs-lookup"><span data-stu-id="cf37d-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**Ошибка \_ \_ номер сертификата Internet sec, \_ \_ без \_ редакции**</span><span class="sxs-lookup"><span data-stu-id="cf37d-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-371">12056</span><span class="sxs-lookup"><span data-stu-id="cf37d-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-372">SSL-сертификат не был отозван.</span><span class="sxs-lookup"><span data-stu-id="cf37d-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**Ошибка \_ \_ при версии \_ сертификата Internet sec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-374">12057</span><span class="sxs-lookup"><span data-stu-id="cf37d-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-375">Сбой отзыва SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="cf37d-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**Ошибка \_ при \_ \_ \_ отзыве сертификата в Интернете (Internet sec)**</span><span class="sxs-lookup"><span data-stu-id="cf37d-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-377">12170</span><span class="sxs-lookup"><span data-stu-id="cf37d-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-378">SSL-сертификат был отозван.</span><span class="sxs-lookup"><span data-stu-id="cf37d-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**Ошибка \_ Интернет \_ с \_ недопустимым \_ сертификатом**</span><span class="sxs-lookup"><span data-stu-id="cf37d-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-380">12169</span><span class="sxs-lookup"><span data-stu-id="cf37d-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-381">Недопустимый SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="cf37d-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**Ошибка \_ \_ канала безопасности \_ Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="cf37d-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-383">12157</span><span class="sxs-lookup"><span data-stu-id="cf37d-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-384">Произошла внутренняя ошибка приложения при загрузке библиотек SSL.</span><span class="sxs-lookup"><span data-stu-id="cf37d-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**Ошибка \_ " \_ сервер в Интернете \_ недоступен"**</span><span class="sxs-lookup"><span data-stu-id="cf37d-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-386">12164</span><span class="sxs-lookup"><span data-stu-id="cf37d-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-387">Указанный веб-сайт или сервер недоступен.</span><span class="sxs-lookup"><span data-stu-id="cf37d-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**Ошибка \_ \_ отключения Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-389">12012</span><span class="sxs-lookup"><span data-stu-id="cf37d-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-390">Поддержка WinINet завершается или выгружается.</span><span class="sxs-lookup"><span data-stu-id="cf37d-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**Ошибка \_ Internet \_ tcpip \_ не \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="cf37d-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-392">12159</span><span class="sxs-lookup"><span data-stu-id="cf37d-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-393">Необходимый стек протокола не загружен, и приложение не может запустить WinSock.</span><span class="sxs-lookup"><span data-stu-id="cf37d-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**Ошибка \_ \_ времени ожидания в Интернете**</span><span class="sxs-lookup"><span data-stu-id="cf37d-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-395">12002</span><span class="sxs-lookup"><span data-stu-id="cf37d-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-396">Истекло время ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="cf37d-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**Ошибка \_ Интернет \_ не \_ удалось \_ кэшировать \_ файл**</span><span class="sxs-lookup"><span data-stu-id="cf37d-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-398">12158</span><span class="sxs-lookup"><span data-stu-id="cf37d-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-399">Функции не удалось кэшировать файл.</span><span class="sxs-lookup"><span data-stu-id="cf37d-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**Ошибка \_ Интернет \_ не \_ может \_ загрузить \_ Скрипт**</span><span class="sxs-lookup"><span data-stu-id="cf37d-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-401">12167</span><span class="sxs-lookup"><span data-stu-id="cf37d-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-402">Не удалось скачать скрипт конфигурации автоматического прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="cf37d-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="cf37d-403">\_Флаг запроса в Интернете \_ должен быть \_ установлен в кэш \_ .</span><span class="sxs-lookup"><span data-stu-id="cf37d-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**Ошибка \_ \_ нераспознанной \_ схемы Интернета**</span><span class="sxs-lookup"><span data-stu-id="cf37d-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf37d-405">12006</span><span class="sxs-lookup"><span data-stu-id="cf37d-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="cf37d-406">Не удалось распознать схему URL-адресов или она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cf37d-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Ошибка \_ недопустимого \_ маркера**</span><span class="sxs-lookup"><span data-stu-id="cf37d-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf37d-408">Маркер, переданный в API, был либо недействительным, либо закрытым.</span><span class="sxs-lookup"><span data-stu-id="cf37d-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="cf37d-409">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="cf37d-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Ошибка \_ дополнительных \_ данных**</span><span class="sxs-lookup"><span data-stu-id="cf37d-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf37d-411">More data is available.</span><span class="sxs-lookup"><span data-stu-id="cf37d-411">More data is available.</span></span>

<span data-ttu-id="cf37d-412">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="cf37d-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Ошибка \_ больше \_ нет \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="cf37d-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf37d-414">Больше файлов не найдено.</span><span class="sxs-lookup"><span data-stu-id="cf37d-414">No more files have been found.</span></span>

<span data-ttu-id="cf37d-415">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="cf37d-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cf37d-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Ошибка \_ больше \_ нет \_ элементов**</span><span class="sxs-lookup"><span data-stu-id="cf37d-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cf37d-417">Больше элементов не найдено.</span><span class="sxs-lookup"><span data-stu-id="cf37d-417">No more items have been found.</span></span>

<span data-ttu-id="cf37d-418">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="cf37d-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf37d-419">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf37d-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cf37d-420">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="cf37d-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="cf37d-421">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="cf37d-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="cf37d-422">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="cf37d-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf37d-423">Требования</span><span class="sxs-lookup"><span data-stu-id="cf37d-423">Requirements</span></span>



| <span data-ttu-id="cf37d-424">Требование</span><span class="sxs-lookup"><span data-stu-id="cf37d-424">Requirement</span></span> | <span data-ttu-id="cf37d-425">Значение</span><span class="sxs-lookup"><span data-stu-id="cf37d-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf37d-426">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf37d-426">Minimum supported client</span></span><br/> | <span data-ttu-id="cf37d-427">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf37d-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cf37d-428">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf37d-428">Minimum supported server</span></span><br/> | <span data-ttu-id="cf37d-429">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf37d-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf37d-430">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf37d-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf37d-431"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf37d-431"><dt>Wininet.h</dt></span></span> </dl> |



 

