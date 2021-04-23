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
# <a name="retrieving-part-of-a-wmi-instance"></a><span data-ttu-id="86ed4-103">Получение части экземпляра WMI</span><span class="sxs-lookup"><span data-stu-id="86ed4-103">Retrieving Part of a WMI Instance</span></span>

<span data-ttu-id="86ed4-104">Извлечение частичных экземпляров — это то, что инструментарий WMI извлекает только подмножество свойств экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86ed4-104">A partial-instance retrieval is when WMI retrieves only a subset of the properties of an instance.</span></span> <span data-ttu-id="86ed4-105">Например, Инструментарий WMI может извлекать только свойства **имени** и **ключа** .</span><span class="sxs-lookup"><span data-stu-id="86ed4-105">For example, WMI could retrieve only the **Name** and **Key** properties.</span></span> <span data-ttu-id="86ed4-106">Наиболее распространенное использование извлечения с частичным экземпляром — для больших перечислений, имеющих несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="86ed4-106">The most common use of partial-instance retrieval is on large enumerations that have multiple properties.</span></span>

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a><span data-ttu-id="86ed4-107">Получение части экземпляра WMI с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="86ed4-107">Retrieving Part of a WMI Instance Using PowerShell</span></span>

<span data-ttu-id="86ed4-108">Получить отдельное свойство экземпляра можно с помощью [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); само свойство можно получить и отобразить несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="86ed4-108">You can retrieve an individual property of an instance by using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); the property itself can be retrieved and displayed a number of ways.</span></span> <span data-ttu-id="86ed4-109">Как и при извлечении экземпляра, PowerShell по умолчанию возвращает все экземпляры данного класса. необходимо указать конкретное значение, если вы хотите получить только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="86ed4-109">As with retrieving an instance, PowerShell will by default return all instances of a given class; you must specify a specific value if you wish to retrieve only a single instance.</span></span>

<span data-ttu-id="86ed4-110">В следующем примере кода отображается серийный номер тома для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="86ed4-110">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a><span data-ttu-id="86ed4-111">Получение части экземпляра WMI с помощью C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="86ed4-111">Retrieving Part of a WMI Instance Using C# (System.Management)</span></span>

<span data-ttu-id="86ed4-112">Можно получить отдельное свойство экземпляра, создав новый [ManagementObject](/dotnet/api/system.management.managementobject) , используя сведения о конкретном экземпляре.</span><span class="sxs-lookup"><span data-stu-id="86ed4-112">You can retrieve an individual property of an instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject) using the details of a specific instance.</span></span> <span data-ttu-id="86ed4-113">Затем можно неявно получить одно или несколько свойств экземпляра с помощью метода [жетпропертивалуе](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .</span><span class="sxs-lookup"><span data-stu-id="86ed4-113">You can then implicitly retrieve one or more properties of the instance with the [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) method.</span></span>

> [!Note]  
> <span data-ttu-id="86ed4-114">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="86ed4-114">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="86ed4-115">В следующем примере кода отображается серийный номер тома для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="86ed4-115">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a><span data-ttu-id="86ed4-116">Получение части экземпляра WMI с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="86ed4-116">Retrieving Part of a WMI Instance Using VBScript</span></span>

<span data-ttu-id="86ed4-117">Можно получить отдельное свойство экземпляра с помощью [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="86ed4-117">You can retrieve an individual property of an instance by using [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="86ed4-118">В следующем примере кода отображается серийный номер тома для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="86ed4-118">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a><span data-ttu-id="86ed4-119">Получение части экземпляра WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="86ed4-119">Retrieving Part of a WMI Instance Using C++</span></span>

<span data-ttu-id="86ed4-120">Следующая процедура используется для запроса получения частичного экземпляра с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="86ed4-120">The following procedure is used to request a partial-instance retrieval using C++.</span></span>

<span data-ttu-id="86ed4-121">**Запрос получения частичного экземпляра с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="86ed4-121">**To request a partial-instance retrieval using C++**</span></span>

1.  <span data-ttu-id="86ed4-122">Создайте объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="86ed4-122">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="86ed4-123">Объект контекста — это объект, который WMI использует для передачи дополнительных сведений поставщику WMI.</span><span class="sxs-lookup"><span data-stu-id="86ed4-123">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="86ed4-124">В этом случае вы используете объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , чтобы указать поставщику обрабатывать извлечение частичного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86ed4-124">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to process a partial-instance retrieval.</span></span>

2.  <span data-ttu-id="86ed4-125">Добавьте \_ \_ Get \_ Extensions, \_ \_ Get \_ \_ \_ WebRequest Client Request и любые другие именованные значения, описывающие свойства, которые необходимо получить в объекте [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="86ed4-125">Add \_\_GET\_EXTENSIONS, \_\_GET\_EXT\_CLIENT\_REQUEST, and any other named values that describe the properties you want to retrieve to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object.</span></span>

    <span data-ttu-id="86ed4-126">В следующей таблице перечислены различные именованные значения, используемые в вызове метода получения.</span><span class="sxs-lookup"><span data-stu-id="86ed4-126">The following table lists the different named values use in your retrieval call.</span></span>

    

    | <span data-ttu-id="86ed4-127">Именованное значение</span><span class="sxs-lookup"><span data-stu-id="86ed4-127">Named value</span></span>                              | <span data-ttu-id="86ed4-128">Описание</span><span class="sxs-lookup"><span data-stu-id="86ed4-128">Description</span></span>                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="86ed4-129">\_\_ПОЛУЧИТЬ \_ расширения</span><span class="sxs-lookup"><span data-stu-id="86ed4-129">\_\_GET\_EXTENSIONS</span></span><br/>           | <span data-ttu-id="86ed4-130">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="86ed4-130">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="86ed4-131">Используется для сигнализации об использовании операций извлечения частичного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86ed4-131">Used to signal that partial-instance retrieval operations are being used.</span></span> <span data-ttu-id="86ed4-132">Это позволяет быстро выполнить одну проверку без перечисления всего объекта контекста.</span><span class="sxs-lookup"><span data-stu-id="86ed4-132">This allows a quick, single check without having to enumerate the entire context object.</span></span> <span data-ttu-id="86ed4-133">Если используется любое из других значений, то оно должно быть.</span><span class="sxs-lookup"><span data-stu-id="86ed4-133">If any of the other values are used, this one must be.</span></span><br/> |
    | <span data-ttu-id="86ed4-134">\_\_ПОЛУЧИТЬ \_ \_ Свойства ext</span><span class="sxs-lookup"><span data-stu-id="86ed4-134">\_\_GET\_EXT\_PROPERTIES</span></span><br/>      | <span data-ttu-id="86ed4-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) строк, в которых перечислены извлекаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="86ed4-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings listing the properties to be retrieved.</span></span> <span data-ttu-id="86ed4-136">Нельзя указывать одновременно только с \_ \_ Get \_ ext \_ Keys \_ .</span><span class="sxs-lookup"><span data-stu-id="86ed4-136">Cannot be simultaneously specified with \_\_GET\_EXT\_KEYS\_ONLY.</span></span><br/> <span data-ttu-id="86ed4-137">Звездочка " \* " является недопустимым именем свойства для \_ \_ получения \_ \_ свойств ext.</span><span class="sxs-lookup"><span data-stu-id="86ed4-137">An asterisk "\*" is an invalid property name for \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                    |
    | <span data-ttu-id="86ed4-138">\_\_ПОЛУЧИТЬ \_ \_ только внешние ключи \_</span><span class="sxs-lookup"><span data-stu-id="86ed4-138">\_\_GET\_EXT\_KEYS\_ONLY</span></span><br/>      | <span data-ttu-id="86ed4-139">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="86ed4-139">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="86ed4-140">Указывает, что в возвращаемом объекте должны быть предоставлены только ключи.</span><span class="sxs-lookup"><span data-stu-id="86ed4-140">Indicates that only keys should be provided in the returned object.</span></span> <span data-ttu-id="86ed4-141">Нельзя указывать одновременно с \_ \_ Get \_ ВДЛ \_ Properties.</span><span class="sxs-lookup"><span data-stu-id="86ed4-141">Cannot be simultaneously specified with \_\_GET\_EXT\_PROPERTIES.</span></span> <span data-ttu-id="86ed4-142">Вместо этого имеет приоритет над \_ \_ получением \_ \_ свойств ext.</span><span class="sxs-lookup"><span data-stu-id="86ed4-142">Instead, takes precedence over \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                            |
    | <span data-ttu-id="86ed4-143">\_\_ПОЛУЧЕНИЕ \_ \_ запроса ext Client \_</span><span class="sxs-lookup"><span data-stu-id="86ed4-143">\_\_GET\_EXT\_CLIENT\_REQUEST</span></span><br/> | <span data-ttu-id="86ed4-144">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="86ed4-144">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="86ed4-145">Указывает, что вызывающей стороной был автор значения в объекте контекста и что он не был распространен из другой зависимой операции.</span><span class="sxs-lookup"><span data-stu-id="86ed4-145">Indicates that the caller was the one who wrote the value into the context object and that it was not propagated from another dependent operation.</span></span><br/>                                                                        |

    

     

3.  <span data-ttu-id="86ed4-146">Передайте объект контекста [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) в любые вызовы [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices:: Жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) через параметр *пкткс* .</span><span class="sxs-lookup"><span data-stu-id="86ed4-146">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) through the *pCtx* parameter.</span></span>

    <span data-ttu-id="86ed4-147">Передача объекта [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) дает поставщику разрешение на извлечение частичных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="86ed4-147">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance retrievals.</span></span> <span data-ttu-id="86ed4-148">При полном извлечении экземпляра необходимо задать для *пкткс* значение **null** .</span><span class="sxs-lookup"><span data-stu-id="86ed4-148">In a full-instance retrieval, you would set *pCtx* to a **null** value.</span></span> <span data-ttu-id="86ed4-149">Если поставщик не поддерживает извлечение с частичным экземпляром, вы получите сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="86ed4-149">If the provider does not support partial-instance retrieval, you will receive an error message.</span></span>

<span data-ttu-id="86ed4-150">Если поставщик не может выполнить операцию с частичным экземпляром, поставщик либо продолжит работу, как если бы вы не вводили Объект контекста, либо иначе возвращает **\_ \_ неподдерживаемый \_ параметр**.</span><span class="sxs-lookup"><span data-stu-id="86ed4-150">If the provider cannot comply with the partial-instance operation, the provider either proceeds as if you did not enter the context object, or else returns **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="86ed4-151">В следующем примере показано, как выполнить полное получение экземпляра для [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), а затем выполняет извлечение с частичным экземпляром свойства **Win32 \_ LogicalDisk. Caption** .</span><span class="sxs-lookup"><span data-stu-id="86ed4-151">The following example describes how to perform a full instance retrieval of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), and then performs a partial-instance retrieval of the **Win32\_LogicalDisk.Caption** property.</span></span>


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



<span data-ttu-id="86ed4-152">При выполнении приведенный выше пример кода записывает следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="86ed4-152">When executed, the previous code example writes the following information.</span></span> <span data-ttu-id="86ed4-153">Первое описание объекта получено из полного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86ed4-153">The first object description is from the full-instance retrieval.</span></span> <span data-ttu-id="86ed4-154">Второе описание объекта относится к извлечению частичного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86ed4-154">The second object description is from the partial-instance retrieval.</span></span> <span data-ttu-id="86ed4-155">В последнем разделе показано, что вы получаете значение **null** , если запрашиваете свойство, которое не было запрошено в исходном вызове [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="86ed4-155">The last section shows that you receive a **null** value if you request a property that was not requested in the original [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) call.</span></span>

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

<span data-ttu-id="86ed4-156">Приведенные ниже выходные данные создаются в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="86ed4-156">The following output is generated by the previous example.</span></span>

``` syntax
file system variable is null - expected
Press any key to continue
```

 

