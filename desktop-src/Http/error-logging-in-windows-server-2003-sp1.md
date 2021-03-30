---
title: Ведение журнала ошибок в Windows Server 2003 SP1
description: Ведение журнала ошибок в Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Регистрация ошибок в Windows Server 2003 с пакетом обновления 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/14/2019
ms.locfileid: "103784875"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="f3f33-104">Ведение журнала ошибок в Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="f3f33-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="f3f33-105">Добавление заголовков в стиле W3C</span><span class="sxs-lookup"><span data-stu-id="f3f33-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="f3f33-106">Начиная с Windows Server 2003 с пакетом обновления 1 (SP1), журнал ошибок API сервера HTTP включает заголовки стилей W3C, позволяющие анализировать файлы журналов с помощью стандартных средств синтаксического анализа журналов.</span><span class="sxs-lookup"><span data-stu-id="f3f33-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="f3f33-107">В приведенном ниже шаблоне перечислены все поля, которые можно зафиксировать в файле журнала ошибок HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3f33-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="f3f33-108">Ведение журнала дополнительных полей</span><span class="sxs-lookup"><span data-stu-id="f3f33-108">Logging Additional Fields</span></span>

<span data-ttu-id="f3f33-109">Журнал ошибок HTTP был расширен и содержит девять дополнительных полей для записи данных о возникших сбоях.</span><span class="sxs-lookup"><span data-stu-id="f3f33-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="f3f33-110">Новые поля ошибок перечислены ниже:</span><span class="sxs-lookup"><span data-stu-id="f3f33-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="f3f33-111">Имя компьютера сервера \[ S-ComputerName\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="f3f33-112">Агент пользователя \[ CS ( \_ Агент пользователя)\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="f3f33-113">Файл cookie \[ CS (cookie)\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="f3f33-114">Источник ссылки \[ CS (Источник ссылки)\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="f3f33-115">Имя узла \[ CS-Host\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="f3f33-116">Количество байт, полученных сервером \[ sc-bytes\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="f3f33-117">Байт получено и обработано сервером \[ CS-bytes\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="f3f33-118">Время, затраченное на обработку \[ времени запроса\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="f3f33-119">Queue-Name (зарезервировано для IIS) \[ S-QUEUENAME\]</span><span class="sxs-lookup"><span data-stu-id="f3f33-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="f3f33-120">Выбор пункта "архивированные" для записи в файл журнала ошибок HTTP</span><span class="sxs-lookup"><span data-stu-id="f3f33-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="f3f33-121">Добавлен раздел реестра **еррорлоггингфиелдс** для управления полями, зарегистрированными в журнале ошибок HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3f33-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="f3f33-122">Эти значения реестра находятся в разделе параметров HTTP, \\ расположенном по адресу:</span><span class="sxs-lookup"><span data-stu-id="f3f33-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="f3f33-123">Значение реестра **еррорлоггингфиелдс** — это значение типа DWORD, которое содержит битовые значения для каждого поля, которое можно зафиксировать в журнале.</span><span class="sxs-lookup"><span data-stu-id="f3f33-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="f3f33-124">Чтобы включить ведение журнала определенного поля, установите соответствующее значение бита равным 1 и перезапустите службу HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3f33-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="f3f33-125">Чтобы отключить ведение журнала, установите значение бита равным 0.</span><span class="sxs-lookup"><span data-stu-id="f3f33-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="f3f33-126">Чтобы настроить несколько полей, используйте побитовую операцию или для отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="f3f33-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="f3f33-127">Например, чтобы включить поля журнала файлов cookie и источника ссылок, значение должно быть 0x00020000 \| 0x00040000 = 0x00060000.</span><span class="sxs-lookup"><span data-stu-id="f3f33-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="f3f33-128">Если раздел реестра **еррорлоггингфиелдс** отсутствует, записываются поля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3f33-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="f3f33-129">Значение **еррорлоггингфиелдс** для записи в журнал полей по умолчанию — 0x7c884c7.</span><span class="sxs-lookup"><span data-stu-id="f3f33-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="f3f33-130">Чтобы включить ведение журнала для всех полей, показанных в таблице ниже, установите значение 0x7dff4e7.</span><span class="sxs-lookup"><span data-stu-id="f3f33-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="f3f33-131">Поля журнала ошибок перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f3f33-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="f3f33-132">Поле журнала</span><span class="sxs-lookup"><span data-stu-id="f3f33-132">Log field</span></span>            | <span data-ttu-id="f3f33-133">Регистрируется по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f3f33-133">Logged by default</span></span> | <span data-ttu-id="f3f33-134">Битовое значение</span><span class="sxs-lookup"><span data-stu-id="f3f33-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="f3f33-135">Дата</span><span class="sxs-lookup"><span data-stu-id="f3f33-135">Date</span></span>                 | <span data-ttu-id="f3f33-136">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-136">Yes</span></span>               | <span data-ttu-id="f3f33-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f3f33-137">0x00000001</span></span> |
| <span data-ttu-id="f3f33-138">Время</span><span class="sxs-lookup"><span data-stu-id="f3f33-138">Time</span></span>                 | <span data-ttu-id="f3f33-139">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-139">Yes</span></span>               | <span data-ttu-id="f3f33-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f3f33-140">0x00000002</span></span> |
| <span data-ttu-id="f3f33-141">Имя компьютера сервера</span><span class="sxs-lookup"><span data-stu-id="f3f33-141">Server Computer Name</span></span> | <span data-ttu-id="f3f33-142">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-142">No</span></span>                | <span data-ttu-id="f3f33-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f3f33-143">0x00000020</span></span> |
| <span data-ttu-id="f3f33-144">IP-адрес клиента</span><span class="sxs-lookup"><span data-stu-id="f3f33-144">Client IP Address</span></span>    | <span data-ttu-id="f3f33-145">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-145">Yes</span></span>               | <span data-ttu-id="f3f33-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f3f33-146">0x00000004</span></span> |
| <span data-ttu-id="f3f33-147">Порт клиента</span><span class="sxs-lookup"><span data-stu-id="f3f33-147">Client Port</span></span>          | <span data-ttu-id="f3f33-148">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-148">Yes</span></span>               | <span data-ttu-id="f3f33-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="f3f33-149">0x00400000</span></span> |
| <span data-ttu-id="f3f33-150">IP-адрес сервера</span><span class="sxs-lookup"><span data-stu-id="f3f33-150">Server IP Address</span></span>    | <span data-ttu-id="f3f33-151">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-151">Yes</span></span>               | <span data-ttu-id="f3f33-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="f3f33-152">0x00000040</span></span> |
| <span data-ttu-id="f3f33-153">Порт сервера</span><span class="sxs-lookup"><span data-stu-id="f3f33-153">Server Port</span></span>          | <span data-ttu-id="f3f33-154">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-154">Yes</span></span>               | <span data-ttu-id="f3f33-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="f3f33-155">0x00008000</span></span> |
| <span data-ttu-id="f3f33-156">Версия протокола</span><span class="sxs-lookup"><span data-stu-id="f3f33-156">Protocol Version</span></span>     | <span data-ttu-id="f3f33-157">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-157">Yes</span></span>               | <span data-ttu-id="f3f33-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="f3f33-158">0x00080000</span></span> |
| <span data-ttu-id="f3f33-159">Метод</span><span class="sxs-lookup"><span data-stu-id="f3f33-159">Method</span></span>               | <span data-ttu-id="f3f33-160">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-160">Yes</span></span>               | <span data-ttu-id="f3f33-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f3f33-161">0x00000080</span></span> |
| <span data-ttu-id="f3f33-162">URI</span><span class="sxs-lookup"><span data-stu-id="f3f33-162">URI</span></span>                  | <span data-ttu-id="f3f33-163">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-163">Yes</span></span>               | <span data-ttu-id="f3f33-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="f3f33-164">0x00800000</span></span> |
| <span data-ttu-id="f3f33-165">Агент пользователя</span><span class="sxs-lookup"><span data-stu-id="f3f33-165">User Agent</span></span>           | <span data-ttu-id="f3f33-166">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-166">No</span></span>                | <span data-ttu-id="f3f33-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="f3f33-167">0x00010000</span></span> |
| <span data-ttu-id="f3f33-168">Куки-файл</span><span class="sxs-lookup"><span data-stu-id="f3f33-168">Cookie</span></span>               | <span data-ttu-id="f3f33-169">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-169">No</span></span>                | <span data-ttu-id="f3f33-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="f3f33-170">0x00020000</span></span> |
| <span data-ttu-id="f3f33-171">ссылок</span><span class="sxs-lookup"><span data-stu-id="f3f33-171">referrer</span></span>             | <span data-ttu-id="f3f33-172">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-172">No</span></span>                | <span data-ttu-id="f3f33-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="f3f33-173">0x00040000</span></span> |
| <span data-ttu-id="f3f33-174">Узел</span><span class="sxs-lookup"><span data-stu-id="f3f33-174">Host</span></span>                 | <span data-ttu-id="f3f33-175">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-175">No</span></span>                | <span data-ttu-id="f3f33-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="f3f33-176">0x00100000</span></span> |
| <span data-ttu-id="f3f33-177">Состояние протокола</span><span class="sxs-lookup"><span data-stu-id="f3f33-177">Protocol Status</span></span>      | <span data-ttu-id="f3f33-178">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-178">Yes</span></span>               | <span data-ttu-id="f3f33-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="f3f33-179">0x00000400</span></span> |
| <span data-ttu-id="f3f33-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="f3f33-180">SC-Bytes</span></span>             | <span data-ttu-id="f3f33-181">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-181">No</span></span>                | <span data-ttu-id="f3f33-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="f3f33-182">0x00001000</span></span> |
| <span data-ttu-id="f3f33-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="f3f33-183">CS-Bytes</span></span>             | <span data-ttu-id="f3f33-184">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-184">No</span></span>                | <span data-ttu-id="f3f33-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="f3f33-185">0x00002000</span></span> |
| <span data-ttu-id="f3f33-186">Затраченное время</span><span class="sxs-lookup"><span data-stu-id="f3f33-186">Time Taken</span></span>           | <span data-ttu-id="f3f33-187">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-187">No</span></span>                | <span data-ttu-id="f3f33-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="f3f33-188">0x00004000</span></span> |
| <span data-ttu-id="f3f33-189">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="f3f33-189">SiteId</span></span>               | <span data-ttu-id="f3f33-190">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-190">Yes</span></span>               | <span data-ttu-id="f3f33-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="f3f33-191">0x01000000</span></span> |
| <span data-ttu-id="f3f33-192">Фраза причины</span><span class="sxs-lookup"><span data-stu-id="f3f33-192">Reason Phrase</span></span>        | <span data-ttu-id="f3f33-193">Да</span><span class="sxs-lookup"><span data-stu-id="f3f33-193">Yes</span></span>               | <span data-ttu-id="f3f33-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="f3f33-194">0x02000000</span></span> |
| <span data-ttu-id="f3f33-195">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="f3f33-195">Queue Name</span></span>           | <span data-ttu-id="f3f33-196">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-196">No</span></span>                | <span data-ttu-id="f3f33-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="f3f33-197">0x04000000</span></span> |
| <span data-ttu-id="f3f33-198">Идентификатор потока</span><span class="sxs-lookup"><span data-stu-id="f3f33-198">Stream Id</span></span>            | <span data-ttu-id="f3f33-199">Нет</span><span class="sxs-lookup"><span data-stu-id="f3f33-199">No</span></span>                | <span data-ttu-id="f3f33-200">0x????????</span><span class="sxs-lookup"><span data-stu-id="f3f33-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="f3f33-201">Смена времени и даты</span><span class="sxs-lookup"><span data-stu-id="f3f33-201">Time and Date Rollover</span></span>

<span data-ttu-id="f3f33-202">По умолчанию создается новый файл журнала ошибок HTTP (с условной сменой файла), когда текущий файл журнала достигает указанного размера.</span><span class="sxs-lookup"><span data-stu-id="f3f33-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="f3f33-203">Начиная с Windows Server 2003 с пакетом обновления 1 (SP1), новые файлы журнала ошибок можно создавать на основе даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f3f33-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="f3f33-204">Смена времени и даты контролируется двумя новыми значениями реестра: **еррорлоггингролловертипе** и **еррорлоггинглокалтимеролловер**.</span><span class="sxs-lookup"><span data-stu-id="f3f33-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="f3f33-205">Чтобы включить смену времени и даты, эти значения реестра необходимо добавить в реестр.</span><span class="sxs-lookup"><span data-stu-id="f3f33-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="f3f33-206">После добавления этих ключей в реестр служба HTTP должна быть перезапущена.</span><span class="sxs-lookup"><span data-stu-id="f3f33-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="f3f33-207">Разделы реестра для продолжения файла журнала создаются в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="f3f33-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="f3f33-208">Раздел реестра **еррорлоггингролловертипе** указывает тип требуемой смены и по умолчанию имеет значение смена на основе размера.</span><span class="sxs-lookup"><span data-stu-id="f3f33-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="f3f33-209">Смена также может выполняться ежедневно, еженедельно, ежемесячно или ежечасно.</span><span class="sxs-lookup"><span data-stu-id="f3f33-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="f3f33-210">Когда операция переключения на файл данных основана на времени, значение **еррорлоггинглокалтимеролловер** , равное 0, указывает, что время переключения выражается в формате GMT, а значение 1 указывает на то, что время переключения выражается в местном времени.</span><span class="sxs-lookup"><span data-stu-id="f3f33-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="f3f33-211">Ключ **еррорлоггингролловертипе** может принимать значение от 0 до 4, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f3f33-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="f3f33-212">Значение типа продолжения</span><span class="sxs-lookup"><span data-stu-id="f3f33-212">Rollover type value</span></span> | <span data-ttu-id="f3f33-213">Описание</span><span class="sxs-lookup"><span data-stu-id="f3f33-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f33-214">0</span><span class="sxs-lookup"><span data-stu-id="f3f33-214">0</span></span>                   | <span data-ttu-id="f3f33-215">Смена на основе размера.</span><span class="sxs-lookup"><span data-stu-id="f3f33-215">Size based rollover.</span></span> <span data-ttu-id="f3f33-216">Происходит откат файлов журналов, когда размер файла достигает размера, определенного в разделе реестра **еррорлогфилетрункатесизе** .</span><span class="sxs-lookup"><span data-stu-id="f3f33-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="f3f33-217">1</span><span class="sxs-lookup"><span data-stu-id="f3f33-217">1</span></span>                   | <span data-ttu-id="f3f33-218">Операция переключения на файл журнала выполняется ежедневно.</span><span class="sxs-lookup"><span data-stu-id="f3f33-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="f3f33-219">2</span><span class="sxs-lookup"><span data-stu-id="f3f33-219">2</span></span>                   | <span data-ttu-id="f3f33-220">Операция переключения на файл журнала выполняется еженедельно.</span><span class="sxs-lookup"><span data-stu-id="f3f33-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="f3f33-221">3</span><span class="sxs-lookup"><span data-stu-id="f3f33-221">3</span></span>                   | <span data-ttu-id="f3f33-222">Операция переключения на файл журнала выполняется ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="f3f33-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="f3f33-223">4</span><span class="sxs-lookup"><span data-stu-id="f3f33-223">4</span></span>                   | <span data-ttu-id="f3f33-224">Операция переключения на файл журнала выполняется каждый час.</span><span class="sxs-lookup"><span data-stu-id="f3f33-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="f3f33-225">Соглашения об именовании для файлов, в которых хранятся журналы ошибок, отличаются в зависимости от размера, даты и смены времени.</span><span class="sxs-lookup"><span data-stu-id="f3f33-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="f3f33-226">В следующей таблице перечислены соглашения об именовании для файлов журнала HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3f33-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="f3f33-227">Тип толловер</span><span class="sxs-lookup"><span data-stu-id="f3f33-227">Tollover type</span></span> | <span data-ttu-id="f3f33-228">Имя файла журнала</span><span class="sxs-lookup"><span data-stu-id="f3f33-228">Log file name</span></span>  | <span data-ttu-id="f3f33-229">Описание</span><span class="sxs-lookup"><span data-stu-id="f3f33-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f33-230">Размер</span><span class="sxs-lookup"><span data-stu-id="f3f33-230">Size</span></span>          | <span data-ttu-id="f3f33-231">Хттперрн. LOG</span><span class="sxs-lookup"><span data-stu-id="f3f33-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="f3f33-232">Файл журнала перезапускается при достижении определенного размера.</span><span class="sxs-lookup"><span data-stu-id="f3f33-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="f3f33-233">n — это номер файла, который увеличивается при изменении файла журнала.</span><span class="sxs-lookup"><span data-stu-id="f3f33-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="f3f33-234">Ежедневно</span><span class="sxs-lookup"><span data-stu-id="f3f33-234">Daily</span></span>         | <span data-ttu-id="f3f33-235">Хтииммдд. log</span><span class="sxs-lookup"><span data-stu-id="f3f33-235">htYYMMDD.log</span></span>   | <span data-ttu-id="f3f33-236">Файл журнала ежедневно перезапускается.</span><span class="sxs-lookup"><span data-stu-id="f3f33-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="f3f33-237">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="f3f33-237">Weekly</span></span>        | <span data-ttu-id="f3f33-238">Хтииммвв. log</span><span class="sxs-lookup"><span data-stu-id="f3f33-238">htYYMMww.log</span></span>   | <span data-ttu-id="f3f33-239">Файл журнала перезапускается еженедельно, где WW — неделя месяца.</span><span class="sxs-lookup"><span data-stu-id="f3f33-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="f3f33-240">Ежемесячно</span><span class="sxs-lookup"><span data-stu-id="f3f33-240">Monthly</span></span>       | <span data-ttu-id="f3f33-241">Хтиимм. log</span><span class="sxs-lookup"><span data-stu-id="f3f33-241">htYYMM.log</span></span>     | <span data-ttu-id="f3f33-242">Файл журнала перезапускается каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="f3f33-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="f3f33-243">Каждый час</span><span class="sxs-lookup"><span data-stu-id="f3f33-243">Hourly</span></span>        | <span data-ttu-id="f3f33-244">Хтииммддхх. log</span><span class="sxs-lookup"><span data-stu-id="f3f33-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="f3f33-245">Файл журнала перезапускается каждый час, где ЧЧ — это час дня, выраженный в 0-24 часе.</span><span class="sxs-lookup"><span data-stu-id="f3f33-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




