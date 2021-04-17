---
description: Квалификатор — это тег, предоставляющий дополнительные сведения об объекте WMI, методе или свойстве.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Доступ к квалификатору WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703008"
---
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="3ab51-103">Доступ к квалификатору WMI</span><span class="sxs-lookup"><span data-stu-id="3ab51-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="3ab51-104">Квалификатор — это тег, предоставляющий дополнительные сведения об объекте WMI, методе или свойстве.</span><span class="sxs-lookup"><span data-stu-id="3ab51-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="3ab51-105">Иногда может потребоваться доступ к данным, хранящимся в квалификаторе.</span><span class="sxs-lookup"><span data-stu-id="3ab51-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="3ab51-106">Например, Общая задача заключается в том, чтобы определить, реализует ли поставщик метод, выполнив попытку получить **реализованный** квалификатор для этого метода.</span><span class="sxs-lookup"><span data-stu-id="3ab51-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="3ab51-107">Дополнительные сведения см. в разделе [квалификаторы WMI](wmi-qualifiers.md) и [Добавление квалификатора](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="3ab51-108">Чтобы получить квалификаторы для объекта WMI в PowerShell, сначала нужно получить объект, а затем проверить квалификаторы так же, как любое другое свойство.</span><span class="sxs-lookup"><span data-stu-id="3ab51-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="3ab51-109">**Извлечение квалификатора с помощью PowerShell**</span><span class="sxs-lookup"><span data-stu-id="3ab51-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="3ab51-110">Получите объект, квалификаторы которого необходимо просмотреть с помощью [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), а затем получите доступ к квалификаторам через свойство **Квалификаторы** :</span><span class="sxs-lookup"><span data-stu-id="3ab51-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    <span data-ttu-id="3ab51-111">Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="3ab51-112">Чтобы получить квалификаторы на экземпляре WMI в C#, сначала нужно получить объект, а затем изучить квалификаторы как коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3ab51-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="3ab51-113">**Извлечение квалификатора с помощью C# (Microsoft.SysTEM. MMC**</span><span class="sxs-lookup"><span data-stu-id="3ab51-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="3ab51-114">Получите класс, квалификаторы которого нужно просмотреть, создав объект CimInstance с использованием указанного имени класса и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3ab51-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="3ab51-115">Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="3ab51-116">Можно получить квалификаторы класса из [ciminstance. Цимкласс. Цимкласскуалифиерс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), квалификаторы свойств из [ciminstance. Цимкласс. Цимкласспропертиес](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))и квалификаторы методов из [ciminstance. Цимкласс. Цимклассмесодс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ab51-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    <span data-ttu-id="3ab51-117">Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="3ab51-118">Чтобы получить квалификаторы для объекта WMI в C#, сначала нужно получить объект, а затем изучить квалификаторы как коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3ab51-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="3ab51-119">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="3ab51-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="3ab51-120">**Извлечение квалификатора с помощью C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="3ab51-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="3ab51-121">Получите объект, квалификаторы которого необходимо просмотреть с помощью [ManagementObject](/dotnet/api/system.management.managementobject).</span><span class="sxs-lookup"><span data-stu-id="3ab51-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="3ab51-122">Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="3ab51-123">Поместите квалификаторы в [куалифиердатаколлектион](/dotnet/api/system.management.qualifierdatacollection)и перечислите значения [куалифиердата](/dotnet/api/system.management.qualifierdata) .</span><span class="sxs-lookup"><span data-stu-id="3ab51-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="3ab51-124">Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="3ab51-125">Следующая процедура описывает, как получить квалификатор с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="3ab51-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="3ab51-126">**Извлечение квалификатора с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="3ab51-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="3ab51-127">Получите объект, квалификаторы которого необходимо просмотреть, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="3ab51-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="3ab51-128">Наиболее распространенным способом извлечения объекта является использование метода [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="3ab51-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="3ab51-129">Дополнительные сведения см. [в разделе Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="3ab51-130">Доступ к квалификаторам объекта осуществляется через свойство [**SWbemObject. квалификаторы \_**](swbemobject-qualifiers-.md) , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="3ab51-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="3ab51-131">В следующем примере кода показано, как получить доступ ко всем квалификаторам объекта [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="3ab51-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="3ab51-132">В следующей процедуре описывается извлечение квалификатора с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="3ab51-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="3ab51-133">**Извлечение квалификатора с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="3ab51-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="3ab51-134">Получите объект, квалификаторы которого необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="3ab51-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="3ab51-135">Наиболее распространенным способом извлечения объекта является использование вызова [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="3ab51-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="3ab51-136">Дополнительные сведения см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="3ab51-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="3ab51-137">Получение квалификатора, заданного для данного свойства, с вызовом методов [**ивбемклассобжект:: жетпропертикуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) или [**Ивбемклассобжект:: жетмесодкуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="3ab51-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="3ab51-138">Доступ к квалификаторам объекта осуществляется через возвращенный интерфейс [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="3ab51-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="3ab51-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="3ab51-139">Examples</span></span>

<span data-ttu-id="3ab51-140">Дополнительные сведения о получении квалификаторов см. в примере кода PowerShell [Get-вмиклассмесодсандвритаблевмипропертиес](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) в коллекции TechNet.</span><span class="sxs-lookup"><span data-stu-id="3ab51-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 
