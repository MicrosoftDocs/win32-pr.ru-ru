---
description: Наиболее распространенным способом обновления экземпляра класса WMI является обновление всего экземпляра.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Обновление всего экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265594"
---
# <a name="updating-an-entire-instance"></a>Обновление всего экземпляра

Наиболее распространенным способом обновления экземпляра класса WMI является обновление всего экземпляра. При обновлении всего экземпляра Инструментарий WMI не нужно анализировать экземпляр в отдельные свойства и передавать его в приложение. Вместо этого инструментарий WMI может просто отправить вам весь экземпляр. По завершении Инструментарий WMI может скопировать весь измененный экземпляр по исходному экземпляру.

Следующая процедура описывает, как изменить или обновить экземпляр с помощью PowerShell.

**Изменение или обновление экземпляра с помощью PowerShell**

1.  Получите локальную копию объекта с помощью вызова Get-WmiObject.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  При необходимости просмотрите свойства объекта, вызвав коллекцию Properties.

    Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Внесите любые изменения в свойства локального объекта.

    Это изменит только локальную копию. Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Поместите объект обратно в репозиторий WMI, используя вызов метода размещения.

    ```PowerShell
    $mySettings.Put()
    ```

    

Следующая процедура описывает, как изменить или обновить экземпляр с помощью C#.

**Изменение или обновление экземпляра с помощью C# (Microsoft. Management. Infrastructure)**

1.  Получите локальную копию объекта с помощью вызова [CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))GetObject, как описано в статье [Получение экземпляра WMI](retrieving-an-instance.md).

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  При необходимости просмотрите свойства объекта, вызвав коллекцию Properties.

    Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Внесите любые изменения в свойства локального объекта.

    Это изменит только локальную копию. Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Поместите объект обратно в репозиторий WMI с помощью вызова [CimSession. модифинстанце](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

Следующая процедура описывает, как изменить или обновить экземпляр с помощью PowerShell.

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

**Изменение или обновление экземпляра с помощью C# (Microsoft. Management)**

1.  Получите локальную копию объекта с помощью вызова [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  При необходимости просмотрите свойства объекта, вызвав коллекцию Properties.

    Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Внесите любые изменения в свойства локального объекта.

    Это изменит только локальную копию. Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Поместите объект обратно в репозиторий WMI, используя вызов метода [ManagementObject.](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) Place или.

    ```CSharp
    myDisk.Put();
    ```

    

Следующая процедура описывает, как изменить или обновить экземпляр с помощью VBScript.

**Изменение или обновление экземпляра с помощью VBScript**

1.  Получите локальную копию объекта с помощью вызова **GetObject**.
2.  При необходимости просмотрите свойства объекта, вызвав метод [**Properties \_**](swbemobject-properties-.md) .

    Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.

3.  Внесите любые изменения в свойства объекта с помощью вызова метода [**SWbemProperty. Value**](swbemproperty-value.md) .

    Метод **value** изменяет только локальную копию. Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.

4.  Поместите объект обратно в репозиторий WMI, вызвав методы [**SWbemObject. \_**](swbemobject-put-.md) Place или [**SWbemObject. путасинк \_**](swbemobject-putasync-.md) .

Как предполагается в именах, [**помещайте \_**](swbemobject-put-.md) обновления синхронно, а обновления [**путасинк \_**](swbemobject-putasync-.md) асинхронно. Любой метод копирует поверх исходного экземпляра с измененным экземпляром. Однако, чтобы воспользоваться преимуществами асинхронной обработки, необходимо создать объект [**свбемсинк**](swbemsink.md) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Следующая процедура описывает, как изменить или обновить экземпляр с помощью C++.

**Изменение или обновление экземпляра с помощью C++**

1.  Получите локальную копию экземпляра с вызовом [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  При необходимости просмотрите свойства объекта, вызвав метод [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.

3.  Внесите необходимые изменения в копию с помощью вызова [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Метод **размещения** изменяет только локальную копию. Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.

4.  Поместите копию обратно в репозиторий WMI, вызвав методы [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    Как предполагается в именах, **PutInstance** обновляется синхронно, а [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) обновляется асинхронно. Любой метод копирует поверх исходного экземпляра с измененным экземпляром. Однако, чтобы воспользоваться преимуществами асинхронной обработки, необходимо реализовать интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .

    Следует иметь в виду, что операция обновления экземпляра, принадлежащего к иерархии классов, может не быть выполнена из-за ошибки, связанной с другим классом в иерархии. Инструментарий WMI вызывает метод [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) каждого из поставщиков, ответственных за классы, от которых наследуется исходный экземпляр. В случае сбоя любого из этих поставщиков исходный запрос на обновление завершится ошибкой. Дополнительные сведения см. в подразделе "Примечания" раздела [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

Дополнительные сведения см. [в разделе вызов метода поставщика](calling-a-provider-method.md).

> [!Note]  
> Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

 

 
