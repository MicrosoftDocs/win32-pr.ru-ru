---
description: Извлечение частичных экземпляров — это то, что инструментарий WMI извлекает только подмножество свойств экземпляра.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Получение части экземпляра WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263816"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Получение части экземпляра WMI

Извлечение частичных экземпляров — это то, что инструментарий WMI извлекает только подмножество свойств экземпляра. Например, Инструментарий WMI может извлекать только свойства **имени** и **ключа** . Наиболее распространенное использование извлечения с частичным экземпляром — для больших перечислений, имеющих несколько свойств.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Получение части экземпляра WMI с помощью PowerShell

Получить отдельное свойство экземпляра можно с помощью [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); само свойство можно получить и отобразить несколькими способами. Как и при извлечении экземпляра, PowerShell по умолчанию возвращает все экземпляры данного класса. необходимо указать конкретное значение, если вы хотите получить только один экземпляр.

В следующем примере кода отображается серийный номер тома для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Получение части экземпляра WMI с помощью C# (System. Management)

Можно получить отдельное свойство экземпляра, создав новый [ManagementObject](/dotnet/api/system.management.managementobject) , используя сведения о конкретном экземпляре. Затем можно неявно получить одно или несколько свойств экземпляра с помощью метода [жетпропертивалуе](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .

> [!Note]  
> **System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .

 

В следующем примере кода отображается серийный номер тома для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Получение части экземпляра WMI с помощью VBScript

Можно получить отдельное свойство экземпляра с помощью [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

В следующем примере кода отображается серийный номер тома для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Получение части экземпляра WMI с помощью C++

Следующая процедура используется для запроса получения частичного экземпляра с помощью C++.

**Запрос получения частичного экземпляра с помощью C++**

1.  Создайте объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Объект контекста — это объект, который WMI использует для передачи дополнительных сведений поставщику WMI. В этом случае вы используете объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , чтобы указать поставщику обрабатывать извлечение частичного экземпляра.

2.  Добавьте \_ \_ Get \_ Extensions, \_ \_ Get \_ \_ \_ WebRequest Client Request и любые другие именованные значения, описывающие свойства, которые необходимо получить в объекте [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .

    В следующей таблице перечислены различные именованные значения, используемые в вызове метода получения.

    

    | Именованное значение                              | Описание                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_ПОЛУЧИТЬ \_ расширения<br/>           | **VT \_ Для BOOL** задано значение **Variant \_ true**. Используется для сигнализации об использовании операций извлечения частичного экземпляра. Это позволяет быстро выполнить одну проверку без перечисления всего объекта контекста. Если используется любое из других значений, то оно должно быть.<br/> |
    | \_\_ПОЛУЧИТЬ \_ \_ Свойства ext<br/>      | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) строк, в которых перечислены извлекаемые свойства. Нельзя указывать одновременно только с \_ \_ Get \_ ext \_ Keys \_ .<br/> Звездочка " \* " является недопустимым именем свойства для \_ \_ получения \_ \_ свойств ext.<br/>                    |
    | \_\_ПОЛУЧИТЬ \_ \_ только внешние ключи \_<br/>      | **VT \_ Для BOOL** задано значение **Variant \_ true**. Указывает, что в возвращаемом объекте должны быть предоставлены только ключи. Нельзя указывать одновременно с \_ \_ Get \_ ВДЛ \_ Properties. Вместо этого имеет приоритет над \_ \_ получением \_ \_ свойств ext.<br/>                            |
    | \_\_ПОЛУЧЕНИЕ \_ \_ запроса ext Client \_<br/> | **VT \_ Для BOOL** задано значение **Variant \_ true**. Указывает, что вызывающей стороной был автор значения в объекте контекста и что он не был распространен из другой зависимой операции.<br/>                                                                        |

    

     

3.  Передайте объект контекста [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) в любые вызовы [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices:: Жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) через параметр *пкткс* .

    Передача объекта [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) дает поставщику разрешение на извлечение частичных экземпляров. При полном извлечении экземпляра необходимо задать для *пкткс* значение **null** . Если поставщик не поддерживает извлечение с частичным экземпляром, вы получите сообщение об ошибке.

Если поставщик не может выполнить операцию с частичным экземпляром, поставщик либо продолжит работу, как если бы вы не вводили Объект контекста, либо иначе возвращает **\_ \_ неподдерживаемый \_ параметр**.

В следующем примере показано, как выполнить полное получение экземпляра для [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), а затем выполняет извлечение с частичным экземпляром свойства **Win32 \_ LogicalDisk. Caption** .


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



При выполнении приведенный выше пример кода записывает следующие сведения. Первое описание объекта получено из полного экземпляра. Второе описание объекта относится к извлечению частичного экземпляра. В последнем разделе показано, что вы получаете значение **null** , если запрашиваете свойство, которое не было запрошено в исходном вызове [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

Приведенные ниже выходные данные создаются в предыдущем примере.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

