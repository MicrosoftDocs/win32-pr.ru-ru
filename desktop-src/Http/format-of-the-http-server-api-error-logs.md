---
title: Формат журналов ошибок API-сервера HTTP
description: В общем случае файлы журнала ошибок HTTP-сервера имеют тот же формат, что и журналы ошибок W3C, за исключением того, что файлы журнала ошибок API-сервера HTTP не содержат заголовков столбцов.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API сервера HTTP, формат журнала ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252970"
---
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="e684d-104">Формат журналов ошибок API-сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="e684d-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="e684d-105">В общем случае файлы журнала ошибок HTTP-сервера имеют тот же формат, что и журналы ошибок W3C, за исключением того, что файлы журнала ошибок API-сервера HTTP не содержат заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="e684d-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="e684d-106">Каждая строка журнала ошибок API-сервера HTTP регистрирует одну ошибку с полями в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="e684d-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="e684d-107">Каждое поле отделяется от предыдущего поля на один символ пробела (0x0020).</span><span class="sxs-lookup"><span data-stu-id="e684d-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="e684d-108">В пределах каждого поля пробелы, символы табуляции и непечатаемые управляющие символы заменяются знаками «плюс» (0x002B).</span><span class="sxs-lookup"><span data-stu-id="e684d-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="e684d-109">В следующей таблице указаны поля и порядок полей в записи журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="e684d-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e684d-110">Поле</span><span class="sxs-lookup"><span data-stu-id="e684d-110">Field</span></span></th>
<th><span data-ttu-id="e684d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e684d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e684d-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Дата</span><span class="sxs-lookup"><span data-stu-id="e684d-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="e684d-113">Поле даты соответствует формату W3C и основывается на времени в формате UTC. Поле даты всегда имеет 10 символов в формате &quot; гггг-мм-дд &quot; .</span><span class="sxs-lookup"><span data-stu-id="e684d-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="e684d-114">Например, 1 мая 2003 выражается как &quot; 2003-05-01 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e684d-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e684d-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Таймаут</span><span class="sxs-lookup"><span data-stu-id="e684d-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="e684d-116">Поле времени соответствует формату W3C и основывается на времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="e684d-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="e684d-117">Поле времени всегда имеет 8 символов в формате &quot; mm: чч: СС &quot; .</span><span class="sxs-lookup"><span data-stu-id="e684d-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="e684d-118">Например, 5:30 PM (UTC) выражается в виде &quot; 17:30:00 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e684d-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e684d-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>IP-адрес клиента</span><span class="sxs-lookup"><span data-stu-id="e684d-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="e684d-120">IP-адрес затронутого клиента, который может быть либо адресом IPv4, либо IPv6-адресом.</span><span class="sxs-lookup"><span data-stu-id="e684d-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="e684d-121">Если IP-адрес клиента является адресом IPv6, поле ScopeId также включается в адрес.</span><span class="sxs-lookup"><span data-stu-id="e684d-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e684d-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Порт клиента</span><span class="sxs-lookup"><span data-stu-id="e684d-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="e684d-123">Номер порта для затронутого клиента.</span><span class="sxs-lookup"><span data-stu-id="e684d-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e684d-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>IP-адрес сервера</span><span class="sxs-lookup"><span data-stu-id="e684d-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="e684d-125">IP-адрес затронутого сервера, который может быть либо адресом IPv4, либо IPv6-адресом.</span><span class="sxs-lookup"><span data-stu-id="e684d-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="e684d-126">Если IP-адрес сервера является адресом IPv6, поле ScopeId также включается в адрес.</span><span class="sxs-lookup"><span data-stu-id="e684d-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e684d-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Порт сервера</span><span class="sxs-lookup"><span data-stu-id="e684d-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="e684d-128">Номер порта затрагиваемого сервера.</span><span class="sxs-lookup"><span data-stu-id="e684d-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e684d-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Версия протокола</span><span class="sxs-lookup"><span data-stu-id="e684d-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="e684d-130">Версия используемого протокола.</span><span class="sxs-lookup"><span data-stu-id="e684d-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="e684d-131">Если соединение не было проанализировано достаточно, чтобы определить версию протокола, то в качестве заполнителя для пустого поля используется дефис (0x002D).</span><span class="sxs-lookup"><span data-stu-id="e684d-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="e684d-132">Если номер основной или дополнительной версии, проанализированной, больше или равен 10, версия заносится в журнал как &quot; http/?.? &quot; .</span><span class="sxs-lookup"><span data-stu-id="e684d-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e684d-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Переключател</span><span class="sxs-lookup"><span data-stu-id="e684d-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="e684d-134">Состояние команды, передаваемое при синтаксическом анализе последнего запроса.</span><span class="sxs-lookup"><span data-stu-id="e684d-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="e684d-135">Неизвестные команды включены, но любая команда, длина которой превышает 255 байт, усекается до этой длины.</span><span class="sxs-lookup"><span data-stu-id="e684d-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="e684d-136">Если команда недоступна, в качестве заполнителя для пустого поля используется дефис (0x002D).</span><span class="sxs-lookup"><span data-stu-id="e684d-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e684d-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>Кукедурл + запрос</span><span class="sxs-lookup"><span data-stu-id="e684d-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="e684d-138">URL-адрес и все связанные с ним запросы регистрируются в виде одного поля, разделенного вопросительным знаком (0x3F).</span><span class="sxs-lookup"><span data-stu-id="e684d-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="e684d-139">Это поле усекается по длине в 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="e684d-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="e684d-140">Если этот URL-адрес был проанализирован ( &quot; обработанные &quot; ), он заносится в журнал с локальным преобразованием кодовой страницы и рассматривается как поле Юникода.</span><span class="sxs-lookup"><span data-stu-id="e684d-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="e684d-141">Если этот URL-адрес не был проанализирован ( &quot; обработанные &quot; ) во время ведения журнала, он копируется в точности без преобразования в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e684d-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="e684d-142">Если API сервера HTTP не может проанализировать этот URL-адрес, в качестве заполнителя для пустого поля используется дефис (0x002D).</span><span class="sxs-lookup"><span data-stu-id="e684d-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e684d-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Состояние протокола</span><span class="sxs-lookup"><span data-stu-id="e684d-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="e684d-144">Состояние протокола не может превышать 999.</span><span class="sxs-lookup"><span data-stu-id="e684d-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="e684d-145">Если состояние протокола ответа на запрос доступен, он заносится в это поле.</span><span class="sxs-lookup"><span data-stu-id="e684d-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="e684d-146">Если состояние протокола недоступно, в качестве заполнителя для пустого поля используется дефис (0x002D).</span><span class="sxs-lookup"><span data-stu-id="e684d-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e684d-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e684d-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="e684d-148">Не используется в этой версии API сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="e684d-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="e684d-149">В этом поле всегда отображается замещающий дефис (0x002D).</span><span class="sxs-lookup"><span data-stu-id="e684d-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e684d-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Фраза причины</span><span class="sxs-lookup"><span data-stu-id="e684d-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="e684d-151">Это поле содержит строку, которая определяет тип регистрируемой ошибки.</span><span class="sxs-lookup"><span data-stu-id="e684d-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="e684d-152">Он никогда не остается пустым.</span><span class="sxs-lookup"><span data-stu-id="e684d-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e684d-153">Следующие примеры строк относятся к журналу ошибок API-сервера HTTP:</span><span class="sxs-lookup"><span data-stu-id="e684d-153">The following sample lines are from an HTTP Server API error log:</span></span>

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





