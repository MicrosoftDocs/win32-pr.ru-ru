---
description: метод поставщика — это метод, реализуемый поставщиком инструментарий управления Windows (WMI) (WMI).
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Вызов метода поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760f014c992e5cb774125db02bcb43b3df64c6622a62c0db1b97e02b393bb175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109452"
---
# <a name="calling-a-provider-method"></a>Вызов метода поставщика

метод поставщика — это метод, реализуемый поставщиком инструментарий управления Windows (WMI) (WMI). Метод находится в классе, определенном поставщиком, для представления данных от программного или аппаратного обеспечения. Например, класс [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) имеет методы для запуска, остановки, возобновления, приостановки и изменения служб.

Методы поставщика не следует путать со следующими типами методов:

-   Методы в [системных классах инструментария WMI](wmi-system-classes.md), например метод, который [**получается**](--systemsecurity-getsd.md) в [**\_ \_ системсекурити**](--systemsecurity.md).
-   Методы для объектов в [API скриптов для WMI](scripting-api-for-wmi.md), например [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md).
-   Методы в [API COM для WMI](com-api-for-wmi.md), например [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

## <a name="calling-a-provider-method-using-scripting"></a>Вызов метода поставщика с помощью сценария

Любой язык автоматизации, такой как VBScript, PowerShell или Perl, может вызывать метод WMI. Некоторые языки могут использовать [прямой доступ](/windows), но для непрямого выполнения метода поставщика другие должны использовать [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md) .

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

В следующей процедуре описывается вызов метода поставщика с помощью API скриптов и использование прямого доступа.

**Вызов метода поставщика с помощью API скриптов и прямого доступа**

1.  Используйте этот подход для VBScript или PowerShell.
2.  Определите, реализован ли метод, который требуется выполнить.

    Некоторые классы имеют определенные методы, которые не поддерживаются поставщиком. Если метод не реализован, его нельзя выполнить. Определить, реализован ли метод, можно, проверив, имеет ли метод [**реализованный**](standard-wmi-qualifiers.md) квалификатор. Дополнительные сведения см. в статьях [квалификаторы WMI](wmi-qualifiers.md) и [доступ к квалификатору WMI](accessing-a-qualifier.md). Можно также определить, имеет ли метод класса поставщика **реализованный** квалификатор, запустив неподдерживаемую Wbemtest.exe служебную программу, доступную в любой операционной системе с УСТАНОВЛЕНным инструментарием WMI.

3.  Определите, является ли метод, который требуется выполнить, [*статическим методом*](gloss-s.md) или нестатическим методом.

    Статические методы применяются только к классам WMI, а не к отдельным экземплярам класса. Например, метод [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) является статическим методом, поскольку он используется для создания нового процесса без экземпляра этого класса. Нестатические методы применяются только к экземплярам класса. Например, метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) класса **\_ процесса Win32** является нестатическим методом, поскольку имеет смысл завершить процесс только в том случае, если экземпляр этого процесса существует. Можно определить, является ли метод статическим, путем проверки, связан ли с методом [**статический**](standard-wmi-qualifiers.md) квалификатор.

4.  Получите класс или экземпляр, содержащий метод, который необходимо выполнить.

    Дополнительные сведения см. в разделе [Получение данных класса или экземпляра WMI](retrieving-class-or-instance-data.md).

5.  Настройте параметры безопасности, которые может требовать метод.

    Вы часто можете определить привилегии, необходимые методу, изучив значения в квалификаторе [**привилегий**](swbemsecurity-privileges.md) метода. Например, для метода [**завершения работы**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) класса [**Win32 без \_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) системы требуется задать привилегию "сешутдовнпривилеже". Дополнительные сведения см. в разделе [выполнение привилегированных операций](executing-privileged-operations.md).

6.  Вызовите метод и проверьте возвращаемое значение, чтобы определить, успешно ли был выполнен метод.

в следующем примере кода создается процесс Блокнот и получается идентификатор процесса с помощью прямого доступа.


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

В следующей процедуре описывается вызов метода поставщика с помощью API скриптов и [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md).

**Вызов метода поставщика с помощью API скриптов и SWbemServices.ExeКмесод**

1.  Получите определение класса WMI для выполнения статического метода. Получите экземпляр класса WMI для выполнения нестатического метода.
2.  Извлеките метод для выполнения из коллекции [**SWbemObject. Methods \_**](swbemobject-methods-.md) класса или экземпляра с помощью метода [**SWbemObjectSet. Item**](swbemobjectset-item.md) .
3.  Получите объект [**параметров**](swbemmethod-inparameters.md) для метода и настройте параметры, как описано в разделе [Создание объектов с параметрами](constructing-inparameters-objects.md).
4.  Вызовите метод **SWbemServices.Exeкмесод** , чтобы выполнить и присвоить возвращаемое значение объекту [**SWbemObject**](swbemobject.md) для хранения выходных параметров.
5.  Проверьте значения в объекте выходных параметров, чтобы убедиться, что метод выполнен правильно.

Следующий пример кода VBScript выполняет ту же операцию, что и предыдущий скрипт, с помощью непрямого подхода, вызывая [**SWBemServices.Exeкмесод**](swbemservices-execmethod.md).


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




В следующей процедуре описывается вызов метода поставщика с помощью C++.

**Вызов метода поставщика с помощью C++**

1.  Подключение WMI.

    Для вызова метода в WMI сначала необходимо иметь рабочее соединение с пространством имен WMI. Дополнительные сведения см. в статьях [Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md) и [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).

    В следующем примере показано, как подключиться к инструментарию WMI. Дополнительные сведения о проблемах безопасности в вызовах поставщика WMI см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).

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

    

2.  Вызовите функцию [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) , чтобы получить определение класса метода, который необходимо вызвать.

    Метод [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) возвращает указатель [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , указывающий на определение класса.

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  Для методов, требующих входных параметров, вызовите метод [**ивбемклассобжект::**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) GetObject, чтобы получить объект класса входного параметра.

    [**Метод WebMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) возвращает указатель [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , указывающий на класс входного параметра.

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  Создайте экземпляр класса входного параметра, вызвав метод [**ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  Задайте свойства класса входного параметра, вызвав метод [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  Вызовите метод с помощью вызова [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) или [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).

    Для метода [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)Инструментарий WMI возвращает все выходные параметры в вызове. Для [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)Инструментарий WMI возвращает выходные параметры через вызов [**ивбемобжектсинк**](iwbemobjectsink.md). Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

Следующий код является полным примером вызова метода поставщика.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

 
