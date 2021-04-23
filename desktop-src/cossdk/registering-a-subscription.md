---
description: После регистрации класса событий в каталоге COM+ можно добавить подписчиков в класс событий и подписки на подписчики.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Регистрация подписки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423442"
---
# <a name="registering-a-subscription"></a><span data-ttu-id="41595-103">Регистрация подписки</span><span class="sxs-lookup"><span data-stu-id="41595-103">Registering a Subscription</span></span>

<span data-ttu-id="41595-104">После регистрации класса событий в каталоге COM+ можно добавить подписчиков в класс событий и подписки на подписчики.</span><span class="sxs-lookup"><span data-stu-id="41595-104">After you have registered an event class in the COM+ catalog, you can add subscribers to the event class and subscriptions to the subscribers.</span></span> <span data-ttu-id="41595-105">Подписки могут подписываться на один метод или на все методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="41595-105">Subscriptions can subscribe to a single method or to all the methods of an interface.</span></span> <span data-ttu-id="41595-106">Для получения вызовов более чем к одному методу, но не ко всем методам интерфейса, необходимо добавить подписку для каждого метода, для которого требуется получить вызов.</span><span class="sxs-lookup"><span data-stu-id="41595-106">To receive calls on more than one method—but not to every method—of an interface, you must add a subscription for each method to which you want to receive a call.</span></span> <span data-ttu-id="41595-107">Средство администрирования служб компонентов может искать в каталоге COM+ зарегистрированные классы событий, которые поддерживают интерфейсы, реализованные подписчиком, и предлагает выбрать подписываться.</span><span class="sxs-lookup"><span data-stu-id="41595-107">The Component Services administration tool can search the COM+ catalog for registered event classes that support the interfaces implemented by the subscriber and offers you the choice to subscribe.</span></span> <span data-ttu-id="41595-108">Выберите издателя, который предлагает нужные события.</span><span class="sxs-lookup"><span data-stu-id="41595-108">Choose the publisher that offers you the desired events.</span></span>

<span data-ttu-id="41595-109">Чтобы добавить подписчиков в компонент подписчика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41595-109">To add subscribers to the subscriber component, use the following steps:</span></span>

1.  <span data-ttu-id="41595-110">После создания нового приложения COM+ и установки компонента подписчика щелкните правой кнопкой мыши папку **подписки** , чтобы включить мастер создания подписки com+.</span><span class="sxs-lookup"><span data-stu-id="41595-110">After creating a new COM+ application and installing the subscriber component, right-click the **Subscriptions** folder to enable the COM+ New Subscription Wizard.</span></span>

2.  <span data-ttu-id="41595-111">Выберите класс событий, из которого требуется получить события.</span><span class="sxs-lookup"><span data-stu-id="41595-111">Choose the event class from which you want to receive events.</span></span>

3.  <span data-ttu-id="41595-112">Введите имя подписки.</span><span class="sxs-lookup"><span data-stu-id="41595-112">Enter a name for the subscription.</span></span>

4.  <span data-ttu-id="41595-113">Включите подписку.</span><span class="sxs-lookup"><span data-stu-id="41595-113">Enable the subscription.</span></span>

5.  <span data-ttu-id="41595-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="41595-114">Click **OK**.</span></span>

<span data-ttu-id="41595-115">Когда приложению издателя требуется запустить событие, издатель создает экземпляр объекта класса событий и вызывает метод для него.</span><span class="sxs-lookup"><span data-stu-id="41595-115">When a publisher application wants to fire an event, the publisher instantiates the event class object and calls a method on it.</span></span> <span data-ttu-id="41595-116">COM+ просматривает каталог COM+, чтобы найти всех подписчиков.</span><span class="sxs-lookup"><span data-stu-id="41595-116">COM+ searches the COM+ catalog to find all the subscribers.</span></span> <span data-ttu-id="41595-117">Он создает объект подписчика (напрямую, в очереди или с моникером) и передает вызов метода, изначально сделанный издателем.</span><span class="sxs-lookup"><span data-stu-id="41595-117">It creates the subscriber object (directly, queued, or with a moniker) and passes on the method call originally made by the publisher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41595-118">См. также</span><span class="sxs-lookup"><span data-stu-id="41595-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41595-119">Регистрация класса событий</span><span class="sxs-lookup"><span data-stu-id="41595-119">Registering an Event Class</span></span>](registering-an-event-class.md)
</dt> </dl>

 

 



