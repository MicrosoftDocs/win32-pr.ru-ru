---
description: Ниже приведены указания и советы, которые следует учитывать при написании приложения для TAPI 3.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: указания и Советы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d51e8c7e3f8c6e4a9e38b27fa5cfe4c10e45d37cfa67af095d573eea319614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762940"
---
# <a name="hints-and-tips"></a>указания и Советы

Ниже приведены указания и советы, которые следует учитывать при написании приложения для TAPI 3.

1.  COM- [**Инициализация**](/windows/desktop/api/objbase/nf-objbase-coinitialize) косвенно создает Windows; Это особенно важно для потоков подразделений. Если поток создает какие-либо окна, он должен обрабатывать сообщения. Если потоки вызывают **Соинициализацию**, запустите конвейер сообщений, чтобы избежать проблем. Например, COM может перестать работать правильно, или методы в интерфейсах COM, например **иглобалинтерфацетабле** , могут зависнуть.

    В потоковом апартаменте необходимо наличие конвейера сообщений независимо от того, ожидаете ли вы ожидание объектов синхронизации. Это особенно важно при наличии консольного приложения или при написании объекта локального или удаленного сервера COM, который является контейнерным потоком (в котором отсутствует консоль или графический интерфейс пользователя, но элемент управления просто «работает» в системе).

    > [!Caution]  
    > При вызове функций Wait и Synchronization, таких как [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**ваитформултиплеобжектсекс**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)и т. д. Вместо этого используйте [**мсгваитформултиплеобжектс**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) и обработайте сообщения или используйте [**коваитформултиплехандлес**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), который автоматически определит тип апартамента, в котором находится поток (STA или MTA), и будет ожидать в модальном цикле com (если STA) или блокировать на **WaitForMultipleObjects** (если MTA). **Мсгваитформултиплеобжектс** и **коваитформултиплехандлес** также обрабатывают сообщения Windows в соответствии с правилами com.

     

    Например, вместо:

    `Sleep (5000);`

    Используйте следующую команду:

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  **Иттапиевентнотификатион:: Event** — это функция события Apps, вызываемая в потоке обратного вызова TAPI 3.

    Выполните минимум в подпрограммых событий. Вместо этого используйте собственный поток, где это возможно.

    Имейте в виду, что следующий пример кода предоставляется, но не является обязательным.

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  Не следует манипулировать COM-объектами после вызова [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Результаты являются непредсказуемыми и неблагоприятными для работоспособного приложения. Некоторые примеры, в которых это может произойти, являются рабочими потоками и деструкторами C++, которые могут выполняться после того, как приложение вызывает метод **CoUninitialize**.

 

 
