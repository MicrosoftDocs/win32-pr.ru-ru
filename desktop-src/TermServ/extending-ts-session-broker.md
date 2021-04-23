---
title: Расширение посредника сеансов служб терминалов
description: Можно расширить TS \ 160; Посредник сеансов с помощью COM-интерфейса Ивтссбплугин.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793117"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="271cd-103">Расширение посредника сеансов служб терминалов</span><span class="sxs-lookup"><span data-stu-id="271cd-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="271cd-104">Посредник сеансов служб терминалов определяет, уже открыт ли сеанс для пользователя, инициирующего подключение.</span><span class="sxs-lookup"><span data-stu-id="271cd-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="271cd-105">В этом случае посредник сеансов служб терминалов направляет входящее подключение к серверу узла сеансов удаленный рабочий стол (на узле сеанса удаленных рабочих столов) с помощью существующего сеанса.</span><span class="sxs-lookup"><span data-stu-id="271cd-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="271cd-106">В противном случае посредник сеансов служб терминалов направляет входящее подключение к серверу узла сеансов удаленных рабочих столов с наименьшим числом сеансов.</span><span class="sxs-lookup"><span data-stu-id="271cd-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="271cd-107">Посредник сеансов служб терминалов можно расширить с помощью COM-интерфейса [**ивтссбплугин**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="271cd-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="271cd-108">Этот интерфейс можно использовать для управления подключениями к серверам узла сеансов удаленных рабочих столов, а также подключения любого типа протокол удаленного рабочего стола (RDP), например, подключения к гостевым виртуальным машинам, на которых работает Windows Vista Enterprise (VECD), на узле виртуальных машин Hyper-V Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="271cd-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="271cd-109">Интерфейс [**ивтссбплугин**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) предоставляет несколько преимуществ:</span><span class="sxs-lookup"><span data-stu-id="271cd-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="271cd-110">Нет необходимости устанавливать агент на клиент или сервер узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="271cd-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="271cd-111">Подключаемый модуль может без проблем взаимодействовать с другими службами ролей службы удаленных рабочих столов, такими как удаленный рабочий стол шлюз (шлюз удаленных рабочих столов), и полагаться на информацию из посредника сеансов служб терминалов о состояниях сеансов и компьютеров.</span><span class="sxs-lookup"><span data-stu-id="271cd-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="271cd-112">Подключаемый модуль можно использовать для управления подключениями к клиентским или серверным устройствам, поддерживающим RDP 5,2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="271cd-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="271cd-113">Подключаемый модуль можно использовать для включения централизованных решений для настольных систем Windows Vista Enterprise.</span><span class="sxs-lookup"><span data-stu-id="271cd-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="271cd-114">При реализации методов этого интерфейса учитывайте следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="271cd-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="271cd-115">Посредник сеансов служб терминалов может вызывать методы этого COM-объекта из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="271cd-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="271cd-116">Если какой-либо из вызванных методов не возвращает немедленно и успешно, посредник сеансов служб терминалов не вызывает подключаемый модуль и возвращается к его собственной логике балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="271cd-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="271cd-117">Чтобы возобновить вызовы к подключаемому модулю, необходимо перезапустить службу посредника сеансов служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="271cd-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="271cd-118">Необходимо зарегистрировать подключаемый модуль в качестве объекта COM на уровне системы с помощью Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="271cd-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="271cd-119">Так как служба посредника сеансов служб терминалов работает под учетной записью NetworkService, необходимо предоставить учетной записи NetworkService необходимые права на запуск, активацию и доступ с помощью Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="271cd-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="271cd-120">Служба посредника сеансов служб терминалов ищет идентификатор CLSID COM-объекта, представляющего подключаемый модуль, в следующем подразделе реестра:</span><span class="sxs-lookup"><span data-stu-id="271cd-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="271cd-121">**HKey \_ \_** CurrentControlSet Services System (локальные компьютеры) \\  \\  \\  \\ **Tssdis** \\ **Параметры** \\ **екстенсибилитиплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="271cd-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="271cd-122">Дополнительные сведения о Dcomcnfg.exe см. в разделе [Включение безопасности COM с помощью DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span><span class="sxs-lookup"><span data-stu-id="271cd-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="271cd-123">См. также</span><span class="sxs-lookup"><span data-stu-id="271cd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="271cd-124">**ивтссбплугин**</span><span class="sxs-lookup"><span data-stu-id="271cd-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 