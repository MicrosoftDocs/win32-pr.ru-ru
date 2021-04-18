---
description: Публикация события
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Публикация события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701226"
---
# <a name="publishing-an-event"></a><span data-ttu-id="9012e-103">Публикация события</span><span class="sxs-lookup"><span data-stu-id="9012e-103">Publishing an Event</span></span>

<span data-ttu-id="9012e-104">Чтобы опубликовать событие, просто создайте экземпляр объекта события, вызвав [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или метод Microsoft Visual Basic **CreateObject** , используя евентклассид или евенткласснаме в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="9012e-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="9012e-105">Издатель вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на объекте события для получения интерфейсов, поддерживаемых объектом класса событий, и вызывает метод для объекта события через интерфейс для публикации события.</span><span class="sxs-lookup"><span data-stu-id="9012e-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="9012e-106">Затем система событий публикует события в классе событий CLSID \_ евентобжектчанже с ИД интерфейса IID \_ иевентобжектчанже.</span><span class="sxs-lookup"><span data-stu-id="9012e-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="9012e-107">Для поддержки доставки событий нескольким подписчикам методы класса событий должны содержать только параметры in.</span><span class="sxs-lookup"><span data-stu-id="9012e-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="9012e-108">С помощью свойства Фиреинпараллел объекта [класса событий](the-com--event-class-object.md) издатели могут запросить, чтобы система событий использовала несколько потоков для доставки события нескольким подписчикам.</span><span class="sxs-lookup"><span data-stu-id="9012e-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="9012e-109">Выбор параллельного механизма доставки не гарантирует одновременной доставки события нескольким подписчикам, но он указывает службе событий COM+ сделать это.</span><span class="sxs-lookup"><span data-stu-id="9012e-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9012e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="9012e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9012e-111">Публикация и доставка событий в COM+</span><span class="sxs-lookup"><span data-stu-id="9012e-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
