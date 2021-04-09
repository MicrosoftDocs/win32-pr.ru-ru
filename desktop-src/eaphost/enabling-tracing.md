---
title: Включение трассировки EAPHost
description: Может помочь пользователям найти основные причины проблем, возникающих в процессе проверки подлинности EAP. Отладочная информация может включать вызовы API, выполненные внутренние вызовы функций и выполненные переходы состояния.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104070896"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="d02a0-104">Включение трассировки EAPHost</span><span class="sxs-lookup"><span data-stu-id="d02a0-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="d02a0-105">Журналы трассировки, содержащие отладочную информацию, могут помочь пользователям найти основные причины проблем, возникающих в процессе проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="d02a0-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="d02a0-106">Отладочная информация может включать вызовы API, выполненные внутренние вызовы функций и выполненные переходы состояния.</span><span class="sxs-lookup"><span data-stu-id="d02a0-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="d02a0-107">Трассировку можно включить как на стороне клиента, так и на стороне средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d02a0-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="d02a0-108">Трассировку также можно включить для вызовов интерфейсов API [службы маршрутизации и удаленного доступа (RRAS)](/windows/desktop/RRAS/routing-start-page) .</span><span class="sxs-lookup"><span data-stu-id="d02a0-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="d02a0-109">Дополнительные сведения см. в разделе [Трассировка в службе маршрутизации и удаленного доступа](#tracing-on-the-routing-and-remote-access-service).</span><span class="sxs-lookup"><span data-stu-id="d02a0-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="d02a0-110">Журналы трассировки доступны только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="d02a0-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="d02a0-111">Когда трассировка EAPHost включена, данные журнала хранятся в ETL-файле в указанном пользователем расположении.</span><span class="sxs-lookup"><span data-stu-id="d02a0-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="d02a0-112">Если во время проверки подлинности EAP возникают ошибки, то трассировка создает ETL-файл, который можно отправить в корпорацию Майкрософт поддержка Developer для анализа основных причин.</span><span class="sxs-lookup"><span data-stu-id="d02a0-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="d02a0-113">Партнеры, имеющие доступ к общим папкам, символам и трацеформат файлам Microsoft Windows, могут преобразовать ETL-файлы в обычный текстовый файл с помощью средства **Tracerpt** .</span><span class="sxs-lookup"><span data-stu-id="d02a0-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="d02a0-114">Сбои сервера политики сети (NPS) не фиксируются в журналах EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d02a0-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="d02a0-115">Если вы пытаетесь устранить сбой NPS, просмотрите ИАССАМ. LOG и [иаснап. Файлы журнала](https://go.microsoft.com/fwlink/p/?linkid=84108) .</span><span class="sxs-lookup"><span data-stu-id="d02a0-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="d02a0-116">Трассировка на клиенте</span><span class="sxs-lookup"><span data-stu-id="d02a0-116">Tracing on the Client</span></span>

<span data-ttu-id="d02a0-117">Чтобы включить трассировку на стороне клиента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d02a0-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="d02a0-118">Откройте окно командной строки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="d02a0-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="d02a0-119">Выполните следующую команду: **Logman** **Start Trace** **еафостпир** **-o** **. \\ Еафостпир. ETL** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **— ETS**</span><span class="sxs-lookup"><span data-stu-id="d02a0-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="d02a0-120">Воспроизведите сценарий, который требуется отслеживать.</span><span class="sxs-lookup"><span data-stu-id="d02a0-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="d02a0-121">Выполните следующую команду: **Logman** **останавливают** **еафостпир** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="d02a0-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="d02a0-122">Преобразуйте ETL-файл в текст с помощью следующей команды **: Tracerpt еафостпир. ETL** **-pdb** **&lt; &gt; пдбпас** **-TP** **&lt; трацемессажефилесдиректорипас &gt;** **/o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="d02a0-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="d02a0-123">Если у вас нет доступа к средству Tracerpt, Избегайте последнего шага и отправьте ETL-файл в Microsoft поддержка Developer.</span><span class="sxs-lookup"><span data-stu-id="d02a0-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="d02a0-124">Трассировка для средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="d02a0-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="d02a0-125">Чтобы включить трассировку на стороне средства проверки подлинности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d02a0-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="d02a0-126">Откройте окно командной строки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="d02a0-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="d02a0-127">Выполните следующую команду: **Logman** **Start Trace** **еафостауср** **-o** **. \\ Еафостауср. ETL** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **— ETS**</span><span class="sxs-lookup"><span data-stu-id="d02a0-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="d02a0-128">Воспроизведите сценарий, который требуется отслеживать.</span><span class="sxs-lookup"><span data-stu-id="d02a0-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="d02a0-129">Выполните следующую команду: **Logman** **останавливают** **еафостауср** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="d02a0-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="d02a0-130">Преобразуйте ETL-файл в текст с помощью следующей команды **: Tracerpt еафостауср. ETL** **-pdb** **&lt; &gt; пдбпас** **-TP** **&lt; трацемессажефилесдиректорипас &gt;** **/o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="d02a0-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="d02a0-131">Если у вас нет доступа к средству Tracerpt, Избегайте последнего шага и отправляйте ETL-файл в Microsoft поддержка Developer.</span><span class="sxs-lookup"><span data-stu-id="d02a0-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="d02a0-132">Трассировка событий</span><span class="sxs-lookup"><span data-stu-id="d02a0-132">Event tracing</span></span>

<span data-ttu-id="d02a0-133">В Windows 7 и более поздних версиях Windows EapHost предоставляет трассировку на основе событий для средства проверки подлинности и однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="d02a0-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="d02a0-134">Преимущество трассировки на основе событий заключается в том, что для просмотра сообщений трассировки не нужны файлы символов.</span><span class="sxs-lookup"><span data-stu-id="d02a0-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="d02a0-135">Чтобы включить трассировку событий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d02a0-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="d02a0-136">Откройте **евентвиевер**.</span><span class="sxs-lookup"><span data-stu-id="d02a0-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="d02a0-137">Критические сообщения EapHost регистрируются в папке: " \\ Административные события для пользовательских представлений"</span><span class="sxs-lookup"><span data-stu-id="d02a0-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="d02a0-138">В журнал заносятся некритические сообщения: "приложения и службы \\ Microsoft \\ Windows \\ EapHost</span><span class="sxs-lookup"><span data-stu-id="d02a0-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="d02a0-139">Сообщения о событиях типа "аналитика" и "Отладка" можно просматривать по тому же пути, выбрав пункт **Показать аналитические и отладочные журналы** в меню **вид** в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="d02a0-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="d02a0-140">Трассировка в службе маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="d02a0-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="d02a0-141">Чтобы включить трассировку RRAS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d02a0-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="d02a0-142">Откройте окно командной строки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="d02a0-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="d02a0-143">Выполните следующую команду: **netsh** **RAS** **Set** **tr** **\* *_ _* EN** .</span><span class="sxs-lookup"><span data-stu-id="d02a0-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="d02a0-144">Открыть **\\ трассировку% systemroot%** для просмотра трассировок RAS</span><span class="sxs-lookup"><span data-stu-id="d02a0-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="d02a0-145">Чтобы отключить трассировку RRAS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d02a0-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="d02a0-146">Откройте окно командной строки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="d02a0-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="d02a0-147">Выполните следующую команду: **netsh** **RAS** **Set** **tr** **\* *_ _* DIS**</span><span class="sxs-lookup"><span data-stu-id="d02a0-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="d02a0-148">Дополнительные сведения см. в разделе [команды netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d02a0-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d02a0-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d02a0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02a0-150">Использование EAPHost</span><span class="sxs-lookup"><span data-stu-id="d02a0-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="d02a0-151">Служба маршрутизации и удаленного доступа (RRAS)</span><span class="sxs-lookup"><span data-stu-id="d02a0-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 