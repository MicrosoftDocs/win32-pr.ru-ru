---
description: Журналы WinHTTP можно использовать для устранения неполадок в приложениях WSDAPI. Это полезно при сбое обмена метаданными или при сбое согласования SSL/TLS.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Запись журналов WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155990"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="f3291-104">Запись журналов WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f3291-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="f3291-105">Журналы [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) можно использовать для устранения неполадок в приложениях WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="f3291-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="f3291-106">Это полезно при сбое обмена метаданными или при сбое согласования SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="f3291-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="f3291-107">В этой процедуре показано, как записать журналы WinHTTP на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="f3291-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="f3291-108">Клиентское приложение на основе WSDAPI не должно выполняться, если включено ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="f3291-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="f3291-109">Если клиентское приложение выполняется при включении ведения журнала, клиент и (или) компьютер должны быть перезапущены, прежде чем WS-Discovery и трафик обмена метаданными появится в журналах WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f3291-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="f3291-110">**Запись журналов WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="f3291-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="f3291-111">Откройте окно командной строки с повышенными привилегиями на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="f3291-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="f3291-112">Выполните следующую команду: **netsh WinHTTP Set Trace трассировка-File-prefix = "C: \\ temp \\ DPWS" уровень = verbose Format = ANSI состояние = включено Max-Trace-File-Size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="f3291-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="f3291-113">Эта команда включает ведение журнала WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f3291-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="f3291-114">Все файлы журналов будут храниться в каталоге C: \\ TEMP, а имена файлов будут начинаться с префикса DPWS.</span><span class="sxs-lookup"><span data-stu-id="f3291-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="f3291-115">Будет храниться не более 1 ГБ файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="f3291-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="f3291-116">Если процесс, использующий WinHTTP на клиенте, уже запущен, перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="f3291-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="f3291-117">Например, если используются API-интерфейсы [обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal) , необходимо перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="f3291-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="f3291-118">API-интерфейсы обнаружения функций вызывают WinHTTP из узла службы, который, возможно, уже запущен при включенной трассировке.</span><span class="sxs-lookup"><span data-stu-id="f3291-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="f3291-119">Запустите клиентское приложение на основе WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="f3291-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="f3291-120">Отлаживаемый приложение или можно использовать клиент отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="f3291-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="f3291-121">Воспроизведение ошибки приложения.</span><span class="sxs-lookup"><span data-stu-id="f3291-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="f3291-122">Завершите работу клиентского приложения на основе WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="f3291-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="f3291-123">Если процесс, использующий WinHTTP, не завершается клиентским приложением, перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="f3291-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="f3291-124">Например, если используются API-интерфейсы [обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal) , необходимо перезапустить компьютер.</span><span class="sxs-lookup"><span data-stu-id="f3291-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="f3291-125">Выполните следующую команду: **netsh WinHTTP set tracing State = Disabled**</span><span class="sxs-lookup"><span data-stu-id="f3291-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="f3291-126">Эта команда отключает ведение журнала WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f3291-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="f3291-127">Проверьте журналы DPWS в C: \\ TEMP и убедитесь, что были отправлены необходимые запросы и сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3291-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="f3291-128">Если используется обмен данными по защищенному каналу (HTTPS), проверьте наличие ошибок SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="f3291-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="f3291-129">После записи журналов WinHTTP журналы можно просмотреть, чтобы найти причину сбоя приложения WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="f3291-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="f3291-130">Обратите внимание, что текстовый редактор, используемый для просмотра этих журналов, должен запускаться от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="f3291-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="f3291-131">Дополнительные сведения см. [в разделе Использование ведения журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="f3291-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3291-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f3291-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3291-133">Известен</span><span class="sxs-lookup"><span data-stu-id="f3291-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="f3291-134">Использование ведения журнала WinHTTP для проверки получения трафика</span><span class="sxs-lookup"><span data-stu-id="f3291-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
