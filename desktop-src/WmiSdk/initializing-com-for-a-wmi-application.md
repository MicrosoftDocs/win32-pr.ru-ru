---
description: Первым шагом при подключении к WMI является настройка вызовов COM для CoInitializeEx и CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Инициализация COM для приложения WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999557"
---
# <a name="initializing-com-for-a-wmi-application"></a>Инициализация COM для приложения WMI

Первым шагом при подключении к WMI является настройка вызовов COM для [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



В следующей процедуре описывается инициализация COM из клиентского приложения.

**Инициализация COM из клиентского приложения**

1.  Инициализируйте COM с помощью вызова [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Вызов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) является стандартной процедурой для настройки COM-интерфейса. Таким образом, Инструментарий WMI не требует наличия дополнительных процедур при вызове **CoInitializeEx**. Дополнительные сведения см. в разделе [com](../com/component-object-model--com--portal.md).

    В следующем примере кода показано, как вызвать [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Задайте общие уровни безопасности COM с помощью вызова интерфейса [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) — это стандартная функция, которую необходимо вызывать при настройке COM-интерфейса для процесса. Вызовите **CoInitializeSecurity** , если хотите задать параметры безопасности по умолчанию для проверки подлинности, олицетворения или службы проверки подлинности для всего процесса. Дополнительные сведения см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md). Если вы хотите задать или изменить безопасность для определенного прокси-сервера, необходимо вызвать метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Используйте **CoSetProxyBlanket** всякий раз, когда необходимо задать или изменить безопасность COM при выполнении внутри другого процесса, где нельзя управлять параметрами безопасности по умолчанию для проверки подлинности, олицетворения или службы проверки подлинности. Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-подключения](setting-the-security-levels-on-a-wmi-connection.md) и [Настройка параметров безопасности для IWbemServices и других прокси-серверов](setting-the-security-on-iwbemservices-and-other-proxies.md).

    Инструментарий WMI имеет несколько проблем безопасности, о которых следует помнить при программировании клиентского приложения WMI. Дополнительные сведения см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md).

    В следующем примере кода показано, как вызвать [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы установить безопасность COM для процесса.

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

После инициализации COM необходимо создать соединение с пространством имен WMI. Дополнительные сведения см. в разделе [Создание подключения к пространству имен WMI](creating-a-connection-to-a-wmi-namespace.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
