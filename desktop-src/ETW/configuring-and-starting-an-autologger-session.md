---
description: Сеанс трассировки событий авторегистратора записывает события, происходящие на ранних этапах процесса загрузки операционной системы.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Настройка и запуск сеанса авторегистратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986137"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="3ca5b-103">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="3ca5b-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="3ca5b-104">Сеанс трассировки событий авторегистратора записывает события, происходящие на ранних этапах процесса загрузки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="3ca5b-105">Приложения и драйверы устройств могут использовать сеанс авторегистратора для записи трассировок перед входом пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="3ca5b-106">Обратите внимание, что некоторые драйверы устройств, например драйверы дисковых устройств, не загружаются во время начала сеанса авторегистратора.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="3ca5b-107">Авторегистратор отличается от глобального средства ведения журнала следующими способами.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="3ca5b-108">Можно указать один или несколько сеансов авторегистратора (глобальное средство ведения журнала было единственным сеансом, в котором регистрируются события).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="3ca5b-109">Авторегистратор отправляет поставщикам уведомления о включении при запуске сеанса (глобальное средство ведения журнала не отправляло уведомления о включении поставщикам, поэтому поставщики должны были полагаться на другие средства, чтобы выяснить, был ли запущен глобальный сеанс ведения журнала для начала ведения журнала событий).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="3ca5b-110">Авторегистратор не поддерживает ведение журнала событий системного журнала NT (см. элемент **енаблефлагс** в [**\_ \_ свойствах трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="3ca5b-111">Чтобы вести журнал событий журнала ядра NT, необходимо использовать [глобальное средство ведения журнала](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="3ca5b-112">Дополнительные сведения о соотношении глобального средства ведения журнала см. в разделе [Настройка и запуск сеанса глобального журнала](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="3ca5b-113">ETW поддерживает авторегистратор в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="3ca5b-114">Используйте [глобальное средство ведения журнала](configuring-and-starting-the-global-logger-session.md) в более ранних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="3ca5b-115">Для настройки сеанса авторегистратора используется реестр.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="3ca5b-116">Добавьте следующий раздел реестра, если он еще не указан:</span><span class="sxs-lookup"><span data-stu-id="3ca5b-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="3ca5b-117">В разделе **авторегистратор** создайте ключ для каждого сеанса авторегистратора, который необходимо настроить, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="3ca5b-118">Для каждого сеанса создайте ключ для каждого поставщика, который необходимо включить в сеанс.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="3ca5b-119">Используйте идентификатор GUID поставщика в качестве ключа.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="3ca5b-120">В следующей таблице описаны значения, которые можно определить для каждого сеанса авторегистратора.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="3ca5b-121">Для задания этих значений реестра необходимо иметь права администратора.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="3ca5b-122">Значения **Start** и **GUID** являются единственными значениями, необходимыми для запуска сеанса авторегистратора. все остальные значения имеют параметры по умолчанию, которые используются, если значение отсутствует в реестре.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="3ca5b-123">Как правило, следует использовать значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-123">Typically, you should use the default values.</span></span> <span data-ttu-id="3ca5b-124">Если указано значение, которое ETW не поддерживает, ETW переопределит это значение.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ca5b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3ca5b-125">Value</span></span></th>
<th><span data-ttu-id="3ca5b-126">Тип</span><span class="sxs-lookup"><span data-stu-id="3ca5b-126">Type</span></span></th>
<th><span data-ttu-id="3ca5b-127">Описание</span><span class="sxs-lookup"><span data-stu-id="3ca5b-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ca5b-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="3ca5b-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-130">Размер каждого буфера в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="3ca5b-131">Должно быть меньше одного мегабайта.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-131">Should be less than one megabyte.</span></span> <span data-ttu-id="3ca5b-132">Для вычисления этого значения ETW использует размер физической памяти.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-133"><strong>клокктипе</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="3ca5b-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-135">Таймер, используемый при записи отметки времени для каждого события.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="3ca5b-136">1 = значение счетчика производительности (высокое разрешение)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="3ca5b-137">2 = системный таймер</span><span class="sxs-lookup"><span data-stu-id="3ca5b-137">2 = System timer</span></span></li>
<li><span data-ttu-id="3ca5b-138">3 = счетчик циклов ЦП</span><span class="sxs-lookup"><span data-stu-id="3ca5b-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="3ca5b-139">Описание каждого типа часов см. в описании элемента <strong>ClientContext</strong> в <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="3ca5b-140">Значение по умолчанию — 1 (значение счетчика производительности) в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="3ca5b-141">До Windows Vista значение по умолчанию — 2 (системный таймер).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-142"><strong>дисаблереалтимеперсистенце</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="3ca5b-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-144">Чтобы отключить сохраняемость в режиме реального времени, задайте для этого параметра значение 1.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="3ca5b-145">Значение по умолчанию — 0 (включено) для сеансов реального времени.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="3ca5b-146">Если включено сохранение в реальном времени, события в реальном времени, которые не были доставлены на момент завершения работы компьютера, будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="3ca5b-147">Затем события будут доставлены потребителю при следующем подключении потребителя к сеансу.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-148"><strong>филекаунтер</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="3ca5b-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-150">Не устанавливайте или не изменяйте это значение.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-150">Do not set or modify this value.</span></span> <span data-ttu-id="3ca5b-151">Это серийный номер, используемый для увеличения имени файла журнала, если задано значение <strong>филемакс</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="3ca5b-152">Если значение недопустимо, то предполагается 1.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="3ca5b-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="3ca5b-155">Полный путь к файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="3ca5b-156">Путь к этому файлу должен существовать.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-156">The path to this file must exist.</span></span> <span data-ttu-id="3ca5b-157">Файл журнала является последовательным файлом журнала.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-157">The log file is a sequential log file.</span></span> <span data-ttu-id="3ca5b-158">Длина пути ограничена 1024 символами.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="3ca5b-159">Если <strong>имя файла</strong> не указано, события записываются в%systemroot%\System32\LogFiles\WMI\ <sessionname> . ETL.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-160"><strong>филемакс</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="3ca5b-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-162">Максимальное число экземпляров файла журнала, создаваемых ETW.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="3ca5b-163">Если файл журнала, указанный в файле <strong>filename</strong> , существует, ETW добавляет значение <strong>филекаунтер</strong> к имени файла.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="3ca5b-164">Например, если используется имя файла журнала по умолчанию, то используется форма%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . ETL. NNNN.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.NNNN.</span></span> <br/> <span data-ttu-id="3ca5b-165">При первом запуске компьютера имя файла — <sessionname> . ETL. 0001, второй раз — имя файла <sessionname> . ETL. 0002 и т. д.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-165">The first time the computer is started, the file name is <sessionname>.etl.0001, the second time the file name is <sessionname>.etl.0002, and so on.</span></span> <span data-ttu-id="3ca5b-166">Если <strong>филемакс</strong> имеет значение 3, то при четвертом перезапуске компьютера ТРАССИРОВКА событий Windows сбрасывает счетчик в значение 1 и перезаписывает <sessionname> . ETL. 0001, если он существует.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites <sessionname>.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="3ca5b-167">Максимальное число поддерживаемых экземпляров файла журнала — 16.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="3ca5b-168">Не используйте эту функцию в режиме файла журнала <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-169"><strong>флуштимер</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="3ca5b-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-171">Частота принудительного сброса буферов трассировки в секундах.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="3ca5b-172">Минимальное время записи на диск — 1 секунда.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="3ca5b-173">Этот принудительный сброс находится в дополнение к автоматическому сбросу, который происходит при заполнении буфера и остановке сеанса трассировки.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="3ca5b-174">В случае средства ведения журнала в реальном времени значение 0 (значение по умолчанию) означает, что время очистки будет равно 1 секунде.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="3ca5b-175">Средство ведения журнала в режиме реального времени используется, когда <strong>логфилемоде</strong> имеет значение <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="3ca5b-176">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-176">The default value is 0.</span></span> <span data-ttu-id="3ca5b-177">По умолчанию буферы сбрасываются только в том случае, если они заполнены.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-178"><strong>Устройства</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="3ca5b-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="3ca5b-180">Строка, содержащая идентификатор GUID, однозначно определяющий сеанс.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="3ca5b-181">Это значение обязательно.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-182"><strong>логфилемоде</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="3ca5b-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-184">Укажите один или несколько режимов ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-184">Specify one or more log modes.</span></span> <span data-ttu-id="3ca5b-185">Возможные значения см. в разделе <a href="logging-mode-constants.md">константы режима ведения журнала</a>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="3ca5b-186">Значение по умолчанию — <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="3ca5b-187">Вместо записи в файл журнала можно указать либо <strong>EVENT_TRACE_BUFFERING_MODE</strong> , либо <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="3ca5b-188">Указание <strong>EVENT_TRACE_BUFFERING_MODE</strong> позволяет избежать издержек на сброс содержимого сеанса на диск после того, как файловая система станет доступной.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="3ca5b-189">Обратите внимание, что использование <strong>EVENT_TRACE_BUFFERING_MODE</strong> приведет к тому, что система будет игнорировать значение <strong>максимумбуфферс</strong> , так как размер буфера будет таким же, как и произведение <strong>MinimumBuffers</strong> и <strong>bufferSize</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="3ca5b-190">Сеансы авторегистратора не поддерживают режим ведения журнала <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="3ca5b-191">Если указан параметр <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> , то параметр <strong>bufferSize</strong> должен быть явно задан и должен быть одинаковым в средстве ведения журнала и в добавляемом файле.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="3ca5b-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-194">Максимальный размер файла журнала в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="3ca5b-195">Сеанс закрывается по достижении максимального размера, если не используется циклический режим файла журнала.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="3ca5b-196">Чтобы не задавать ограничение, задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="3ca5b-197">Значение по умолчанию — 100 МБ, если не задано.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="3ca5b-198">Поведение, которое происходит при достижении максимального размера файла, зависит от значения <strong>логфилемоде</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="3ca5b-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-201">Максимальное количество выделяемых буферов.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="3ca5b-202">Обычно это значение является минимальным числом буферов плюс двадцать.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="3ca5b-203">Для вычисления этого значения ETW использует размер буфера и размер физической памяти.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="3ca5b-204">Это значение должно быть больше или равно значению для <strong>MinimumBuffers</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="3ca5b-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-207">Минимальное число буферов, выделяемых при запуске.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="3ca5b-208">Минимальное число буферов, которые можно указать, — два буфера на процессор.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="3ca5b-209">Например, на компьютере с одним процессором минимальное число буферов равно двум.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-210"><strong>Запуск</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="3ca5b-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-212">Чтобы сеанс авторегистратора запускался при следующем перезапуске компьютера, присвойте этому параметру значение 1; в противном случае присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-213"><strong>Состояние</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="3ca5b-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-215">Состояние запуска авторегистратора.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="3ca5b-216">Если не удалось запустить авторегистратор, значение этого раздела соответствует коду ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="3ca5b-217">Если авторегистратор успешно запущен, значение этого параметра — <strong>ERROR_SUCCESS</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ca5b-218">В следующей таблице описаны значения, которые можно определить для каждого поставщика, который необходимо включить в сеанс.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="3ca5b-219">Для задания этих значений реестра необходимо иметь права администратора.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="3ca5b-220">Если указано значение, которое ETW не поддерживает, ETW переопределит это значение.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ca5b-221">Значение</span><span class="sxs-lookup"><span data-stu-id="3ca5b-221">Value</span></span></th>
<th><span data-ttu-id="3ca5b-222">Тип</span><span class="sxs-lookup"><span data-stu-id="3ca5b-222">Type</span></span></th>
<th><span data-ttu-id="3ca5b-223">Описание</span><span class="sxs-lookup"><span data-stu-id="3ca5b-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ca5b-224"><strong>Enabled</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="3ca5b-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-226">Определяет, включен ли поставщик.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="3ca5b-227">Чтобы включить поставщик, присвойте этому параметру значение 1.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="3ca5b-228">Чтобы отключить поставщик, присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="3ca5b-229">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-230"><strong>енаблефлагс</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="3ca5b-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-232">Определяемое поставщиком значение, указывающее класс событий, для которых поставщик создает события.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="3ca5b-233">Дополнительные сведения см. в описании параметра <em>енаблефлагс</em> функции <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>енаблетраце</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="3ca5b-234">Укажите это имя значения, если поставщик не поддерживает <strong>матчаникэйворд</strong> или <strong>матчаллкэйворд</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-235"><strong>енаблелевел</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="3ca5b-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-237">Определяемое поставщиком значение, указывающее уровень детализации, включаемый в событие.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="3ca5b-238">Например, это значение можно использовать для указания степени серьезности событий (информационное, предупреждение, ошибка), создаваемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="3ca5b-239">Список предварительно определенных уровней см. в описании параметра <em>Level</em> функции <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>енаблетрацеекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-240"><strong>енаблепроперти</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="3ca5b-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-242">Используйте это значение, чтобы включить в файл журнала один или несколько следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="3ca5b-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="3ca5b-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = включить в Расширенные данные идентификатор безопасности (SID) пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="3ca5b-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = включить в Расширенные данные идентификатор сеанса терминала.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="3ca5b-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = включить в Расширенные данные трассировку стека вызовов для событий, написанных с помощью <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="3ca5b-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = отфильтровывает все события, для которых не указано ключевое слово, отличное от нуля.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="3ca5b-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = указывает, что этот вызов <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> должен включать <a href="provider-traits.md">группу поставщиков</a> , а не отдельный поставщик событий.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="3ca5b-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = включить стартовый ключ процесса в Расширенные данные.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="3ca5b-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = включить ключ события в Расширенные данные.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="3ca5b-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = отфильтровывает все события, помеченные как события InPrivate или поступающие из процесса, помеченного как InPrivate.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="3ca5b-251">Дополнительные сведения об этих элементах см. в разделе <strong>енаблепроперти</strong> структуры <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca5b-252"><strong>матчаникэйворд</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="3ca5b-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-254">Битовая маска ключевых слов, определяющая категорию событий, которые должен записывать поставщик.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="3ca5b-255">Поставщик записывает событие, если любое из битов ключевых слов события соответствует любому из битов, заданных в этой маске.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="3ca5b-256">Чтобы указать, что поставщик записывает все события, присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="3ca5b-257">Пример см. в разделе "Примечания" функции <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>енаблетрацеекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca5b-258"><strong>матчаллкэйворд</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="3ca5b-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="3ca5b-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="3ca5b-260">Эта битовая маска является необязательной.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-260">This bitmask is optional.</span></span> <span data-ttu-id="3ca5b-261">Кроме того, эта маска позволяет ограничить категорию событий, которые должен записывать поставщик.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="3ca5b-262">Если ключевое слово события соответствует условию <em>матчаникэйворд</em> , поставщик будет записывать событие только в том случае, если все биты в этой маске существуют в ключевом слове события.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="3ca5b-263">Эта маска не используется, если <em>матчаникэйворд</em> имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="3ca5b-264">Пример см. в разделе "Примечания" функции <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>енаблетрацеекс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ca5b-265">После изменения реестра сеанс авторегистратора запускается при следующем перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="3ca5b-266">Сеанс авторегистратора вызывает функцию [**енаблетрацеекс**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) для включения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="3ca5b-267">Сеансы авторегистратора увеличивают время загрузки системы и должны использоваться с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="3ca5b-268">Службы, которые хотят собирать информацию во время процесса загрузки, должны рассмотреть возможность добавления логики контроллера к самой себе вместо использования сеанса авторегистратора.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="3ca5b-269">Чтобы прерывать сеанс авторегистратора, вызовите функцию [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea) .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="3ca5b-270">Имя сеанса, передаваемое в функцию, является именем раздела реестра, который использовался для определения сеанса в реестре.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="3ca5b-271">В Windows 8.1, в Windows Server 2012 R2 и более поздних версиях фильтры анализа полезных данных события, области действия и стека могут использоваться функцией [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) , [**а \_ \_ параметры включения трассировки**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) и [**\_ \_ дескриптора фильтра событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) — для фильтрации по конкретным условиям сеанса ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="3ca5b-272">Дополнительные сведения о фильтрах полезных данных событий см. в статьях функции [**тдхкреатепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)и [**тдхаггрегатепайлоадфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , а также структуры [**\_ \_ предикатов**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **включения \_ трассировки \_**, **\_ \_ дескриптора фильтра событий** и фильтра полезных данных.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="3ca5b-273">Дополнительные сведения о запуске сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="3ca5b-274">Дополнительные сведения о запуске закрытого сеанса ведения журнала см. в разделе [Настройка и запуск закрытого сеанса ведения журнала](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="3ca5b-275">Дополнительные сведения о запуске сеанса ведения журнала ядра NT см. в разделе [Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="3ca5b-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ca5b-276">См. также</span><span class="sxs-lookup"><span data-stu-id="3ca5b-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ca5b-277">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="3ca5b-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="3ca5b-278">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="3ca5b-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="3ca5b-279">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="3ca5b-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="3ca5b-280">Настройка и запуск сеанса ведения журнала ядра NT</span><span class="sxs-lookup"><span data-stu-id="3ca5b-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="3ca5b-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="3ca5b-282">**ВКЛЮЧИТЬ \_ \_ Параметры трассировки**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="3ca5b-283">**\_дескриптор фильтра \_ событий**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="3ca5b-284">**\_предикат фильтра полезных данных \_**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="3ca5b-285">**тдхаггрегатепайлоадфилтерс**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="3ca5b-286">**тдхкреатепайлоадфилтер**</span><span class="sxs-lookup"><span data-stu-id="3ca5b-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="3ca5b-287">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="3ca5b-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
