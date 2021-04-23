---
title: Наблюдение за подключениями и отсоединениями сеансов
description: Чтобы зарегистрировать приложение в службы удаленных рабочих столов, сохраните имя серверного приложения виртуального канала в реестре, добавив подраздел.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070108"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="60f68-103">Наблюдение за подключениями и отсоединениями сеансов</span><span class="sxs-lookup"><span data-stu-id="60f68-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="60f68-104">Для приложения службы, такого как серверное приложение виртуального канала, для мониторинга соединений и отсоединений сеансов необходимо зарегистрировать его в службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="60f68-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="60f68-105">Чтобы зарегистрировать приложение в службы удаленных рабочих столов, сохраните имя серверного приложения виртуального канала в реестре, добавив подраздел в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="60f68-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="60f68-106">**HKey \_ \_** \\  \\  \\  \\  \\ **Надстройки** терминалсервер управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="60f68-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="60f68-107">У подраздела может быть любое имя.</span><span class="sxs-lookup"><span data-stu-id="60f68-107">The subkey can have any name.</span></span> <span data-ttu-id="60f68-108">Он должен иметь значение **reg \_ SZ** , **имя**, которое содержит символическое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="60f68-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="60f68-109">Максимальная длина подраздела и значения **имени** — 99 символов.</span><span class="sxs-lookup"><span data-stu-id="60f68-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="60f68-110">Подраздел также должен иметь значение **reg \_ DWORD** , указывающее тип серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="60f68-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="60f68-111">*Аддинтипе* должно иметь следующее значение.</span><span class="sxs-lookup"><span data-stu-id="60f68-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="60f68-112">Значение</span><span class="sxs-lookup"><span data-stu-id="60f68-112">Value</span></span> | <span data-ttu-id="60f68-113">Значение</span><span class="sxs-lookup"><span data-stu-id="60f68-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="60f68-114">3</span><span class="sxs-lookup"><span data-stu-id="60f68-114">3</span></span>     | <span data-ttu-id="60f68-115">Приложение пользовательского режима, пространство сеанса.</span><span class="sxs-lookup"><span data-stu-id="60f68-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="60f68-116">Регистрация приложения службы вступает в силу только в сеансах, созданных после выполнения регистрации.</span><span class="sxs-lookup"><span data-stu-id="60f68-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="60f68-117">Для каждого зарегистрированного приложения службы службы удаленных рабочих столов задаст набор объектов событий, когда клиент подключится к сеансу или отключится от него.</span><span class="sxs-lookup"><span data-stu-id="60f68-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="60f68-118">Каждый подключаемый модуль виртуального канала должен зарегистрироваться и создать события уведомления путем вызова функции [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span><span class="sxs-lookup"><span data-stu-id="60f68-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="60f68-119">Имена этих объектов событий соответствуют следующему формату.</span><span class="sxs-lookup"><span data-stu-id="60f68-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="60f68-120">*AddinName* — это строка, указанная в значении **имени** подраздела реестра, в котором зарегистрировано серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="60f68-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="60f68-121">Создание этих событий в сеансе приводит к их созданию в специальном каталоге событий для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="60f68-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="60f68-122">Каталог событий обеспечивает дополнительную безопасность, предотвращая изменение состояния этих событий приложениями в других сеансах.</span><span class="sxs-lookup"><span data-stu-id="60f68-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="60f68-123">Чтобы контролировать, получены ли на сервере события повторного подключения и отключения, можно поместить флаг **ремотеконтролперсистент** в реестр в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="60f68-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="60f68-124">**HKey \_ Локальный \_ компьютер** \\ **система** \\ **CurrentControlSet** \\ **Управление** \\  \\ **надстройками** терминалсервер \\ *AddinName*</span><span class="sxs-lookup"><span data-stu-id="60f68-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="60f68-125">Флаг включает или отключает сигнал о событиях повторного подключения и отключения при запуске или остановке сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="60f68-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="60f68-126">Синтаксис значения **\_ DWORD реестра** следующий.</span><span class="sxs-lookup"><span data-stu-id="60f68-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="60f68-127">Значение *флага* может быть равно одному или нулю.</span><span class="sxs-lookup"><span data-stu-id="60f68-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="60f68-128">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="60f68-128">Zero is the default value.</span></span> <span data-ttu-id="60f68-129">Если задано значение One, приложение службы не будет уведомлено о запуске или остановке сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="60f68-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="60f68-130">Если задано нулевое значение, событие повторного подключения получает сигнал при запуске сеанса клиента, а событие отключения сигнализирует о остановке сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="60f68-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="60f68-131">Предыдущий формат имени объекта события по-прежнему поддерживается в Windows Server 2008 для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="60f68-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="60f68-132">Рекомендуется использовать новый формат Windows Server 2008, так как он более безопасен.</span><span class="sxs-lookup"><span data-stu-id="60f68-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="60f68-133">Формат предыдущего события выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="60f68-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="60f68-134">*AddinName* — это строка, указанная в значении **имени** подраздела реестра, в котором зарегистрировано серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="60f68-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="60f68-135">*SessionID* — это идентификатор сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="60f68-135">*SessionId* is the session identifier of a client session.</span></span>

 

 