---
description: В следующих примерах кода демонстрируется реализация простого обработчика событий, регистрация основного интерфейса событий TAPI, Настройка фильтра событий и регистрация уведомлений о вызовах.
ms.assetid: e7662a26-d7b2-4bff-aa72-e38b58bc15df
title: Регистрация событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0a554c2e1ea5c226aa4a3c432f3430a30a978e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674470"
---
# <a name="register-events"></a><span data-ttu-id="f1395-103">Регистрация событий</span><span class="sxs-lookup"><span data-stu-id="f1395-103">Register Events</span></span>

<span data-ttu-id="f1395-104">В следующих примерах кода демонстрируется реализация простого обработчика событий, регистрация основного интерфейса событий TAPI, Настройка фильтра событий и регистрация уведомлений о вызовах.</span><span class="sxs-lookup"><span data-stu-id="f1395-104">The following code examples demonstrate implementation of a simple event handler, registration of the main TAPI event interface, setting of the event filter, and registration for call notifications.</span></span>

<span data-ttu-id="f1395-105">Показанный обработчик событий является примером, а не требованием.</span><span class="sxs-lookup"><span data-stu-id="f1395-105">The event handler shown is an example rather than a requirement.</span></span> <span data-ttu-id="f1395-106">Основная цель состоит в том, чтобы убедиться, что поток, получающий события, выполняет минимальную обработку перед передачей работы в другой поток.</span><span class="sxs-lookup"><span data-stu-id="f1395-106">The primary goal is to ensure that the thread that receives events does minimal processing before passing work to another thread.</span></span> <span data-ttu-id="f1395-107">Это предотвращает возникновение проблем с производительностью обработчиком событий в ситуациях высокой загрузки событий.</span><span class="sxs-lookup"><span data-stu-id="f1395-107">This prevents the event handler from becoming a performance problem in situations of high event load.</span></span>

<span data-ttu-id="f1395-108">Перед использованием этого примера кода необходимо выполнить операции в оснастке [инициализации TAPI](initialize-tapi.md) и [выбрать адрес](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="f1395-108">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

> [!Note]  
> <span data-ttu-id="f1395-109">В этом примере отсутствует проверка ошибок и выпуски, соответствующие рабочему коду.</span><span class="sxs-lookup"><span data-stu-id="f1395-109">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
//
// Example 1: Implement a simple event handler.
//
HRESULT STDMETHODCALLTYPE
CTAPIEventNotification::Event(
    TAPI_EVENT  TapiEvent,
    IDispatch * pEvent
    )
{
    // AddRef the event so it does not go away.
    pEvent->AddRef();

    // Post a message to our own UI thread.
    BOOL bMessage;
    bMessage = PostMessage( 
                           ghDlg,
                           WM_PRIVATETAPIEVENT,
                           (WPARAM) TapiEvent,
                           (LPARAM) pEvent
                           );
    // If (bMessage == 0) process the error here. 
    return S_OK;
}
```

``` syntax
//
// Example 2: Register the event interface.
//
long                         gulAdvise;  // Globally declared
IConnectionPointContainer   * pCPC;
IConnectionPoint            * pCP;
IUnknown                    * pUnk;

// Get the connection point container interface pointer from the TAPI object.
hr = gpTapi->QueryInterface(
      IID_IConnectionPointContainer,
      (void **)&pCPC
);
// If ( hr != S_OK O) process the error here. 

// Get the ITTAPIEventNotification interface pointer from the container.
hr = pCPC->FindConnectionPoint(
      IID_ITTAPIEventNotification,
      &pCP
     );
// If ( hr != S_OK O) process the error here. 

pCPC->Release();

// Create a private event notification object.
CTAPIEventNotification* pTapiEventNotification = new CTAPIEventNotification;

hr = pTapiEventNotification->QueryInterface(
      IID_IUnknown,
      (void **)&pUnk
     );
// If ( hr != S_OK O) process the error here. 

// Call the advise method to give TAPI the IUnknown pointer for the event handler.
hr = pCP->Advise(
      pUnk,
      (ULONG *)&gulAdvise
     );
// If ( hr != S_OK O) process the error here. 

pCP->Release();
```

``` syntax
//
// Example 3: Set the event filter.
//
// Assume we are interested only in call-related events.
hr = gpTapi->put_EventFilter(
    TE_CALLNOTIFICATION | TE_CALLSTATE | TE_CALLMEDIA
    );
// If ( hr != S_OK O) process the error here. 
```

``` syntax
//
// Example 4: Register an address with TAPI
// for call notifications. Assume we are interested
// in video and audio calls, and that pAddress
// is a pointer to the ITAddress interface of
// an address that can handle both media types.

long glRegister; // Globally declared

hr = gpTapi->RegisterCallNotifications(
      pAddress,
      VARIANT_TRUE,   // monitor privileges
      VARIANT_TRUE,   // owner privileges
      TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
      gulAdvise,      // As returned by Advise
      &glRegister
      );
// If ( hr != S_OK O) process the error here.
```

## <a name="related-topics"></a><span data-ttu-id="f1395-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f1395-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1395-111">**Иттапиевентнотификатион:: Event**</span><span class="sxs-lookup"><span data-stu-id="f1395-111">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="f1395-112">**\_событие TAPI**</span><span class="sxs-lookup"><span data-stu-id="f1395-112">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="f1395-113">**ИТТАПИ::p UT \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="f1395-113">**ITTAPI::put\_EventFilter**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)
</dt> <dt>

[<span data-ttu-id="f1395-114">\_Константы тапимедиатипе</span><span class="sxs-lookup"><span data-stu-id="f1395-114">TAPIMEDIATYPE\_ Constants</span></span>](tapimediatype--constants.md)
</dt> <dt>

[<span data-ttu-id="f1395-115">**ИТТАПИ:: Регистеркаллнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="f1395-115">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> </dl>

 

 



