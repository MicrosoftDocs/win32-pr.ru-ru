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
# <a name="example-getting-wmi-data-from-the-local-computer"></a>Пример. получение данных WMI с локального компьютера

Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к WMI на локальном компьютере, извлекает данные полусинхронном, а затем очищает. Этот пример возвращает имя операционной системы на локальном компьютере и отображает ее. Сведения о получении данных с удаленного компьютера см. в разделе [пример. получение данных WMI с удаленного компьютера](example--getting-wmi-data-from-a-remote-computer.md). Сведения о асинхронном получении данных см. в статье [Пример: асинхронное получение данных WMI с локального компьютера](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

Для выполнения приложения WMI используется следующая процедура. Шаги с 1 по 5 содержат все шаги, необходимые для установки и подключения к WMI, а в шагах 6 и 7 — место запроса и получения данных.

1.  Инициализируйте параметры COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).

2.  Инициализируйте безопасность процессов COM путем вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md).

3.  Получите исходный указатель WMI, вызвав [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для корневого \\ пространства имен CIMV2 на локальном компьютере, вызвав [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Сведения о подключении к удаленному компьютеру см. в разделе [пример. получение данных WMI с удаленного компьютера](example--getting-wmi-data-from-a-remote-computer.md).

    Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).

5.  Настройте безопасность прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , чтобы служба WMI могла олицетворять клиента, вызвав метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).

6.  Используйте указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для создания запросов WMI. В этом примере выполняется запрос для имени операционной системы путем вызова [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    Следующий WQL-запрос является одним из аргументов метода.

    `SELECT * FROM Win32_OperatingSystem`

    Результат этого запроса хранится в указателе [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Это позволяет получать объекты данных из запроса полусинхронном с помощью интерфейса **иенумвбемклассобжект** . Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md). Сведения о асинхронном получении данных см. в статье [Пример: асинхронное получение данных WMI с локального компьютера](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

    Дополнительные сведения о выполнении запросов к WMI см. в статьях [Управление сведениями о классах и экземплярах](manipulating-class-and-instance-information.md), [запрос WMI](querying-wmi.md)и [вызов метода](calling-a-method.md).

7.  Получение и отображение данных из WQL-запроса. Указатель [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) связан с объектами данных, возвращаемыми запросом, и объекты данных можно получить с помощью метода [**Иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) . Этот метод связывает объекты данных с указателем [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , который передается в метод. Используйте метод [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) , чтобы получить нужную информацию из объектов данных.

    Следующий пример кода используется для получения свойства Name из объекта данных, который предоставляет имя операционной системы.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    После того как значение свойства Name сохраняется в переменной [**типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) втпроп, оно может быть отображено пользователю.

    Дополнительные сведения см. в разделе [перечисление WMI](enumerating-wmi.md).

В следующем примере кода данные WMI полусинхронном извлекаются с локального компьютера.


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



 

 
