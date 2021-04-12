---
title: Создание подписок на события оборудования
description: На компьютерах с установленным контроллером управления основной платой (BMC) события оборудования вызываются и регистрируются в журнале системных событий (SEL), который представляет собой хранилище событий BMC, которое хранится в энергонезависимой памяти.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338516"
---
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="3cbb1-103">Создание подписок на события оборудования</span><span class="sxs-lookup"><span data-stu-id="3cbb1-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="3cbb1-104">На компьютерах с установленным контроллером управления основной платой (BMC) события оборудования вызываются и регистрируются в журнале системных событий (SEL), который представляет собой хранилище событий BMC, которое хранится в энергонезависимой памяти.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="3cbb1-105">Чтобы считать эти события оборудования в Windows Server 2008 с помощью Просмотр событий, необходимо создать подписку на эти события.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="3cbb1-106">Аппаратные подписки на события будут работать только в Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="3cbb1-107">Следующая процедура определяет, как создать подписку на событие SEL для получения событий оборудования:</span><span class="sxs-lookup"><span data-stu-id="3cbb1-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="3cbb1-108">Сохраните следующий XML-код в XML-файле (в этом примере файл называется Wsmanselrg.xml).</span><span class="sxs-lookup"><span data-stu-id="3cbb1-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="3cbb1-109">Этот XML определяет подписку.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-109">This XML defines the subscription.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  <span data-ttu-id="3cbb1-110">Создайте подписку на событие, выполнив следующую команду в окне командной строки (Wecutil.exe программа находится в каталоге% SYSTEMROOT% \\ System32):</span><span class="sxs-lookup"><span data-stu-id="3cbb1-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="3cbb1-111">**Wecutil CS** *<path> \\wsmanselrg.xml*</span><span class="sxs-lookup"><span data-stu-id="3cbb1-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="3cbb1-112">Убедитесь, что Подписка активна, выполнив следующую команду в окне командной строки:</span><span class="sxs-lookup"><span data-stu-id="3cbb1-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="3cbb1-113">**Wecutil GR** *всманселрг*</span><span class="sxs-lookup"><span data-stu-id="3cbb1-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="3cbb1-114">Контроллер BMC — это микроконтроллер, подключенный локально к серверу.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="3cbb1-115">Контроллеры BMC имеют датчики, отслеживающие физическое состояние сервера и отдельное сетевое подключение, которое может взаимодействовать по сети, даже если сервер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="3cbb1-116">У вас есть доступ к данным BMC через поставщик IPMI WMI.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="3cbb1-117">Дополнительные сведения о поставщике IPMI см. в разделе [поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="3cbb1-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="3cbb1-118">Для работы подписки на события на компьютере должен быть установлен контроллер BMC и поставщик IPMI.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="3cbb1-119">Для компьютеров под управлением Windows Server 2008 поставщик IPMI устанавливается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cbb1-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="3cbb1-120">Если контроллер BMC недоступен, то драйвер IPMI не может быть установлен, а состояние среды выполнения подписки всегда будет содержать ошибку (0x8004001-WMI, общий сбой).</span><span class="sxs-lookup"><span data-stu-id="3cbb1-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 