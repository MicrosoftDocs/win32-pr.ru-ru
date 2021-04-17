---
description: Средство настройки трассировки служб Microsoft Windows HTTP (WinHTTP), WinHttpTraceCfg.exe, используется для настройки возможностей трассировки для отладки и целей сканирования пакетов.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, средство настройки трассировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711064"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="24bf9-103">WinHttpTraceCfg.exe, средство настройки трассировки</span><span class="sxs-lookup"><span data-stu-id="24bf9-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="24bf9-104">Средство настройки трассировки [служб Microsoft Windows HTTP (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, используется для настройки возможностей трассировки для отладки и целей сканирования пакетов.</span><span class="sxs-lookup"><span data-stu-id="24bf9-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="24bf9-105">Важна возможность отслеживать функции WinHTTP и их соответствующий сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="24bf9-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="24bf9-106">Отладка приложений, использующих зашифрованные протоколы передачи данных, такие как SSL (SSL), исключает перехват пакетов на транспортном уровне сети и требует возможность перехвата трафика между клиентом и сервером после его расшифровки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="24bf9-107">Службы Microsoft Windows HTTP Services (WinHTTP) предоставляют средство трассировки, имеющее ряд возможностей для перехвата потока трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="24bf9-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="24bf9-108">Это средство трассировки может быть ценным инструментом для отладки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="24bf9-109">Его можно использовать, например, для просмотра параметров, передаваемых в различные вызовы функций, а также для просмотра фактических данных, отправляемых и получаемых приложением WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="24bf9-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="24bf9-110">Использование средства трассировки</span><span class="sxs-lookup"><span data-stu-id="24bf9-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="24bf9-111">Анализ данных трассировки</span><span class="sxs-lookup"><span data-stu-id="24bf9-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="24bf9-112">Использование средства трассировки</span><span class="sxs-lookup"><span data-stu-id="24bf9-112">Using the Trace Facility</span></span>

<span data-ttu-id="24bf9-113">WinHTTP получает параметры управления трассировкой из реестра.</span><span class="sxs-lookup"><span data-stu-id="24bf9-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="24bf9-114">Эти параметры управления влияют на то, как WinHTTP создает выходные данные трассировки и как форматирует выходные данные.</span><span class="sxs-lookup"><span data-stu-id="24bf9-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="24bf9-115">Все приложения, использующие WinHTTP, имеют одни и те же параметры.</span><span class="sxs-lookup"><span data-stu-id="24bf9-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="24bf9-116">Средство настройки средства трассировки, WinHttpTraceCfg.exe, доступно для загрузки на веб-сайте [средств комплекта ресурсов Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="24bf9-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="24bf9-117">Средство настройки конфигурации задает или получает параметры реестра средства трассировки на основе указанных параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="24bf9-118">В следующей таблице перечислены возможные параметры для средства настройки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24bf9-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="24bf9-119">Parameter</span></span></th>
<th><span data-ttu-id="24bf9-120">Описание</span><span class="sxs-lookup"><span data-stu-id="24bf9-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24bf9-121">-?</span><span class="sxs-lookup"><span data-stu-id="24bf9-121">-?</span></span></td>
<td><span data-ttu-id="24bf9-122">Отображает данные синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="24bf9-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-123">-E</span><span class="sxs-lookup"><span data-stu-id="24bf9-123">-e</span></span></td>
<td><span data-ttu-id="24bf9-124">Указывает, включено или отключено средство трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24bf9-125">0</span><span class="sxs-lookup"><span data-stu-id="24bf9-125">0</span></span></td>
<td><span data-ttu-id="24bf9-126">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24bf9-126">Default setting.</span></span> <span data-ttu-id="24bf9-127">Отключает трассировку.</span><span class="sxs-lookup"><span data-stu-id="24bf9-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-128">1</span><span class="sxs-lookup"><span data-stu-id="24bf9-128">1</span></span></td>
<td><span data-ttu-id="24bf9-129">Включение трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24bf9-130">-l</span><span class="sxs-lookup"><span data-stu-id="24bf9-130">-l</span></span></td>
<td><p><span data-ttu-id="24bf9-131">Задает префикс для файла журнала.</span><span class="sxs-lookup"><span data-stu-id="24bf9-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="24bf9-132">Префикс может включать путь.</span><span class="sxs-lookup"><span data-stu-id="24bf9-132">The prefix can include a path.</span></span> <span data-ttu-id="24bf9-133">Файл журнала записывается в текущий каталог или каталог, указанный в префиксе, и имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="24bf9-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="24bf9-134"><<em></em> > префикс -< <em>имя приложения</em> > . <<em>время</em> > . журнал</span><span class="sxs-lookup"><span data-stu-id="24bf9-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="24bf9-135">Если префикс не указан, используется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="24bf9-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="24bf9-136">Укажите &quot; \* &quot; , чтобы удалить существующий префикс.</span><span class="sxs-lookup"><span data-stu-id="24bf9-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-137">-d</span><span class="sxs-lookup"><span data-stu-id="24bf9-137">-d</span></span></td>
<td><p><span data-ttu-id="24bf9-138">Указывает, отображаются ли выходные данные трассировки в отладчике или записываются в файл.</span><span class="sxs-lookup"><span data-stu-id="24bf9-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24bf9-139">0</span><span class="sxs-lookup"><span data-stu-id="24bf9-139">0</span></span></td>
<td><span data-ttu-id="24bf9-140">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24bf9-140">Default setting.</span></span> <span data-ttu-id="24bf9-141">Выполняет запись в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="24bf9-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-142">1</span><span class="sxs-lookup"><span data-stu-id="24bf9-142">1</span></span></td>
<td><span data-ttu-id="24bf9-143">Отображается в отладчике.</span><span class="sxs-lookup"><span data-stu-id="24bf9-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24bf9-144">-S</span><span class="sxs-lookup"><span data-stu-id="24bf9-144">-s</span></span></td>
<td><p><span data-ttu-id="24bf9-145">Указывает способ отображения сетевого трафика (запросов и ответов).</span><span class="sxs-lookup"><span data-stu-id="24bf9-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24bf9-146">0</span><span class="sxs-lookup"><span data-stu-id="24bf9-146">0</span></span></td>
<td><span data-ttu-id="24bf9-147">Отображаются только заголовки HTTP.</span><span class="sxs-lookup"><span data-stu-id="24bf9-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-148">1</span><span class="sxs-lookup"><span data-stu-id="24bf9-148">1</span></span></td>
<td><span data-ttu-id="24bf9-149">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24bf9-149">Default setting.</span></span> <span data-ttu-id="24bf9-150">Показывает сетевой трафик в формате Американский национальный институт стандартов (ANSI) (ANSI).</span><span class="sxs-lookup"><span data-stu-id="24bf9-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24bf9-151">2</span><span class="sxs-lookup"><span data-stu-id="24bf9-151">2</span></span></td>
<td><span data-ttu-id="24bf9-152">Показывает сетевой трафик в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="24bf9-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-153">-T</span><span class="sxs-lookup"><span data-stu-id="24bf9-153">-t</span></span></td>
<td><p><span data-ttu-id="24bf9-154">Указывает, записываются ли в трассировке вызовы функций верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="24bf9-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24bf9-155">0</span><span class="sxs-lookup"><span data-stu-id="24bf9-155">0</span></span></td>
<td><span data-ttu-id="24bf9-156">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24bf9-156">Default setting.</span></span> <span data-ttu-id="24bf9-157">Вызовы функций не записываются.</span><span class="sxs-lookup"><span data-stu-id="24bf9-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24bf9-158">1</span><span class="sxs-lookup"><span data-stu-id="24bf9-158">1</span></span></td>
<td><span data-ttu-id="24bf9-159">Записываются вызовы функций верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="24bf9-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24bf9-160">-M</span><span class="sxs-lookup"><span data-stu-id="24bf9-160">-m</span></span></td>
<td><p><span data-ttu-id="24bf9-161">Указывает максимальный размер (в байтах) файла журнала, созданного средством трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="24bf9-162">Если этот параметр указан без размера, минимальное значение — 65 535 байт.</span><span class="sxs-lookup"><span data-stu-id="24bf9-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="24bf9-163">Если размер файла журнала достигает максимального значения, содержимое файла удаляется.</span><span class="sxs-lookup"><span data-stu-id="24bf9-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="24bf9-164">Данные трассировки по мере продолжения записываются в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="24bf9-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="24bf9-165">Запуск средства настройки средства трассировки и указание параметра без параметров извлекает и отображает текущие параметры реестра.</span><span class="sxs-lookup"><span data-stu-id="24bf9-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="24bf9-166">Файлы журналов быстро увеличиваются и снижают производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="24bf9-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="24bf9-167">Перед включением средства трассировки убедитесь в наличии необходимого места на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="24bf9-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="24bf9-168">Анализ данных трассировки</span><span class="sxs-lookup"><span data-stu-id="24bf9-168">Interpreting Trace Data</span></span>

<span data-ttu-id="24bf9-169">Поток данных средства трассировки отражает функции WinHTTP, вызываемые в приложении, и любые отправленные или полученные данные HTTP.</span><span class="sxs-lookup"><span data-stu-id="24bf9-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="24bf9-170">В некоторых случаях также показаны функции, называемые внутренними WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="24bf9-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="24bf9-171">На следующем рисунке показана часть файла журнала, созданного средством трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="24bf9-172">Несколько элементов выделены и помечаются меткой.</span><span class="sxs-lookup"><span data-stu-id="24bf9-172">Several items are highlighted and labeled.</span></span>

![Пример трассировки](images/ss-tracer-wco.png)

<span data-ttu-id="24bf9-174">Каждая строка выходных данных трассировки содержит сведения в трех столбцах.</span><span class="sxs-lookup"><span data-stu-id="24bf9-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="24bf9-175">В первом столбце отображаются дата и время записи.</span><span class="sxs-lookup"><span data-stu-id="24bf9-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="24bf9-176">Во втором столбце показан идентификатор запроса (ID), который можно использовать для различения нескольких запросов.</span><span class="sxs-lookup"><span data-stu-id="24bf9-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="24bf9-177">Если запись журнала не соответствует определенному запросу, \* \* в этом столбце отображается "Session".</span><span class="sxs-lookup"><span data-stu-id="24bf9-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="24bf9-178">Можно отсортировать файл журнала по этому ИДЕНТИФИКАТОРу, чтобы просмотреть только события, происходящие в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="24bf9-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="24bf9-179">В следующем примере показана команда, которую можно использовать для сортировки файла журнала.</span><span class="sxs-lookup"><span data-stu-id="24bf9-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="24bf9-180">**Findstr 00000001 файл_журнала. log**</span><span class="sxs-lookup"><span data-stu-id="24bf9-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="24bf9-181">В третьем столбце показан вызов функции, HTTP-трафик или сообщение о состоянии, добавленное для интерпретации трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="24bf9-182">Если запись журнала соответствует вызову функции, также записываются параметры функции.</span><span class="sxs-lookup"><span data-stu-id="24bf9-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="24bf9-183">Адреса памяти отображаются в шестнадцатеричном виде, а все остальные значения отображаются в виде строки ASCII.</span><span class="sxs-lookup"><span data-stu-id="24bf9-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="24bf9-184">Средство трассировки также записывает время и значение возврата для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="24bf9-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="24bf9-185">Формат данных HTTP зависит от параметров реестра, заданных в средстве настройки средства трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="24bf9-186">При шифровании данных HTTP расшифрованные данные также отображаются в выходных данных трассировки.</span><span class="sxs-lookup"><span data-stu-id="24bf9-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




