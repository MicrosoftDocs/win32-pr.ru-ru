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
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="4c70c-104">Создание нового экземпляра из старых свойств</span><span class="sxs-lookup"><span data-stu-id="4c70c-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="4c70c-105">Класс представления соединения содержит свойства из экземпляров исходного класса, которые соединены общим значением свойства, например **Class1. Prop1**  =  **class2. Prop2**.</span><span class="sxs-lookup"><span data-stu-id="4c70c-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="4c70c-106">Каждый экземпляр в классе представления join состоит из частей различных экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="4c70c-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="4c70c-107">Можно создать класс представления объединения на неравенство значений свойств, например **Class1. Prop1**  <>  **class2. Prop2** , где **Prop1** и **Prop2** не сопоставлены с одним и тем же свойством в классе представления.</span><span class="sxs-lookup"><span data-stu-id="4c70c-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="4c70c-108">Класс представления Join полезен, если искомая информация содержится в отдельных, но связанных классах.</span><span class="sxs-lookup"><span data-stu-id="4c70c-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="4c70c-109">Например, если требуется получить сведения о принтере и о конфигурации принтера, можно создать класс представления объединения, который содержит некоторые свойства класса [**\_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) и некоторые свойства класса [**\_ принтерконфигуратион Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="4c70c-110">Без поставщика представления необходимо получить и объединить свойства отдельных экземпляров, чтобы получить необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="4c70c-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="4c70c-111">В следующей процедуре описывается создание класса представления JOIN.</span><span class="sxs-lookup"><span data-stu-id="4c70c-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="4c70c-112">**Создание класса представления Join**</span><span class="sxs-lookup"><span data-stu-id="4c70c-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="4c70c-113">Начните определение класса с квалификатором строки [**жоинон**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="4c70c-114">Квалификаторы [**жоинон**](qualifiers-specific-to-the-view-provider.md), **Association** и **Union** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="4c70c-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="4c70c-115">При необходимости отфильтруйте нужные экземпляры в классе JOIN, применив квалификатор [**постжоинфилтер**](postjoinfilter-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="4c70c-116">Поставщик [**постжоинфилтер**](postjoinfilter-qualifier.md) позволяет ограничить экземпляры класса представления экземплярами, которые соответствуют определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="4c70c-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="4c70c-117">Создайте запросы, определяющие исходные экземпляры класса представления с квалификатором [**виевсаурцес**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="4c70c-118">Определите имена и расположения пространств имен, в которых находятся исходные экземпляры с квалификатором [**виевспацес**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="4c70c-119">Определите нужные свойства в классе представления JOIN с квалификатором [**пропертисаурцес**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="4c70c-120">Когда свойства добавляются в представление объединения на основе равенства, два исходных свойства должны быть сопоставлены в одном квалификаторе [**пропертисаурцес**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="4c70c-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="4c70c-121">В следующем примере кода показаны два свойства, сопоставленные в одном квалификаторе **пропертисаурцес** .</span><span class="sxs-lookup"><span data-stu-id="4c70c-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="4c70c-122">С помощью квалификатора [**хиддендефаулт**](qualifiers-specific-to-the-view-provider.md) можно пометить свойства, принадлежащие исходному классу.</span><span class="sxs-lookup"><span data-stu-id="4c70c-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="4c70c-123">В следующем примере кода показан класс представления соединения, созданный из классов поставщика монитора производительности [**Win32 \_ перфравдата \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) и [**Win32 \_ перфравдата \_ PerfProc \_**](/previous-versions//aa394325(v=vs.85)) , со свойствами обоих классов, присоединенных свойством **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="4c70c-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

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

 

 
