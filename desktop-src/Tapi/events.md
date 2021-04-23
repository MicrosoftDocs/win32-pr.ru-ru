---
description: События являются важной частью обработки вызовов в TAPI 3. Обработка событий включает четыре этапа.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: События (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545455"
---
# <a name="events-telephony-api"></a><span data-ttu-id="a71d9-104">События (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="a71d9-104">Events (Telephony API)</span></span>

<span data-ttu-id="a71d9-105">События являются важной частью обработки вызовов в TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="a71d9-105">Events are a crucial part of call handling under TAPI 3.</span></span> <span data-ttu-id="a71d9-106">Обработка событий включает четыре этапа.</span><span class="sxs-lookup"><span data-stu-id="a71d9-106">Event handling includes four stages.</span></span>

<span data-ttu-id="a71d9-107">**Регистрация и включение приема событий**</span><span class="sxs-lookup"><span data-stu-id="a71d9-107">**To register for and enable the reception of events**</span></span>

1.  <span data-ttu-id="a71d9-108">Реализуйте метод [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) .</span><span class="sxs-lookup"><span data-stu-id="a71d9-108">Implement the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method.</span></span> <span data-ttu-id="a71d9-109">(TAPI вызывает этот метод при возникновении события.) Как правило, эта реализация не превышает **AddRef** указателя интерфейса **IDispatch** , а затем POST в конвейер сообщений приложения.</span><span class="sxs-lookup"><span data-stu-id="a71d9-109">(TAPI calls this method when an event occurs.) Typically, this implementation does no more than **AddRef** the **IDispatch** interface pointer, then post to the application's message pump.</span></span>
2.  <span data-ttu-id="a71d9-110">Зарегистрируйте исходящий интерфейс [**иттапиевентнотификатион**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) , используя интерфейсы COM Standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) и [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) , и передайте метод [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) в указатель на [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span><span class="sxs-lookup"><span data-stu-id="a71d9-110">Register the [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) outgoing interface using the COM standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) and [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interfaces, and pass the [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) method a pointer to [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span></span>
3.  <span data-ttu-id="a71d9-111">Вызовите метод [**иттапи::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) , чтобы сообщить TAPI о том, какие события будут обработаны приложением.</span><span class="sxs-lookup"><span data-stu-id="a71d9-111">Call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method to tell TAPI which events the application will handle.</span></span> <span data-ttu-id="a71d9-112">Фильтр событий состоит из элементов **или** ED в перечислении [**\_ событий TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .</span><span class="sxs-lookup"><span data-stu-id="a71d9-112">The event filter consists of **OR** ed members of the [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) enumeration.</span></span>
    > [!Note]  
    > <span data-ttu-id="a71d9-113">Необходимо вызвать метод **иттапи::p UT \_ EventFilter** , чтобы задать маску фильтра событий и включить прием событий.</span><span class="sxs-lookup"><span data-stu-id="a71d9-113">You must call the **ITTAPI::put\_EventFilter** method to set the event filter mask and enable reception of events.</span></span> <span data-ttu-id="a71d9-114">Если не вызвать **иттапи::p UT \_ EventFilter**, приложение не будет принимать никаких событий.</span><span class="sxs-lookup"><span data-stu-id="a71d9-114">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span>

     

<span data-ttu-id="a71d9-115">Также необходимо вызвать метод [**иттапи:: регистеркаллнотификатионс**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) для каждого объекта адреса, для которого приложение будет выполнять вызовы.</span><span class="sxs-lookup"><span data-stu-id="a71d9-115">You must also call the [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) method for each address object on which the application will handle calls.</span></span>

<span data-ttu-id="a71d9-116">Список всех интерфейсов событий см. в разделе [интерфейсы событий](./event-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="a71d9-116">See [Event Interfaces](./event-interfaces.md) for a list of all event interfaces.</span></span> <span data-ttu-id="a71d9-117">В разделе [Регистрация событий](register-events.md) приведены примеры кода, иллюстрирующие процесс регистрации и [получающий вызов](receive-a-call.md) примера кода, в котором показано одно использование событий.</span><span class="sxs-lookup"><span data-stu-id="a71d9-117">See [Register Events](register-events.md) for code examples that illustrate the registration process and [Receive a Call](receive-a-call.md) for a code example that shows one use of events.</span></span>

 

 
