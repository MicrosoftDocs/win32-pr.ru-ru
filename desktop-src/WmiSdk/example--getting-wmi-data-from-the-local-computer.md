---
description: Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, извлекает данные полусинхронном, а затем очищает.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: Пример. получение данных WMI с локального компьютера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840cd4ada941bdfd8ba7fca9b8ca9393c0b5eb55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898786"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a><span data-ttu-id="99efd-103">Пример. получение данных WMI с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="99efd-103">Example: Getting WMI Data from the Local Computer</span></span>

<span data-ttu-id="99efd-104">Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, извлекает данные полусинхронном, а затем очищает.</span><span class="sxs-lookup"><span data-stu-id="99efd-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, retrieves data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="99efd-105">Этот пример возвращает имя операционной системы на локальном компьютере и отображает ее.</span><span class="sxs-lookup"><span data-stu-id="99efd-105">This example gets the name of the operating system on the local computer and displays it.</span></span> <span data-ttu-id="99efd-106">Сведения о получении данных с удаленного компьютера см. в разделе [пример. получение данных WMI с удаленного компьютера](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-106">To retrieve data from a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="99efd-107">Сведения о асинхронном получении данных см. в статье [Пример: асинхронное получение данных WMI с локального компьютера](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-107">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

<span data-ttu-id="99efd-108">Для выполнения приложения WMI используется следующая процедура.</span><span class="sxs-lookup"><span data-stu-id="99efd-108">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="99efd-109">Шаги с 1 по 5 содержат все шаги, необходимые для установки и подключения к WMI, а в шагах 6 и 7 — место запроса и получения данных.</span><span class="sxs-lookup"><span data-stu-id="99efd-109">Steps 1 through 5 contain all the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

1.  <span data-ttu-id="99efd-110">Инициализируйте параметры COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="99efd-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="99efd-111">Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-111">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="99efd-112">Инициализируйте безопасность процессов COM путем вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="99efd-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="99efd-113">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="99efd-114">Получите исходный указатель WMI, вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="99efd-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="99efd-115">Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="99efd-116">Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для корневого \\ пространства имен CIMV2 на локальном компьютере, вызвав [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="99efd-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="99efd-117">Сведения о подключении к удаленному компьютеру см. в разделе [пример. получение данных WMI с удаленного компьютера](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="99efd-118">Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="99efd-119">Настройте безопасность прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , чтобы служба WMI могла олицетворять клиента, вызвав метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="99efd-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="99efd-120">Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="99efd-121">Используйте указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для создания запросов WMI.</span><span class="sxs-lookup"><span data-stu-id="99efd-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="99efd-122">В этом примере выполняется запрос для имени операционной системы путем вызова [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="99efd-122">This example executes a query for the name of the operating system by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="99efd-123">Следующий WQL-запрос является одним из аргументов метода.</span><span class="sxs-lookup"><span data-stu-id="99efd-123">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="99efd-124">Результат этого запроса хранится в указателе [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="99efd-124">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="99efd-125">Это позволяет получать объекты данных из запроса полусинхронном с помощью интерфейса **иенумвбемклассобжект** .</span><span class="sxs-lookup"><span data-stu-id="99efd-125">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="99efd-126">Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-126">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="99efd-127">Сведения о асинхронном получении данных см. в статье [Пример: асинхронное получение данных WMI с локального компьютера](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-127">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="99efd-128">Дополнительные сведения о выполнении запросов к WMI см. в статьях [Управление сведениями о классах и экземплярах](manipulating-class-and-instance-information.md), [запрос WMI](querying-wmi.md)и [вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-128">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="99efd-129">Получение и отображение данных из WQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="99efd-129">Get and display the data from the WQL query.</span></span> <span data-ttu-id="99efd-130">Указатель [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) связан с объектами данных, возвращаемыми запросом, и объекты данных можно получить с помощью метода [**Иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="99efd-130">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="99efd-131">Этот метод связывает объекты данных с указателем [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , который передается в метод.</span><span class="sxs-lookup"><span data-stu-id="99efd-131">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="99efd-132">Используйте метод [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) , чтобы получить нужную информацию из объектов данных.</span><span class="sxs-lookup"><span data-stu-id="99efd-132">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="99efd-133">Следующий пример кода используется для получения свойства Name из объекта данных, который предоставляет имя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="99efd-133">The following code example is used to get the Name property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    <span data-ttu-id="99efd-134">После того как значение свойства Name сохраняется в переменной [**типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) втпроп, оно может быть отображено пользователю.</span><span class="sxs-lookup"><span data-stu-id="99efd-134">After the value of the Name property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable vtProp, it can then be displayed to the user.</span></span>

    <span data-ttu-id="99efd-135">Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="99efd-135">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="99efd-136">В следующем примере кода данные WMI полусинхронном извлекаются с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="99efd-136">The following code example retrieves WMI data semisynchronously from a local computer.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



 

 
