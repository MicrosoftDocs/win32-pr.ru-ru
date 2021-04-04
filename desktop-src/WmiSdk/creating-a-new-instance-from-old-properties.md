---
description: Класс представления соединения содержит свойства из экземпляров исходного класса, которые соединены общим значением свойства, например Class1. Prop1 = class2. Prop2. Каждый экземпляр в классе представления join состоит из частей различных экземпляров класса.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Создание нового экземпляра из старых свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999375"
---
# <a name="creating-a-new-instance-from-old-properties"></a>Создание нового экземпляра из старых свойств

Класс представления соединения содержит свойства из экземпляров исходного класса, которые соединены общим значением свойства, например **Class1. Prop1**  =  **class2. Prop2**. Каждый экземпляр в классе представления join состоит из частей различных экземпляров класса.

Можно создать класс представления объединения на неравенство значений свойств, например **Class1. Prop1**  <>  **class2. Prop2** , где **Prop1** и **Prop2** не сопоставлены с одним и тем же свойством в классе представления.

Класс представления Join полезен, если искомая информация содержится в отдельных, но связанных классах. Например, если требуется получить сведения о принтере и о конфигурации принтера, можно создать класс представления объединения, который содержит некоторые свойства класса [**\_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) и некоторые свойства класса [**\_ принтерконфигуратион Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) . Без поставщика представления необходимо получить и объединить свойства отдельных экземпляров, чтобы получить необходимую информацию.

В следующей процедуре описывается создание класса представления JOIN.

**Создание класса представления Join**

1.  Начните определение класса с квалификатором строки [**жоинон**](qualifiers-specific-to-the-view-provider.md) .

    Квалификаторы [**жоинон**](qualifiers-specific-to-the-view-provider.md), **Association** и **Union** являются взаимоисключающими.

2.  При необходимости отфильтруйте нужные экземпляры в классе JOIN, применив квалификатор [**постжоинфилтер**](postjoinfilter-qualifier.md) .

    Поставщик [**постжоинфилтер**](postjoinfilter-qualifier.md) позволяет ограничить экземпляры класса представления экземплярами, которые соответствуют определенным условиям.

3.  Создайте запросы, определяющие исходные экземпляры класса представления с квалификатором [**виевсаурцес**](viewsources-qualifier.md) .
4.  Определите имена и расположения пространств имен, в которых находятся исходные экземпляры с квалификатором [**виевспацес**](viewspaces-qualifier.md) .
5.  Определите нужные свойства в классе представления JOIN с квалификатором [**пропертисаурцес**](propertysources-qualifier.md) .

    Когда свойства добавляются в представление объединения на основе равенства, два исходных свойства должны быть сопоставлены в одном квалификаторе [**пропертисаурцес**](propertysources-qualifier.md) .

    В следующем примере кода показаны два свойства, сопоставленные в одном квалификаторе **пропертисаурцес** .

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    С помощью квалификатора [**хиддендефаулт**](qualifiers-specific-to-the-view-provider.md) можно пометить свойства, принадлежащие исходному классу.

В следующем примере кода показан класс представления соединения, созданный из классов поставщика монитора производительности [**Win32 \_ перфравдата \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) и [**Win32 \_ перфравдата \_ PerfProc \_**](/previous-versions//aa394325(v=vs.85)) , со свойствами обоих классов, присоединенных свойством **ProcessID** .

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
