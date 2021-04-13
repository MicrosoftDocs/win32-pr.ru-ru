---
title: Настройка исходной подписки, инициированной источником
description: Подписки, инициированные источником, позволяют определить подписку на компьютере сборщика событий, не определяя исходные компьютеры событий, а затем можно настроить несколько удаленных компьютеров источника событий (с помощью параметра групповой политики) для перенаправления событий на компьютер сборщика событий.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/04/2020
ms.locfileid: "104412761"
---
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="d6a93-103">Настройка исходной подписки, инициированной источником</span><span class="sxs-lookup"><span data-stu-id="d6a93-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="d6a93-104">Подписки, инициированные источником, позволяют определить подписку на компьютере сборщика событий, не определяя исходные компьютеры событий, а затем можно настроить несколько удаленных компьютеров источника событий (с помощью параметра групповой политики) для перенаправления событий на компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="d6a93-105">Это отличается от подписки, инициированной сборщиком, так как в модели подписки, инициированной сборщиком, сборщик событий должен определить все источники событий в подписке на события.</span><span class="sxs-lookup"><span data-stu-id="d6a93-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="d6a93-106">При настройке подписки, инициированной источником, определите, находятся ли компьютеры-источники событий в том же домене, что и компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="d6a93-107">В следующих разделах описаны действия, которые необходимо выполнить, когда источники событий находятся в одном домене или не находятся в том же домене, что и компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="d6a93-108">Любой компьютер в домене, локальный или удаленный, может быть сборщиком событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="d6a93-109">Однако при выборе сборщика событий важно выбрать компьютер, топологически близко к месту, где будет создано большинство событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="d6a93-110">Отправка событий на компьютер в удаленном сетевом расположении в глобальной сети может снизить общую производительность и эффективность сбора событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="d6a93-111">Настройка инициированной источником подписки, в которой источники событий находятся в том же домене, что и компьютер сборщика событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="d6a93-112">Как компьютеры источника событий, так и компьютер сборщика событий должны быть настроены для настройки подписки, инициированной источником.</span><span class="sxs-lookup"><span data-stu-id="d6a93-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="d6a93-113">В этих инструкциях предполагается, что у вас есть доступ администратора к контроллеру домена Windows Server, обслуживающему домен, в котором будет настроено получение событий на удаленном компьютере или компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d6a93-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="d6a93-114">Настройка компьютера источника событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="d6a93-115">Выполните следующую команду из командной строки с повышенными привилегиями на контроллере домена Windows Server, чтобы настроить служба удаленного управления Windows:</span><span class="sxs-lookup"><span data-stu-id="d6a93-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="d6a93-116">**WinRM QCS-q**</span><span class="sxs-lookup"><span data-stu-id="d6a93-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="d6a93-117">Запустите групповую политику, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d6a93-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="d6a93-118">**% SYSTEMROOT% \\ system32 \\ gpedit. msc**</span><span class="sxs-lookup"><span data-stu-id="d6a93-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="d6a93-119">В узле **Конфигурация компьютера** разверните узел **Административные шаблоны** , разверните узел **компоненты Windows** , а затем выберите узел **Пересылка событий** .</span><span class="sxs-lookup"><span data-stu-id="d6a93-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="d6a93-120">Щелкните правой кнопкой мыши параметр **SubscriptionManager** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="d6a93-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="d6a93-121">Включите параметр **SubscriptionManager** и нажмите кнопку " **Показывать** ", чтобы добавить адрес сервера в параметр.</span><span class="sxs-lookup"><span data-stu-id="d6a93-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="d6a93-122">Добавьте хотя бы один параметр, указывающий компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="d6a93-123">Окно **Свойства SubscriptionManager** содержит вкладку **Объяснение** , описывающую синтаксис параметра.</span><span class="sxs-lookup"><span data-stu-id="d6a93-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="d6a93-124">После добавления параметра **SubscriptionManager** выполните следующую команду, чтобы убедиться, что политика применена:</span><span class="sxs-lookup"><span data-stu-id="d6a93-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="d6a93-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="d6a93-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="d6a93-126">Настройка компьютера сборщика событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="d6a93-127">Выполните следующую команду из командной строки с повышенными привилегиями на контроллере домена Windows Server, чтобы настроить служба удаленного управления Windows:</span><span class="sxs-lookup"><span data-stu-id="d6a93-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="d6a93-128">**WinRM QCS-q**</span><span class="sxs-lookup"><span data-stu-id="d6a93-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="d6a93-129">Выполните следующую команду, чтобы настроить службу сборщика событий:</span><span class="sxs-lookup"><span data-stu-id="d6a93-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="d6a93-130">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="d6a93-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="d6a93-131">Создайте исходную подписку.</span><span class="sxs-lookup"><span data-stu-id="d6a93-131">Create a source initiated subscription.</span></span> <span data-ttu-id="d6a93-132">Это можно сделать программно, с помощью Просмотр событий или с помощью [**Wecutil.exe**](wecutil.md).</span><span class="sxs-lookup"><span data-stu-id="d6a93-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="d6a93-133">Дополнительные сведения о создании подписки программным путем см. в примере кода в статье [Создание инициированной источником подписки](creating-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="d6a93-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="d6a93-134">При использовании Wecutil.exe необходимо создать XML-файл подписки на события и использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d6a93-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="d6a93-135">**wecutil cs** *configurationFile.xml*</span><span class="sxs-lookup"><span data-stu-id="d6a93-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="d6a93-136">Следующий код XML является примером содержимого файла конфигурации подписки, который создает подписку, инициированную источником, для перенаправления событий из журнала событий приложений удаленного компьютера в журнал ForwardedEvents на компьютере сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > <span data-ttu-id="d6a93-137">При создании исходной инициированной подписки, если Алловедсаурцедомаинкомпутерс, Алловедсаурценондомаинкомпутерс/Иссуеркалист, Алловедсубжектлист и DeniedSubjectList все пусты, то "O:NSG: NSD: (A;; GA;;;D C) (A;; Общедоступный;;; NS) "будет использоваться в качестве дескриптора безопасности по умолчанию для Алловедсаурцедомаинкомпутерс.</span><span class="sxs-lookup"><span data-stu-id="d6a93-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="d6a93-138">Дескриптор по умолчанию предоставляет членам группы домена Доменные компьютеры, а также группу локальных сетевых служб (для локального сервера пересылки) возможность создавать события для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="d6a93-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="d6a93-139">Проверка правильности работы подписки</span><span class="sxs-lookup"><span data-stu-id="d6a93-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="d6a93-140">На компьютере сборщика событий выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d6a93-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="d6a93-141">Выполните следующую команду из командной строки с повышенными привилегиями на контроллере домена Windows Server, чтобы получить состояние выполнения подписки:</span><span class="sxs-lookup"><span data-stu-id="d6a93-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="d6a93-142">**wecutil GR** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="d6a93-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="d6a93-143">Убедитесь, что источник событий подключен.</span><span class="sxs-lookup"><span data-stu-id="d6a93-143">Verify that the event source has connected.</span></span> <span data-ttu-id="d6a93-144">Возможно, потребуется подождать, пока интервал обновления, указанный в политике, не пойдет после создания подписки для подключения к источнику событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="d6a93-145">Выполните следующую команду, чтобы получить сведения о подписке:</span><span class="sxs-lookup"><span data-stu-id="d6a93-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="d6a93-146">**wecutil GS** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="d6a93-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="d6a93-147">Получите значение Деливеримакситемс из сведений о подписке.</span><span class="sxs-lookup"><span data-stu-id="d6a93-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="d6a93-148">На компьютере источника событий создайте события, которые соответствуют запросу, из подписки на события.</span><span class="sxs-lookup"><span data-stu-id="d6a93-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="d6a93-149">Деливеримакситемс число событий должно быть сгенерировано для перенаправляемых событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="d6a93-150">На компьютере сборщика событий проверьте, что события были перенаправлены в журнал ForwardedEvents или в журнал, указанный в подписке.</span><span class="sxs-lookup"><span data-stu-id="d6a93-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="d6a93-151">Пересылка журнала безопасности</span><span class="sxs-lookup"><span data-stu-id="d6a93-151">Forwarding the security log</span></span>

<span data-ttu-id="d6a93-152">Чтобы можно было перенаправить журнал безопасности, необходимо добавить учетную запись сетевой службы в группу читателей EventLog.</span><span class="sxs-lookup"><span data-stu-id="d6a93-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="d6a93-153">Настройка исходной подписки, в которой источники событий находятся не в том же домене, что и компьютер сборщика событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="d6a93-154">В этих инструкциях предполагается, что у вас есть права администратора на доступ к контроллеру домена Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d6a93-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="d6a93-155">В этом случае, поскольку компьютер или компьютеры сборщика удаленных событий не находятся в домене, обслуживаемом контроллером домена, важно запустить отдельный клиент, установив для служба удаленного управления Windows значение "автоматически" с помощью служб (Services. msc).</span><span class="sxs-lookup"><span data-stu-id="d6a93-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="d6a93-156">Кроме того, можно выполнить команду "winrm quickconfig" на каждом удаленном клиенте.</span><span class="sxs-lookup"><span data-stu-id="d6a93-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="d6a93-157">Перед созданием подписки должны быть выполнены следующие предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="d6a93-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="d6a93-158">На компьютере сборщика событий выполните следующие команды из командной строки с повышенными привилегиями, чтобы настроить служба удаленного управления Windows и службу сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="d6a93-159">**WinRM QCS-q**</span><span class="sxs-lookup"><span data-stu-id="d6a93-159">**winrm qc -q**</span></span>

    <span data-ttu-id="d6a93-160">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="d6a93-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="d6a93-161">Компьютер сборщика должен иметь сертификат проверки подлинности сервера (сертификат с целью проверки подлинности сервера) в хранилище сертификатов локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d6a93-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="d6a93-162">На компьютере источника событий выполните следующую команду, чтобы настроить служба удаленного управления Windows:</span><span class="sxs-lookup"><span data-stu-id="d6a93-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="d6a93-163">**WinRM QCS-q**</span><span class="sxs-lookup"><span data-stu-id="d6a93-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="d6a93-164">На исходном компьютере должен быть сертификат проверки подлинности клиента (сертификат с целью проверки подлинности клиента) в хранилище сертификатов локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d6a93-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="d6a93-165">Порт 5986 открыт на компьютере сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="d6a93-166">Чтобы открыть этот порт, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d6a93-166">To open this port, run the command:</span></span>

    <span data-ttu-id="d6a93-167">**netsh firewall Add открытие портов TCP 5986 "WinRM HTTPS Remote Management"**</span><span class="sxs-lookup"><span data-stu-id="d6a93-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="d6a93-168">Требования к сертификатам</span><span class="sxs-lookup"><span data-stu-id="d6a93-168">Certificates requirements</span></span>

- <span data-ttu-id="d6a93-169">Сертификат проверки подлинности сервера должен быть установлен на компьютере сборщика событий в личном хранилище локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d6a93-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="d6a93-170">Субъект этого сертификата должен соответствовать полному доменному имени сборщика.</span><span class="sxs-lookup"><span data-stu-id="d6a93-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="d6a93-171">Сертификат проверки подлинности клиента должен быть установлен на компьютерах-источниках событий в личном хранилище локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="d6a93-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="d6a93-172">Субъект этого сертификата должен соответствовать полному доменному имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="d6a93-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="d6a93-173">Если сертификат клиента выдан другим центром сертификации, чем один из сборщиков событий, то эти корневые и промежуточные сертификаты необходимо установить и в сборщике событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="d6a93-174">Если сертификат клиента был выдан промежуточным центром сертификации, а сборщик работает под управлением Windows 2012 или более поздней версии, потребуется настроить следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="d6a93-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="d6a93-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="d6a93-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="d6a93-176">Убедитесь, что сервер и клиент могут успешно проверить состояние отзыва для всех сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d6a93-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="d6a93-177">Использование команды **certutil** может помочь в устранении любых ошибок.</span><span class="sxs-lookup"><span data-stu-id="d6a93-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="d6a93-178">Дополнительные сведения см. в этой статье: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="d6a93-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="d6a93-179">Настройка прослушивателя в сборщике событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="d6a93-180">Настройте проверку подлинности на сертификате с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="d6a93-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="d6a93-181">**WinRM set winrm/config/Service/auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="d6a93-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="d6a93-182">На компьютере сборщика событий должен существовать прослушиватель HTTPS для WinRM с бегунком сертификата проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="d6a93-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="d6a93-183">Это можно проверить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="d6a93-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="d6a93-184">**WinRM e/config/Listener**</span><span class="sxs-lookup"><span data-stu-id="d6a93-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="d6a93-185">Если прослушиватель HTTPS не отображается или отпечаток прослушивателя HTTPS не совпадает с бегунком печати сертификата проверки подлинности сервера на компьютере сборщика, можно удалить этот прослушиватель и создать новый с правильной печатью Thumb.</span><span class="sxs-lookup"><span data-stu-id="d6a93-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="d6a93-186">Чтобы удалить прослушиватель HTTPS, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d6a93-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="d6a93-187">**WinRM удалить WinRM/config/Listener? Адрес = \* + транспорт = HTTPS**</span><span class="sxs-lookup"><span data-stu-id="d6a93-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="d6a93-188">Чтобы создать новый прослушиватель, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d6a93-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="d6a93-189">**WinRM создать WinRM/config/Listener? Адрес =&#42;+ Transport = HTTPS @ {имя_узла = "** &lt; _полное доменное имя сборщика_ &gt; **"; CertificateThumbprint = "** &lt; _бегунка сертификата проверки подлинности сервера_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="d6a93-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="d6a93-190">Настройка сопоставления сертификатов в сборщике событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="d6a93-191">Создайте нового локального пользователя и добавьте его в локальную группу администраторов.</span><span class="sxs-lookup"><span data-stu-id="d6a93-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="d6a93-192">Создайте сопоставление сертификата с помощью сертификата, который имеется в "доверенных корневых центрах сертификации" или "промежуточных центрах сертификации".</span><span class="sxs-lookup"><span data-stu-id="d6a93-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="d6a93-193">Это сертификат корневого или промежуточного ЦС, который выдал сертификаты, установленные на компьютерах-источниках событий *(чтобы избежать путаницы, это центр сертификации, находящийся непосредственно над сертификатом в цепочке сертификатов)*:</span><span class="sxs-lookup"><span data-stu-id="d6a93-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="d6a93-194">**WinRM Create WinRM/config/Service/certmapping?** = &lt; _Отпечаток издателя выдающего сертификата ЦС_ &gt; **+ subject =&#42;+ URI =&#42; @ {имя_пользователя = "** &lt; _username_ &gt; **"; Password = "** &lt; _пароль_ &gt; **"} — удаленный: localhost**</span><span class="sxs-lookup"><span data-stu-id="d6a93-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="d6a93-195">В клиенте проверьте прослушиватель и сопоставление сертификата с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="d6a93-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="d6a93-196">**WinRM g WinRM/config-р:хттпс://** &lt; _Полное доменное имя_ &gt; сборщика событий **: 5986-а:цертификате-Certificate: "** &lt; _Отпечаток сертификата_ &gt; проверки подлинности клиента **"**</span><span class="sxs-lookup"><span data-stu-id="d6a93-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="d6a93-197">Это должно вернуть конфигурацию WinRM сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="d6a93-198">**Не перейдем за** этот шаг, если конфигурация не отображается.</span><span class="sxs-lookup"><span data-stu-id="d6a93-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="d6a93-199">**Что происходит на этом этапе?**</span><span class="sxs-lookup"><span data-stu-id="d6a93-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="d6a93-200">Клиент подключается к сборщику событий и отправляет указанный сертификат.</span><span class="sxs-lookup"><span data-stu-id="d6a93-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="d6a93-201">Сборщик событий ищет выдающий ЦС и проверяет, соответствует ли он сопоставлению сертификата.</span><span class="sxs-lookup"><span data-stu-id="d6a93-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="d6a93-202">Сборщик событий проверяет цепочку сертификатов клиента и состояние отзыва</span><span class="sxs-lookup"><span data-stu-id="d6a93-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="d6a93-203">Если описанные выше действия выполнены успешно, проверка подлинности завершается.</span><span class="sxs-lookup"><span data-stu-id="d6a93-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="d6a93-204">Может возникнуть ошибка отказа в доступе, посвященная методу проверки подлинности, что может привести к неверному получению.</span><span class="sxs-lookup"><span data-stu-id="d6a93-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="d6a93-205">Чтобы устранить неполадки, проверьте журнал CAPI в сборщике событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="d6a93-206">Перечислите настроенные записи certmapping с помощью команды **WinRM enum WinRM/config/Service/certmapping** .</span><span class="sxs-lookup"><span data-stu-id="d6a93-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="d6a93-207">Конфигурация компьютера источника событий</span><span class="sxs-lookup"><span data-stu-id="d6a93-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="d6a93-208">Войдите в систему с учетной записью администратора и откройте редактор локальных групповых политик (gpedit. msc).</span><span class="sxs-lookup"><span data-stu-id="d6a93-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="d6a93-209">Перейдите к локальному компьютеру Полици\компутер конфигурация \ административные шаблоны \ компоненты Компонентс\евент пересылки.</span><span class="sxs-lookup"><span data-stu-id="d6a93-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="d6a93-210">Откройте "Настройка адреса сервера, интервала обновления и центра сертификации поставщика для целевой версии диспетчера подписки".</span><span class="sxs-lookup"><span data-stu-id="d6a93-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="d6a93-211">Включите политику и щелкните SubscriptionManagers "показывать...". переключатель.</span><span class="sxs-lookup"><span data-stu-id="d6a93-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="d6a93-212">В окне SubscriptionManagers введите следующую строку:</span><span class="sxs-lookup"><span data-stu-id="d6a93-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="d6a93-213">**Сервер = HTTPS://** &lt; _Полное доменное имя сервера_ &gt; сборщика событий **: 5986/WSMan/SubscriptionManager/WEC, обновление =** &lt; _Интервал обновления в секундах_ &gt; **, Иссуерка =** &lt; _Отпечаток выдающего сертификата ЦС_&gt;</span><span class="sxs-lookup"><span data-stu-id="d6a93-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="d6a93-214">Выполните следующую командную строку, чтобы обновить локальные параметры групповая политика: gpupdate/force.</span><span class="sxs-lookup"><span data-stu-id="d6a93-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="d6a93-215">Эти действия должны привести к созданию события 104 на исходном компьютере Просмотр событий приложений и служб журнал Логс\микрософт\виндовс\евентлог-форвардингплугин\оператионал с помощью следующего сообщения:</span><span class="sxs-lookup"><span data-stu-id="d6a93-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="d6a93-216">"Сервер пересылки успешно подключился к диспетчеру подписки по адресу &lt; FQDN &gt; , за которым следует событие 100 с сообщением:" &lt; sub_name подписка &gt; успешно создана ".</span><span class="sxs-lookup"><span data-stu-id="d6a93-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="d6a93-217">В сборщике событий состояние выполнения подписки отобразится 1 активный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d6a93-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="d6a93-218">Откройте журнал ForwardedEvents в сборщике событий и проверьте, имеются ли события, перенаправляемые с исходных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d6a93-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="d6a93-219">Предоставление разрешения на закрытый ключ сертификата клиента в источнике события</span><span class="sxs-lookup"><span data-stu-id="d6a93-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="d6a93-220">Откройте консоль управления сертификатами для локального компьютера на компьютере источника событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="d6a93-221">Щелкните сертификат клиента правой кнопкой мыши и выберите Управление закрытыми ключами.</span><span class="sxs-lookup"><span data-stu-id="d6a93-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="d6a93-222">Предоставьте разрешение на чтение пользователю сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="d6a93-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="d6a93-223">Конфигурация подписки на события</span><span class="sxs-lookup"><span data-stu-id="d6a93-223">Event subscription configuration</span></span>

1. <span data-ttu-id="d6a93-224">Откройте Просмотр событий в сборщике событий и перейдите к узлу подписки.</span><span class="sxs-lookup"><span data-stu-id="d6a93-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="d6a93-225">Щелкните правой кнопкой мыши элемент подписки и выберите команду "создать подписку...".</span><span class="sxs-lookup"><span data-stu-id="d6a93-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="d6a93-226">Укажите имя и описание (необязательно) для новой подписки.</span><span class="sxs-lookup"><span data-stu-id="d6a93-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="d6a93-227">Выберите параметр "инициированный исходным компьютером" и щелкните "выбрать группы компьютеров...".</span><span class="sxs-lookup"><span data-stu-id="d6a93-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="d6a93-228">В окне группы компьютеров нажмите кнопку "добавить компьютеры, не являющиеся доменами".</span><span class="sxs-lookup"><span data-stu-id="d6a93-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="d6a93-229">и введите имя узла источника события.</span><span class="sxs-lookup"><span data-stu-id="d6a93-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="d6a93-230">Нажмите кнопку "добавить сертификаты".</span><span class="sxs-lookup"><span data-stu-id="d6a93-230">Click “Add Certificates…”</span></span> <span data-ttu-id="d6a93-231">и добавьте сертификат центра сертификации, выдающий сертификаты клиентов.</span><span class="sxs-lookup"><span data-stu-id="d6a93-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="d6a93-232">Для проверки сертификата можно щелкнуть в окне Просмотр сертификата.</span><span class="sxs-lookup"><span data-stu-id="d6a93-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="d6a93-233">В окне центры сертификации нажмите кнопку ОК, чтобы добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="d6a93-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="d6a93-234">По завершении добавления компьютеров нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="d6a93-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="d6a93-235">Вернитесь к свойствам подписки, щелкните в области выбрать события...</span><span class="sxs-lookup"><span data-stu-id="d6a93-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="d6a93-236">Настройте фильтр запросов событий, указав уровни событий, журналы событий или источники событий, ИДЕНТИФИКАТОРы событий и любые другие параметры фильтрации данных.</span><span class="sxs-lookup"><span data-stu-id="d6a93-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="d6a93-237">Вернитесь к свойствам подписки, щелкните Дополнительно...</span><span class="sxs-lookup"><span data-stu-id="d6a93-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="d6a93-238">Выберите один из вариантов оптимизации для доставки событий из события источник в сборщик событий или оставьте значение по умолчанию обычная.</span><span class="sxs-lookup"><span data-stu-id="d6a93-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="d6a93-239">**Уменьшить пропускную способность**. события будут доставляться с меньшей частотой для экономии пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="d6a93-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="d6a93-240">**Свести к минимальным задержкам**. события будут доставляться сразу после их возникновения для сокращения задержки событий.</span><span class="sxs-lookup"><span data-stu-id="d6a93-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="d6a93-241">Измените протокол на HTTPS и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="d6a93-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="d6a93-242">Нажмите кнопку ОК, чтобы создать новую подписку.</span><span class="sxs-lookup"><span data-stu-id="d6a93-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="d6a93-243">Проверьте состояние среды выполнения подписки, щелкнув ее правой кнопкой мыши и выбрав пункт "состояние среды выполнения".</span><span class="sxs-lookup"><span data-stu-id="d6a93-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>
