---
title: Трассировка
description: Трассировка использует трассировку событий для Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Трассировка веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414177"
---
# <a name="tracing"></a><span data-ttu-id="a4461-106">Трассировка</span><span class="sxs-lookup"><span data-stu-id="a4461-106">Tracing</span></span>

<span data-ttu-id="a4461-107">Трассировка использует трассировку событий для Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="a4461-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="a4461-108">Чтобы воспользоваться средствами трассировки, доступными в Windows Server 2008 R2, установите Microsoft Windows SDK на сайте [загрузки MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .</span><span class="sxs-lookup"><span data-stu-id="a4461-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="a4461-109">Поддерживаются три уровня трассировки:</span><span class="sxs-lookup"><span data-stu-id="a4461-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="a4461-110">Verbose (все доступные трассировки).</span><span class="sxs-lookup"><span data-stu-id="a4461-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="a4461-111">INFO (информационные трассировки).</span><span class="sxs-lookup"><span data-stu-id="a4461-111">Info (informational traces).</span></span>
-   <span data-ttu-id="a4461-112">Ошибка (трассировки ошибок).</span><span class="sxs-lookup"><span data-stu-id="a4461-112">Error (error traces).</span></span>

<span data-ttu-id="a4461-113">Отслеживаются следующие события:</span><span class="sxs-lookup"><span data-stu-id="a4461-113">The following events are traced:</span></span>

-   <span data-ttu-id="a4461-114">Любые ошибки (уровень = ошибка, уровень = сведения или уровень = подробный).</span><span class="sxs-lookup"><span data-stu-id="a4461-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="a4461-115">Вход и выход из API (Level = info или Level = verbose).</span><span class="sxs-lookup"><span data-stu-id="a4461-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="a4461-116">Начало и завершение любых операций ввода-вывода (уровень = info или Level = verbose)</span><span class="sxs-lookup"><span data-stu-id="a4461-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="a4461-117">Обмен сообщениями SOAP (Level = Verbose, доступный в Windows 2003 с пакетом обновления 1 (SP1) и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a4461-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="a4461-118">Создание и Просмотр трассировок ВВСАПИ</span><span class="sxs-lookup"><span data-stu-id="a4461-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="a4461-119">ВВСАПИ использует события на основе манифеста в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a4461-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="a4461-120">В результате трассировка имеет некоторые отличия, основанные на версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a4461-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="a4461-121">Создание трассировок трассировки событий Windows можно выполнить с помощью встроенных средств ETW на всех поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="a4461-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="a4461-122">Однако для просмотра трассировки ETW в удобном формате требуются пользовательские средства в Windows XP SP2 и Windows 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a4461-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="a4461-123">Существует несколько различных способов сбора и просмотра трассировок событий ETW ВВСАПИ в зависимости от версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a4461-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="a4461-124">Включение и Просмотр трассировок ВВСАПИ в Просмотр событий (работает в Windows Vista и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a4461-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="a4461-125">Запустите eventvwr. msc из командной строки или из меню выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4461-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="a4461-126">Щелкните ссылку Просмотр на панели действия справа и включите параметр Показать журналы аналитики и отладки.</span><span class="sxs-lookup"><span data-stu-id="a4461-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="a4461-127">Перейдите к журналу приложений и служб \\ Microsoft \\ Windows веб \\ Services в левой области.</span><span class="sxs-lookup"><span data-stu-id="a4461-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="a4461-128">Щелкните правой кнопкой мыши поставщик трассировки и выберите Включить журнал.</span><span class="sxs-lookup"><span data-stu-id="a4461-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="a4461-129">Выполните сценарий.</span><span class="sxs-lookup"><span data-stu-id="a4461-129">Run your scenario.</span></span>
-   <span data-ttu-id="a4461-130">При обновлении страницы "Просмотр событий" следует начать просмотр записей трассировки ВВСАПИ.</span><span class="sxs-lookup"><span data-stu-id="a4461-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="a4461-131">Включение и Просмотр трассировок ВВСАПИ с помощью скрипта Wstrace.bat (работает в XPSP2 и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a4461-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="a4461-132">Пакетный файл wstrace.bat предоставляет удобный способ:</span><span class="sxs-lookup"><span data-stu-id="a4461-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="a4461-133">Создание журнала трассировки</span><span class="sxs-lookup"><span data-stu-id="a4461-133">Create a trace log</span></span>
-   <span data-ttu-id="a4461-134">Удаление журнала трассировки</span><span class="sxs-lookup"><span data-stu-id="a4461-134">Delete a trace log</span></span>
-   <span data-ttu-id="a4461-135">Включение и отключение трассировки</span><span class="sxs-lookup"><span data-stu-id="a4461-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="a4461-136">Обновление уровня трассировки (info, Error/verbose)</span><span class="sxs-lookup"><span data-stu-id="a4461-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="a4461-137">Преобразование журналов трассировки в CSV-файлы</span><span class="sxs-lookup"><span data-stu-id="a4461-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="a4461-138">Пакетный файл использует logman.exe для всех команд, за исключением преобразования журналов в CSV-файл, для которого требуется настраиваемое средство (wstracedump.exe).</span><span class="sxs-lookup"><span data-stu-id="a4461-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="a4461-139">Использование команд трассировки</span><span class="sxs-lookup"><span data-stu-id="a4461-139">Using tracing commands</span></span>

<span data-ttu-id="a4461-140">Следующая команда создает журнал, в котором используются сведения, ошибка или уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="a4461-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="a4461-141">Для этой команды требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="a4461-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="a4461-142">**wstrace.bat \[ подробные сведения \| об ошибке создания сведений \|\]**</span><span class="sxs-lookup"><span data-stu-id="a4461-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="a4461-143">Следующая команда удаляет журнал.</span><span class="sxs-lookup"><span data-stu-id="a4461-143">The following command deletes the log.</span></span> <span data-ttu-id="a4461-144">Для этой команды требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="a4461-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="a4461-145">**wstrace.bat удалить**</span><span class="sxs-lookup"><span data-stu-id="a4461-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="a4461-146">Следующая команда включает трассировку.</span><span class="sxs-lookup"><span data-stu-id="a4461-146">The following command enables tracing.</span></span> <span data-ttu-id="a4461-147">Сначала необходимо создать журнал.</span><span class="sxs-lookup"><span data-stu-id="a4461-147">You must first create a log.</span></span>

<span data-ttu-id="a4461-148">**wstrace.bat на**</span><span class="sxs-lookup"><span data-stu-id="a4461-148">**wstrace.bat on**</span></span>

<span data-ttu-id="a4461-149">Уровень трассировки (info, Error или verbose) можно изменить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a4461-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="a4461-150">**wstrace.bat \[ подробные сведения \| об ошибке обновления \|\]**</span><span class="sxs-lookup"><span data-stu-id="a4461-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="a4461-151">Чтобы выгрузить выходные данные трассировки, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a4461-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="a4461-152">**> дампаwstrace.bat temp.csv**</span><span class="sxs-lookup"><span data-stu-id="a4461-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="a4461-153">События будут записываться в файл CSV до нажатия клавиши CTRL-C или отключения трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="a4461-154">Формат файла трассировки</span><span class="sxs-lookup"><span data-stu-id="a4461-154">Tracing File format</span></span>

<span data-ttu-id="a4461-155">Файлы CSV, созданные wstrace.bat, представляют собой простые текстовые файлы с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="a4461-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="a4461-156">Эти файлы могут быть открыты в Excel, блокноте и т. д.</span><span class="sxs-lookup"><span data-stu-id="a4461-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="a4461-157">Ниже приведены столбцы файла.</span><span class="sxs-lookup"><span data-stu-id="a4461-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="a4461-158">TimeStamp — метка времени, когда событие было записано</span><span class="sxs-lookup"><span data-stu-id="a4461-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="a4461-159">ProcessID — идентификатор ULONG процесса, записывающего событие</span><span class="sxs-lookup"><span data-stu-id="a4461-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="a4461-160">ThreadID-ULONG идентификатор потока, записывающего событие</span><span class="sxs-lookup"><span data-stu-id="a4461-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="a4461-161">Перечислимое по событиям значение типа события может быть ("API Enter" \| "API ожидание" \| "API екситсинксукцесс" \| "API екситсинкфаилуре" \| "API Екситасинксукцесс" \| "API екситасинкфаилуре" \| "IO Started" \| "ввод-вывод завершен" \| "произошел сбой ввода-вывода" " \| Ошибка" \| "получено сообщение начало" \| \| \| \| \| "получено сообщение" "получено сообщение останавливается" "Отправка сообщения" "Отправка сообщения" "</span><span class="sxs-lookup"><span data-stu-id="a4461-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="a4461-162">Operation — имя вызываемой операции.</span><span class="sxs-lookup"><span data-stu-id="a4461-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="a4461-163">Обычно это сопоставляется с вызываемым API.</span><span class="sxs-lookup"><span data-stu-id="a4461-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="a4461-164">Ошибка-необязательный номер ошибки HRESULT</span><span class="sxs-lookup"><span data-stu-id="a4461-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="a4461-165">Сведения — необязательные сведения о событии</span><span class="sxs-lookup"><span data-stu-id="a4461-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="a4461-166">Сбор файла трассировки событий Windows ВВСАПИ с помощью средств ETW (работает в XPSP2 и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a4461-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="a4461-167">Включение трассировки ETW для ВВСАПИ</span><span class="sxs-lookup"><span data-stu-id="a4461-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="a4461-168">**Программа Logman Start встраце-BS 64-ft 1-RT-p Microsoft-Windows-WebService \[ Флаги \[ Level \] \] \[ -o <EtlLogFileName> \] -ETS**</span><span class="sxs-lookup"><span data-stu-id="a4461-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="a4461-169">для создания и запуска сеанса трассировки событий Windows.</span><span class="sxs-lookup"><span data-stu-id="a4461-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="a4461-170">Logman.exe — это встроенное средство ETW, доступное на всех поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="a4461-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="a4461-171">Обратите внимание, что необходимо использовать веб \_ службы Microsoft Windows в \_ качестве имени поставщика в XPsp2 и W2K3.</span><span class="sxs-lookup"><span data-stu-id="a4461-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="a4461-172">Вы можете запустить поставщики запросов logman, чтобы просмотреть список зарегистрированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a4461-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="a4461-173">\_ \_ Если он не зарегистрирован, то должен быть указан поставщик Microsoft-Windows-WebService (или Microsoft Windows WebService).</span><span class="sxs-lookup"><span data-stu-id="a4461-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="a4461-174">Поставщик обычно регистрируется во время установки.</span><span class="sxs-lookup"><span data-stu-id="a4461-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="a4461-175">Однако его также можно зарегистрировать вручную, запустив wevtutil.exe IM <ManifestFileName> (в Windows Vista и более поздних версиях) или mofcomp.exe <MofFileName> (в XPsp2 и W2K3).</span><span class="sxs-lookup"><span data-stu-id="a4461-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="a4461-176">Флаги можно использовать для фильтрации трассировок по их типу.</span><span class="sxs-lookup"><span data-stu-id="a4461-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="a4461-177">Это может быть или значение следующих типов трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="a4461-178">Если не указано, включаются все виды трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="a4461-179">0x1 — трассировка входа/выхода API.</span><span class="sxs-lookup"><span data-stu-id="a4461-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="a4461-180">0x2 — трассировки ошибок.</span><span class="sxs-lookup"><span data-stu-id="a4461-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="a4461-181">0x4 — трассировки операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a4461-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="a4461-182">0x8 — трассировки сообщений SOAP.</span><span class="sxs-lookup"><span data-stu-id="a4461-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="a4461-183">0x10 — двоичные трассировки сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4461-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="a4461-184">Level можно использовать для фильтрации трассировок по их уровню.</span><span class="sxs-lookup"><span data-stu-id="a4461-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="a4461-185">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4461-185">It should be one of the following values.</span></span> <span data-ttu-id="a4461-186">Если не указано, включаются все уровни трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="a4461-187">0x1 — неустранимые трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="a4461-188">0x2 — трассировки ошибок.</span><span class="sxs-lookup"><span data-stu-id="a4461-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="a4461-189">0x3 — трассировка предупреждений.</span><span class="sxs-lookup"><span data-stu-id="a4461-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="a4461-190">0x4 — информационные трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="a4461-191">0x5 — подробные трассировки.</span><span class="sxs-lookup"><span data-stu-id="a4461-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="a4461-192">Етллогфиленаме — путь к создаваемому файлу журнала событий ETW (используйте расширение ETL).</span><span class="sxs-lookup"><span data-stu-id="a4461-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="a4461-193">Если не указано, ETW выберет случайное имя, которое можно будет запросить позже.</span><span class="sxs-lookup"><span data-stu-id="a4461-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="a4461-194">Этот файл не должен находиться в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4461-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="a4461-195">Файл журнала событий ETW (ETL-файл) имеет двоичный формат.</span><span class="sxs-lookup"><span data-stu-id="a4461-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="a4461-196">Его можно использовать в приложениях ETW, но не в удобочитаемом формате.</span><span class="sxs-lookup"><span data-stu-id="a4461-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="a4461-197">На следующем шаге описывается, как просмотреть его содержимое.</span><span class="sxs-lookup"><span data-stu-id="a4461-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="a4461-198">Выполнение сценария</span><span class="sxs-lookup"><span data-stu-id="a4461-198">Run your scenario</span></span>

<span data-ttu-id="a4461-199">Сбор данных о файле журнала событий ETW.</span><span class="sxs-lookup"><span data-stu-id="a4461-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="a4461-200">**Logman остановкой встраце-ETS**</span><span class="sxs-lookup"><span data-stu-id="a4461-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="a4461-201">для завершения сеанса трассировки ETW.</span><span class="sxs-lookup"><span data-stu-id="a4461-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="a4461-202">Это происходит, когда ETW прекращает запись событий в журнал.</span><span class="sxs-lookup"><span data-stu-id="a4461-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="a4461-203">Файл журнала событий ETW (указанный в параметре Етллогфиленаме) готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="a4461-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="a4461-204">Его можно просмотреть локально (инструкции приведены ниже) или отправить в группу продуктов для изучения.</span><span class="sxs-lookup"><span data-stu-id="a4461-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="a4461-205">Сквозной пример с использованием средств ETW:</span><span class="sxs-lookup"><span data-stu-id="a4461-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="a4461-206">**Logman Start встраце-BS 64-ft 1-RT-p Microsoft-Windows-WebService-o митраце. ETL-ETS**</span><span class="sxs-lookup"><span data-stu-id="a4461-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="a4461-207">**echo. Выполните сценарий.**</span><span class="sxs-lookup"><span data-stu-id="a4461-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="a4461-208">**Logman остановкой встраце-ETS**</span><span class="sxs-lookup"><span data-stu-id="a4461-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="a4461-209">**Tracerpt митраце. ETL-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="a4461-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="a4461-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="a4461-210">**wstrace.htm**</span></span>

<span data-ttu-id="a4461-211">**echo. Используйте mytrace.xml и встраце. XSL на открытой странице..**</span><span class="sxs-lookup"><span data-stu-id="a4461-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="a4461-212">Просмотр трассировки файлов трассировки событий Windows ВВСАПИ с помощью средства wstracedump.exe (работает в Windows XP и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a4461-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="a4461-213">Wstracedump.exe — это настраиваемое средство для потребителей ETW, которое обрабатывает события в файле трассировки событий Windows ВВСАПИ и создает понятные для человека выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a4461-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="a4461-214">Он может создавать выходные данные со всех поддерживаемых платформ.</span><span class="sxs-lookup"><span data-stu-id="a4461-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="a4461-215">Дополнительные сведения см. в описании использования (wstracedump.exe-?).</span><span class="sxs-lookup"><span data-stu-id="a4461-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="a4461-216">Просмотр трассировки файлов трассировки событий Windows ВВСАПИ с помощью средств ETW (работает в Windows Vista и более поздних версиях)</span><span class="sxs-lookup"><span data-stu-id="a4461-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="a4461-217">Tracerpt.exe — это средство для просмотра содержимого файла журнала событий ETW, которое доступно на всех поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="a4461-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="a4461-218">Его можно использовать для создания файлов дампа CSV, EVTX или XML из файла журнала событий ETW.</span><span class="sxs-lookup"><span data-stu-id="a4461-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="a4461-219">Однако созданный выходной файл имеет доступную для чтения трассировку только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a4461-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="a4461-220">Эти инструкции описывают, как создать XML-файл дампа и использовать его вместе с XSL-файлом для отображения трассировок в удобном формате (XSL-файл очень тривиальный и может быть изменен в случае необходимости в различных форматах).</span><span class="sxs-lookup"><span data-stu-id="a4461-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="a4461-221">Выполнить</span><span class="sxs-lookup"><span data-stu-id="a4461-221">Run</span></span>

    <span data-ttu-id="a4461-222">**Tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="a4461-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="a4461-223">для создания дампа XML из двоичного ETL-файла (tracerpt.exe по умолчанию создает выходной файл в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a4461-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="a4461-224">Запустить Tracerpt-?</span><span class="sxs-lookup"><span data-stu-id="a4461-224">Run tracerpt -?</span></span> <span data-ttu-id="a4461-225">Для просмотра других доступных форматов).</span><span class="sxs-lookup"><span data-stu-id="a4461-225">To see other available formats).</span></span>

-   <span data-ttu-id="a4461-226">На этом этапе данные трассировки можно просмотреть в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="a4461-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="a4461-227">Кроме того, можно открыть файл wstrace.htm и использовать XML-файл дампа и файл встраце. XSL для просмотра трассировок в формате лучше.</span><span class="sxs-lookup"><span data-stu-id="a4461-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="a4461-228">Обратите внимание, что файлы должны находиться на локальном компьютере, чтобы иметь возможность использовать этот HTML-файл в IE.</span><span class="sxs-lookup"><span data-stu-id="a4461-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="a4461-229">Безопасность</span><span class="sxs-lookup"><span data-stu-id="a4461-229">Security</span></span>

<span data-ttu-id="a4461-230">При включении трассировки администраторам следует учитывать, что она потребляет дополнительное дисковое пространство и вычислительную мощность.</span><span class="sxs-lookup"><span data-stu-id="a4461-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="a4461-231">Вредоносный клиент или приложение могут вычерпать системные ресурсы, если только параметры трассировки не настроены с разумными ограничениями.</span><span class="sxs-lookup"><span data-stu-id="a4461-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="a4461-232">При использовании функции трассировки сообщений сообщения, хранящие конфиденциальные данные, такие как учетные данные, персональные данные и т. д., могут быть сохранены на диске или просмотрены любым пользователем, имеющим доступ к средству просмотра системных событий.</span><span class="sxs-lookup"><span data-stu-id="a4461-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="a4461-233">Для устранения этой проблемы трассировка может быть включена пользователями системы или администратора в Windows 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a4461-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="a4461-234">Трассировка сообщений отключена в Windows XP, в которой любой пользователь может включить трассировку.</span><span class="sxs-lookup"><span data-stu-id="a4461-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="a4461-235">С трассировкой используется следующее перечисление:</span><span class="sxs-lookup"><span data-stu-id="a4461-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="a4461-236">**\_API трассировки \_ WS**</span><span class="sxs-lookup"><span data-stu-id="a4461-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




