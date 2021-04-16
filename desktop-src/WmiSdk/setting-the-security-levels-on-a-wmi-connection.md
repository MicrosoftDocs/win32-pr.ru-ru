---
description: После получения указателя на прокси-сервер IWbemServices необходимо настроить безопасность прокси-сервера для доступа к WMI через прокси-сервер.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Установка уровней безопасности для WMI-соединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712945"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Установка уровней безопасности для WMI-соединения

После получения указателя на прокси-сервер [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) необходимо настроить безопасность прокси-сервера для доступа к WMI через прокси-сервер. Необходимо задать безопасность, так как прокси-сервер **IWbemServices** предоставляет доступ к необработанному объекту. Как правило, безопасность COM не позволяет одному процессу получить доступ к другому процессу, если не заданы соответствующие свойства безопасности. Дополнительные сведения см. в разделе [Настройка параметров безопасности для IWbemServices и других учетных записей-посредников](setting-the-security-on-iwbemservices-and-other-proxies.md). Для подключений к разным операционным системам требуются разные уровни проверки подлинности и олицетворения. Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).

В примерах кода в этом разделе для правильной компиляции требуются следующие ссылки и \# инструкции include.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Следующая процедура описывает, как задать уровни безопасности для WMI-соединения.

**Установка уровней безопасности для WMI-соединения**

-   Задайте уровни безопасности для прокси-сервера [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) с помощью вызова [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    В следующем примере кода описывается распространенный способ вызова [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

После установки уровней безопасности для указателя [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) можно получить доступ к различным возможностям инструментария WMI. После завершения работы с инструментарием WMI необходимо завершить работу приложения. Дополнительные сведения см. [в разделе Очистка и завершение работы приложения WMI](cleaning-up-and-shutting-down-a-wmi-application.md).

 

 
