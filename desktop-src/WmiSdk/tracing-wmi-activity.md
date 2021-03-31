---
description: Начиная с Windows Vista, служба WMI не использует файлы журнала WMI. Вместо этого он использует трассировку событий для Windows (ETW) и события, доступные с помощью Просмотр событий или программы командной строки wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Трассировка действий WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815697"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="4beab-104">Трассировка действий WMI</span><span class="sxs-lookup"><span data-stu-id="4beab-104">Tracing WMI Activity</span></span>

<span data-ttu-id="4beab-105">Начиная с Windows Vista, служба WMI не использует [файлы журнала WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="4beab-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="4beab-106">Вместо этого он использует [трассировку событий для Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) и события, доступные с помощью **Просмотр событий** или программы командной строки wevtutil.</span><span class="sxs-lookup"><span data-stu-id="4beab-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="4beab-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="4beab-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="4beab-108">Получение событий WMI с помощью Просмотр событий</span><span class="sxs-lookup"><span data-stu-id="4beab-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="4beab-109">Включение трассировки WMI в командной строке</span><span class="sxs-lookup"><span data-stu-id="4beab-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="4beab-110">Использование трассировки WMI на основе WPP</span><span class="sxs-lookup"><span data-stu-id="4beab-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="4beab-111">См. также</span><span class="sxs-lookup"><span data-stu-id="4beab-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="4beab-112">Получение событий WMI с помощью Просмотр событий</span><span class="sxs-lookup"><span data-stu-id="4beab-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="4beab-113">Файл ВмитраЦинг. log содержит события, которые отслеживаются WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="4beab-114">Однако это двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="4beab-114">However, this is a binary file.</span></span> <span data-ttu-id="4beab-115">Чтобы просмотреть эти события в формате, читаемом людьми, используйте **Просмотр событий**.</span><span class="sxs-lookup"><span data-stu-id="4beab-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="4beab-116">По умолчанию события WMI не отслеживаются.</span><span class="sxs-lookup"><span data-stu-id="4beab-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="4beab-117">В этой процедуре описывается использование **Просмотр событий** для включения трассировки событий WMI и нахождение событий WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="4beab-118">Те же операции можно выполнить с помощью программы командной строки wevtutil.</span><span class="sxs-lookup"><span data-stu-id="4beab-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="4beab-119">**Просмотр событий WMI в Просмотр событий**</span><span class="sxs-lookup"><span data-stu-id="4beab-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="4beab-120">Откройте средство **просмотра событий**.</span><span class="sxs-lookup"><span data-stu-id="4beab-120">Open **Event Viewer**.</span></span> <span data-ttu-id="4beab-121">В меню **вид** выберите команду **Показать журналы аналитики и отладки**.</span><span class="sxs-lookup"><span data-stu-id="4beab-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="4beab-122">Выберите журнал канала **трассировки** для инструментария WMI в разделе приложения и службы журналы \| \| действие Microsoft Windows \| WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="4beab-123">Щелкните правой кнопкой мыши журнал **трассировки** и выберите пункт **Свойства журнала**.</span><span class="sxs-lookup"><span data-stu-id="4beab-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="4beab-124">Установите флажок **включить ведение журнала** , чтобы запустить трассировку событий WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="4beab-125">Дополнительные сведения о каналах см. [в разделе журналы событий и каналы в журнале событий Windows](/previous-versions//aa385225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4beab-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="4beab-126">События WMI отображаются в окне событий для **WMI-Activity**.</span><span class="sxs-lookup"><span data-stu-id="4beab-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="4beab-127">Дважды щелкните событие в списке, чтобы просмотреть подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="4beab-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="4beab-128">Событие можно просмотреть в **представлении XML** или в **удобном** для просмотра формате.</span><span class="sxs-lookup"><span data-stu-id="4beab-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="4beab-129">В поле **Event ID (идентификатор события** ) отображается значение, содержащее следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="4beab-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="4beab-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Событие 1</span><span class="sxs-lookup"><span data-stu-id="4beab-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="4beab-131">Начало последовательности событий для определенной операции.</span><span class="sxs-lookup"><span data-stu-id="4beab-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="4beab-132">Одно вхождение для каждой последовательности.</span><span class="sxs-lookup"><span data-stu-id="4beab-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="4beab-133">Поля событий для события 1:</span><span class="sxs-lookup"><span data-stu-id="4beab-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="4beab-134">**Граупоператионид** — это уникальный идентификатор, используемый для всех событий, сообщаемых для конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="4beab-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="4beab-135">Идентификатор **операции указывает на** последовательность операций.</span><span class="sxs-lookup"><span data-stu-id="4beab-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="4beab-136">**Операция** указывает соединение или запрос к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="4beab-137">**Пользователь** указывает учетную запись, которая выполняет запрос к WMI, запустив сценарий или CIM Studio.</span><span class="sxs-lookup"><span data-stu-id="4beab-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="4beab-138">**Пространство имен** отображает пространство имен WMI, в которое устанавливается соединение.</span><span class="sxs-lookup"><span data-stu-id="4beab-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="4beab-139">Например, скрипт может запросить все экземпляры класса WMI, например [**\_ службу Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="4beab-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="4beab-140">Первая операция может быть соединением с WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="4beab-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Событие 2</span><span class="sxs-lookup"><span data-stu-id="4beab-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="4beab-142">События, составляющие операцию.</span><span class="sxs-lookup"><span data-stu-id="4beab-142">Events that make up the operation.</span></span> <span data-ttu-id="4beab-143">Одно или несколько вхождений в последовательности.</span><span class="sxs-lookup"><span data-stu-id="4beab-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="4beab-144">Поля событий для события 2:</span><span class="sxs-lookup"><span data-stu-id="4beab-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="4beab-145">**Граупоператионид** указывает последовательность, в которой происходит событие.</span><span class="sxs-lookup"><span data-stu-id="4beab-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="4beab-146">**Граупоператионид** указывает последовательность, в которой происходит событие.</span><span class="sxs-lookup"><span data-stu-id="4beab-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="4beab-147">**ProviderName** указывает имя поставщика, предоставляющего данные.</span><span class="sxs-lookup"><span data-stu-id="4beab-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="4beab-148">**Path** — это WMI-путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="4beab-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="4beab-149">Например, операция может быть перечислением [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="4beab-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="4beab-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Событие 3</span><span class="sxs-lookup"><span data-stu-id="4beab-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="4beab-151">Конец последовательности событий для определенной операции.</span><span class="sxs-lookup"><span data-stu-id="4beab-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="4beab-152">Одно вхождение для каждой последовательности.</span><span class="sxs-lookup"><span data-stu-id="4beab-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="4beab-153">Отображается только **граупоператионид** .</span><span class="sxs-lookup"><span data-stu-id="4beab-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="4beab-154">Включение трассировки WMI в командной строке</span><span class="sxs-lookup"><span data-stu-id="4beab-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="4beab-155">Можно также включить трассировку событий WMI с помощью программы командной строки wevtutil.</span><span class="sxs-lookup"><span data-stu-id="4beab-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="4beab-156">Используйте следующую команду: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**.</span><span class="sxs-lookup"><span data-stu-id="4beab-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="4beab-157">Источником событий WMI является Microsoft-Windows-WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="4beab-158">Дополнительные сведения о Wevtutil.exe см. в статье [о журнале событий Windows](/previous-versions//aa382610(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4beab-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="4beab-159">Использование трассировки WMI на основе WPP</span><span class="sxs-lookup"><span data-stu-id="4beab-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="4beab-160">В операционных системах Windows, начиная с Windows Vista, Инструментарий WMI создает активный канал трассировки во время процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="4beab-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="4beab-161">Имя канала — \_ сеанс трассировки WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="4beab-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="4beab-162">В канал записываются только ошибки.</span><span class="sxs-lookup"><span data-stu-id="4beab-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="4beab-163">Препроцессор трассировки программного обеспечения Windows записывает сведения в двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="4beab-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="4beab-164">Для чтения файла необходимо сначала преобразовать его в текстовый формат для чтения.</span><span class="sxs-lookup"><span data-stu-id="4beab-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="4beab-165">Для перевода используется средство с именем tracefmt.exe из [набора драйверов Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) .</span><span class="sxs-lookup"><span data-stu-id="4beab-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="4beab-166">Для этого средства требуются сведения, хранящиеся в некоторых связанных файлах.</span><span class="sxs-lookup"><span data-stu-id="4beab-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="4beab-167">Файлы находятся в каталоге% SystemRoot% \\ system32 \\ WBEM \\ ТМФ и имеют расширение имени файла ТМФ.</span><span class="sxs-lookup"><span data-stu-id="4beab-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="4beab-168">Для этого средства требуется один ТМФ-файл.</span><span class="sxs-lookup"><span data-stu-id="4beab-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="4beab-169">Чтобы сделать этот файл, объедините все ТМФ файлы в другой файл ТМФ.</span><span class="sxs-lookup"><span data-stu-id="4beab-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="4beab-170">Дополнительные сведения о файлах. ТМФ см. в разделе [файл форматирования сообщений трассировки](/windows-hardware/drivers/devtest/trace-message-format-file).</span><span class="sxs-lookup"><span data-stu-id="4beab-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="4beab-171">После установки [набора драйверов Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) для получения tracelog.exe и tracefmt.exe программ командной строки выполните следующие действия, чтобы получить трассировку WMI на основе WPP.</span><span class="sxs-lookup"><span data-stu-id="4beab-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="4beab-172">**Просмотр трассировки WMI на основе WPP**</span><span class="sxs-lookup"><span data-stu-id="4beab-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="4beab-173">Чтобы создать отдельный файл ТМФ, откройте окно командной строки с повышенными привилегиями и перейдите к каталогу% SystemRoot% \\ system32 \\ WBEM \\ ТМФ.</span><span class="sxs-lookup"><span data-stu-id="4beab-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="4beab-174">Введите **Copy/y% systemroot% \\ system32 \\ WBEM \\ ТМФ \\ \* . ТМФ% systemroot% \\ system32 \\ WBEM \\ ТМФ \\ WMI. ТМФ**.</span><span class="sxs-lookup"><span data-stu-id="4beab-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="4beab-175">При этом будет создан файл с именем WMI. ТМФ, содержащий содержимое всех остальных файлов. ТМФ.</span><span class="sxs-lookup"><span data-stu-id="4beab-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="4beab-176">Введите **tracelog-Flush \_ \_ сеанс трассировки WMI**.</span><span class="sxs-lookup"><span data-stu-id="4beab-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="4beab-177">Это приведет к сбросу буферов WPP на диске.</span><span class="sxs-lookup"><span data-stu-id="4beab-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="4beab-178">Введите **префикс формата трассировки, равный \_ \_ \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! КОМПНАМЕ!:%! FUNC!: %2! s!)**.</span><span class="sxs-lookup"><span data-stu-id="4beab-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="4beab-179">Средство трацефмт добавляет некоторые сведения по умолчанию в каждое сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="4beab-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="4beab-180">Вы можете настроить, какие сведения включаются, задав \_ \_ переменную среды префикса формата трассировки.</span><span class="sxs-lookup"><span data-stu-id="4beab-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="4beab-181">Дополнительные сведения об используемом синтаксисе см. в разделе [Трассировка префикса сообщения](https://msdn.microsoft.com/library/aa139695.aspx).</span><span class="sxs-lookup"><span data-stu-id="4beab-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="4beab-182">Введите **трацефмт-ТМФ% systemroot% \\ system32 \\ WBEM \\ ТМФ \\ wmi. ТМФ-o OUTPUT.TXT% systemroot% \\ system32 \\ WBEM \\ журналы \\ вмитраЦинг. log**.</span><span class="sxs-lookup"><span data-stu-id="4beab-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="4beab-183">При этом выполняется преобразование из двоичного формата в текстовый формат, доступный для чтения.</span><span class="sxs-lookup"><span data-stu-id="4beab-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="4beab-184">Введите **Notepad% systemroot% \\ system32 \\ WBEM \\ ТМФ \\OUTPUT.TXT**.</span><span class="sxs-lookup"><span data-stu-id="4beab-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="4beab-185">Файл трассировки откроется в блокноте.</span><span class="sxs-lookup"><span data-stu-id="4beab-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="4beab-186">Ниже приведены некоторые другие задачи, связанные с КОНВЕЙЕРом, которые может потребоваться выполнить.</span><span class="sxs-lookup"><span data-stu-id="4beab-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="4beab-187">**Отключение трассировки WMI на основе WPP**</span><span class="sxs-lookup"><span data-stu-id="4beab-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="4beab-188">Введите **tracelog — останавливает \_ \_ сеанс трассировки WMI**.</span><span class="sxs-lookup"><span data-stu-id="4beab-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="4beab-189">**Запуск трассировки WMI на основе WPP**</span><span class="sxs-lookup"><span data-stu-id="4beab-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="4beab-190">Введите **tracelog-Start WMI \_ \_ сеанс трассировки-GUID \# 1FF6B227-2CA7-40f9-9A66-980EADAA602E-RT-Level 5-Flag 0x7-f митраце. BIN**</span><span class="sxs-lookup"><span data-stu-id="4beab-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="4beab-191">**Windows Vista:** По умолчанию для трассировки WMI на основе WPP задан уровень 2, который включает только сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="4beab-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="4beab-192">Чтобы включить информационные сообщения, установите уровень равным 4.</span><span class="sxs-lookup"><span data-stu-id="4beab-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="4beab-193">По умолчанию отслеживаются все области инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="4beab-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="4beab-194">Существует три различающихся области, которые можно отслеживать: ядро (флаг = 0x1), ESS (Flag = 0x2) и Prov (Flag = 0x4).</span><span class="sxs-lookup"><span data-stu-id="4beab-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="4beab-195">В приведенной выше команде Start **флаг 0x7** приводит к тому, что все три области будут трассироваться.</span><span class="sxs-lookup"><span data-stu-id="4beab-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="4beab-196">**Windows 7:** По умолчанию трассировка WMI на основе WPP отключена, и для нее устанавливается уровень 0.</span><span class="sxs-lookup"><span data-stu-id="4beab-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="4beab-197">Чтобы использовать трассировку WMI на основе WPP, эта функция должна быть включена и иметь уровень 2 для сообщений об ошибках или уровень 4 как для сообщения об ошибках, так и для информационных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4beab-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="4beab-198">**Вывод списка всех сеансов трассировки WPP**</span><span class="sxs-lookup"><span data-stu-id="4beab-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="4beab-199">Введите **tracelog-l**.</span><span class="sxs-lookup"><span data-stu-id="4beab-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="4beab-200">**Вывод списка сведений о сеансе трассировки WPP в WMI**</span><span class="sxs-lookup"><span data-stu-id="4beab-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="4beab-201">Введите **tracelog-l \| findstr/i "WMI \_ Trace"**.</span><span class="sxs-lookup"><span data-stu-id="4beab-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="4beab-202">**Просмотр параметров сеанса трассировки WMI WPP**</span><span class="sxs-lookup"><span data-stu-id="4beab-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="4beab-203">Введите **tracelog-q \_ \_ сеанс трассировки WMI**.</span><span class="sxs-lookup"><span data-stu-id="4beab-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4beab-204">См. также</span><span class="sxs-lookup"><span data-stu-id="4beab-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4beab-205">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="4beab-205">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="4beab-206">Файлы журналов WMI</span><span class="sxs-lookup"><span data-stu-id="4beab-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
