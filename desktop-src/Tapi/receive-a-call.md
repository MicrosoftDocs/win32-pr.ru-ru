---
description: В следующем примере кода демонстрируется обработка новых уведомлений о вызовах, например поиск или создание соответствующих терминалов для подготовки к просмотру мультимедиа.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Получение вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a78ebf5b77569f8468a8b2c0a30217f4f7430e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684318"
---
# <a name="receive-a-call"></a><span data-ttu-id="5f68f-103">Получение вызова</span><span class="sxs-lookup"><span data-stu-id="5f68f-103">Receive a Call</span></span>

<span data-ttu-id="5f68f-104">В следующем примере кода демонстрируется обработка новых уведомлений о вызовах, например поиск или создание соответствующих терминалов для подготовки к просмотру мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5f68f-104">The following code example demonstrates handling of new call notifications, such as finding or creating appropriate terminals to render the media.</span></span> <span data-ttu-id="5f68f-105">Этот пример представляет собой часть оператора switch, которую приложение должно реализовать для обработки событий.</span><span class="sxs-lookup"><span data-stu-id="5f68f-105">This example is a portion of the switch statement an application must implement for event handling.</span></span> <span data-ttu-id="5f68f-106">Сам код может содержаться в реализации [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), или метод **события** может поместить сообщение в рабочий поток, содержащий параметр.</span><span class="sxs-lookup"><span data-stu-id="5f68f-106">The code itself may be contained in the implementation of [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), or the **Event** method may post a message to a worker thread that contains the switch.</span></span>

<span data-ttu-id="5f68f-107">Перед использованием этого примера кода необходимо выполнить операции в оснастке [инициализации TAPI](initialize-tapi.md), [выбрать адрес](select-an-address.md)и [зарегистрировать события](register-events.md).</span><span class="sxs-lookup"><span data-stu-id="5f68f-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md), [Select an Address](select-an-address.md), and [Register Events](register-events.md).</span></span>

<span data-ttu-id="5f68f-108">Кроме того, необходимо выполнить операции, показанные в окне [Выбор терминала](select-a-terminal.md) после получения указателей интерфейса [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) и [**итаддресс**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) .</span><span class="sxs-lookup"><span data-stu-id="5f68f-108">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the retrieval of the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) interface pointers.</span></span>

> [!Note]  
> <span data-ttu-id="5f68f-109">В этом примере отсутствует проверка ошибок и выпуски, соответствующие рабочему коду.</span><span class="sxs-lookup"><span data-stu-id="5f68f-109">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a><span data-ttu-id="5f68f-110">См. также</span><span class="sxs-lookup"><span data-stu-id="5f68f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f68f-111">События</span><span class="sxs-lookup"><span data-stu-id="5f68f-111">Events</span></span>](events.md)
</dt> <dt>

[<span data-ttu-id="5f68f-112">**иттапиевентнотификатион**</span><span class="sxs-lookup"><span data-stu-id="5f68f-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[<span data-ttu-id="5f68f-113">**ИТТАПИ:: Регистеркаллнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="5f68f-113">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[<span data-ttu-id="5f68f-114">**иткаллнотификатионевент**</span><span class="sxs-lookup"><span data-stu-id="5f68f-114">**ITCallNotificationEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[<span data-ttu-id="5f68f-115">**иткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="5f68f-115">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="5f68f-116">**итбасиккаллконтрол**</span><span class="sxs-lookup"><span data-stu-id="5f68f-116">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="5f68f-117">**иттерминалсуппорт**</span><span class="sxs-lookup"><span data-stu-id="5f68f-117">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
