---
description: После установки уровней безопасности для указателя IWbemServices можно получить доступ к различным возможностям инструментария WMI. После завершения работы с инструментарием WMI необходимо завершить работу приложения.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Очистка и завершение работы приложения WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d2093b16491bcb600438d781fa833a09754fdc5d0cc8cc83feb710a6d2727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120914"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Очистка и завершение работы приложения WMI

После установки уровней безопасности для указателя [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) можно получить доступ к различным возможностям инструментария WMI. После завершения работы с инструментарием WMI необходимо завершить работу приложения.

Ниже описана процедура очистки и завершения работы приложения WMI.

**Очистка и завершение работы приложения WMI**

1.  Освободите все открытые COM-интерфейсы.

    Необходимо помнить два основных интерфейса: [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) и [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

2.  Вызов [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

    Как и для всех приложений COM, необходимо вызвать [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) в конце приложения.

3.  Выйдите из приложения.

    В следующем примере кода показано, как выйти из клиентского приложения WMI.

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > `pSvc`Переменная имеет тип [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* , а переменная Плок имеет тип [**ивбемлокатор**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

Инициализация COM, доступ к инструментарию WMI и выход из приложения успешно завершены. Дополнительные сведения см. в разделе [пример. Создание приложения WMI](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
