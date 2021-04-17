---
title: Флаги параметров (WinInet. h)
description: С функциями Интернеткуерйоптион и Интернетсетоптион используются следующие флаги параметров. Все допустимые флаги параметров имеют значение, большее или равное \_ первому \_ варианту Internet и меньшее или равное \_ последнему \_ параметру в Интернете.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672917"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="377dc-104">Флаги параметров (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="377dc-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="377dc-105">С функциями [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) используются следующие флаги параметров.</span><span class="sxs-lookup"><span data-stu-id="377dc-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="377dc-106">Все допустимые флаги параметров имеют значение, большее или равное **\_ первому \_ варианту Internet** и меньшее или равное **\_ последнему \_ параметру в Интернете**.</span><span class="sxs-lookup"><span data-stu-id="377dc-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="377dc-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**\_параметр " \_ изменить \_ удостоверение" в Интернете**</span><span class="sxs-lookup"><span data-stu-id="377dc-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-108">80</span><span class="sxs-lookup"><span data-stu-id="377dc-108">80</span></span>
</dt> <dt>



<span data-ttu-id="377dc-109">Не реализовано</span><span class="sxs-lookup"><span data-stu-id="377dc-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**\_параметр Интернета \_ Async**</span><span class="sxs-lookup"><span data-stu-id="377dc-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-111">30</span><span class="sxs-lookup"><span data-stu-id="377dc-111">30</span></span>
</dt> <dt>



<span data-ttu-id="377dc-112">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ асинхронный идентификатор параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-114">15</span><span class="sxs-lookup"><span data-stu-id="377dc-114">15</span></span>
</dt> <dt>



<span data-ttu-id="377dc-115">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_ \_ приоритет асинхронного режима Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-117">16</span><span class="sxs-lookup"><span data-stu-id="377dc-117">16</span></span>
</dt> <dt>



<span data-ttu-id="377dc-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**\_параметр "не \_ использовать" \_ в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-120">64</span><span class="sxs-lookup"><span data-stu-id="377dc-120">64</span></span>
</dt> <dt>



<span data-ttu-id="377dc-121">Задает или получает логическое значение, определяющее, должна ли система проверять наличие нового содержимого в сети и перезаписывать измененные записи кэша при обнаружении более новой версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="377dc-122">Если задано значение **true**, система проверяет сеть на наличие нового содержимого и перезаписывает измененную запись кэша новой версией.</span><span class="sxs-lookup"><span data-stu-id="377dc-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="377dc-123">Значение по умолчанию — **false**, что означает, что измененная запись кэша должна использоваться без проверки сети.</span><span class="sxs-lookup"><span data-stu-id="377dc-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="377dc-124">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-125">Она допустима только в Microsoft Internet Explorer 5 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**\_ \_ \_ обработчик потока параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-127">27</span><span class="sxs-lookup"><span data-stu-id="377dc-127">27</span></span>
</dt> <dt>



<span data-ttu-id="377dc-128">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="377dc-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**\_ \_ метки времени кэша параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-130">69</span><span class="sxs-lookup"><span data-stu-id="377dc-130">69</span></span>
</dt> <dt>



<span data-ttu-id="377dc-131">Извлекает структуру [**\_ \_ отметок времени кэша Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) , содержащую время LastModified и истечение срока действия из ресурса, хранящегося в кэше Интернета.</span><span class="sxs-lookup"><span data-stu-id="377dc-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="377dc-132">Это значение используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**\_ \_ обратный вызов параметра Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-134">1</span><span class="sxs-lookup"><span data-stu-id="377dc-134">1</span></span>
</dt> <dt>



<span data-ttu-id="377dc-135">Задает или получает адрес функции обратного вызова, определенной для этого маркера.</span><span class="sxs-lookup"><span data-stu-id="377dc-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="377dc-136">Этот параметр можно использовать для всех дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="377dc-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="377dc-137">Используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_ \_ фильтр обратного вызова параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-139">54</span><span class="sxs-lookup"><span data-stu-id="377dc-139">54</span></span>
</dt> <dt>



<span data-ttu-id="377dc-140">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_ \_ \_ контекст сертификата клиента для параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-142">84</span><span class="sxs-lookup"><span data-stu-id="377dc-142">84</span></span>
</dt> <dt>



<span data-ttu-id="377dc-143">Этот флаг не поддерживается [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="377dc-144">Параметр *лпбуффер* должен быть указателем на структуру [**\_ контекста сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) , а не указателем на указатель **\_ контекста сертификата** .</span><span class="sxs-lookup"><span data-stu-id="377dc-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="377dc-145">Если приложение получает **сообщение об ошибке " \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента Интернета**", он должен вызвать [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) или использовать [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) для предоставления сертификата перед повторной попыткой запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="377dc-146">Затем вызывается [**цертдупликатецертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) , чтобы переданный контекст сертификата можно было независимо освободить от приложения.</span><span class="sxs-lookup"><span data-stu-id="377dc-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**\_Страница параметров \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-148">68</span><span class="sxs-lookup"><span data-stu-id="377dc-148">68</span></span>
</dt> <dt>



<span data-ttu-id="377dc-149">По умолчанию узел или область центра URL-адреса в Юникоде кодируется в соответствии со спецификацией IDN.</span><span class="sxs-lookup"><span data-stu-id="377dc-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="377dc-150">Установка этого параметра для запроса или маркера соединения при отключенном IDN указывает схему кодировки кодовой страницы для части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="377dc-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="377dc-151">Параметр *лпбуффер* в вызове [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) содержит нужную кодовую страницу DBCS.</span><span class="sxs-lookup"><span data-stu-id="377dc-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="377dc-152">Если в *лпбуффер* не указана кодовая страница, WinInet использует системную кодовую страницу по умолчанию (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="377dc-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="377dc-153">Примечание. Этот параметр игнорируется, если IDN не отключены.</span><span class="sxs-lookup"><span data-stu-id="377dc-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="377dc-154">Дополнительные сведения об отключении IDN см. в разделе **параметр Интернета \_ \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="377dc-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="377dc-155">**Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (SP1):** Этот флаг не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="377dc-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="377dc-156">**Версия:** Требуется Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="377dc-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**\_ \_ путь к странице параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-158">100</span><span class="sxs-lookup"><span data-stu-id="377dc-158">100</span></span>
</dt> <dt>



<span data-ttu-id="377dc-159">По умолчанию часть пути URL-адреса кодируется в кодировке UTF8.</span><span class="sxs-lookup"><span data-stu-id="377dc-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="377dc-160">API WinINet выполняет escape-символ (%) Кодировка для старших символов.</span><span class="sxs-lookup"><span data-stu-id="377dc-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="377dc-161">Установка этого параметра для запроса или маркера подключения отключает кодирование UTF8 и задает определенную кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="377dc-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="377dc-162">Параметр *лпбуффер* в вызове [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) содержит нужную кодовую страницу DBCS для пути.</span><span class="sxs-lookup"><span data-stu-id="377dc-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="377dc-163">Если в *лпбуффер* не указана кодовая страница, WinInet использует по умолчанию CP \_ UTF8.</span><span class="sxs-lookup"><span data-stu-id="377dc-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="377dc-164">**Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (SP1):** Этот флаг не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="377dc-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="377dc-165">**Версия:** Требуется Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="377dc-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**\_ \_ Вспомогательная страница параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-167">101</span><span class="sxs-lookup"><span data-stu-id="377dc-167">101</span></span>
</dt> <dt>



<span data-ttu-id="377dc-168">По умолчанию часть пути в URL-адресе является системной кодовой страницей по умолчанию (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="377dc-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="377dc-169">Escape-символ (%) преобразования в дополнительной части не выполняются.</span><span class="sxs-lookup"><span data-stu-id="377dc-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="377dc-170">Установка этого параметра для запроса или маркера подключения отключает \_ кодировку CP ACP.</span><span class="sxs-lookup"><span data-stu-id="377dc-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="377dc-171">Параметр *лпбуффер* в вызове [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) содержит нужную кодовую страницу DBCS для дополнительной части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="377dc-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="377dc-172">Если в *лпбуффер* не указана кодовая страница, WinInet использует системную кодовую страницу по умолчанию (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="377dc-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="377dc-173">**Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (SP1):** Этот флаг не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="377dc-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="377dc-174">**Версия:** Требуется Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="377dc-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**параметр Интернета, \_ \_ Сжатая \_ \_ длина содержимого**</span><span class="sxs-lookup"><span data-stu-id="377dc-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-176">147</span><span class="sxs-lookup"><span data-stu-id="377dc-176">147</span></span>
</dt> <dt>



<span data-ttu-id="377dc-177">Для запроса, в котором WinInet распаковать предоставленное сервером кодирование содержимого, извлекает из сообщения о сервере содержимое ответа в виде УЛОНГЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="377dc-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="377dc-178">Поддерживается в Windows 10 версии 1507 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_подключение режима \_ подключения к \_ Интернету**</span><span class="sxs-lookup"><span data-stu-id="377dc-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-180">4</span><span class="sxs-lookup"><span data-stu-id="377dc-180">4</span></span>
</dt> <dt>



<span data-ttu-id="377dc-181">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**\_Параметры \_ подключения к Интернету, \_ повторные попытки**</span><span class="sxs-lookup"><span data-stu-id="377dc-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-183">3</span><span class="sxs-lookup"><span data-stu-id="377dc-183">3</span></span>
</dt> <dt>



<span data-ttu-id="377dc-184">Задает или получает длинное целое число без знака, которое содержит количество попыток WinINet выполнить разрешение и подключение к узлу.</span><span class="sxs-lookup"><span data-stu-id="377dc-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="377dc-185">Он пытается выполнить только один раз для каждого IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="377dc-185">It only attempts once per IP address.</span></span> <span data-ttu-id="377dc-186">Например, при попытке подключения к многодомашнему узлу с десятью IP-адресами и \_ \_ \_ повторными ПОПЫТКАМИ подключения через Интернет функция WinInet пытается разрешить и подключаться к первым семи IP-адресам.</span><span class="sxs-lookup"><span data-stu-id="377dc-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="377dc-187">И наоборот, если один набор из десяти IP-адресов установлен \_ \_ в значение 20, то функция \_ WinInet пытается выполнить каждую из десяти только один раз.</span><span class="sxs-lookup"><span data-stu-id="377dc-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="377dc-188">Если узел имеет только один IP-адрес и первая попытка соединения завершается неудачно, дальнейшие попытки не выполняются.</span><span class="sxs-lookup"><span data-stu-id="377dc-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="377dc-189">Если попытка соединения по-прежнему завершается ошибкой после указанного числа попыток, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="377dc-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="377dc-190">Значение по умолчанию для \_ параметра \_ подключения через Интернет \_ — пять попыток.</span><span class="sxs-lookup"><span data-stu-id="377dc-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="377dc-191">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) , включая маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="377dc-192">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**\_ \_ время подключения к \_ Интернету**</span><span class="sxs-lookup"><span data-stu-id="377dc-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-194">55</span><span class="sxs-lookup"><span data-stu-id="377dc-194">55</span></span>
</dt> <dt>



<span data-ttu-id="377dc-195">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_ \_ время ожидания подключения к Интернету \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-197">2</span><span class="sxs-lookup"><span data-stu-id="377dc-197">2</span></span>
</dt> <dt>



<span data-ttu-id="377dc-198">Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах), используемое для запросов на подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="377dc-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="377dc-199">Если установить для этого параметра значение Infinite (0xFFFFFFFF), этот таймер будет отключен.</span><span class="sxs-lookup"><span data-stu-id="377dc-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="377dc-200">Если запрос на соединение занимает больше времени, чем это значение, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="377dc-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="377dc-201">При попытке подключения к нескольким IP-адресам для одного узла (многодомашний узел) предельное время ожидания будет кумулятивным для всех IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="377dc-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="377dc-202">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) , включая маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="377dc-203">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_ \_ подключенное состояние "Интернет" \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-205">50</span><span class="sxs-lookup"><span data-stu-id="377dc-205">50</span></span>
</dt> <dt>



<span data-ttu-id="377dc-206">Задает или получает длинное целое число без знака, которое содержит состояние Connected.</span><span class="sxs-lookup"><span data-stu-id="377dc-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="377dc-207">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**\_ \_ значение контекстного параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-209">45</span><span class="sxs-lookup"><span data-stu-id="377dc-209">45</span></span>
</dt> <dt>



<span data-ttu-id="377dc-210">Задает или получает двойное слово типа DWORD \_ , содержащее адрес значения контекста, связанного с данным обработчиком [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="377dc-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="377dc-211">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="377dc-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="377dc-212">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-213">Ранее в этом случае в качестве значения контекста задается адрес, хранящийся в указателе **лпбуффер** .</span><span class="sxs-lookup"><span data-stu-id="377dc-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="377dc-214">Это было исправлено таким образом, что используется значение, хранящееся в буфере, а для флага [Internet \_ параметру " \_ контекст \_ значения"](/windows) задано новое значение.</span><span class="sxs-lookup"><span data-stu-id="377dc-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="377dc-215">Старое значение, 10, было сохранено таким образом, чтобы приложения, написанные для старого поведения, по-прежнему поддерживались.</span><span class="sxs-lookup"><span data-stu-id="377dc-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_ \_ \_ время ожидания получения элемента управления "параметр Интернета" \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-217">6</span><span class="sxs-lookup"><span data-stu-id="377dc-217">6</span></span>
</dt> <dt>



<span data-ttu-id="377dc-218">Аналогично [ \_ \_ \_ времени ожидания получения параметра Интернета](/windows).</span><span class="sxs-lookup"><span data-stu-id="377dc-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="377dc-219">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_ \_ \_ время ожидания отправки для управления параметром Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-221">5</span><span class="sxs-lookup"><span data-stu-id="377dc-221">5</span></span>
</dt> <dt>



<span data-ttu-id="377dc-222">Аналогично [ \_ \_ \_ времени ожидания отправки через Интернет](/windows).</span><span class="sxs-lookup"><span data-stu-id="377dc-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="377dc-223">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_ \_ \_ время ожидания получения данных для параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-225">8</span><span class="sxs-lookup"><span data-stu-id="377dc-225">8</span></span>
</dt> <dt>



<span data-ttu-id="377dc-226">Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах), которое получает ответ на запрос канала данных транзакции FTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="377dc-227">Если ответ длится дольше этого значения времени ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="377dc-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="377dc-228">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) , включая маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="377dc-229">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="377dc-230">Этот флаг не влияет на функциональность HTTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_ \_ \_ время ожидания отправки данных для параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-232">7</span><span class="sxs-lookup"><span data-stu-id="377dc-232">7</span></span>
</dt> <dt>



<span data-ttu-id="377dc-233">Задает или получает длинное целое число без знака в миллисекундах, которое содержит значение времени ожидания для отправки запроса к каналу данных транзакции FTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="377dc-234">Если отправка занимает больше времени, чем это значение, отправка отменяется.</span><span class="sxs-lookup"><span data-stu-id="377dc-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="377dc-235">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) , включая маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="377dc-236">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="377dc-237">Этот флаг не влияет на функциональность HTTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**\_ \_ имя файла параметров в \_ Интернете**</span><span class="sxs-lookup"><span data-stu-id="377dc-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-239">33</span><span class="sxs-lookup"><span data-stu-id="377dc-239">33</span></span>
</dt> <dt>



<span data-ttu-id="377dc-240">Извлекает строковое значение, содержащее имя файла, в котором хранится загруженная сущность.</span><span class="sxs-lookup"><span data-stu-id="377dc-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="377dc-241">Этот флаг действителен после завершения [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="377dc-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="377dc-242">Запрос к этому параметру можно запросить только с помощью [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**\_ \_ расширение файла параметров в \_ Интернете**</span><span class="sxs-lookup"><span data-stu-id="377dc-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-244">96</span><span class="sxs-lookup"><span data-stu-id="377dc-244">96</span></span>
</dt> <dt>



<span data-ttu-id="377dc-245">Задает строковое значение, содержащее расширение файла, в котором хранится скачанная сущность.</span><span class="sxs-lookup"><span data-stu-id="377dc-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="377dc-246">Этот флаг следует задать перед вызовом [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="377dc-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="377dc-247">Этот параметр может быть установлен только параметром [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**\_ \_ \_ сведения о сокете диагностики параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-249">67</span><span class="sxs-lookup"><span data-stu-id="377dc-249">67</span></span>
</dt> <dt>



<span data-ttu-id="377dc-250">Извлекает [**\_ \_ \_ информационную структуру сокета диагностики Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) , содержащую данные об указанном HTTP-запросе.</span><span class="sxs-lookup"><span data-stu-id="377dc-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="377dc-251">Этот флаг используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="377dc-252">**Windows 7:** Этот параметр больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="377dc-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET \_ \_ Load Digest \_ AUTH, \_ выгрузка**</span><span class="sxs-lookup"><span data-stu-id="377dc-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-254">76</span><span class="sxs-lookup"><span data-stu-id="377dc-254">76</span></span>
</dt> <dt>



<span data-ttu-id="377dc-255">Заставляет систему выйти из пакета SSPI для дайджест-проверки подлинности, что приведет к очистке всех учетных данных, созданных для процесса.</span><span class="sxs-lookup"><span data-stu-id="377dc-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="377dc-256">Для этого параметра не требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="377dc-256">No buffer is required for this option.</span></span> <span data-ttu-id="377dc-257">Он используется [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**\_параметр Интернета \_ Отключить \_ автонабор номера**</span><span class="sxs-lookup"><span data-stu-id="377dc-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-259">70</span><span class="sxs-lookup"><span data-stu-id="377dc-259">70</span></span>
</dt> <dt>



<span data-ttu-id="377dc-260">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**\_ \_ время ожидания отключенного режима Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-262">49</span><span class="sxs-lookup"><span data-stu-id="377dc-262">49</span></span>
</dt> <dt>



<span data-ttu-id="377dc-263">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**\_параметр Интернета \_ включить \_ \_ протокол HTTP**</span><span class="sxs-lookup"><span data-stu-id="377dc-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-265">148</span><span class="sxs-lookup"><span data-stu-id="377dc-265">148</span></span>
</dt> <dt>



<span data-ttu-id="377dc-266">Задает битовую маску DWORD допустимых расширенных версий HTTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="377dc-267">Может быть задан для любого типа обработчика.</span><span class="sxs-lookup"><span data-stu-id="377dc-267">May be set on any handle type.</span></span> <span data-ttu-id="377dc-268">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="377dc-268">Possible values are:</span></span>

-   <span data-ttu-id="377dc-269">\_Флаг протокола \_ HTTP \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="377dc-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="377dc-270">Поддерживается в Windows 10 версии 1507 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="377dc-271">Устаревшие версии протокола HTTP (1,1 и более ранних версий) нельзя отключить с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="377dc-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="377dc-272">Значение по умолчанию — 0x0.</span><span class="sxs-lookup"><span data-stu-id="377dc-272">The default is 0x0.</span></span> <span data-ttu-id="377dc-273">Поддерживается в Windows 10 версии 1507 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**\_параметр Интернета \_ включить \_ \_ чтение кэша перенаправления \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-275">122</span><span class="sxs-lookup"><span data-stu-id="377dc-275">122</span></span>
</dt> <dt>



<span data-ttu-id="377dc-276">В обработчике запроса задает логическое значение, определяющее, будут ли перенаправления возвращаться из кэша WinInet для данного запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="377dc-277">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="377dc-277">The default is FALSE.</span></span> <span data-ttu-id="377dc-278">Поддерживается в Windows 8 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**\_дополнительный формат \_ шифрования \_ параметров Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-280">155</span><span class="sxs-lookup"><span data-stu-id="377dc-280">155</span></span>
</dt> <dt>



<span data-ttu-id="377dc-281">Возвращает или задает логическое значение, указывающее, следует ли кодировать символы, не входящие в набор ASCII, в строке запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="377dc-282">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="377dc-282">The default is FALSE.</span></span> <span data-ttu-id="377dc-283">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**подключение к Интернету для \_ параметра Internet \_ \_ Explorer \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-285">42</span><span class="sxs-lookup"><span data-stu-id="377dc-285">42</span></span>
</dt> <dt>



<span data-ttu-id="377dc-286">Сбрасывает неиспользуемые записи из кэша паролей на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="377dc-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="377dc-287">Также сбрасывает время кэширования, используемое, когда режим синхронизации один раз в сеансе.</span><span class="sxs-lookup"><span data-stu-id="377dc-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="377dc-288">Для этого параметра не требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="377dc-288">No buffer is required for this option.</span></span> <span data-ttu-id="377dc-289">Он используется [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_ \_ Маска ошибки параметра \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-291">62</span><span class="sxs-lookup"><span data-stu-id="377dc-291">62</span></span>
</dt> <dt>



<span data-ttu-id="377dc-292">Задает длинное целочисленное значение без знака, содержащее маски ошибок, которые могут обрабатываться клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="377dc-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="377dc-293">Это может быть сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="377dc-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="377dc-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>\_общий сертификат маски ошибок Интернета (в \_ \_ \_ секундах \_ )</span><span class="sxs-lookup"><span data-stu-id="377dc-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-295">0x2</span><span class="sxs-lookup"><span data-stu-id="377dc-295">0x2</span></span>

<span data-ttu-id="377dc-296">Указывает, что все ошибки сертификата должны выводиться с использованием одного и того же возврата ошибки, а именно — **ошибки \_ \_ \_ сертификата \_ в Интернете**.</span><span class="sxs-lookup"><span data-stu-id="377dc-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="377dc-297">Если этот флаг установлен, вызовите **интернетеррордлг** после получения ошибки **с ошибками \_ \_ \_ сертификата \_ Internet sec** , чтобы пользователь мог ответить на знакомое диалоговое окно с описанием проблемы.</span><span class="sxs-lookup"><span data-stu-id="377dc-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="377dc-298">Невозможность информирования пользователя об этой ошибке предоставляет пользователю возможность обманных атак.</span><span class="sxs-lookup"><span data-stu-id="377dc-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="377dc-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>\_Маска ошибки Интернета при \_ \_ вставке \_ компакт</span><span class="sxs-lookup"><span data-stu-id="377dc-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="377dc-300">0x1</span><span class="sxs-lookup"><span data-stu-id="377dc-300">0x1</span></span>

<span data-ttu-id="377dc-301">Указывает, что клиентское приложение может выполнить ошибку код ошибки при **\_ \_ вставке \_ в Интернет** .</span><span class="sxs-lookup"><span data-stu-id="377dc-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>Ошибка \_ подключения к ошибке \_ \_ при входе в сеть \_ \_ Отображение \_ \_ тела сущности</span><span class="sxs-lookup"><span data-stu-id="377dc-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="377dc-303">0x8</span><span class="sxs-lookup"><span data-stu-id="377dc-303">0x8</span></span>

<span data-ttu-id="377dc-304">Указывает, что клиентское приложение может обработано **сообщение об ошибке входа в Интернет ошибка при входе в систему. код ошибки \_ \_ \_ \_ \_ \_ тела объекта** .</span><span class="sxs-lookup"><span data-stu-id="377dc-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>для \_ маски ошибок Интернета \_ \_ требуется пакет \_ MSN \_ SSPI \_ pkg</span><span class="sxs-lookup"><span data-stu-id="377dc-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="377dc-306">0x4</span><span class="sxs-lookup"><span data-stu-id="377dc-306">0x4</span></span>

<span data-ttu-id="377dc-307">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="377dc-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**\_ \_ Корпоративный контекст "параметр Интернета" \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-309">159</span><span class="sxs-lookup"><span data-stu-id="377dc-309">159</span></span>
</dt> <dt>



<span data-ttu-id="377dc-310">Задает ПВСТР, содержащий идентификатор предприятия (см https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) . раздел, который применяется к запросу.</span><span class="sxs-lookup"><span data-stu-id="377dc-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="377dc-311">Поддерживается в Windows 10 версии 1507 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_ \_ Расширенная ошибка в ПАРАМЕТРах Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-313">24</span><span class="sxs-lookup"><span data-stu-id="377dc-313">24</span></span>
</dt> <dt>



<span data-ttu-id="377dc-314">Извлекает длинное целое число без знака, содержащее код ошибки Winsock, сопоставленный с сообщением об ошибке **\_ Интернета \_** , которые были возвращены в этом контексте потока.</span><span class="sxs-lookup"><span data-stu-id="377dc-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="377dc-315">Этот параметр используется для **нулевого**[**хинтернет**](appendix-a-hinternet-handles.md) -маркера [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_параметр Интернета \_ из \_ \_ времени ожидания кэша**</span><span class="sxs-lookup"><span data-stu-id="377dc-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-317">63</span><span class="sxs-lookup"><span data-stu-id="377dc-317">63</span></span>
</dt> <dt>



<span data-ttu-id="377dc-318">Задает или получает A1N длинное целое число без знака, которое содержит период времени, в течение которого система должна ожидать ответа на сетевой запрос, прежде чем проверять кэш для копии ресурса.</span><span class="sxs-lookup"><span data-stu-id="377dc-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="377dc-319">Если сетевой запрос занимает больше времени, чем указано, а запрошенный ресурс доступен в кэше, ресурс извлекается из кэша.</span><span class="sxs-lookup"><span data-stu-id="377dc-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="377dc-320">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**\_ \_ тип обработчика параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-322">9</span><span class="sxs-lookup"><span data-stu-id="377dc-322">9</span></span>
</dt> <dt>



<span data-ttu-id="377dc-323">Извлекает длинное целое число без знака, содержащее тип переданных дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="377dc-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="377dc-324">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) в любом обработчике [хинтернет](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="377dc-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="377dc-325">Возможные возвращаемые значения включают следующее.</span><span class="sxs-lookup"><span data-stu-id="377dc-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="377dc-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>\_тип веб \_ -обработчика \_ подключение \_ FTP</span><span class="sxs-lookup"><span data-stu-id="377dc-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="377dc-327">2</span><span class="sxs-lookup"><span data-stu-id="377dc-327">2</span></span>

</dd> <dt>

<span data-ttu-id="377dc-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>\_тип обработчика Интернета \_ \_ Connect \_ Gopher</span><span class="sxs-lookup"><span data-stu-id="377dc-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="377dc-329">3</span><span class="sxs-lookup"><span data-stu-id="377dc-329">3</span></span>

</dd> <dt>

<span data-ttu-id="377dc-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>\_тип обработчика Интернета \_ \_ подключение \_ http</span><span class="sxs-lookup"><span data-stu-id="377dc-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="377dc-331">4</span><span class="sxs-lookup"><span data-stu-id="377dc-331">4</span></span>

</dd> <dt>

<span data-ttu-id="377dc-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_ \_ \_ запрос файла типа для обработчика Интернета \_</span><span class="sxs-lookup"><span data-stu-id="377dc-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="377dc-333">14</span><span class="sxs-lookup"><span data-stu-id="377dc-333">14</span></span>

</dd> <dt>

<span data-ttu-id="377dc-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>\_тип обработчика Интернета \_ \_ FTP- \_ файл</span><span class="sxs-lookup"><span data-stu-id="377dc-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-335">7</span><span class="sxs-lookup"><span data-stu-id="377dc-335">7</span></span>

</dd> <dt>

<span data-ttu-id="377dc-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>\_тип обработчика Интернета — \_ \_ \_ \_ HTML-файл</span><span class="sxs-lookup"><span data-stu-id="377dc-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="377dc-337">8</span><span class="sxs-lookup"><span data-stu-id="377dc-337">8</span></span>

</dd> <dt>

<span data-ttu-id="377dc-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>\_тип обработчика Интернета \_ \_ \_ Find FTP</span><span class="sxs-lookup"><span data-stu-id="377dc-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="377dc-339">5</span><span class="sxs-lookup"><span data-stu-id="377dc-339">5</span></span>

</dd> <dt>

<span data-ttu-id="377dc-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>тип веб- \_ обработчика \_ \_ \_ Поиск \_ HTML</span><span class="sxs-lookup"><span data-stu-id="377dc-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="377dc-341">6</span><span class="sxs-lookup"><span data-stu-id="377dc-341">6</span></span>

</dd> <dt>

<span data-ttu-id="377dc-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_тип обработчика Интернета — \_ \_ \_ файл gopher</span><span class="sxs-lookup"><span data-stu-id="377dc-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-343">11</span><span class="sxs-lookup"><span data-stu-id="377dc-343">11</span></span>

</dd> <dt>

<span data-ttu-id="377dc-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>\_тип обработчика Интернета. \_ \_ \_ \_ код HTML-файла gopher</span><span class="sxs-lookup"><span data-stu-id="377dc-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="377dc-345">12</span><span class="sxs-lookup"><span data-stu-id="377dc-345">12</span></span>

</dd> <dt>

<span data-ttu-id="377dc-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>Тип обработчика Интернета, поиск по протоколу \_ \_ \_ Gopher \_</span><span class="sxs-lookup"><span data-stu-id="377dc-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="377dc-347">9</span><span class="sxs-lookup"><span data-stu-id="377dc-347">9</span></span>

</dd> <dt>

<span data-ttu-id="377dc-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>\_тип обработчика Интернета — \_ \_ \_ найти \_ HTML</span><span class="sxs-lookup"><span data-stu-id="377dc-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="377dc-349">10</span><span class="sxs-lookup"><span data-stu-id="377dc-349">10</span></span>

</dd> <dt>

<span data-ttu-id="377dc-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ \_ http-запрос типа "тип обработчика" \_</span><span class="sxs-lookup"><span data-stu-id="377dc-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="377dc-351">13</span><span class="sxs-lookup"><span data-stu-id="377dc-351">13</span></span>

</dd> <dt>

<span data-ttu-id="377dc-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>\_тип обработчика Интернета \_ \_</span><span class="sxs-lookup"><span data-stu-id="377dc-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="377dc-353">1</span><span class="sxs-lookup"><span data-stu-id="377dc-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="377dc-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**\_параметр Интернета \_ HSTS**</span><span class="sxs-lookup"><span data-stu-id="377dc-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-355">157</span><span class="sxs-lookup"><span data-stu-id="377dc-355">157</span></span>
</dt> <dt>



<span data-ttu-id="377dc-356">Получает или задает логическое значение, указывающее, должна ли WinInet следовать директивам HTTP с протоколом безопасности транспорта (HSTS) на серверах.</span><span class="sxs-lookup"><span data-stu-id="377dc-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="377dc-357">Если этот параметр включен, https://запросы к доменам, которые имеют политику HSTS, кэшированную WinInet, будут перенаправляться на соответствующие URL-адреса https://.</span><span class="sxs-lookup"><span data-stu-id="377dc-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="377dc-358">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="377dc-358">The default is FALSE.</span></span> <span data-ttu-id="377dc-359">Поддерживается в Windows 8.1 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**\_возможность \_ \_ декодирования HTTP в Интернете**</span><span class="sxs-lookup"><span data-stu-id="377dc-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-361">65</span><span class="sxs-lookup"><span data-stu-id="377dc-361">65</span></span>
</dt> <dt>



<span data-ttu-id="377dc-362">Позволяет WinINet выполнять декодирование для схем кодирования gzip и Deflate.</span><span class="sxs-lookup"><span data-stu-id="377dc-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="377dc-363">Дополнительные сведения см. в разделе [**кодирование содержимого**](content-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="377dc-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**\_ \_ \_ используемый протокол HTTP (Internet) \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-365">149</span><span class="sxs-lookup"><span data-stu-id="377dc-365">149</span></span>
</dt> <dt>



<span data-ttu-id="377dc-366">Возвращает значение типа DWORD, указывающее, какая расширенная версия HTTP использовалась для данного запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="377dc-367">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="377dc-367">Possible values are:</span></span>

-   <span data-ttu-id="377dc-368">\_Флаг протокола \_ HTTP \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="377dc-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="377dc-369">Поддерживается в Windows 10 версии 1507 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="377dc-370">0x0 указывает HTTP/1.1 или более раннюю версию; \_ \_ \_ Если требуется больше точности, чем используется устаревшая версия, см. раздел HTTP-версия с параметром Internet.</span><span class="sxs-lookup"><span data-stu-id="377dc-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="377dc-371">Поддерживается в Windows 10 версии 1507 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**\_ \_ Версия HTTP параметра \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="377dc-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-373">59</span><span class="sxs-lookup"><span data-stu-id="377dc-373">59</span></span>
</dt> <dt>



<span data-ttu-id="377dc-374">Задает или получает структуру [**\_ \_ сведений о версии HTTP**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) , которая содержит поддерживаемую версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="377dc-375">Он должен использоваться для маркера **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="377dc-376">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="377dc-377">В Windows 7, Windows Server 2008 R2 и более поздних версиях значение элемента **двминорверсион** в структуре [**\_ \_ сведений о версии HTTP**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) переопределяется параметрами Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="377dc-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="377dc-378">**EnableHttp1 \_ 1** — это значение реестра в разделе **HKLM \\ Software \\ Microsoft \\ InternetExplorer \\ Адвакнедоптионс \\ HTTP \\ женабле** , которое управляется параметрами Интернета, установленными в Internet Explorer для системы.</span><span class="sxs-lookup"><span data-stu-id="377dc-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="377dc-379">Значение **EnableHttp1 \_ 1** по умолчанию равно 1.</span><span class="sxs-lookup"><span data-stu-id="377dc-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="377dc-380">Структура **\_ \_ сведений о версии HTTP** игнорируется для любой версии HTTP меньше 1,1, если для **EnableHttp1 \_ 1** задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="377dc-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**\_ \_ удостоверение параметра Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-382">78</span><span class="sxs-lookup"><span data-stu-id="377dc-382">78</span></span>
</dt> <dt>



<span data-ttu-id="377dc-383">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**\_режим \_ ПРОСТОя \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-385">51</span><span class="sxs-lookup"><span data-stu-id="377dc-385">51</span></span>
</dt> <dt>



<span data-ttu-id="377dc-386">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**\_параметр Интернета \_ IDN**</span><span class="sxs-lookup"><span data-stu-id="377dc-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-388">102</span><span class="sxs-lookup"><span data-stu-id="377dc-388">102</span></span>
</dt> <dt>



<span data-ttu-id="377dc-389">По умолчанию узел или область полномочий в URL-адресе кодируется в соответствии со спецификацией IDN как для прямых, так и для прокси-подключений.</span><span class="sxs-lookup"><span data-stu-id="377dc-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="377dc-390">Этот параметр можно использовать в запросе или в обработчике соединения для включения или отключения IDN.</span><span class="sxs-lookup"><span data-stu-id="377dc-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="377dc-391">Если IDN отключены, WinINet использует системную кодовую страницу для кодирования части узла или центра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="377dc-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="377dc-392">Чтобы отключить преобразование узла IDN, задайте для параметра *лпбуффер* в вызове [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) значение 0.</span><span class="sxs-lookup"><span data-stu-id="377dc-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="377dc-393">Чтобы включить преобразование IDN только в прямом соединении, **укажите \_ флаг Интернета \_ IDN \_ Direct** в параметре *лпбуффер* в вызове **интернетсетоптион**.</span><span class="sxs-lookup"><span data-stu-id="377dc-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="377dc-394">Чтобы включить преобразование IDN только для прокси-соединения, укажите **\_ флаг Internet \_ \_ proxy IDN** в параметре *лпбуффер* в вызове **интернетсетоптион**.</span><span class="sxs-lookup"><span data-stu-id="377dc-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="377dc-395">**Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (SP1):** Этот флаг не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="377dc-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="377dc-396">**Версия:** Требуется Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="377dc-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**\_параметр "в Интернете" \_ игнорировать " \_ вне сети"**</span><span class="sxs-lookup"><span data-stu-id="377dc-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-398">77</span><span class="sxs-lookup"><span data-stu-id="377dc-398">77</span></span>
</dt> <dt>



<span data-ttu-id="377dc-399">Задает или получает значение, определяющее, пропускается ли флаг глобального автономного режима для указанного маркера запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="377dc-400">Для этого параметра не требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="377dc-400">No buffer is required for this option.</span></span> <span data-ttu-id="377dc-401">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) с маркером запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="377dc-402">Этот параметр допустим только в Internet Explorer 5 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**\_возможность \_ \_ подключения к Интернету**</span><span class="sxs-lookup"><span data-stu-id="377dc-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-404">22</span><span class="sxs-lookup"><span data-stu-id="377dc-404">22</span></span>
</dt> <dt>



<span data-ttu-id="377dc-405">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_параметр " \_ \_ время ожидания прослушивания через Интернет"**</span><span class="sxs-lookup"><span data-stu-id="377dc-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-407">11</span><span class="sxs-lookup"><span data-stu-id="377dc-407">11</span></span>
</dt> <dt>



<span data-ttu-id="377dc-408">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**\_Параметр Интернета \_ Максимальное число подключений \_ \_ на \_ \_ сервер 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-410">74</span><span class="sxs-lookup"><span data-stu-id="377dc-410">74</span></span>
</dt> <dt>



<span data-ttu-id="377dc-411">Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="377dc-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="377dc-412">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-413">Этот параметр допустим только в Internet Explorer 5 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_параметр Интернета \_ Максимальное число \_ \_ подключений на \_ прокси-сервер**</span><span class="sxs-lookup"><span data-stu-id="377dc-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-415">103</span><span class="sxs-lookup"><span data-stu-id="377dc-415">103</span></span>
</dt> <dt>



<span data-ttu-id="377dc-416">Задает или получает длинное целое число без знака, содержащее максимальное число разрешенных подключений для прокси-сервера CERN.</span><span class="sxs-lookup"><span data-stu-id="377dc-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="377dc-417">При установке или получении этого параметра для параметра *хинтернет* должно быть задано значение Handle, равное **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="377dc-418">Значение маркера **null** указывает, что параметр должен быть установлен или запрошен для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="377dc-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="377dc-419">При вызове [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) с этим параметром все существующие прокси-объекты получат новое значение.</span><span class="sxs-lookup"><span data-stu-id="377dc-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="377dc-420">Это значение ограничено диапазоном от 2 до 128 включительно.</span><span class="sxs-lookup"><span data-stu-id="377dc-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="377dc-421">**Версия:** Требуется Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="377dc-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**\_параметр " \_ Максимальное число подключений в Интернете" \_ \_ на \_ сервер**</span><span class="sxs-lookup"><span data-stu-id="377dc-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-423">73</span><span class="sxs-lookup"><span data-stu-id="377dc-423">73</span></span>
</dt> <dt>



<span data-ttu-id="377dc-424">Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер.</span><span class="sxs-lookup"><span data-stu-id="377dc-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="377dc-425">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-426">Этот параметр допустим только в Internet Explorer 5 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**режим "в сети Интернет \_ " \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-428">26</span><span class="sxs-lookup"><span data-stu-id="377dc-428">26</span></span>
</dt> <dt>



<span data-ttu-id="377dc-429">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_семантика режима "в Интернете" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-431">52</span><span class="sxs-lookup"><span data-stu-id="377dc-431">52</span></span>
</dt> <dt>



<span data-ttu-id="377dc-432">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_параметр Интернета \_ OPT \_ в \_ ненадежной \_ подписи**</span><span class="sxs-lookup"><span data-stu-id="377dc-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-434">176</span><span class="sxs-lookup"><span data-stu-id="377dc-434">176</span></span>
</dt> <dt>



<span data-ttu-id="377dc-435">Явное согласие на ненадежные подписи (например, SHA-1) считается небезопасным.</span><span class="sxs-lookup"><span data-stu-id="377dc-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="377dc-436">Это позволит WinInet вызывать [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) , используя параметр **\_ \_ \_ \_ ненадежной \_ подписи в цепочке сертификатов** .</span><span class="sxs-lookup"><span data-stu-id="377dc-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ родительский маркер параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-438">21</span><span class="sxs-lookup"><span data-stu-id="377dc-438">21</span></span>
</dt> <dt>



<span data-ttu-id="377dc-439">Получает родительский маркер для этого маркера.</span><span class="sxs-lookup"><span data-stu-id="377dc-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="377dc-440">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) с помощью [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**\_пароль для параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-442">29</span><span class="sxs-lookup"><span data-stu-id="377dc-442">29</span></span>
</dt> <dt>



<span data-ttu-id="377dc-443">Задает или получает строковое значение, содержащее пароль, связанный с маркером, возвращенным [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="377dc-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="377dc-444">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**параметр \_ "Интернет" \_ для \_ подключения \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-446">75</span><span class="sxs-lookup"><span data-stu-id="377dc-446">75</span></span>
</dt> <dt>



<span data-ttu-id="377dc-447">Задает или получает структуру [**\_ \_ \_ \_ списка**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) параметров в Интернете, указывающую список параметров для конкретного соединения.</span><span class="sxs-lookup"><span data-stu-id="377dc-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="377dc-448">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-449">Этот параметр допустим только в Internet Explorer 5 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="377dc-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="377dc-450">**Интернет \_ ПАРАМЕТР \_ для \_ каждого \_ подключения** приводит к изменению параметров на уровне системы, когда в вызове [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)используется маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-451">Чтобы обновить глобальные параметры прокси-сервера, необходимо вызвать **интернетсетоптион** с помощью флага параметра **\_ \_ обновления Internet** .</span><span class="sxs-lookup"><span data-stu-id="377dc-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="377dc-452">Чтобы изменить сведения о прокси-сервере для всего процесса, не влияя на глобальные параметры Internet Explorer 5 и более поздних версий, используйте этот параметр для маркера, возвращаемого из [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="377dc-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="377dc-453">В следующем примере кода изменяется прокси-сервер для всего процесса, несмотря на то, что обработчик [**хинтернет**](appendix-a-hinternet-handles.md) закрыт и не используется ни одним запросом.</span><span class="sxs-lookup"><span data-stu-id="377dc-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="377dc-454">Дополнительные сведения и примеры кода см. в [статье базы знаний 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="377dc-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_Политика параметров \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-456">48</span><span class="sxs-lookup"><span data-stu-id="377dc-456">48</span></span>
</dt> <dt>



<span data-ttu-id="377dc-457">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_ \_ прокси-сервер параметров Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-459">38</span><span class="sxs-lookup"><span data-stu-id="377dc-459">38</span></span>
</dt> <dt>



<span data-ttu-id="377dc-460">Задает или получает информационную структуру [**Интернет \_ - \_ прокси**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) , которая содержит данные прокси-сервера для существующего обработчика [**Интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , если [**хинтернет**](appendix-a-hinternet-handles.md) -значение не равно **null**.</span><span class="sxs-lookup"><span data-stu-id="377dc-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="377dc-461">Если обработчик [**хинтернет**](appendix-a-hinternet-handles.md) имеет **значение NULL**, функция устанавливает или запрашивает данные глобального прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="377dc-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="377dc-462">Этот параметр можно использовать с маркером, возвращаемым функцией **интернетопен**.</span><span class="sxs-lookup"><span data-stu-id="377dc-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="377dc-463">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="377dc-464">\_ \_ \_ \_ Вместо \_ прокси-сервера параметров Интернета рекомендуется использовать параметр Интернет для каждого подключения \_ .</span><span class="sxs-lookup"><span data-stu-id="377dc-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="377dc-465">Дополнительные сведения см. в [статье базы знаний 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="377dc-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_ \_ пароль прокси-сервера для Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-467">44</span><span class="sxs-lookup"><span data-stu-id="377dc-467">44</span></span>
</dt> <dt>



<span data-ttu-id="377dc-468">Задает или получает строковое значение, содержащее пароль, используемый для доступа к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="377dc-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="377dc-469">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-470">Этот параметр можно задать для маркера, возвращаемого [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="377dc-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**\_ \_ Параметры прокси-сервера для параметров Интернета \_ \_ изменены**</span><span class="sxs-lookup"><span data-stu-id="377dc-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-472">95</span><span class="sxs-lookup"><span data-stu-id="377dc-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="377dc-473">Оповещает текущий экземпляр WinInet о том, что параметры прокси-сервера изменились и должны быть обновлены с учетом новых параметров.</span><span class="sxs-lookup"><span data-stu-id="377dc-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="377dc-474">Чтобы оповестить все доступные экземпляры WinInet, присвойте  параметру buffer [](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) параметра интернетсетоптион **значение NULL** , а *BufferLength* — 0 при передаче этого параметра.</span><span class="sxs-lookup"><span data-stu-id="377dc-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="377dc-475">Этот параметр можно задать для маркера, возвращаемого [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="377dc-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_ \_ имя пользователя прокси-сервера для Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-477">43</span><span class="sxs-lookup"><span data-stu-id="377dc-477">43</span></span>
</dt> <dt>



<span data-ttu-id="377dc-478">Задает или получает строковое значение, содержащее имя пользователя, используемое для доступа к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="377dc-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="377dc-479">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-480">Этот параметр можно задать для маркера, возвращаемого [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="377dc-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_ \_ \_ Размер буфера чтения параметра \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-482">12</span><span class="sxs-lookup"><span data-stu-id="377dc-482">12</span></span>
</dt> <dt>



<span data-ttu-id="377dc-483">Задает или получает длинное целочисленное значение без знака, которое содержит размер буфера чтения.</span><span class="sxs-lookup"><span data-stu-id="377dc-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="377dc-484">Этот параметр можно использовать для дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) , возвращаемых [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)и [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (только сеанс FTP).</span><span class="sxs-lookup"><span data-stu-id="377dc-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="377dc-485">Этот параметр используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**\_ \_ пропускная способность получения параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-487">57</span><span class="sxs-lookup"><span data-stu-id="377dc-487">57</span></span>
</dt> <dt>



<span data-ttu-id="377dc-488">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_ \_ время ожидания получения параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-490">6</span><span class="sxs-lookup"><span data-stu-id="377dc-490">6</span></span>
</dt> <dt>



<span data-ttu-id="377dc-491">Задает или получает длинное целое число без знака, которое содержит значение времени ожидания в миллисекундах для получения ответа на запрос.</span><span class="sxs-lookup"><span data-stu-id="377dc-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="377dc-492">Если ответ длится дольше этого значения времени ожидания, запрос отменяется.</span><span class="sxs-lookup"><span data-stu-id="377dc-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="377dc-493">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) , включая маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="377dc-494">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="377dc-495">Этот параметр не предназначен для точного представления времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="377dc-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="377dc-496">Время ожидания может истечет до шести секунд после установленного значения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="377dc-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="377dc-497">При использовании в ссылке на FTP-транзакцию этот параметр относится к каналу управления.</span><span class="sxs-lookup"><span data-stu-id="377dc-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**\_Обновление параметров \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-499">37</span><span class="sxs-lookup"><span data-stu-id="377dc-499">37</span></span>
</dt> <dt>



<span data-ttu-id="377dc-500">Вызывает перечтение данных прокси-сервера из реестра для обработчика.</span><span class="sxs-lookup"><span data-stu-id="377dc-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="377dc-501">Буфер не требуется.</span><span class="sxs-lookup"><span data-stu-id="377dc-501">No buffer is required.</span></span> <span data-ttu-id="377dc-502">Этот параметр можно использовать для маркера [**хинтернет**](appendix-a-hinternet-handles.md) , возвращаемого [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="377dc-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="377dc-503">Он используется [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**\_параметр Internet \_ Remove \_ Identity**</span><span class="sxs-lookup"><span data-stu-id="377dc-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-505">79</span><span class="sxs-lookup"><span data-stu-id="377dc-505">79</span></span>
</dt> <dt>



<span data-ttu-id="377dc-506">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_ \_ флаги запроса параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-508">23</span><span class="sxs-lookup"><span data-stu-id="377dc-508">23</span></span>
</dt> <dt>



<span data-ttu-id="377dc-509">Извлекает длинное целое число без знака, содержащее специальные флаги состояния, которые указывают состояние процесса скачивания.</span><span class="sxs-lookup"><span data-stu-id="377dc-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="377dc-510">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="377dc-511">Параметр [Интернет \_ — \_ \_ флаги запроса](/windows) может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="377dc-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="377dc-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>Интернет \_ рекфлаг \_ Async</span><span class="sxs-lookup"><span data-stu-id="377dc-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="377dc-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="377dc-513">0x00000002</span></span>

<span data-ttu-id="377dc-514">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_запись кэша РЕКФЛАГ через Интернет \_ \_ \_ отключена</span><span class="sxs-lookup"><span data-stu-id="377dc-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="377dc-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="377dc-516">0x00000040</span></span>

<span data-ttu-id="377dc-517">Интернет-запрос не может быть кэширован (например, HTTPS-запрос).</span><span class="sxs-lookup"><span data-stu-id="377dc-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>Интернет \_ рекфлаг \_ из \_ кэша</span><span class="sxs-lookup"><span data-stu-id="377dc-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="377dc-519">0x00000001</span></span>

<span data-ttu-id="377dc-520">Ответ получен из кэша.</span><span class="sxs-lookup"><span data-stu-id="377dc-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>\_ \_ время ожидания Internet рекфлаг NET \_</span><span class="sxs-lookup"><span data-stu-id="377dc-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="377dc-522">0x00000080</span></span>

<span data-ttu-id="377dc-523">Время ожидания Интернет – запроса истекло.</span><span class="sxs-lookup"><span data-stu-id="377dc-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>Интернет \_ рекфлаг \_ без \_ заголовков</span><span class="sxs-lookup"><span data-stu-id="377dc-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="377dc-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="377dc-525">0x00000008</span></span>

<span data-ttu-id="377dc-526">Исходный ответ не содержал заголовков.</span><span class="sxs-lookup"><span data-stu-id="377dc-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>\_ \_ пассивный Интернет рекфлаг</span><span class="sxs-lookup"><span data-stu-id="377dc-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="377dc-528">0x00000010</span></span>

<span data-ttu-id="377dc-529">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>Интернет \_ рекфлаг \_ через \_ прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="377dc-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="377dc-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="377dc-531">0x00000004</span></span>

<span data-ttu-id="377dc-532">Запрос выполнен через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="377dc-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="377dc-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**\_ \_ приоритет запроса параметра \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-534">58</span><span class="sxs-lookup"><span data-stu-id="377dc-534">58</span></span>
</dt> <dt>



<span data-ttu-id="377dc-535">Задает или получает длинное целое число без знака, которое содержит приоритет запросов, которые конкурируют за соединение в HTTP-маркере.</span><span class="sxs-lookup"><span data-stu-id="377dc-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="377dc-536">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_Сброс параметров \_ Интернета \_ урлкаче \_ сеанс**</span><span class="sxs-lookup"><span data-stu-id="377dc-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-538">60</span><span class="sxs-lookup"><span data-stu-id="377dc-538">60</span></span>
</dt> <dt>



<span data-ttu-id="377dc-539">Запускает новый сеанс кэша для процесса.</span><span class="sxs-lookup"><span data-stu-id="377dc-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="377dc-540">Буфер не требуется.</span><span class="sxs-lookup"><span data-stu-id="377dc-540">No buffer is required.</span></span> <span data-ttu-id="377dc-541">Он используется [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-542">Этот параметр зарезервирован только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="377dc-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_ \_ дополнительный \_ ключ кэша при выборе в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-544">53</span><span class="sxs-lookup"><span data-stu-id="377dc-544">53</span></span>
</dt> <dt>



<span data-ttu-id="377dc-545">Задает или получает строковое значение, содержащее ключ вторичного кэша.</span><span class="sxs-lookup"><span data-stu-id="377dc-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="377dc-546">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="377dc-547">Этот параметр зарезервирован только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="377dc-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**\_ \_ сертификат безопасности параметров \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-549">35</span><span class="sxs-lookup"><span data-stu-id="377dc-549">35</span></span>
</dt> <dt>



<span data-ttu-id="377dc-550">Извлекает сертификат для сервера SSL/PCT (SSL и частных коммуникаций) в отформатированную строку.</span><span class="sxs-lookup"><span data-stu-id="377dc-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="377dc-551">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_ \_ \_ Структура сертификата безопасности параметра \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="377dc-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-553">32</span><span class="sxs-lookup"><span data-stu-id="377dc-553">32</span></span>
</dt> <dt>



<span data-ttu-id="377dc-554">Извлекает сертификат для сервера SSL/PCT в \_ \_ структуру сведений о сертификате Интернета.</span><span class="sxs-lookup"><span data-stu-id="377dc-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="377dc-555">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**\_ \_ Флаги безопасности Internet Option \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-557">31</span><span class="sxs-lookup"><span data-stu-id="377dc-557">31</span></span>
</dt> <dt>



<span data-ttu-id="377dc-558">Извлекает длинное целочисленное значение без знака, содержащее флаги безопасности для маркера.</span><span class="sxs-lookup"><span data-stu-id="377dc-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="377dc-559">Этот параметр используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="377dc-560">Это может быть сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="377dc-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="377dc-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>\_Флаг безопасности \_ 128BIT</span><span class="sxs-lookup"><span data-stu-id="377dc-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="377dc-562">0x20000000</span></span>

<span data-ttu-id="377dc-563">Идентично значению [ \_ флага \_ \_ безопасности](/windows)предпочтительного значения.</span><span class="sxs-lookup"><span data-stu-id="377dc-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="377dc-564">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>\_Флаг безопасности \_ 40BIT</span><span class="sxs-lookup"><span data-stu-id="377dc-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="377dc-566">0x10000000</span></span>

<span data-ttu-id="377dc-567">Аналогично [ \_ \_ \_ ненадежной стойкости флага безопасности](/windows)значения.</span><span class="sxs-lookup"><span data-stu-id="377dc-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="377dc-568">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>\_Флаг безопасности \_ 56BIT</span><span class="sxs-lookup"><span data-stu-id="377dc-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="377dc-570">0x40000000</span></span>

<span data-ttu-id="377dc-571">То же, что и предпочтительный уровень [ \_ стойкости флага \_ \_ безопасности](/windows)значения.</span><span class="sxs-lookup"><span data-stu-id="377dc-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="377dc-572">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>\_флаг безопасности \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="377dc-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="377dc-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="377dc-574">0x08000000</span></span>

<span data-ttu-id="377dc-575">Указывает, что было использовано значение Fortezza, чтобы обеспечить безопасность, проверку подлинности и (или) целостность для указанного соединения.</span><span class="sxs-lookup"><span data-stu-id="377dc-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>\_Флаг безопасности \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="377dc-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="377dc-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="377dc-577">0x00000020</span></span>

<span data-ttu-id="377dc-578">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_флаг безопасности \_ игнорирует \_ \_ недопустимое общее имя сертификата \_</span><span class="sxs-lookup"><span data-stu-id="377dc-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="377dc-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="377dc-580">0x00001000</span></span>

<span data-ttu-id="377dc-581">Игнорирует ошибку "Общее сообщение об ошибке [ \_ \_ с \_ \_ \_ недопустимым сертификатом Internet sec](wininet-errors.md) ".</span><span class="sxs-lookup"><span data-stu-id="377dc-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>\_ \_ \_ \_ Недопустимый срок игнорирования даты сертификата \_ для флага безопасности</span><span class="sxs-lookup"><span data-stu-id="377dc-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="377dc-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="377dc-583">0x00002000</span></span>

<span data-ttu-id="377dc-584">Игнорирует сообщение [об ошибке "ошибка \_ сертификата в Интернете ( \_ сек \_ \_ \_ ](wininet-errors.md) .)".</span><span class="sxs-lookup"><span data-stu-id="377dc-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_флаг безопасности \_ пропустить \_ Перенаправление \_ на \_ http</span><span class="sxs-lookup"><span data-stu-id="377dc-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="377dc-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="377dc-586">0x00008000</span></span>

<span data-ttu-id="377dc-587">Игнорирует ошибку " [ \_ Интернет \_ -HTTPS — HTTP" \_ \_ \_ в \_ ](wininet-errors.md) сообщении об ошибке редир.</span><span class="sxs-lookup"><span data-stu-id="377dc-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_флаг безопасности \_ пропустить \_ Перенаправление \_ на \_ HTTPS</span><span class="sxs-lookup"><span data-stu-id="377dc-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="377dc-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="377dc-589">0x00004000</span></span>

<span data-ttu-id="377dc-590">Игнорирует сообщение об ошибке [ \_ Internet \_ HTTP \_ to \_ HTTPS \_ On \_ редир](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="377dc-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>\_ \_ отзыв игнорирования ФЛАГа безопасности \_</span><span class="sxs-lookup"><span data-stu-id="377dc-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="377dc-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="377dc-592">0x00000080</span></span>

<span data-ttu-id="377dc-593">Игнорирует проблемы отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="377dc-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ пропуск \_ неизвестного \_ ЦС в качестве флага безопасности</span><span class="sxs-lookup"><span data-stu-id="377dc-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="377dc-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="377dc-595">0x00000100</span></span>

<span data-ttu-id="377dc-596">Игнорирует неизвестные проблемы с центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="377dc-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_флаг безопасности \_ игнорирует \_ слабую \_ подпись</span><span class="sxs-lookup"><span data-stu-id="377dc-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="377dc-598">0x00010000</span></span>

<span data-ttu-id="377dc-599">Пропускает проблемы с подписью слабых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="377dc-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>\_ \_ пропуск \_ неправильного использования флага безопасности \_</span><span class="sxs-lookup"><span data-stu-id="377dc-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="377dc-601">0x00000200</span></span>

<span data-ttu-id="377dc-602">Пропускает неправильные проблемы использования.</span><span class="sxs-lookup"><span data-stu-id="377dc-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>\_флаг безопасности \_ нормалбитнесс</span><span class="sxs-lookup"><span data-stu-id="377dc-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="377dc-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="377dc-604">0x10000000</span></span>

<span data-ttu-id="377dc-605">Аналогично [ \_ стойкости флага безопасности \_ значение \_ слабое](/windows).</span><span class="sxs-lookup"><span data-stu-id="377dc-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="377dc-606">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>\_флаг безопасности \_ PCT</span><span class="sxs-lookup"><span data-stu-id="377dc-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="377dc-608">0x00000008</span></span>

<span data-ttu-id="377dc-609">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>\_Флаг безопасности \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="377dc-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="377dc-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="377dc-611">0x00000010</span></span>

<span data-ttu-id="377dc-612">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_безопасный флаг \_ безопасности</span><span class="sxs-lookup"><span data-stu-id="377dc-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="377dc-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="377dc-614">0x00000001</span></span>

<span data-ttu-id="377dc-615">Использует безопасные передачи.</span><span class="sxs-lookup"><span data-stu-id="377dc-615">Uses secure transfers.</span></span> <span data-ttu-id="377dc-616">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>\_флаг безопасности \_ SSL</span><span class="sxs-lookup"><span data-stu-id="377dc-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="377dc-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="377dc-618">0x00000002</span></span>

<span data-ttu-id="377dc-619">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>\_Флаг безопасности \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="377dc-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="377dc-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="377dc-621">0x00000004</span></span>

<span data-ttu-id="377dc-622">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>уровень \_ стойкости флага безопасности \_ \_</span><span class="sxs-lookup"><span data-stu-id="377dc-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="377dc-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="377dc-624">0x40000000</span></span>

<span data-ttu-id="377dc-625">Использует среднее (56-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="377dc-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="377dc-626">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_сильная стойкость флага безопасности \_ \_</span><span class="sxs-lookup"><span data-stu-id="377dc-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="377dc-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="377dc-628">0x20000000</span></span>

<span data-ttu-id="377dc-629">Использует стойкое (128-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="377dc-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="377dc-630">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ слабая стойкость ФЛАГа безопасности \_</span><span class="sxs-lookup"><span data-stu-id="377dc-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="377dc-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="377dc-632">0x10000000</span></span>

<span data-ttu-id="377dc-633">Использует слабое (40-разрядное) шифрование.</span><span class="sxs-lookup"><span data-stu-id="377dc-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="377dc-634">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="377dc-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>\_флаг безопасности \_ ункновнбит</span><span class="sxs-lookup"><span data-stu-id="377dc-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="377dc-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="377dc-636">0x80000000</span></span>

<span data-ttu-id="377dc-637">В шифровании используется неизвестный размер бита.</span><span class="sxs-lookup"><span data-stu-id="377dc-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="377dc-638">Это значение возвращается только при вызове [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="377dc-639">Имейте в виду, что данные, полученные таким образом, относятся к произошедшей транзакции, уровень безопасности которых больше не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="377dc-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="377dc-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**\_параметр " \_ \_ \_ разрядность ключа безопасности в Интернете"**</span><span class="sxs-lookup"><span data-stu-id="377dc-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-641">36</span><span class="sxs-lookup"><span data-stu-id="377dc-641">36</span></span>
</dt> <dt>



<span data-ttu-id="377dc-642">Извлекает длинное целое число без знака, содержащее бит ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="377dc-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="377dc-643">Чем больше это значение, тем больше степень шифрования используется.</span><span class="sxs-lookup"><span data-stu-id="377dc-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="377dc-644">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="377dc-645">Имейте в виду, что данные, полученные таким образом, относятся к уже произошедшим транзакциям, уровень безопасности которых больше не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="377dc-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_возможность \_ отправки \_ пропускной способности Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-647">56</span><span class="sxs-lookup"><span data-stu-id="377dc-647">56</span></span>
</dt> <dt>



<span data-ttu-id="377dc-648">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="377dc-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_ \_ время ожидания отправки для параметра Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-650">5</span><span class="sxs-lookup"><span data-stu-id="377dc-650">5</span></span>
</dt> <dt>



<span data-ttu-id="377dc-651">Задает или получает длинное целое число без знака в миллисекундах, которое содержит значение времени ожидания для отправки запроса.</span><span class="sxs-lookup"><span data-stu-id="377dc-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="377dc-652">Если отправка занимает больше времени, чем это значение, отправка отменяется.</span><span class="sxs-lookup"><span data-stu-id="377dc-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="377dc-653">Этот параметр можно использовать для любого обработчика [**хинтернет**](appendix-a-hinternet-handles.md) , включая маркер **null** .</span><span class="sxs-lookup"><span data-stu-id="377dc-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="377dc-654">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="377dc-655">При использовании в ссылке на FTP-транзакцию этот параметр относится к каналу управления.</span><span class="sxs-lookup"><span data-stu-id="377dc-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**\_ \_ \_ \_ контекст цепочки сертификатов сервера параметров Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-657">105</span><span class="sxs-lookup"><span data-stu-id="377dc-657">105</span></span>
</dt> <dt>



<span data-ttu-id="377dc-658">Извлекает контекст цепочки сертификатов сервера в виде повторяющегося [ \_ \_ контекста цепочки пкцерт](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span><span class="sxs-lookup"><span data-stu-id="377dc-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="377dc-659">Этот дубликат контекста можно передать любой функции Crypto API, которая принимает [ \_ \_ контекст цепочки пкцерт](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span><span class="sxs-lookup"><span data-stu-id="377dc-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="377dc-660">Необходимо вызвать [**цертфрицертификатечаин**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) в возвращенном [ \_ \_ контексте цепочки пкцерт](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) , когда вы завершите работу с контекстом цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="377dc-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="377dc-661">**Версия:** Требуется Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="377dc-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**\_ \_ настройки параметров Интернета \_ изменились**</span><span class="sxs-lookup"><span data-stu-id="377dc-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-663">39</span><span class="sxs-lookup"><span data-stu-id="377dc-663">39</span></span>
</dt> <dt>



<span data-ttu-id="377dc-664">Уведомляет систему о том, что параметры реестра были изменены, чтобы проверить параметры при следующем вызове [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="377dc-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="377dc-665">Он используется [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_параметр Интернета \_ подавлять \_ проверку \_ подлинности сервера**</span><span class="sxs-lookup"><span data-stu-id="377dc-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-667">104</span><span class="sxs-lookup"><span data-stu-id="377dc-667">104</span></span>
</dt> <dt>



<span data-ttu-id="377dc-668">Задает объект HTTP-запроса таким, что он не будет выполнять вход на серверы-источники, но будет автоматически входить на прокси-серверы HTTP.</span><span class="sxs-lookup"><span data-stu-id="377dc-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="377dc-669">Этот параметр отличается от флага запроса **Internet \_ Flag \_ без \_ проверки** подлинности, что предотвращает аутентификацию как на прокси-серверах, так и на исходных серверах.</span><span class="sxs-lookup"><span data-stu-id="377dc-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="377dc-670">Установка этого режима подавляет использование любого материала учетных данных (ранее предоставленные имя пользователя, пароль или SSL-сертификат клиента) при взаимодействии с сервером-источником.</span><span class="sxs-lookup"><span data-stu-id="377dc-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="377dc-671">Однако если запрос должен пройти через прокси-сервер с проверкой подлинности, WinINet будет по-прежнему выполнять автоматическую проверку подлинности прокси-сервера HTTP согласно параметрам зоны интрасети для пользователя.</span><span class="sxs-lookup"><span data-stu-id="377dc-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="377dc-672">Параметр зоны интрасети по умолчанию позволяет автоматически входить в систему, используя учетные данные пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="377dc-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="377dc-673">Чтобы предотвратить подавление всех идентифицирующих сведений, вызывающий объект должен **сочетать \_ параметр \_ Internet \_ \_ AUTH** Authentication с **\_ флагом Internet flags \_ No \_ cookies** Request.</span><span class="sxs-lookup"><span data-stu-id="377dc-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="377dc-674">Этот параметр может быть установлен только для объектов запроса перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="377dc-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="377dc-675">Попытки установить этот параметр после отправки запроса будут возвращать **сообщение об ошибке "ошибка в \_ Интернете \_ неверный \_ \_** режим работы".</span><span class="sxs-lookup"><span data-stu-id="377dc-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="377dc-676">Для этого параметра не требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="377dc-676">No buffer is required for this option.</span></span> <span data-ttu-id="377dc-677">Он используется [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) для дескрипторов, возвращаемых только [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="377dc-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="377dc-678">**Версия:** Требуется Internet Explorer 8,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**\_поведение при \_ подавлении в Интернете \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-680">81</span><span class="sxs-lookup"><span data-stu-id="377dc-680">81</span></span>
</dt> <dt>



<span data-ttu-id="377dc-681">Параметр общего назначения, который используется для подавления поведений на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="377dc-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="377dc-682">Параметр *лпбуффер* функции должен быть указателем на DWORD, который содержит определенное поведение для подавления.</span><span class="sxs-lookup"><span data-stu-id="377dc-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="377dc-683">Этот параметр нельзя запрашивать с помощью [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="377dc-684">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="377dc-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="377dc-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>\_отключение \_ сброса \_ всех параметров Интернета</span><span class="sxs-lookup"><span data-stu-id="377dc-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="377dc-686">0</span><span class="sxs-lookup"><span data-stu-id="377dc-686">0</span></span>

<span data-ttu-id="377dc-687">Отключает все подавления, повторно включает по умолчанию и настроенное поведение.</span><span class="sxs-lookup"><span data-stu-id="377dc-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="377dc-688">Этот параметр аналогичен параметру **Internet \_ подавлять \_ \_ \_ Сброс политики файлов cookie** и **\_ отключение \_ сохранения файлов \_ cookie \_** по отдельности.</span><span class="sxs-lookup"><span data-stu-id="377dc-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="377dc-689">**Версия:** Требуется Internet Explorer 6,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_Политика отключения \_ файлов cookie \_ в Интернете</span><span class="sxs-lookup"><span data-stu-id="377dc-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="377dc-691">1</span><span class="sxs-lookup"><span data-stu-id="377dc-691">1</span></span>

<span data-ttu-id="377dc-692">Пропускает все настроенные политики файлов cookie и позволяет задавать файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="377dc-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="377dc-693">**Версия:** Требуется Internet Explorer 6,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET \_ подавлять \_ \_ Сброс политики файлов cookie \_</span><span class="sxs-lookup"><span data-stu-id="377dc-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="377dc-695">2</span><span class="sxs-lookup"><span data-stu-id="377dc-695">2</span></span>

<span data-ttu-id="377dc-696">Отключает запрет на подавление **\_ \_ \_ политики файлов cookie в Интернете** , позволяя выполнять оценку файлов cookie в соответствии с настроенной политикой файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="377dc-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="377dc-697">**Версия:** Требуется Internet Explorer 6,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span>\_запрет на \_ Сохранение файлов cookie \_ в Интернете</span><span class="sxs-lookup"><span data-stu-id="377dc-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="377dc-699">3</span><span class="sxs-lookup"><span data-stu-id="377dc-699">3</span></span>

<span data-ttu-id="377dc-700">Подавляет сохранение файлов cookie, даже если сервер указал их как постоянные.</span><span class="sxs-lookup"><span data-stu-id="377dc-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="377dc-701">**Версия:** Требуется Internet Explorer 8,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="377dc-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET \_ подавлять \_ \_ Сброс сохраненных файлов cookie \_</span><span class="sxs-lookup"><span data-stu-id="377dc-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="377dc-703">4</span><span class="sxs-lookup"><span data-stu-id="377dc-703">4</span></span>

<span data-ttu-id="377dc-704">Отключает запрет **\_ \_ \_ сохранения файлов cookie в Интернете** , повторно включает сохраняемость файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="377dc-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="377dc-705">Все ранее подавленные файлы cookie не будут постоянными.</span><span class="sxs-lookup"><span data-stu-id="377dc-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="377dc-706">**Версия:** Требуется Internet Explorer 8,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="377dc-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="377dc-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**\_ \_ URL-адрес параметра Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-708">34</span><span class="sxs-lookup"><span data-stu-id="377dc-708">34</span></span>
</dt> <dt>



<span data-ttu-id="377dc-709">Извлекает строковое значение, содержащее полный URL-адрес скачанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="377dc-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="377dc-710">Если исходный URL-адрес содержал дополнительные данные, например строки поиска или привязки, или если вызов был перенаправлен, то возвращаемый URL-адрес отличается от исходного.</span><span class="sxs-lookup"><span data-stu-id="377dc-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="377dc-711">Этот параметр допустим для дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) , возвращаемых [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="377dc-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="377dc-712">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**\_Агент пользователя "Интернет" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="377dc-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-714">41</span><span class="sxs-lookup"><span data-stu-id="377dc-714">41</span></span>
</dt> <dt>



<span data-ttu-id="377dc-715">Задает или получает строку агента пользователя для дескрипторов, предоставляемых [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , и используется в последующих функциях [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) , если она не переопределяется заголовком, добавленным [**хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) или [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="377dc-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="377dc-716">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**\_параметр " \_ имя пользователя Интернета"**</span><span class="sxs-lookup"><span data-stu-id="377dc-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-718">28</span><span class="sxs-lookup"><span data-stu-id="377dc-718">28</span></span>
</dt> <dt>



<span data-ttu-id="377dc-719">Задает или получает строку, содержащую имя пользователя, связанное с маркером, возвращаемым функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="377dc-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="377dc-720">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**\_версия параметра \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="377dc-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-722">40</span><span class="sxs-lookup"><span data-stu-id="377dc-722">40</span></span>
</dt> <dt>



<span data-ttu-id="377dc-723">Извлекает структуру **\_ \_ сведений о версии в Интернете** , содержащую номер версии Wininet.dll.</span><span class="sxs-lookup"><span data-stu-id="377dc-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="377dc-724">Этот параметр можно использовать с **нулевым**[**хинтернет**](appendix-a-hinternet-handles.md) -маркером [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="377dc-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_ \_ \_ Размер буфера записи параметра \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="377dc-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="377dc-726">13</span><span class="sxs-lookup"><span data-stu-id="377dc-726">13</span></span>
</dt> <dt>



<span data-ttu-id="377dc-727">Задает или получает длинное целое число без знака, которое содержит размер буфера записи в байтах.</span><span class="sxs-lookup"><span data-stu-id="377dc-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="377dc-728">Этот параметр можно использовать для дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) , возвращаемых [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (только сеанс FTP).</span><span class="sxs-lookup"><span data-stu-id="377dc-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="377dc-729">Он используется [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) и [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="377dc-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="377dc-730">Комментарии</span><span class="sxs-lookup"><span data-stu-id="377dc-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="377dc-731">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="377dc-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="377dc-732">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="377dc-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="377dc-733">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="377dc-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="377dc-734">Требования</span><span class="sxs-lookup"><span data-stu-id="377dc-734">Requirements</span></span>



| <span data-ttu-id="377dc-735">Требование</span><span class="sxs-lookup"><span data-stu-id="377dc-735">Requirement</span></span> | <span data-ttu-id="377dc-736">Значение</span><span class="sxs-lookup"><span data-stu-id="377dc-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="377dc-737">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="377dc-737">Minimum supported client</span></span><br/> | <span data-ttu-id="377dc-738">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="377dc-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="377dc-739">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="377dc-739">Minimum supported server</span></span><br/> | <span data-ttu-id="377dc-740">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="377dc-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="377dc-741">Заголовок</span><span class="sxs-lookup"><span data-stu-id="377dc-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="377dc-742"><dt>WinInet. h; </dt> <dt>Вининети. h</dt></span><span class="sxs-lookup"><span data-stu-id="377dc-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

