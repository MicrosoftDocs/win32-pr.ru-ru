---
title: Обнаружение профиля DMTF с помощью обхода взаимосвязей
description: ключевым компонентом инфраструктуры инструментарий управления Windows (WMI) (WMI) является объектно-ориентированная модель управляемых сущностей в системе.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f49d1433d8263dff2c1d50007f9aa0daf1573c09ebc8d7a513eda658c51997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643154"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Обнаружение профиля DMTF с помощью обхода взаимосвязей

ключевым компонентом инфраструктуры инструментарий управления Windows (WMI) (WMI) является объектно-ориентированная модель управляемых сущностей в системе. Модель соответствует стандарту, поддерживаемому задачей «Управление рабочим столом» ([DMTF](https://www.dmtf.org/standards/wsman)) и называется модель CIM (CIM). Некоторые классы в модели, такие как [ \_ файл CIM](../cimwin32prov/cim-datafile.md) или [ \_ процесс Win32](../cimwin32prov/win32-process.md), соответствуют непосредственно управляемым сущностям. Другие классы в модели, такие как [Win32 \_ системсервицес](../cimwin32prov/win32-systemservices.md), представляют отношения между управляемыми сущностями. Эти классы моделирования связей называются классами взаимосвязей.

С помощью языка запросов, зависящего от инструментария WMI, можно получить экземпляры классов, представляющие управляемые сущности или экземпляры классов взаимосвязей. Но WQL зависит от реализации. он работает только с реализацией Windows стандарта DMTF (WMI). Кроме того, синтаксис WQL для получения классов взаимосвязей довольно сложен.

инфраструктура служба удаленного управления Windows (WinRM) обеспечивает отличный способ использования функциональных возможностей WMI. Ранним версиям WinRM пришлось использовать WQL для получения экземпляров классов взаимосвязей. WinRM 2,0 включает новую функцию, известную как обнаружение профиля DMTF с помощью обхода взаимосвязей. Обход взаимосвязей позволяет пользователю WinRM получать экземпляры классов взаимосвязей с помощью стандартного механизма фильтрации — диалекта АссоЦиатионфилтер, определенного в спецификации привязки CIM DMTF. Дополнительные сведения об обходе связей см. в WS-Management спецификации привязки CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

Служебная программа WinRM предоставляет простой механизм для прохода по соответствующей ассоциации и получения профиля устройства.

## <a name="configuration-implementation-details"></a>Сведения о реализации конфигурации

Теперь служебная программа WinRM поддерживает диалект запроса на сопоставление. Либо универсальный код ресурса (URI), либо псевдоним можно указать с помощью служебной программы WinRM.



| Псевдоним       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| связь | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Получение экземпляров класса Association с помощью диалекта АссоЦиатионфилтер

Служебная программа WinRM может получать экземпляры классов взаимосвязей WMI определенного экземпляра источника. Следующая команда демонстрирует использование служебной программы WinRM для получения экземпляров классов ассоциаций [ \_ служб Win32](../cimwin32prov/win32-service.md) . Для возврата классов связей необходимо использовать переключатель "-Associations".

**WinRM Enumerate wmicimv2/ \* -диалект: Ассоциация-Associations-Filter: {объект = \_ служба Win32? имя = WinRM; ресулткласснаме = Win32 \_ депендентсервице; роль = зависимая}**

Следующий текстовый фрагмент — это выходные данные приведенной выше команды:

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Получение экземпляров связанного класса с помощью диалекта АссоЦиатионфилтер

Служебная программа WinRM может получать экземпляры классов WMI, связанные с определенным исходным экземпляром. Следующая команда демонстрирует использование служебной программы WinRM для получения экземпляров классов, связанных [со \_ службой Win32](../cimwin32prov/win32-service.md) .

**WinRM Enumerate wmicimv2/ \* -диалект: Association-Filter: {Object = Win32 \_ Service? Name = WinRM; ассоЦиатионкласснаме = Win32 \_ депендентсервице; ресулткласснаме = служба Win32 \_ ; ресултроле = Antecedent; Role = Dependent}**

Следующий текстовый фрагмент — это выходные данные приведенной выше команды:

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

 

 