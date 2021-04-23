---
title: Флаги API (WinInet. h)
description: Многие функции WinINet принимают массив флагов в качестве параметра. Ниже приведено краткое описание определенных флагов.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710511"
---
# <a name="api-flags"></a><span data-ttu-id="2c2af-104">Флаги API</span><span class="sxs-lookup"><span data-stu-id="2c2af-104">API Flags</span></span>

<span data-ttu-id="2c2af-105">Многие функции WinINet принимают массив флагов в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="2c2af-105">Many of the WinINet functions accept an array of flags as a parameter.</span></span> <span data-ttu-id="2c2af-106">Ниже приведено краткое описание определенных флагов.</span><span class="sxs-lookup"><span data-stu-id="2c2af-106">The following is a brief description of the defined flags.</span></span>

<dl> <dt>

<span data-ttu-id="2c2af-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**\_Файл cookie Интернета \_ оценивает \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="2c2af-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET\_COOKIE\_EVALUATE\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-108">0x80</span><span class="sxs-lookup"><span data-stu-id="2c2af-108">0x80</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-109">Указывает, что для файла cookie будет связан заголовок платформы для защиты конфиденциальности (P3P).</span><span class="sxs-lookup"><span data-stu-id="2c2af-109">Indicates that a Platform for Privacy Protection (P3P) header is to be associated with a cookie.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**\_сторонние файлы cookie Интернета \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET\_COOKIE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-111">0x10</span><span class="sxs-lookup"><span data-stu-id="2c2af-111">0x10</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-112">Указывает, что файл cookie стороннего производителя устанавливается или извлекается.</span><span class="sxs-lookup"><span data-stu-id="2c2af-112">Indicates that a third-party cookie is being set or retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**\_флаг Интернета \_ Async**</span><span class="sxs-lookup"><span data-stu-id="2c2af-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-114">0x10000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-114">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-115">Делает только асинхронные запросы к дескрипторам в порядке убывания из дескриптора, возвращенного этой функцией.</span><span class="sxs-lookup"><span data-stu-id="2c2af-115">Makes only asynchronous requests on handles descended from the handle returned from this function.</span></span> <span data-ttu-id="2c2af-116">Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-116">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**\_кэш флагов Интернета \_ \_ Async**</span><span class="sxs-lookup"><span data-stu-id="2c2af-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-118">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2c2af-118">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-119">Разрешает отложенную запись в кэш.</span><span class="sxs-lookup"><span data-stu-id="2c2af-119">Allows a lazy cache write.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_кэш флагов Интернета в \_ \_ случае \_ \_ сбоя NET**</span><span class="sxs-lookup"><span data-stu-id="2c2af-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-121">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2c2af-121">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-122">Возвращает ресурс из кэша в случае сбоя сетевого запроса ресурса из-за [ошибки \_ \_ \_ сброса подключения к Интернету](wininet-errors.md) или [ошибки подключения \_ \_ \_ к Интернету](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-122">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="2c2af-123">Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="2c2af-123">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_ \_ кэш не Internet \_ Flag**</span><span class="sxs-lookup"><span data-stu-id="2c2af-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET\_FLAG\_DONT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-125">0x04000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-125">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-126">Не добавляет возвращенную сущность в кэш.</span><span class="sxs-lookup"><span data-stu-id="2c2af-126">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="2c2af-127">Это эквивалентно предпочтительному значению, [ \_ флагу \_ Интернета \_ нет \_ записи в кэш](/windows).</span><span class="sxs-lookup"><span data-stu-id="2c2af-127">This is identical to the preferred value, [INTERNET\_FLAG\_NO\_CACHE\_WRITE](/windows).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**Флаг Интернета — \_ \_ существующее \_ подключение**</span><span class="sxs-lookup"><span data-stu-id="2c2af-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**INTERNET\_FLAG\_EXISTING\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-129">0x20000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-129">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-130">Пытается использовать существующий объект [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , если он существует с теми же атрибутами, которые требуются для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="2c2af-130">Attempts to use an existing [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) object if one exists with the same attributes required to make the request.</span></span> <span data-ttu-id="2c2af-131">Это полезно только при использовании FTP-операций, так как FTP является единственным протоколом, который обычно выполняет несколько операций во время одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="2c2af-131">This is useful only with FTP operations, since FTP is the only protocol that typically performs multiple operations during the same session.</span></span> <span data-ttu-id="2c2af-132">WinINet кэширует один обработчик соединения для каждого [**хинтернетного**](appendix-a-hinternet-handles.md) маркера, созданного [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="2c2af-132">WinINet caches a single connection handle for each [**HINTERNET**](appendix-a-hinternet-handles.md) handle generated by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="2c2af-133">Функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и **интернетконнект** используют этот флаг для соединений HTTP и FTP.</span><span class="sxs-lookup"><span data-stu-id="2c2af-133">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and **InternetConnect** functions use this flag for Http and Ftp connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_Отправка форм флагов Интернета \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**INTERNET\_FLAG\_FORMS\_SUBMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-135">0x00000040</span><span class="sxs-lookup"><span data-stu-id="2c2af-135">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-136">Указывает, что это отправка форм.</span><span class="sxs-lookup"><span data-stu-id="2c2af-136">Indicates that this is a Forms submission.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_флаг Интернета \_ из \_ кэша**</span><span class="sxs-lookup"><span data-stu-id="2c2af-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET\_FLAG\_FROM\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-138">0x01000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-138">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-139">Не выполняет сетевые запросы.</span><span class="sxs-lookup"><span data-stu-id="2c2af-139">Does not make network requests.</span></span> <span data-ttu-id="2c2af-140">Все сущности возвращаются из кэша.</span><span class="sxs-lookup"><span data-stu-id="2c2af-140">All entities are returned from the cache.</span></span> <span data-ttu-id="2c2af-141">Если запрошенный элемент отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="2c2af-141">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="2c2af-142">Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-142">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_флаг Интернета \_ ФВД \_ назад**</span><span class="sxs-lookup"><span data-stu-id="2c2af-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET\_FLAG\_FWD\_BACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-144">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2c2af-144">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-145">Указывает, что функция должна использовать копию ресурса, который в данный момент находится в кэше Интернета.</span><span class="sxs-lookup"><span data-stu-id="2c2af-145">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="2c2af-146">Дата окончания срока действия и другие сведения о ресурсе не проверяются.</span><span class="sxs-lookup"><span data-stu-id="2c2af-146">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="2c2af-147">Если запрошенный элемент не найден в кэше Интернета, система пытается найти ресурс в сети.</span><span class="sxs-lookup"><span data-stu-id="2c2af-147">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="2c2af-148">Это значение было представлено в Microsoft Internet Explorer 5 и связано с операциями « **вперед** » и « **назад** » обозревателя Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2c2af-148">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_Гиперссылка для Internet Flag \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**INTERNET\_FLAG\_HYPERLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-150">0x00000400</span><span class="sxs-lookup"><span data-stu-id="2c2af-150">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-151">Принудительная перезагрузка при отсутствии истечения срока действия и отсутствии времени LastModified, возвращенного сервером при определении необходимости перезагрузки элемента из сети.</span><span class="sxs-lookup"><span data-stu-id="2c2af-151">Forces a reload if there is no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.</span></span> <span data-ttu-id="2c2af-152">Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2c2af-152">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2c2af-153">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-153">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**\_флаг Интернета \_ игнорирует \_ \_ недопустимое общее имя сертификата \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-155">0x00001000</span><span class="sxs-lookup"><span data-stu-id="2c2af-155">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-156">Отключает проверку сертификатов на основе SSL/PCT, возвращаемых с сервера по имени узла, заданному в запросе.</span><span class="sxs-lookup"><span data-stu-id="2c2af-156">Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request.</span></span> <span data-ttu-id="2c2af-157">WinINet использует простую проверку сертификатов, сравнивая их с именами узлов и простыми правилами с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="2c2af-157">WinINet uses a simple check against certificates by comparing for matching host names and simple wildcarding rules.</span></span> <span data-ttu-id="2c2af-158">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-158">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**Флаг Интернета не \_ \_ учитывать \_ \_ дату сертификата \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="2c2af-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-161">Отключает проверку сертификатов на основе SSL/PCT для правильных дат действия.</span><span class="sxs-lookup"><span data-stu-id="2c2af-161">Disables checking of SSL/PCT-based certificates for proper validity dates.</span></span> <span data-ttu-id="2c2af-162">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-162">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_флаг Интернета \_ пропустить \_ Перенаправление \_ на \_ http**</span><span class="sxs-lookup"><span data-stu-id="2c2af-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-164">0x00008000</span><span class="sxs-lookup"><span data-stu-id="2c2af-164">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-165">Отключает обнаружение этого специального типа перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2c2af-165">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="2c2af-166">При использовании этого флага WinINet прозрачно разрешает перенаправление с URL-адресов HTTPS на HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c2af-166">When this flag is used, WinINet transparently allows redirects from HTTPS to HTTP URLs.</span></span> <span data-ttu-id="2c2af-167">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-167">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_флаг Интернета \_ пропустить \_ Перенаправление \_ на \_ HTTPS**</span><span class="sxs-lookup"><span data-stu-id="2c2af-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-169">0x00004000</span><span class="sxs-lookup"><span data-stu-id="2c2af-169">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-170">Отключает обнаружение этого специального типа перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2c2af-170">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="2c2af-171">При использовании этого флага WinINet явным образом разрешает перенаправление с URL-адресов HTTP на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2c2af-171">When this flag is used, WinINet transparently allow redirects from HTTP to HTTPS URLs.</span></span> <span data-ttu-id="2c2af-172">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-172">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_Подключение флага Интернета \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET\_FLAG\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-174">0x00400000</span><span class="sxs-lookup"><span data-stu-id="2c2af-174">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-175">Использует для соединения семантику проверки активности, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="2c2af-175">Uses keep-alive semantics, if available, for the connection.</span></span> <span data-ttu-id="2c2af-176">Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-176">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span> <span data-ttu-id="2c2af-177">Этот флаг является обязательным для Microsoft Network (MSN), NTLM и других типов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2c2af-177">This flag is required for Microsoft Network (MSN), NTLM, and other types of authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**\_флаг Интернета \_ сделать \_ постоянным**</span><span class="sxs-lookup"><span data-stu-id="2c2af-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-179">0x02000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-179">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-180">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c2af-180">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**\_флаг Интернета \_ должен \_ кэшировать \_ запрос**</span><span class="sxs-lookup"><span data-stu-id="2c2af-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c2af-182">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-183">Аналогично предпочтительному значению, для **\_ флага Интернета \_ требуется \_ файл**.</span><span class="sxs-lookup"><span data-stu-id="2c2af-183">Identical to the preferred value, **INTERNET\_FLAG\_NEED\_FILE**.</span></span> <span data-ttu-id="2c2af-184">Вызывает создание временного файла, если файл не может быть кэширован.</span><span class="sxs-lookup"><span data-stu-id="2c2af-184">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="2c2af-185">Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2c2af-185">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2c2af-186">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-186">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**для \_ флага Интернета \_ требуется \_ файл**</span><span class="sxs-lookup"><span data-stu-id="2c2af-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET\_FLAG\_NEED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-188">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c2af-188">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-189">Вызывает создание временного файла, если файл не может быть кэширован.</span><span class="sxs-lookup"><span data-stu-id="2c2af-189">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="2c2af-190">Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2c2af-190">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2c2af-191">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-191">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET \_ Flag \_ без \_ проверки подлинности**</span><span class="sxs-lookup"><span data-stu-id="2c2af-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET\_FLAG\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-193">0x00040000</span><span class="sxs-lookup"><span data-stu-id="2c2af-193">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-194">Не пытается автоматически пройти проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="2c2af-194">Does not attempt authentication automatically.</span></span> <span data-ttu-id="2c2af-195">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-195">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_флаг Интернета \_ без \_ автоматического \_ перенаправления**</span><span class="sxs-lookup"><span data-stu-id="2c2af-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET\_FLAG\_NO\_AUTO\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-197">0x00200000</span><span class="sxs-lookup"><span data-stu-id="2c2af-197">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-198">Не обрабатывает перенаправление в [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)автоматически.</span><span class="sxs-lookup"><span data-stu-id="2c2af-198">Does not automatically handle redirection in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="2c2af-199">Этот флаг также может использоваться [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) для HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="2c2af-199">This flag can also be used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) for HTTP requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_флаг Интернета \_ без \_ записи в кэш \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-201">0x04000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-201">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-202">Не добавляет возвращенную сущность в кэш.</span><span class="sxs-lookup"><span data-stu-id="2c2af-202">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="2c2af-203">Этот флаг используется, [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2c2af-203">This flag is used by , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2c2af-204">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-204">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_флаг Интернета \_ нет \_ файлов cookie**</span><span class="sxs-lookup"><span data-stu-id="2c2af-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET\_FLAG\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-206">0x00080000</span><span class="sxs-lookup"><span data-stu-id="2c2af-206">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-207">Не добавляет к запросам заголовки файлов cookie автоматически и не добавляет возвращенные файлы cookie в базу данных cookie.</span><span class="sxs-lookup"><span data-stu-id="2c2af-207">Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.</span></span> <span data-ttu-id="2c2af-208">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).</span><span class="sxs-lookup"><span data-stu-id="2c2af-208">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_флаг Интернета \_ нет \_ пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="2c2af-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET\_FLAG\_NO\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="2c2af-210">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-211">Отключает диалоговое окно "файл cookie".</span><span class="sxs-lookup"><span data-stu-id="2c2af-211">Disables the cookie dialog box.</span></span> <span data-ttu-id="2c2af-212">Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только HTTP-запросы).</span><span class="sxs-lookup"><span data-stu-id="2c2af-212">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_отключить флаг \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="2c2af-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET\_FLAG\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-214">0x01000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-214">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-215">Аналогично **\_ флагу Интернета \_ из \_ кэша**.</span><span class="sxs-lookup"><span data-stu-id="2c2af-215">Identical to **INTERNET\_FLAG\_FROM\_CACHE**.</span></span> <span data-ttu-id="2c2af-216">Не выполняет сетевые запросы.</span><span class="sxs-lookup"><span data-stu-id="2c2af-216">Does not make network requests.</span></span> <span data-ttu-id="2c2af-217">Все сущности возвращаются из кэша.</span><span class="sxs-lookup"><span data-stu-id="2c2af-217">All entities are returned from the cache.</span></span> <span data-ttu-id="2c2af-218">Если запрошенный элемент отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="2c2af-218">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="2c2af-219">Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-219">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_ \_ пассивный флаг Интернета**</span><span class="sxs-lookup"><span data-stu-id="2c2af-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET\_FLAG\_PASSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-221">0x08000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-221">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-222">Использует пассивную семантику FTP.</span><span class="sxs-lookup"><span data-stu-id="2c2af-222">Uses passive FTP semantics.</span></span> <span data-ttu-id="2c2af-223">Этот флаг используется только для [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-223">Only [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) use this flag.</span></span> <span data-ttu-id="2c2af-224">[**Интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) использует этот флаг для FTP-запросов, а [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) использует этот флаг для FTP-файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="2c2af-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses this flag for FTP requests, and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses this flag for FTP files and directories.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**параметр INTERNET \_ Flag \_ pragma \ \_ Cache**</span><span class="sxs-lookup"><span data-stu-id="2c2af-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-226">0x00000100</span><span class="sxs-lookup"><span data-stu-id="2c2af-226">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-227">Вызывает принудительное разрешение запроса сервером-источником, даже если кэшированная копия существует на прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="2c2af-227">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="2c2af-228">Функция [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только для запросов HTTP и HTTPS) и функция [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) используют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="2c2af-228">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_ \_ необработанные \_ данные Internet Flag**</span><span class="sxs-lookup"><span data-stu-id="2c2af-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**INTERNET\_FLAG\_RAW\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-230">0x40000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-230">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-231">Возвращает данные в виде структуры [**Win32 \_ Find \_**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) при получении данных из каталога FTP.</span><span class="sxs-lookup"><span data-stu-id="2c2af-231">Returns the data as a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure when retrieving FTP directory information.</span></span> <span data-ttu-id="2c2af-232">Если этот флаг не указан или вызов осуществляется через прокси-сервер CERN, [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Возвращает HTML-версию каталога.</span><span class="sxs-lookup"><span data-stu-id="2c2af-232">If this flag is not specified or if the call is made through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) returns the HTML version of the directory.</span></span> <span data-ttu-id="2c2af-233">Этот флаг используется только в функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-233">Only the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function uses this flag.</span></span>

<span data-ttu-id="2c2af-234">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также возвращает структуру [**\_ \_ данных Gopher Find**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) при получении сведений о каталоге Gopher.</span><span class="sxs-lookup"><span data-stu-id="2c2af-234">**Windows XP and Windows Server 2003 R2 and earlier:** Also returns a [**GOPHER\_FIND\_DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) structure when retrieving Gopher directory information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**Предвыборка для чтения с \_ флагом Интернета \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET\_FLAG\_READ\_PREFETCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-236">0x00100000</span><span class="sxs-lookup"><span data-stu-id="2c2af-236">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-237">Этот флаг сейчас отключен.</span><span class="sxs-lookup"><span data-stu-id="2c2af-237">This flag is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**\_Перезагрузка флага Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**INTERNET\_FLAG\_RELOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-239">0x80000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-239">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-240">Принудительно загружает запрошенный файл, объект или каталог с сервера-источника, а не из кэша.</span><span class="sxs-lookup"><span data-stu-id="2c2af-240">Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.</span></span> <span data-ttu-id="2c2af-241">Функции [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) используют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="2c2af-241">The [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) functions use this flag.</span></span>

<span data-ttu-id="2c2af-242">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-242">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_зона Internet Flag \_ ограниченной \_ зоны**</span><span class="sxs-lookup"><span data-stu-id="2c2af-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**INTERNET\_FLAG\_RESTRICTED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-244">0x00020000</span><span class="sxs-lookup"><span data-stu-id="2c2af-244">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-245">Указывает, что заданный куки-файл связан с недоверенным сайтом.</span><span class="sxs-lookup"><span data-stu-id="2c2af-245">Indicates that the cookie being set is associated with an untrusted site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**\_ \_ Повторная синхронизация ФЛАГа Интернета**</span><span class="sxs-lookup"><span data-stu-id="2c2af-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-247">0x00000800</span><span class="sxs-lookup"><span data-stu-id="2c2af-247">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-248">Перезагружает ресурсы HTTP, если ресурс был изменен с момента последней загрузки.</span><span class="sxs-lookup"><span data-stu-id="2c2af-248">Reloads HTTP resources if the resource has been modified since the last time it was downloaded.</span></span> <span data-ttu-id="2c2af-249">Все ресурсы FTP перегружаются.</span><span class="sxs-lookup"><span data-stu-id="2c2af-249">All FTP resources are reloaded.</span></span> <span data-ttu-id="2c2af-250">Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="2c2af-250">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="2c2af-251">**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется в [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), и ресурсы Gopher перегружаются.</span><span class="sxs-lookup"><span data-stu-id="2c2af-251">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), and Gopher resources are reloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_безопасный флаг \_ Интернета**</span><span class="sxs-lookup"><span data-stu-id="2c2af-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET\_FLAG\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-253">0x00800000</span><span class="sxs-lookup"><span data-stu-id="2c2af-253">0x00800000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-254">Использует безопасную семантику транзакций.</span><span class="sxs-lookup"><span data-stu-id="2c2af-254">Uses secure transaction semantics.</span></span> <span data-ttu-id="2c2af-255">Это означает использование технологии SSL/частной связи (SSL/PCT) и имеет смысл только в HTTP-запросах.</span><span class="sxs-lookup"><span data-stu-id="2c2af-255">This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.</span></span> <span data-ttu-id="2c2af-256">Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), но он является избыточным, если HTTPS://отображается в URL-адресе. Функция [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) использует этот флаг для HTTP-соединений; Этот флаг будет унаследован всеми дескрипторами запросов, созданными при этом соединении.</span><span class="sxs-lookup"><span data-stu-id="2c2af-256">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), but this is redundant if https:// appears in the URL.The [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function uses this flag for HTTP connections; all the request handles created under this connection will inherit this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**код \_ \_ ASCII для перевода с ФЛАГом Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET\_FLAG\_TRANSFER\_ASCII**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-258">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c2af-258">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-259">Передает файл как ASCII (только FTP).</span><span class="sxs-lookup"><span data-stu-id="2c2af-259">Transfers file as ASCII (FTP only).</span></span> <span data-ttu-id="2c2af-260">Этот флаг может использоваться [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)и [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-260">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_ \_ двоичный файл передаваемых ФЛАГов Интернета \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET\_FLAG\_TRANSFER\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-262">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2c2af-262">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-263">Передает файл как двоичный (только FTP).</span><span class="sxs-lookup"><span data-stu-id="2c2af-263">Transfers file as binary (FTP only).</span></span> <span data-ttu-id="2c2af-264">Этот флаг может использоваться [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)и [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="2c2af-264">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**\_ \_ обратный вызов через Интернет**</span><span class="sxs-lookup"><span data-stu-id="2c2af-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c2af-266">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-267">Указывает, что для этого API не нужно создавать обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="2c2af-267">Indicates that no callbacks should be made for that API.</span></span> <span data-ttu-id="2c2af-268">Используется для параметра *дксконтекст* функций, которые позволяют выполнять асинхронные операции.</span><span class="sxs-lookup"><span data-stu-id="2c2af-268">This is used for the *dxContext* parameter of the functions that allow asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_параметр Интернета \_ подавлять \_ проверку \_ подлинности сервера**</span><span class="sxs-lookup"><span data-stu-id="2c2af-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-270">104</span><span class="sxs-lookup"><span data-stu-id="2c2af-270">104</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-271">Задает объект HTTP-запроса таким, что он не будет выполнять вход на серверы-источники, но будет автоматически входить на прокси-серверы HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c2af-271">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="2c2af-272">Этот параметр отличается от флага запроса INTERNET \_ Flag \_ без \_ проверки подлинности, что предотвращает аутентификацию как на прокси-серверах, так и на исходных серверах.</span><span class="sxs-lookup"><span data-stu-id="2c2af-272">This option differs from the Request flag INTERNET\_FLAG\_NO\_AUTH, which prevents authentication to both proxy servers and origin servers.</span></span> <span data-ttu-id="2c2af-273">Установка этого режима подавляет использование любого материала учетных данных (ранее предоставленные имя пользователя, пароль или SSL-сертификат клиента) при взаимодействии с сервером-источником.</span><span class="sxs-lookup"><span data-stu-id="2c2af-273">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="2c2af-274">Однако если запрос должен пройти через прокси-сервер с проверкой подлинности, WinINet будет по-прежнему выполнять автоматическую проверку подлинности прокси-сервера HTTP согласно параметрам зоны интрасети для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c2af-274">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="2c2af-275">Параметр зоны интрасети по умолчанию позволяет автоматически входить в систему, используя учетные данные пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c2af-275">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span> <span data-ttu-id="2c2af-276">Чтобы предотвратить подавление всех идентифицирующих сведений, вызывающий объект должен сочетать \_ параметр \_ Internet \_ \_ AUTH Authentication с \_ флагом Internet flags \_ No \_ cookies Request.</span><span class="sxs-lookup"><span data-stu-id="2c2af-276">To ensure suppression of all identifying information, the caller should combine INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH with the INTERNET\_FLAG\_NO\_COOKIES request flag.</span></span> <span data-ttu-id="2c2af-277">Этот параметр может быть установлен только для объектов запроса перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="2c2af-277">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="2c2af-278">Попытки установить этот параметр после отправки запроса будут возвращать сообщение об ошибке "ошибка в \_ Интернете неверный режим работы" \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2c2af-278">Attempts to set this option after the request has been sent will return ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE.</span></span> <span data-ttu-id="2c2af-279">Для этого параметра не требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="2c2af-279">No buffer is required for this option.</span></span> <span data-ttu-id="2c2af-280">Он используется Интернетсетоптион для дескрипторов, возвращаемых только Хттпопенрекуест.</span><span class="sxs-lookup"><span data-stu-id="2c2af-280">This is used by InternetSetOption on handles returned by HttpOpenRequest only.</span></span> <span data-ttu-id="2c2af-281">Версия: требуется Internet Explorer 8,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2c2af-281">Version: Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_флаг API \_ WinInet \_ Async**</span><span class="sxs-lookup"><span data-stu-id="2c2af-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET\_API\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c2af-283">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-284">Принудительно выполняет асинхронные операции.</span><span class="sxs-lookup"><span data-stu-id="2c2af-284">Forces asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_ \_ Синхронизация флагов API WinInet \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET\_API\_FLAG\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-286">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2c2af-286">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-287">Принудительно выполняет синхронные операции.</span><span class="sxs-lookup"><span data-stu-id="2c2af-287">Forces synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c2af-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**\_ \_ контекст использования флага API WinInet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c2af-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET\_API\_FLAG\_USE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2af-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2c2af-289">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="2c2af-290">Заставляет API использовать значение контекста, даже если оно равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2c2af-290">Forces the API to use the context value, even if it is set to zero.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c2af-291">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c2af-291">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c2af-292">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="2c2af-292">WinINet does not support server implementations.</span></span> <span data-ttu-id="2c2af-293">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="2c2af-293">In addition, it should not be used from a service.</span></span> <span data-ttu-id="2c2af-294">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="2c2af-294">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c2af-295">Требования</span><span class="sxs-lookup"><span data-stu-id="2c2af-295">Requirements</span></span>



| <span data-ttu-id="2c2af-296">Требование</span><span class="sxs-lookup"><span data-stu-id="2c2af-296">Requirement</span></span> | <span data-ttu-id="2c2af-297">Значение</span><span class="sxs-lookup"><span data-stu-id="2c2af-297">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2af-298">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c2af-298">Minimum supported client</span></span><br/> | <span data-ttu-id="2c2af-299">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c2af-299">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2c2af-300">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c2af-300">Minimum supported server</span></span><br/> | <span data-ttu-id="2c2af-301">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c2af-301">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2c2af-302">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c2af-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c2af-303"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c2af-303"><dt>Wininet.h</dt></span></span> </dl> |



 

