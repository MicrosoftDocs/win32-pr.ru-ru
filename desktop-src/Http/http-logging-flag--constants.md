---
title: Константы HTTP_LOGGING_FLAG_ (HTTP. h)
description: Определите параметры для настройки ведения журнала в API-интерфейсе HTTP Server.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803028"
---
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="9d474-103">\_ \_ Константы флага ведения журнала HTTP \_</span><span class="sxs-lookup"><span data-stu-id="9d474-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="9d474-104">Константы **\_ \_ флага \_ ведения журнала HTTP** определяют параметры для настройки ведения журнала в API-интерфейсе сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d474-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="9d474-105">Эти константы используются в структуре [**\_ \_ сведений о ведении журнала HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="9d474-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="9d474-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_флаг ведения журнала HTTP — \_ \_ Локальная \_ \_ Смена времени**</span><span class="sxs-lookup"><span data-stu-id="9d474-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9d474-107">Операция переключения на файл журнала основана на местном времени.</span><span class="sxs-lookup"><span data-stu-id="9d474-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="9d474-108">По умолчанию смена файлов журнала основана на времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="9d474-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d474-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Протокол HTTP \_ Флаг ведения журнала \_ \_ использование \_ \_ преобразования UTF8**</span><span class="sxs-lookup"><span data-stu-id="9d474-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9d474-110">При записи в файлы журнала поля Юникода преобразуются в кодировки UTF8 (многобайты).</span><span class="sxs-lookup"><span data-stu-id="9d474-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="9d474-111">По умолчанию файлы журнала записываются с помощью локального преобразования кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="9d474-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d474-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_флаг ведения журнала HTTP — \_ \_ \_ только ошибки журнала \_**</span><span class="sxs-lookup"><span data-stu-id="9d474-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9d474-113">Файлы журнала содержат только сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="9d474-113">The log files include error information only.</span></span> <span data-ttu-id="9d474-114">По умолчанию в журнал записываются как ответы об ошибках, так и успешные запросы.</span><span class="sxs-lookup"><span data-stu-id="9d474-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="9d474-115">Если ни один **из \_ флагов ведения журнала HTTP не имеет значения \_ \_ только для журнала \_ ошибок \_** или **\_ \_ \_ \_ \_ только для флага журнала HTTP** , то регистрируются как ошибки, так и сведения об успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="9d474-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="9d474-116">Этот флаг не может быть установлен, если установлен флаг " **\_ \_ \_ Журнал \_ \_ только флагов регистрации HTTP** ".</span><span class="sxs-lookup"><span data-stu-id="9d474-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="9d474-117">Эти два флага являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="9d474-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9d474-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Протокол HTTP \_ \_Журнал флагов ведения журнала \_ \_ \_ только успешно выполнен**</span><span class="sxs-lookup"><span data-stu-id="9d474-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9d474-119">В файлы журнала входят только сведения об успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="9d474-119">The log files include success information only.</span></span> <span data-ttu-id="9d474-120">По умолчанию регистрируются ошибки и успешные транзакции.</span><span class="sxs-lookup"><span data-stu-id="9d474-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="9d474-121">Если ни один **из \_ флагов ведения журнала HTTP не имеет значения \_ \_ только для журнала \_ ошибок \_** или **\_ \_ \_ \_ \_ только для флага журнала HTTP** , то регистрируются как ошибки, так и сведения об успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="9d474-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="9d474-122">Этот флаг не может быть установлен, если установлен флаг "журнал **\_ \_ \_ \_ ошибок \_ только флагов регистрации HTTP** ".</span><span class="sxs-lookup"><span data-stu-id="9d474-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="9d474-123">Эти два флага являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="9d474-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d474-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9d474-124">Requirements</span></span>



| <span data-ttu-id="9d474-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9d474-125">Requirement</span></span> | <span data-ttu-id="9d474-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9d474-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9d474-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d474-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d474-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d474-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d474-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d474-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d474-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d474-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d474-131">Header</span><span class="sxs-lookup"><span data-stu-id="9d474-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d474-132"><dt>HTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d474-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d474-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d474-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d474-134">Константы API сервера HTTP версии 2,0</span><span class="sxs-lookup"><span data-stu-id="9d474-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="9d474-135">**\_сведения о ведении журнала HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="9d474-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="9d474-136">**хттпсетурлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="9d474-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="9d474-137">**хттпсетсерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="9d474-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="9d474-138">**хттпкуерюрлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="9d474-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="9d474-139">**хттпкуерисерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="9d474-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





