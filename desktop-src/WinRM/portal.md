---
title: Удаленное управление Windows
description: Служба удаленного управления Windows (служба удаленного управления Windows) — это реализация корпорацией Майкрософт протокола WS-Management, стандартного интерфейса, поддерживающего брандмауэр на основе SOAP, который обеспечивает взаимодействие оборудования и операционных систем от разных поставщиков.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Служба удаленного управления Windows (WinRM), начальная страница
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987541"
---
# <a name="windows-remote-management"></a><span data-ttu-id="7ffe2-105">Удаленное управление Windows</span><span class="sxs-lookup"><span data-stu-id="7ffe2-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="7ffe2-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="7ffe2-106">Purpose</span></span>

<span data-ttu-id="7ffe2-107">С помощью удаленного управления Windows (WinRM) корпорация Майкрософт реализует стандартный [протокол WS-Management](ws-management-protocol.md), основанный на протоколе SOAP. Он удобен для брандмауэров и обеспечивает взаимодействие оборудования и операционных систем различных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="7ffe2-108">Спецификация протокола WS-Management предоставляет системам общий способ доступа и обмена данными управления в ИТ-инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="7ffe2-109">WinRM и [*интерфейс IPMI*](windows-remote-management-glossary.md), а также [сборщик событий](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) являются компонентами функций [управления оборудованием Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="7ffe2-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7ffe2-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="7ffe2-110">Where applicable</span></span>

<span data-ttu-id="7ffe2-111">Для получения данных управления с локальных и удаленных компьютеров, на которых могут использоваться [*контроллеры управления основной платой (BMC)*](windows-remote-management-glossary.md), можно использовать объекты скриптов WinRM, программу командной строки WinRM или средство командной строки удаленной оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="7ffe2-112">Если компьютер работает под управлением операционной системы Windows, которая включает WinRM, данные управления поставляются [инструментарий управления Windows (WMI) (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="7ffe2-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="7ffe2-113">Данные об оборудовании и системе также можно получить из реализаций протокола WS-Management, работающих в других операционных системах (не Windows) на предприятии.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="7ffe2-114">WinRM устанавливает сеанс связи с другим компьютером по протоколу WS-Management на основе SOAP, а не подключается через DCOM, как WMI.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="7ffe2-115">Данные возвращаются протоколу WS-Management в формате XML, а не в виде объектов.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="7ffe2-116">Поставщик [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI — это стандартный поставщик WMI с классами, получающими данные датчика BMC с компьютеров с соответствующим оборудованием.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="7ffe2-117">Доступ к данным IPMI можно получить с помощью API-интерфейсов WinRM, [скриптов](/windows/desktop/WmiSdk/scripting-api-for-wmi)WMI или [com](/windows/desktop/WmiSdk/com-api-for-wmi) .</span><span class="sxs-lookup"><span data-stu-id="7ffe2-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7ffe2-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="7ffe2-118">Developer audience</span></span>

<span data-ttu-id="7ffe2-119">Аудитория разработчика — ИТ-специалист, который пишет сценарии для автоматизации управления серверами или разработчиком ISV, получающим данные для приложений управления.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7ffe2-120">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="7ffe2-120">Run-time requirements</span></span>

<span data-ttu-id="7ffe2-121">WinRM является частью операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="7ffe2-122">Однако для получения данных с удаленных компьютеров необходимо настроить [*прослушиватель*](windows-remote-management-glossary.md#l)WinRM.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="7ffe2-123">Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="7ffe2-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="7ffe2-124">Если контроллер BMC обнаруживается при запуске системы, поставщик IPMI загружается; в противном случае объекты скриптов WinRM и средство командной строки WinRM остаются доступными.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7ffe2-125">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7ffe2-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7ffe2-126">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="7ffe2-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="7ffe2-127">Ссылка на общедоступную спецификацию протокола WS-Management, архитектуру WinRM, связь с WMI, управление оборудованием с помощью поставщика IPMI, конфигурации и установки.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="7ffe2-128">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="7ffe2-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="7ffe2-129">Приступая к работе с API-интерфейсом WinRM Scripting и аппаратным управлением.</span><span class="sxs-lookup"><span data-stu-id="7ffe2-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="7ffe2-130">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="7ffe2-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="7ffe2-131">Список интерфейсов сценариев, определенных веб-службами Майкрософт для автоматизации управления (WS-Management) и определений классов классов WMI, созданных поставщиком IPMI и классами, взаимодействующими с драйвером IPMI для получения данных [контроллера управления основной платой (BMC)](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffe2-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 