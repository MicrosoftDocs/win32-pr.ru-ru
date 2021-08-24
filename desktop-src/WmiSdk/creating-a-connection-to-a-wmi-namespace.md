---
description: 'После установки стандартных вызовов COM необходимо подключиться к WMI с помощью вызова метода Ивбемлокатор:: Коннектсервер.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Создание соединения с пространством имен WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587024d7f581cd28a8fdaf339db9567b17c509599c01aca0599b701186fb786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412144"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Создание соединения с пространством имен WMI

После установки стандартных вызовов COM необходимо подключиться к WMI с помощью вызова метода [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . Метод **коннектсервер** возвращает прокси-сервер интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . С помощью **IWbemServices** можно получить доступ к различным возможностям инструментария WMI.

В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



В следующей процедуре описывается создание соединения с пространством имен WMI.

**Создание соединения с пространством имен WMI**

-   Инициализируйте интерфейс [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) с помощью вызова [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Инструментарий WMI не требует выполнения каких либо дополнительных процедур при вызове [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    В следующем примере кода показано, как инициализировать [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   Подключение WMI с помощью вызова метода [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .

        Метод [**коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) возвращает прокси-сервер для интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , который использует для доступа к локальному или удаленному пространству имен WMI, указанному в вызове **коннектсервер**.

        В следующем примере кода показано, как вызвать [**коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

После получения указателя на прокси-сервер [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) необходимо установить безопасность на прокси-сервере для доступа к WMI. Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Поддержка IPv6 и IPv4 в WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
