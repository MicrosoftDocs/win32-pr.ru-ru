---
title: Обнаружение профиля DMTF с помощью обхода взаимосвязей
description: Ключевым компонентом инфраструктуры инструментарий управления Windows (WMI) (WMI) является объектно-ориентированная модель управляемых сущностей в системе.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413945"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="6e1cb-103">Обнаружение профиля DMTF с помощью обхода взаимосвязей</span><span class="sxs-lookup"><span data-stu-id="6e1cb-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="6e1cb-104">Ключевым компонентом инфраструктуры инструментарий управления Windows (WMI) (WMI) является объектно-ориентированная модель управляемых сущностей в системе.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="6e1cb-105">Модель соответствует стандарту, поддерживаемому задачей «Управление рабочим столом» ([DMTF](https://www.dmtf.org/standards/wsman)) и называется модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="6e1cb-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="6e1cb-106">Некоторые классы в модели, такие как [ \_ файл CIM](../cimwin32prov/cim-datafile.md) или [ \_ процесс Win32](../cimwin32prov/win32-process.md), соответствуют непосредственно управляемым сущностям.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="6e1cb-107">Другие классы в модели, такие как [Win32 \_ системсервицес](../cimwin32prov/win32-systemservices.md), представляют отношения между управляемыми сущностями.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="6e1cb-108">Эти классы моделирования связей называются классами взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="6e1cb-109">С помощью языка запросов, зависящего от инструментария WMI, можно получить экземпляры классов, представляющие управляемые сущности или экземпляры классов взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="6e1cb-110">Но WQL зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-110">But WQL is implementation specific.</span></span> <span data-ttu-id="6e1cb-111">Он работает только с реализацией Windows стандарта DMTF (WMI).</span><span class="sxs-lookup"><span data-stu-id="6e1cb-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="6e1cb-112">Кроме того, синтаксис WQL для получения классов взаимосвязей довольно сложен.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="6e1cb-113">Инфраструктура служба удаленного управления Windows (WinRM) обеспечивает отличный способ использования функциональных возможностей WMI.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="6e1cb-114">Ранним версиям WinRM пришлось использовать WQL для получения экземпляров классов взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="6e1cb-115">WinRM 2,0 включает новую функцию, известную как обнаружение профиля DMTF с помощью обхода взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="6e1cb-116">Обход взаимосвязей позволяет пользователю WinRM получать экземпляры классов взаимосвязей с помощью стандартного механизма фильтрации — диалекта АссоЦиатионфилтер, определенного в спецификации привязки CIM DMTF.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="6e1cb-117">Дополнительные сведения об обходе связей см. в WS-Management спецификации привязки CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).</span><span class="sxs-lookup"><span data-stu-id="6e1cb-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="6e1cb-118">Служебная программа WinRM предоставляет простой механизм для прохода по соответствующей ассоциации и получения профиля устройства.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="6e1cb-119">Сведения о реализации конфигурации</span><span class="sxs-lookup"><span data-stu-id="6e1cb-119">Configuration Implementation Details</span></span>

<span data-ttu-id="6e1cb-120">Теперь служебная программа WinRM поддерживает диалект запроса на сопоставление.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="6e1cb-121">Либо универсальный код ресурса (URI), либо псевдоним можно указать с помощью служебной программы WinRM.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="6e1cb-122">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="6e1cb-122">Alias</span></span>       | <span data-ttu-id="6e1cb-123">URI</span><span class="sxs-lookup"><span data-stu-id="6e1cb-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="6e1cb-124">связь</span><span class="sxs-lookup"><span data-stu-id="6e1cb-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="6e1cb-125">Получение экземпляров класса Association с помощью диалекта АссоЦиатионфилтер</span><span class="sxs-lookup"><span data-stu-id="6e1cb-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="6e1cb-126">Служебная программа WinRM может получать экземпляры классов взаимосвязей WMI определенного экземпляра источника.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="6e1cb-127">Следующая команда демонстрирует использование служебной программы WinRM для получения экземпляров классов ассоциаций [ \_ служб Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="6e1cb-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="6e1cb-128">Для возврата классов связей необходимо использовать переключатель "-Associations".</span><span class="sxs-lookup"><span data-stu-id="6e1cb-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="6e1cb-129">**WinRM Enumerate wmicimv2/ \* -диалект: Ассоциация-Associations-Filter: {объект = \_ служба Win32? имя = WinRM; ресулткласснаме = Win32 \_ депендентсервице; роль = зависимая}**</span><span class="sxs-lookup"><span data-stu-id="6e1cb-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="6e1cb-130">Следующий текстовый фрагмент — это выходные данные приведенной выше команды:</span><span class="sxs-lookup"><span data-stu-id="6e1cb-130">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="6e1cb-131">Получение экземпляров связанного класса с помощью диалекта АссоЦиатионфилтер</span><span class="sxs-lookup"><span data-stu-id="6e1cb-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="6e1cb-132">Служебная программа WinRM может получать экземпляры классов WMI, связанные с определенным исходным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="6e1cb-133">Следующая команда демонстрирует использование служебной программы WinRM для получения экземпляров классов, связанных [со \_ службой Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="6e1cb-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="6e1cb-134">**WinRM Enumerate wmicimv2/ \* -диалект: Association-Filter: {Object = Win32 \_ Service? Name = WinRM; ассоЦиатионкласснаме = Win32 \_ депендентсервице; ресулткласснаме = служба Win32 \_ ; ресултроле = Antecedent; Role = Dependent}**</span><span class="sxs-lookup"><span data-stu-id="6e1cb-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="6e1cb-135">Следующий текстовый фрагмент — это выходные данные приведенной выше команды:</span><span class="sxs-lookup"><span data-stu-id="6e1cb-135">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 