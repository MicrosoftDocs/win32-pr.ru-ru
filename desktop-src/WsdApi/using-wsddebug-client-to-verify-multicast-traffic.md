---
description: Если универсальный узел и клиент могут видеть друг друга в сети, но фактический узел и клиент не могут, скорее всего, проблема заключается в сообщениях, передаваемых между конечными точками по сети.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Использование клиента отладки WSD для проверки трафика многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712031"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="924b8-103">Использование клиента отладки WSD для проверки трафика многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="924b8-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="924b8-104">Если универсальный узел и клиент могут видеть друг друга в сети, но фактический узел и клиент не могут, скорее всего, проблема заключается в сообщениях, передаваемых между конечными точками по сети.</span><span class="sxs-lookup"><span data-stu-id="924b8-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="924b8-105">Дополнительные сведения об универсальном узле и клиенте см. в разделе [Использование универсального узла и клиента для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="924b8-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="924b8-106">Так как полная трассировка сети может быть трудной для собираются, фильтрации и чтения, клиентское средство отладки WSD можно использовать для печати сторон многоадресной рассылки WS-Discovery сообщений.</span><span class="sxs-lookup"><span data-stu-id="924b8-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="924b8-107">Клиент отладки WSD в режиме многоадресной рассылки может проверять только половину сообщений, так как клиент не может печатать одноадресные сообщения.</span><span class="sxs-lookup"><span data-stu-id="924b8-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="924b8-108">Если требуется одноадресный трафик, пропустите процедуру непосредственно, чтобы [проверить трассировку сети для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="924b8-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="924b8-109">В этой процедуре показан метод, который будет отображать весь многоадресный трафик в сети.</span><span class="sxs-lookup"><span data-stu-id="924b8-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="924b8-110">Сведения о том, как отобразить только многоадресный трафик с устройства, см. в разделе [Фильтрация результатов отладки WSD для клиента](#filtering-wsd-debug-client-results) ниже.</span><span class="sxs-lookup"><span data-stu-id="924b8-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="924b8-111">**Использование клиента отладки WSD для проверки трафика многоадресной рассылки**</span><span class="sxs-lookup"><span data-stu-id="924b8-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="924b8-112">Настройте узел и клиент для работы по сети (то есть убедитесь, что узел и клиент будут работать на разных компьютерах).</span><span class="sxs-lookup"><span data-stu-id="924b8-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="924b8-113">Откройте командную строку и выполните следующую команду: **всддебуг \_client.exe/Mode multicast**</span><span class="sxs-lookup"><span data-stu-id="924b8-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="924b8-114">Воспроизведите ошибку, запустив узел и клиент или нажав клавишу F5 в обозревателе сети.</span><span class="sxs-lookup"><span data-stu-id="924b8-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="924b8-115">Убедитесь, что сообщения являются многоадресными.</span><span class="sxs-lookup"><span data-stu-id="924b8-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="924b8-116">Если требуемые сообщения отображаются в выходных данных клиента отладки WSD, то ошибка приложения может находиться в содержимом многоадресного сообщения, в случае существования или содержимого соответствующих одноадресных ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="924b8-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="924b8-117">Продолжайте устранение неполадок, следуя указаниям в разделе [Проверка трассировки сети для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="924b8-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="924b8-118">Если требуемые сообщения отображаются в выходных данных клиента отладки WSD, скорее всего, обнаружена проблема с источником проблемы приложения.</span><span class="sxs-lookup"><span data-stu-id="924b8-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="924b8-119">Вероятно, трафик многоадресной рассылки не передается по сети.</span><span class="sxs-lookup"><span data-stu-id="924b8-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="924b8-120">Эта ошибка может произойти, если приложение не перечисляет адаптеры многоадресной рассылки правильно.</span><span class="sxs-lookup"><span data-stu-id="924b8-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="924b8-121">Приложения должны явно передавать многоадресный трафик по всем сетевым интерфейсам; в противном случае пакеты не могут быть созданы для интерфейса замыкания на себя или для других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="924b8-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="924b8-122">Чтобы убедиться, что пакеты не отображаются в сети, следуйте инструкциям в разделе [Проверка трассировки сети для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) и найдите свидетельство об отсутствии многоадресных сообщений.</span><span class="sxs-lookup"><span data-stu-id="924b8-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="924b8-123">Проверка многоадресной рассылки сообщений</span><span class="sxs-lookup"><span data-stu-id="924b8-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="924b8-124">Всегда проверяйте, что сообщения [зонда](probe-message.md) являются многоадресными.</span><span class="sxs-lookup"><span data-stu-id="924b8-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="924b8-125">При необходимости убедитесь, что сообщения " [Привет](hello-message.md) " и " [разрешение](resolve-message.md) " являются многоадресными.</span><span class="sxs-lookup"><span data-stu-id="924b8-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="924b8-126">Обратите внимание, что не все приложения используют сообщения разрешения.</span><span class="sxs-lookup"><span data-stu-id="924b8-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="924b8-127">Дополнительные сведения о шаблонах сообщений, используемых клиентами и узлами, см. в статьях [шаблоны сообщений обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md) и [Начало работы с использованием WSDAPI устранение неполадок](getting-started-with-wsdapi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="924b8-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="924b8-128">Сообщения должны быть активированы для отправки, как описано в шаге 3 выше.</span><span class="sxs-lookup"><span data-stu-id="924b8-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="924b8-129">Клиент отладки WSD отображает необработанное сообщение SOAP в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="924b8-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="924b8-130">Так как все сообщения, выводимые клиентом отладки WSD в режиме многоадресной рассылки, получаются через сокет многоадресной рассылки, адрес назначения сообщения не отображается.</span><span class="sxs-lookup"><span data-stu-id="924b8-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="924b8-131">В следующем примере выходных данных клиента отладки WSD отображается сообщение пробы.</span><span class="sxs-lookup"><span data-stu-id="924b8-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="924b8-132">Элемент <WSA: Action> идентифицирует сообщение как сообщение пробы.</span><span class="sxs-lookup"><span data-stu-id="924b8-132">The <wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="924b8-133">Изучите поле <WSA: Action>, чтобы убедиться, что полученное сообщение является сообщением пробы.</span><span class="sxs-lookup"><span data-stu-id="924b8-133">Inspect the <wsa:Action> field to verify that the received message was a Probe message.</span></span>

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

<span data-ttu-id="924b8-134">В следующем примере выходных данных клиента отладки WSD отображается сообщение Hello.</span><span class="sxs-lookup"><span data-stu-id="924b8-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="924b8-135">Элемент <WSA: Action> идентифицирует сообщение как сообщение Hello.</span><span class="sxs-lookup"><span data-stu-id="924b8-135">The <wsa:Action> element identifies the message as a Hello message.</span></span>

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="924b8-136">Фильтрация результатов отладки клиента для WSD</span><span class="sxs-lookup"><span data-stu-id="924b8-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="924b8-137">Фильтрация результатов отладки клиента WSD может помочь определить трафик инцидента, включающий устройство.</span><span class="sxs-lookup"><span data-stu-id="924b8-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="924b8-138">Фильтрация необходима только для бесшумных сетей.</span><span class="sxs-lookup"><span data-stu-id="924b8-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="924b8-139">Существует два способа фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="924b8-139">There are two ways to filter results.</span></span> <span data-ttu-id="924b8-140">IP-адреса для фильтрации можно определить явным образом при запуске клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="924b8-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="924b8-141">Кроме того, IP-адреса можно указать после запуска клиента.</span><span class="sxs-lookup"><span data-stu-id="924b8-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="924b8-142">В этом разделе описываются оба метода.</span><span class="sxs-lookup"><span data-stu-id="924b8-142">This section describes both methods.</span></span>

<span data-ttu-id="924b8-143">**Указание IP-адресов для фильтрации при запуске клиента отладки WSD**</span><span class="sxs-lookup"><span data-stu-id="924b8-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="924b8-144">Настройте узел и клиент для работы по сети (то есть убедитесь, что узел и клиент будут работать на разных компьютерах).</span><span class="sxs-lookup"><span data-stu-id="924b8-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="924b8-145">Собирайте IP-адреса устройства.</span><span class="sxs-lookup"><span data-stu-id="924b8-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="924b8-146">Если устройство имеет несколько адресов (например, в нем есть адреса IPv4 и IPv6), необходимо собрать все адреса.</span><span class="sxs-lookup"><span data-stu-id="924b8-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="924b8-147">Откройте командную строку и выполните следующую команду: \**всддебуг \_client.exe/Mode multicast/IP Add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="924b8-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="924b8-148">*<device IP>* — Это IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="924b8-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="924b8-149">В следующем списке приведены некоторые примеры форматов для этого IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="924b8-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="924b8-150">адреса</span><span class="sxs-lookup"><span data-stu-id="924b8-150">192.168.0.1</span></span>
-   <span data-ttu-id="924b8-151">::1</span><span class="sxs-lookup"><span data-stu-id="924b8-151">::1</span></span>
-   <span data-ttu-id="924b8-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="924b8-152">mydevice.contoso.com</span></span>

<span data-ttu-id="924b8-153">Клиент отладки WSD автоматически разрешает имена узлов, предоставленные в командной строке.</span><span class="sxs-lookup"><span data-stu-id="924b8-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="924b8-154">**Фильтрация результатов после запуска клиента отладки WSD**</span><span class="sxs-lookup"><span data-stu-id="924b8-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="924b8-155">Настройте узел и клиент для работы по сети (то есть убедитесь, что узел и клиент будут работать на разных компьютерах).</span><span class="sxs-lookup"><span data-stu-id="924b8-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="924b8-156">Собирайте IP-адреса устройства.</span><span class="sxs-lookup"><span data-stu-id="924b8-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="924b8-157">Если устройство имеет несколько адресов (например, в нем есть адреса IPv4 и IPv6), необходимо собрать все адреса.</span><span class="sxs-lookup"><span data-stu-id="924b8-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="924b8-158">Откройте командную строку и выполните следующую команду: **всддебуг \_client.exe/Mode multicast**</span><span class="sxs-lookup"><span data-stu-id="924b8-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="924b8-159">В командной строке клиента отладки WSD выполните следующую команду: **IP Add** . *<device IP>*</span><span class="sxs-lookup"><span data-stu-id="924b8-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="924b8-160">Повторите шаг 4, пока не будут добавлены все IP-адреса устройств.</span><span class="sxs-lookup"><span data-stu-id="924b8-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="924b8-161">В следующей процедуре предполагается, что клиент отладки WSD запущен и выполняется фильтрация по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="924b8-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="924b8-162">**Проверка фильтрации правильных IP-адресов**</span><span class="sxs-lookup"><span data-stu-id="924b8-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="924b8-163">В командной строке клиента отладки WSD выполните следующую команду: **IP-печать** .</span><span class="sxs-lookup"><span data-stu-id="924b8-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="924b8-164">Отобразится список фильтруемых IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="924b8-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="924b8-165">В следующей процедуре предполагается, что клиент отладки WSD запущен и выполняется фильтрация по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="924b8-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="924b8-166">**Отключение фильтрации**</span><span class="sxs-lookup"><span data-stu-id="924b8-166">**To disable filtering**</span></span>

-   <span data-ttu-id="924b8-167">В командной строке клиента отладки WSD выполните следующую команду: **IP Clear** .</span><span class="sxs-lookup"><span data-stu-id="924b8-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="924b8-168">Весь трафик многоадресной рассылки теперь будет отображаться в выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="924b8-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="924b8-169">См. также</span><span class="sxs-lookup"><span data-stu-id="924b8-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="924b8-170">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="924b8-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="924b8-171">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="924b8-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



