---
description: Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к инструментарию WMI на локальном компьютере, считывает некоторые данные и очищает.
ms.assetid: d80bcf9f-e57c-499f-b7b8-cf25678c5a82
ms.tgt_platform: multiple
title: Пример. Создание приложения WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e7633c666beb900da4cdbe41909880d9766c903be0fc8b6aa1d4e45be8d90f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319313"
---
# <a name="example-creating-a-wmi-application"></a>Пример. Создание приложения WMI

Вы можете использовать процедуры и примеры кода в этом разделе, чтобы создать полное клиентское приложение WMI, которое выполняет инициализацию COM, подключается к инструментарию WMI на локальном компьютере, считывает некоторые данные и очищает. [Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md) описывает получение данных с удаленных компьютеров.

Следующая процедура включает все шаги, необходимые для всех приложений WMI C++.

1.  Инициализируйте параметры COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Дополнительные сведения см. в разделе [Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).

2.  Инициализируйте безопасность процессов COM путем вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md).

3.  Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для пространства имен на указанном главном компьютере — локальный компьютер в простом случае — путем вызова [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

    Чтобы подключиться к удаленному компьютеру, например компьютер \_ а, используйте следующий параметр пути объекта:

    ```C++
    _bstr_t(L"\\COMPUTER_A\ROOT\\CIMV2")
    ```

    

    Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Задайте безопасность прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , чтобы служба WMI могла олицетворять клиента, вызвав метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).

5.  Используйте указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для создания запросов WMI. Например, можно запросить все экземпляры [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , чтобы определить, какие службы остановлены.

    Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [запрос WMI](querying-wmi.md)и [Получение события WMI](receiving-a-wmi-event.md).

6.  Очистка объектов и COM.

    Дополнительные сведения см. [в разделе Очистка и завершение работы приложения WMI](cleaning-up-and-shutting-down-a-wmi-application.md).

Следующий пример кода является полным клиентским приложением WMI.


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

    // Initialize COM.
    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        return 1;              // Program has failed.
    }

    // Initialize 
    hres =  CoInitializeSecurity(
        NULL,     
        -1,      // COM negotiates service                  
        NULL,    // Authentication services
        NULL,    // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,    // authentication
        RPC_C_IMP_LEVEL_IMPERSONATE,  // Impersonation
        NULL,             // Authentication info 
        EOAC_NONE,        // Additional capabilities
        NULL              // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;          // Program has failed.
    }

    // Obtain the initial locator to Windows Management
    // on a particular host computer.
    IWbemLocator *pLoc = 0;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
            << "Error code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;       // Program has failed.
    }

    IWbemServices *pSvc = 0;

    // Connect to the root\cimv2 namespace with the
    // current user and obtain pointer pSvc
    // to make IWbemServices calls.

    hres = pLoc->ConnectServer(
        
        _bstr_t(L"ROOT\\CIMV2"), // WMI namespace
        NULL,                    // User name
        NULL,                    // User password
        0,                       // Locale
        NULL,                    // Security flags                 
        0,                       // Authority       
        0,                       // Context object
        &pSvc                    // IWbemServices proxy
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

    // Set the IWbemServices proxy so that impersonation
    // of the user (client) occurs.
    hres = CoSetProxyBlanket(
       
       pSvc,                         // the proxy to set
       RPC_C_AUTHN_WINNT,            // authentication service
       RPC_C_AUTHZ_NONE,             // authorization service
       NULL,                         // Server principal name
       RPC_C_AUTHN_LEVEL_CALL,       // authentication level
       RPC_C_IMP_LEVEL_IMPERSONATE,  // impersonation level
       NULL,                         // client identity 
       EOAC_NONE                     // proxy capabilities     
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


    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:

    // For example, query for all the running processes
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_Process"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
    else
    { 
        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
   
        while (pEnumerator)
        {
            hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                &pclsObj, &uReturn);

            if(0 == uReturn)
            {
                break;
            }

            VARIANT vtProp;

            // Get the value of the Name property
            hres = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
            wcout << "Process Name : " << vtProp.bstrVal << endl;
            VariantClear(&vtProp);
            
            pclsObj->Release();
            pclsObj = NULL;
        }
         
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



 

 
