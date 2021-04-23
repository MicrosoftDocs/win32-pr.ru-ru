---
description: Ниже приведены указания и советы, которые следует учитывать при написании приложения для TAPI 3.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Указания и советы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684828"
---
# <a name="hints-and-tips"></a><span data-ttu-id="d8a0a-103">Указания и советы</span><span class="sxs-lookup"><span data-stu-id="d8a0a-103">Hints and Tips</span></span>

<span data-ttu-id="d8a0a-104">Ниже приведены указания и советы, которые следует учитывать при написании приложения для TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="d8a0a-105">COM- [**Инициализация**](/windows/desktop/api/objbase/nf-objbase-coinitialize) косвенно создает Windows; Это особенно важно для потоков подразделений.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="d8a0a-106">Если поток создает какие-либо окна, он должен обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="d8a0a-107">Если потоки вызывают **Соинициализацию**, запустите конвейер сообщений, чтобы избежать проблем.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="d8a0a-108">Например, COM может перестать работать правильно, или методы в интерфейсах COM, например **иглобалинтерфацетабле** , могут зависнуть.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="d8a0a-109">В потоковом апартаменте необходимо наличие конвейера сообщений независимо от того, ожидаете ли вы ожидание объектов синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="d8a0a-110">Это особенно важно при наличии консольного приложения или при написании объекта локального или удаленного сервера COM, который является контейнерным потоком (в котором отсутствует консоль или графический интерфейс пользователя, но элемент управления просто «работает» в системе).</span><span class="sxs-lookup"><span data-stu-id="d8a0a-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="d8a0a-111">При вызове функций Wait и Synchronization, таких как [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**ваитформултиплеобжектсекс**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)и т. д.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="d8a0a-112">Вместо этого используйте [**мсгваитформултиплеобжектс**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) и обработайте сообщения или используйте [**коваитформултиплехандлес**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), который автоматически определит тип апартамента, в котором находится поток (STA или MTA), и будет ожидать в модальном цикле com (если STA) или блокировать на **WaitForMultipleObjects** (если MTA).</span><span class="sxs-lookup"><span data-stu-id="d8a0a-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="d8a0a-113">**Мсгваитформултиплеобжектс** и **коваитформултиплехандлес** также обрабатывают сообщения Windows в соответствии с правилами com.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="d8a0a-114">Например, вместо:</span><span class="sxs-lookup"><span data-stu-id="d8a0a-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="d8a0a-115">Используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d8a0a-115">Use:</span></span>

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

2.  <span data-ttu-id="d8a0a-116">**Иттапиевентнотификатион:: Event** — это функция события Apps, вызываемая в потоке обратного вызова TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="d8a0a-117">Выполните минимум в подпрограммых событий. Вместо этого используйте собственный поток, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="d8a0a-118">Имейте в виду, что следующий пример кода предоставляется, но не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

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

3.  <span data-ttu-id="d8a0a-119">Не следует манипулировать COM-объектами после вызова [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="d8a0a-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="d8a0a-120">Результаты являются непредсказуемыми и неблагоприятными для работоспособного приложения.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="d8a0a-121">Некоторые примеры, в которых это может произойти, являются рабочими потоками и деструкторами C++, которые могут выполняться после того, как приложение вызывает метод **CoUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="d8a0a-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 
