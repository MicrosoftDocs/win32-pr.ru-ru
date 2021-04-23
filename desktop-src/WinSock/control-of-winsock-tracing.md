---
description: .
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Управление трассировкой Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b15ece4581525fddc25213c630e24d0e49110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701548"
---
# <a name="control-of-winsock-tracing"></a><span data-ttu-id="22ae8-103">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-103">Control of Winsock Tracing</span></span>

<span data-ttu-id="22ae8-104">Трассировку Winsock можно контролировать с помощью любого из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="22ae8-104">Winsock tracing can be controlled by using either of the following methods:</span></span>

-   <span data-ttu-id="22ae8-105">Программы командной строки</span><span class="sxs-lookup"><span data-stu-id="22ae8-105">Command-line tools</span></span>

    <span data-ttu-id="22ae8-106">В Windows Vista и Windows Server 2008 включены два средства командной строки, которые используются для управления трассировкой и преобразования двоичного файла журнала трассировки в читаемый текст.</span><span class="sxs-lookup"><span data-stu-id="22ae8-106">Two command-line tools are included with Windows Vista and Windows Server 2008 that are used to control tracing and convert the binary trace log file to readable text.</span></span>

    <span data-ttu-id="22ae8-107">Средство **logman.exe** используется для запуска или завершения трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="22ae8-107">The **logman.exe** tool is used to start or stop Winsock tracing.</span></span>

    <span data-ttu-id="22ae8-108">Средство **tracerpt.exe** используется для преобразования двоичного файла журнала трассировки в читаемый текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="22ae8-108">The **tracerpt.exe** tool is used to convert the binary trace log file to a readable text file.</span></span>

-   <span data-ttu-id="22ae8-109">Просмотр событий</span><span class="sxs-lookup"><span data-stu-id="22ae8-109">Event Viewer</span></span>

    <span data-ttu-id="22ae8-110">Просмотр событий в Windows Vista и более поздних версиях также можно использовать для включения трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="22ae8-110">The Event Viewer on Windows Vista and later can also be used to enable Winsock tracing.</span></span> <span data-ttu-id="22ae8-111">Просмотр событий доступен в меню "Пуск" в разделе "Администрирование".</span><span class="sxs-lookup"><span data-stu-id="22ae8-111">The Event Viewer is accessible under the Administrative Tools from the Start menu.</span></span>

## <a name="using-logman-and-tracert"></a><span data-ttu-id="22ae8-112">Использование программы Logman и tracert</span><span class="sxs-lookup"><span data-stu-id="22ae8-112">Using logman and tracert</span></span>

<span data-ttu-id="22ae8-113">По умолчанию в Windows Vista и более поздних версиях трассировка событий сети Winsock отключена.</span><span class="sxs-lookup"><span data-stu-id="22ae8-113">Winsock network event tracing is disabled by default on Windows Vista and later.</span></span>

<span data-ttu-id="22ae8-114">Следующая команда запускает трассировку событий сети Winsock на компьютере, устанавливает имя сеанса трассировки событий в мивинсокксессион и отправляет выходные данные в двоичный файл журнала с именем винсокклогфиле. ETL:</span><span class="sxs-lookup"><span data-stu-id="22ae8-114">The following command starts Winsock network event tracing on a computer, sets the name of event trace session to mywinsocksession, and sends output to a binary log file called winsocklogfile.etl:</span></span>

<span data-ttu-id="22ae8-115">**Logman Start-ETS мивинсокксессион-o винсокклогфиле. ETL-p Microsoft-Windows-Winsock-АФД**</span><span class="sxs-lookup"><span data-stu-id="22ae8-115">**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**</span></span>

<span data-ttu-id="22ae8-116">Файлы журнала создаются в текущем каталоге с именами файлов в формате винсокклогфиле \_ 000001. ETL.</span><span class="sxs-lookup"><span data-stu-id="22ae8-116">Log files are created in the current directory with filenames of the form winsocklogfile\_000001.etl</span></span>

<span data-ttu-id="22ae8-117">Следующая команда останавливает приведенную выше трассировку Winsock на компьютере для сеанса с именем мивинсокксессион:</span><span class="sxs-lookup"><span data-stu-id="22ae8-117">The following command stops the above Winsock tracing on a computer for the session named mywinsocksession:</span></span>

<span data-ttu-id="22ae8-118">**Logman-ETS мивинсокксессион**</span><span class="sxs-lookup"><span data-stu-id="22ae8-118">**logman stop -ets mywinsocksession**</span></span>

<span data-ttu-id="22ae8-119">Двоичный файл журнала будет записан в расположение, указанное параметром – o.</span><span class="sxs-lookup"><span data-stu-id="22ae8-119">A binary log file will be written to the location specified by the –o parameter.</span></span> <span data-ttu-id="22ae8-120">Чтобы преобразовать двоичный файл в читаемый текстовый файл, используется **tracerpt.exe** :</span><span class="sxs-lookup"><span data-stu-id="22ae8-120">To translate the binary file into a readable text file, **tracerpt.exe** is used:</span></span>

<span data-ttu-id="22ae8-121">**tracerpt.exe <имя ETL-файла> – o winsocktracelog.txt**</span><span class="sxs-lookup"><span data-stu-id="22ae8-121">**tracerpt.exe <name of the .etl file> –o winsocktracelog.txt**</span></span>

<span data-ttu-id="22ae8-122">Если предпочтительным является выходной файл, содержащий XML, а не обычный текст, используется следующая команда:</span><span class="sxs-lookup"><span data-stu-id="22ae8-122">If an output file containing xml rather than plain text is preferred, the following command is used:</span></span>

<span data-ttu-id="22ae8-123">**tracerpt.exe <имя ETL-файла> – o winsocktracelog.xml – of XML.**</span><span class="sxs-lookup"><span data-stu-id="22ae8-123">**tracerpt.exe <name of the .etl file> –o winsocktracelog.xml –of xml**</span></span>

<span data-ttu-id="22ae8-124">Трассировка изменений каталога Winsock включена по умолчанию в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="22ae8-124">Winsock catalog change tracing is enabled by default on Windows Vista and later.</span></span>

> [!Note]  
> <span data-ttu-id="22ae8-125">Многоуровневые поставщики служб являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="22ae8-125">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="22ae8-126">Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="22ae8-126">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="22ae8-127">Следующая команда запускает трассировку изменений каталога Winsock для многоуровневых поставщиков служб (LSP) на компьютере, устанавливает имя сеанса трассировки событий в мивинсокккаталогсессион и отправляет выходные данные в двоичный файл журнала с именем винсокккаталоглогфиле. ETL:</span><span class="sxs-lookup"><span data-stu-id="22ae8-127">The following command starts Winsock Catalog Change tracing for layered service providers (LSPs) on a computer, sets the name of event trace session to mywinsockcatalogsession, and sends output to a binary log file called winsockcataloglogfile.etl:</span></span>

<span data-ttu-id="22ae8-128">**Logman Start-ETS мивинсокккаталогсессион-o винсокккаталоглогфиле. ETL-p Microsoft-Windows-Winsock-WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="22ae8-128">**logman start -ets mywinsockcatalogsession -o winsockcataloglogfile.etl -p Microsoft-Windows-Winsock-WS2HELP**</span></span>

<span data-ttu-id="22ae8-129">Файлы журнала создаются в текущем каталоге с именами файлов в формате винсокккаталоглогфиле \_ 000001. ETL.</span><span class="sxs-lookup"><span data-stu-id="22ae8-129">Log files are created in the current directory with filenames of the form winsockcataloglogfile\_000001.etl</span></span>

<span data-ttu-id="22ae8-130">Следующая команда останавливает приведенную выше трассировку Winsock на компьютере для сеанса с именем MySession:</span><span class="sxs-lookup"><span data-stu-id="22ae8-130">The following command stops the above Winsock tracing on a computer for the session named mysession:</span></span>

<span data-ttu-id="22ae8-131">**Logman-ETS мивинсокккаталогсессион**</span><span class="sxs-lookup"><span data-stu-id="22ae8-131">**logman stop -ets mywinsockcatalogsession**</span></span>

<span data-ttu-id="22ae8-132">Двоичный файл журнала будет записан в расположение, указанное параметром – o.</span><span class="sxs-lookup"><span data-stu-id="22ae8-132">A binary log file will be written to the location specified by the –o parameter.</span></span> <span data-ttu-id="22ae8-133">Чтобы преобразовать двоичный файл в читаемый текстовый файл, используется **tracerpt.exe** :</span><span class="sxs-lookup"><span data-stu-id="22ae8-133">To translate the binary file into a readable text file, **tracerpt.exe** is used:</span></span>

<span data-ttu-id="22ae8-134">**tracerpt.exe <имя ETL-файла> – o winsockcatalogtracelog.txt**</span><span class="sxs-lookup"><span data-stu-id="22ae8-134">**tracerpt.exe <name of the .etl file> –o winsockcatalogtracelog.txt**</span></span>

<span data-ttu-id="22ae8-135">Если предпочтительным является выходной файл, содержащий XML, а не обычный текст, используется следующая команда:</span><span class="sxs-lookup"><span data-stu-id="22ae8-135">If an output file containing xml rather than plain text is preferred, the following command is used:</span></span>

<span data-ttu-id="22ae8-136">**tracerpt.exe <имя ETL-файла> – o winsockcatalogtracelog.xml – of XML.**</span><span class="sxs-lookup"><span data-stu-id="22ae8-136">**tracerpt.exe <name of the .etl file> –o winsockcatalogtracelog.xml –of xml**</span></span>

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a><span data-ttu-id="22ae8-137">Использование Просмотр событий для запуска трассировки событий сети Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-137">Using Event Viewer to Start Winsock Network Event Tracing</span></span>

<span data-ttu-id="22ae8-138">При открытии Просмотр событий в левой области содержится список событий.</span><span class="sxs-lookup"><span data-stu-id="22ae8-138">When you open Event Viewer, the left pane contains the list of events.</span></span> <span data-ttu-id="22ae8-139">Откройте **журналы приложений и служб** и перейдите к **\\ \\ сетевому событию Microsoft Windows Winsock** в качестве источника и выберите пункт **Операционная**.</span><span class="sxs-lookup"><span data-stu-id="22ae8-139">Open **Applications and Services Logs** and navigate to **Microsoft\\Windows\\Winsock Network Event** as the source and select **Operational**.</span></span>

<span data-ttu-id="22ae8-140">В области Действие выберите **Свойства журнала** и установите флажок **включить ведение журнала** .</span><span class="sxs-lookup"><span data-stu-id="22ae8-140">In the Action pane, select **Log Properties** and check the **Enable Logging** check box.</span></span> <span data-ttu-id="22ae8-141">После включения ведения журнала можно также изменить размер файла журнала, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="22ae8-141">Once logging is enabled, you can also change the size of the log file if this is needed.</span></span>

<span data-ttu-id="22ae8-142">Теперь трассировка событий сети Winsock включена, и все, что нужно сделать, — это действие Обновить, чтобы обновить список событий, которые были занесены в журнал.</span><span class="sxs-lookup"><span data-stu-id="22ae8-142">Winsock network event tracing is now enabled and all you need to do is hit the Refresh action to update the list of events that have been logged.</span></span> <span data-ttu-id="22ae8-143">Чтобы прерывать ведение журнала, просто снимите флажок в том же переключателе.</span><span class="sxs-lookup"><span data-stu-id="22ae8-143">To stop logging, simply uncheck the same radio button.</span></span>

<span data-ttu-id="22ae8-144">Может потребоваться увеличить размер журнала в зависимости от количества событий, которые вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="22ae8-144">You may need to increase the log size depending on how many events you want to see.</span></span> <span data-ttu-id="22ae8-145">Недостаток использования Просмотр событий для трассировки Winsock заключается в том, что он не загружает все строковые ресурсы, поэтому сообщения, отображаемые в поле Описание (после выбора события), иногда трудно читать (например, аргумент, который должен быть отформатирован как шестнадцатеричный, будет отображаться в десятичном формате).</span><span class="sxs-lookup"><span data-stu-id="22ae8-145">One drawback to using the Event Viewer for Winsock tracing is that it does not load all the string resources so the messages displayed in the Description field (once you select an event) is sometimes hard to read (an argument that should be formatted as hex will be displayed in decimal, for example).</span></span> <span data-ttu-id="22ae8-146">Однако можно выбрать вкладку **сведения** в описании события, которая показывает необработанную запись в журнале XML, которая обычно упрощает понимание аргументов.</span><span class="sxs-lookup"><span data-stu-id="22ae8-146">However, you can select the **Details** tab in the event description which shows the raw XML log entry which usually has easier to understand arguments.</span></span>

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a><span data-ttu-id="22ae8-147">Использование Просмотр событий для запуска трассировки изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-147">Using Event Viewer to Start Winsock Catalog Change Tracing</span></span>

<span data-ttu-id="22ae8-148">При открытии Просмотр событий в левой области содержится список событий.</span><span class="sxs-lookup"><span data-stu-id="22ae8-148">When you open Event Viewer, the left pane contains the list of events.</span></span> <span data-ttu-id="22ae8-149">Откройте **журналы приложений и служб** и перейдите в раздел **Microsoft \\ Windows \\ Winsock Каталог изменение** в качестве источника и выберите **Операционная**.</span><span class="sxs-lookup"><span data-stu-id="22ae8-149">Open **Applications and Services Logs** and navigate to **Microsoft\\Windows\\Winsock Catalog Change** as the source and select **Operational**.</span></span>

<span data-ttu-id="22ae8-150">В области Действие выберите **Свойства журнала** и установите флажок **включить ведение журнала** .</span><span class="sxs-lookup"><span data-stu-id="22ae8-150">In the Action pane, select **Log Properties** and check the **Enable Logging** check box.</span></span> <span data-ttu-id="22ae8-151">После включения ведения журнала можно также изменить размер файла журнала, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="22ae8-151">Once logging is enabled, you can also change the size of the log file if this is needed.</span></span>

<span data-ttu-id="22ae8-152">Трассировка изменений каталога Winsock теперь включена, и все, что нужно сделать, — это действие Обновить, чтобы обновить список событий, которые были занесены в журнал.</span><span class="sxs-lookup"><span data-stu-id="22ae8-152">Winsock catalog change tracing is now enabled and all you need to do is hit the Refresh action to update the list of events that have been logged.</span></span> <span data-ttu-id="22ae8-153">Чтобы прерывать ведение журнала, просто снимите флажок в том же переключателе.</span><span class="sxs-lookup"><span data-stu-id="22ae8-153">To stop logging, simply uncheck the same radio button.</span></span>

<span data-ttu-id="22ae8-154">Может потребоваться увеличить размер журнала в зависимости от количества событий, которые вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="22ae8-154">You may need to increase the log size depending on how many events you want to see.</span></span> <span data-ttu-id="22ae8-155">Недостаток использования Просмотр событий для трассировки Winsock заключается в том, что он не загружает все строковые ресурсы, поэтому сообщения, отображаемые в поле Описание (после выбора события), иногда трудно читать (например, аргумент, который должен быть отформатирован как шестнадцатеричный, будет отображаться в десятичном формате).</span><span class="sxs-lookup"><span data-stu-id="22ae8-155">One drawback to using the Event Viewer for Winsock tracing is that it does not load all the string resources so the messages displayed in the Description field (once you select an event) is sometimes hard to read (an argument that should be formatted as hex will be displayed in decimal, for example).</span></span> <span data-ttu-id="22ae8-156">Однако можно выбрать вкладку **сведения** в описании события, которая показывает необработанную запись в журнале XML, которая обычно упрощает понимание аргументов.</span><span class="sxs-lookup"><span data-stu-id="22ae8-156">However, you can select the **Details** tab in the event description which shows the raw XML log entry which usually has easier to understand arguments.</span></span>

## <a name="interpreting-winsock-tracing-logs"></a><span data-ttu-id="22ae8-157">Анализ журналов трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-157">Interpreting Winsock Tracing Logs</span></span>

<span data-ttu-id="22ae8-158">Все события трассировки Winsock в журнале содержат два типа данных:</span><span class="sxs-lookup"><span data-stu-id="22ae8-158">All Winsock tracing events in a log contain two types of information:</span></span>

-   <span data-ttu-id="22ae8-159">Система</span><span class="sxs-lookup"><span data-stu-id="22ae8-159">System</span></span>
-   <span data-ttu-id="22ae8-160">EventData</span><span class="sxs-lookup"><span data-stu-id="22ae8-160">EventData</span></span>

<span data-ttu-id="22ae8-161">Сведения о системе содержат уровень ведения журнала, время создания записи журнала, идентификатор события, представляющий тип события, идентификатор процесса выполнения, идентификатор потока выполнения и другие сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="22ae8-161">The system information contains the logging level, the time the log entry was created, the event ID that represents the event type, the execution Process ID, the execution Thread ID, and other system information.</span></span> <span data-ttu-id="22ae8-162">Уровень журнала 4 в трассировке Winsock представляет ведение журнала информационных событий.</span><span class="sxs-lookup"><span data-stu-id="22ae8-162">A log level of 4 in Winsock tracing represents information event logging.</span></span> <span data-ttu-id="22ae8-163">Уровень журнала 5 в трассировке Winsock представляет подробное ведение журнала событий.</span><span class="sxs-lookup"><span data-stu-id="22ae8-163">A log level of 5 in Winsock tracing represents verbose event logging.</span></span>

<span data-ttu-id="22ae8-164">Идентификатор процесса выполнения и идентификатор потока в сведениях о системе указывают процесс и поток, которые выполнялись при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="22ae8-164">The execution process ID and thread ID in the system information indicates the process and thread that was running when the event occurred.</span></span> <span data-ttu-id="22ae8-165">Во многих случаях это будет представлять ядро, Рабочий поток и процесс, а не поток пользовательского режима и процесс приложения.</span><span class="sxs-lookup"><span data-stu-id="22ae8-165">In many cases, this will represent a kernel or worker thread and process, not a user-mode thread and or the process of the application.</span></span> <span data-ttu-id="22ae8-166">Это поле обычно не очень полезно.</span><span class="sxs-lookup"><span data-stu-id="22ae8-166">So this field is normally not very useful.</span></span>

<span data-ttu-id="22ae8-167">Каждый тип события трассировки Winsock имеет уникальный идентификатор события в системном разделе записанных данных.</span><span class="sxs-lookup"><span data-stu-id="22ae8-167">Each Winsock tracing event type has a unique event ID in the system section of the logged data.</span></span> <span data-ttu-id="22ae8-168">Эти идентификаторы событий можно легко использовать для фильтрации файла журнала для конкретных событий трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="22ae8-168">These event IDs can easily be used to filter a log file for specific Winsock tracing events.</span></span>

<span data-ttu-id="22ae8-169">В процессе EVENTDATA содержатся сведения, относящиеся к типу события.</span><span class="sxs-lookup"><span data-stu-id="22ae8-169">The eventdata contains information specific to the event type.</span></span>

<span data-ttu-id="22ae8-170">Параметр Process в сведениях о EVENTDATA представляет собой адрес структуры ядра ЕПРОЦЕСС для процесса, а не для фактического PID.</span><span class="sxs-lookup"><span data-stu-id="22ae8-170">The Process parameter in the eventdata information is the kernel EPROCESS structure address for the process, not the actual PID.</span></span> <span data-ttu-id="22ae8-171">Чтобы сопоставить событие с ИДЕНТИФИКАТОРом пользовательского режима, Возьмите значение процесса из любой записи журнала и просмотрите его ранее в журнале для события создания сокета со значением Process.</span><span class="sxs-lookup"><span data-stu-id="22ae8-171">To match an event to the user mode PID, take the Process value from the eventdata information from any log entry and look earlier in the log for a socket creation event with the Process value.</span></span> <span data-ttu-id="22ae8-172">После обнаружения совпадения последний параметр в данных события создания сокета — это идентификатор процесса пользовательского режима, создавший сокет.</span><span class="sxs-lookup"><span data-stu-id="22ae8-172">Once a match is found, the last parameter in the socket creation event data is the user-mode Process ID that created the socket.</span></span>

<span data-ttu-id="22ae8-173">Параметр Address в сведениях о EVENTDATA возвращается в некоторых событиях трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="22ae8-173">An Address parameter in the eventdata information is returned in some Winsock tracing events.</span></span> <span data-ttu-id="22ae8-174">Параметр Address представляет IP-адрес, но он отображается в текстовом файле, созданном средством **tracerpt.exe** или в Просмотр событий как необработанные байты или числа.</span><span class="sxs-lookup"><span data-stu-id="22ae8-174">An Address parameter represents an IP address, but it is displayed in the text file created by the **tracerpt.exe** tool or in Event Viewer as raw bytes or a number.</span></span> <span data-ttu-id="22ae8-175">Адреса IPv6 отображаются в шестнадцатеричном виде, поэтому их легче понять.</span><span class="sxs-lookup"><span data-stu-id="22ae8-175">IPv6 addresses are displayed in hexadecimal, so they are more easily understood.</span></span> <span data-ttu-id="22ae8-176">IPv4-адреса отображаются в виде большого десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="22ae8-176">IPv4 addresses are displayed as a large decimal number.</span></span> <span data-ttu-id="22ae8-177">Разработчикам потребуется вручную преобразовать необработанные байты IPv4-адреса в более знакомую нотацию с точками в формате IPv4, чтобы лучше интерпретировать это значение.</span><span class="sxs-lookup"><span data-stu-id="22ae8-177">Developers will need to manually convert the raw bytes of an IPv4 address to the more familiar IPv4 dotted-decimal address notation to be better able to interpret the value.</span></span>

<span data-ttu-id="22ae8-178">Параметр ошибки в EVENTDATA возвращается в некоторых событиях трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="22ae8-178">An Error parameter in the eventdata is returned in some Winsock tracing events.</span></span> <span data-ttu-id="22ae8-179">Параметр ошибки имеет вид кода ошибки NTSTATUS или HRESULT.</span><span class="sxs-lookup"><span data-stu-id="22ae8-179">An Error parameter is of the form of an NTSTATUS or HRESULT error code.</span></span> <span data-ttu-id="22ae8-180">Этот параметр ошибки отображается в текстовом файле, созданном средством **tracerpt.exe** , или в Просмотр событий в виде десятичного числа.</span><span class="sxs-lookup"><span data-stu-id="22ae8-180">This error parameter is displayed in the text file created by the **tracerpt.exe** tool or in Event Viewer as a decimal number.</span></span> <span data-ttu-id="22ae8-181">Разработчикам придется вручную преобразовать десятичное число в шестнадцатеричное число, чтобы лучше интерпретировать код ошибки в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="22ae8-181">Developers will need to manually convert the decimal number to a hex number in order to better interpret the error code in some cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22ae8-182">См. также</span><span class="sxs-lookup"><span data-stu-id="22ae8-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22ae8-183">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-183">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="22ae8-184">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-184">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="22ae8-185">Сведения о трассировке событий сети Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-185">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="22ae8-186">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="22ae8-186">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
