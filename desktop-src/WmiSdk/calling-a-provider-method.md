---
description: Метод поставщика — это метод, реализуемый поставщиком инструментарий управления Windows (WMI) (WMI).
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Вызов метода поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702674"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="a29ec-103">Вызов метода поставщика</span><span class="sxs-lookup"><span data-stu-id="a29ec-103">Calling a Provider Method</span></span>

<span data-ttu-id="a29ec-104">Метод поставщика — это метод, реализуемый поставщиком инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a29ec-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="a29ec-105">Метод находится в классе, определенном поставщиком, для представления данных от программного или аппаратного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a29ec-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="a29ec-106">Например, класс [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) имеет методы для запуска, остановки, возобновления, приостановки и изменения служб.</span><span class="sxs-lookup"><span data-stu-id="a29ec-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="a29ec-107">Методы поставщика не следует путать со следующими типами методов:</span><span class="sxs-lookup"><span data-stu-id="a29ec-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="a29ec-108">Методы в [системных классах инструментария WMI](wmi-system-classes.md), например метод, который [**получается**](--systemsecurity-getsd.md) в [**\_ \_ системсекурити**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="a29ec-109">Методы для объектов в [API скриптов для WMI](scripting-api-for-wmi.md), например [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="a29ec-110">Методы в [API COM для WMI](com-api-for-wmi.md), например [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="a29ec-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="a29ec-111">Вызов метода поставщика с помощью сценария</span><span class="sxs-lookup"><span data-stu-id="a29ec-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="a29ec-112">Любой язык автоматизации, такой как VBScript, PowerShell или Perl, может вызывать метод WMI.</span><span class="sxs-lookup"><span data-stu-id="a29ec-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="a29ec-113">Некоторые языки могут использовать [прямой доступ](/windows), но для непрямого выполнения метода поставщика другие должны использовать [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="a29ec-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="a29ec-114">В следующей процедуре описывается вызов метода поставщика с помощью API скриптов и использование прямого доступа.</span><span class="sxs-lookup"><span data-stu-id="a29ec-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="a29ec-115">**Вызов метода поставщика с помощью API скриптов и прямого доступа**</span><span class="sxs-lookup"><span data-stu-id="a29ec-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="a29ec-116">Используйте этот подход для VBScript или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a29ec-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="a29ec-117">Определите, реализован ли метод, который требуется выполнить.</span><span class="sxs-lookup"><span data-stu-id="a29ec-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="a29ec-118">Некоторые классы имеют определенные методы, которые не поддерживаются поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a29ec-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="a29ec-119">Если метод не реализован, его нельзя выполнить.</span><span class="sxs-lookup"><span data-stu-id="a29ec-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="a29ec-120">Определить, реализован ли метод, можно, проверив, имеет ли метод [**реализованный**](standard-wmi-qualifiers.md) квалификатор.</span><span class="sxs-lookup"><span data-stu-id="a29ec-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="a29ec-121">Дополнительные сведения см. в статьях [квалификаторы WMI](wmi-qualifiers.md) и [доступ к квалификатору WMI](accessing-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="a29ec-122">Можно также определить, имеет ли метод класса поставщика **реализованный** квалификатор, запустив неподдерживаемую Wbemtest.exe служебную программу, доступную в любой операционной системе с УСТАНОВЛЕНным инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a29ec-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="a29ec-123">Определите, является ли метод, который требуется выполнить, [*статическим методом*](gloss-s.md) или нестатическим методом.</span><span class="sxs-lookup"><span data-stu-id="a29ec-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="a29ec-124">Статические методы применяются только к классам WMI, а не к отдельным экземплярам класса.</span><span class="sxs-lookup"><span data-stu-id="a29ec-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="a29ec-125">Например, метод [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) является статическим методом, поскольку он используется для создания нового процесса без экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="a29ec-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="a29ec-126">Нестатические методы применяются только к экземплярам класса.</span><span class="sxs-lookup"><span data-stu-id="a29ec-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="a29ec-127">Например, метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) класса **\_ процесса Win32** является нестатическим методом, поскольку имеет смысл завершить процесс только в том случае, если экземпляр этого процесса существует.</span><span class="sxs-lookup"><span data-stu-id="a29ec-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="a29ec-128">Можно определить, является ли метод статическим, путем проверки, связан ли с методом [**статический**](standard-wmi-qualifiers.md) квалификатор.</span><span class="sxs-lookup"><span data-stu-id="a29ec-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="a29ec-129">Получите класс или экземпляр, содержащий метод, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="a29ec-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="a29ec-130">Дополнительные сведения см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="a29ec-131">Настройте параметры безопасности, которые может требовать метод.</span><span class="sxs-lookup"><span data-stu-id="a29ec-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="a29ec-132">Вы часто можете определить привилегии, необходимые методу, изучив значения в квалификаторе [**привилегий**](swbemsecurity-privileges.md) метода.</span><span class="sxs-lookup"><span data-stu-id="a29ec-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="a29ec-133">Например, для метода [**завершения работы**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) класса [**Win32 без \_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) системы требуется задать привилегию "сешутдовнпривилеже".</span><span class="sxs-lookup"><span data-stu-id="a29ec-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="a29ec-134">Дополнительные сведения см. в разделе [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="a29ec-135">Вызовите метод и проверьте возвращаемое значение, чтобы определить, успешно ли был выполнен метод.</span><span class="sxs-lookup"><span data-stu-id="a29ec-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="a29ec-136">Следующий пример кода создает процесс блокнота и получает идентификатор процесса с помощью прямого доступа.</span><span class="sxs-lookup"><span data-stu-id="a29ec-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="a29ec-137">В следующей процедуре описывается вызов метода поставщика с помощью API скриптов и [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="a29ec-138">**Вызов метода поставщика с помощью API скриптов и SWbemServices.ExeКмесод**</span><span class="sxs-lookup"><span data-stu-id="a29ec-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="a29ec-139">Получите определение класса WMI для выполнения статического метода.</span><span class="sxs-lookup"><span data-stu-id="a29ec-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="a29ec-140">Получите экземпляр класса WMI для выполнения нестатического метода.</span><span class="sxs-lookup"><span data-stu-id="a29ec-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="a29ec-141">Извлеките метод для выполнения из коллекции [**SWbemObject. Methods \_**](swbemobject-methods-.md) класса или экземпляра с помощью метода [**SWbemObjectSet. Item**](swbemobjectset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="a29ec-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="a29ec-142">Получите объект [**параметров**](swbemmethod-inparameters.md) для метода и настройте параметры, как описано в разделе [Создание объектов с параметрами](constructing-inparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="a29ec-143">Вызовите метод **SWbemServices.Exeкмесод** , чтобы выполнить и присвоить возвращаемое значение объекту [**SWbemObject**](swbemobject.md) для хранения выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="a29ec-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="a29ec-144">Проверьте значения в объекте выходных параметров, чтобы убедиться, что метод выполнен правильно.</span><span class="sxs-lookup"><span data-stu-id="a29ec-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="a29ec-145">Следующий пример кода VBScript выполняет ту же операцию, что и предыдущий скрипт, с помощью непрямого подхода, вызывая [**SWBemServices.Exeкмесод**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="a29ec-146">В следующей процедуре описывается вызов метода поставщика с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="a29ec-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="a29ec-147">**Вызов метода поставщика с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="a29ec-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="a29ec-148">Подключитесь к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="a29ec-148">Connect to WMI.</span></span>

    <span data-ttu-id="a29ec-149">Для вызова метода в WMI сначала необходимо иметь рабочее соединение с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="a29ec-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="a29ec-150">Дополнительные сведения см. в статьях [Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md) и [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="a29ec-151">В следующем примере показано, как подключиться к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="a29ec-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="a29ec-152">Дополнительные сведения о проблемах безопасности в вызовах поставщика WMI см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="a29ec-153">Вызовите функцию [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) , чтобы получить определение класса метода, который необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="a29ec-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="a29ec-154">Метод [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) возвращает указатель [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , указывающий на определение класса.</span><span class="sxs-lookup"><span data-stu-id="a29ec-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="a29ec-155">Для методов, требующих входных параметров, вызовите метод [**ивбемклассобжект::**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) GetObject, чтобы получить объект класса входного параметра.</span><span class="sxs-lookup"><span data-stu-id="a29ec-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="a29ec-156">[**Метод WebMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) возвращает указатель [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , указывающий на класс входного параметра.</span><span class="sxs-lookup"><span data-stu-id="a29ec-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="a29ec-157">Создайте экземпляр класса входного параметра, вызвав метод [**ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="a29ec-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="a29ec-158">Задайте свойства класса входного параметра, вызвав метод [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="a29ec-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="a29ec-159">Вызовите метод с помощью вызова [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) или [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="a29ec-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="a29ec-160">Для метода [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)Инструментарий WMI возвращает все выходные параметры в вызове.</span><span class="sxs-lookup"><span data-stu-id="a29ec-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="a29ec-161">Для [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)Инструментарий WMI возвращает выходные параметры через вызов [**ивбемобжектсинк**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="a29ec-162">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a29ec-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="a29ec-163">Следующий код является полным примером вызова метода поставщика.</span><span class="sxs-lookup"><span data-stu-id="a29ec-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="a29ec-164">См. также</span><span class="sxs-lookup"><span data-stu-id="a29ec-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a29ec-165">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="a29ec-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
