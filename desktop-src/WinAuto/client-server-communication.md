---
title: Обмен данными между клиентом и сервером
description: Механизм Виневентс предоставляет серверам возможность легко обмениваться данными с клиентами Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "105700791"
---
# <a name="clientserver-communication"></a><span data-ttu-id="f2fa0-103">Обмен данными между клиентом и сервером</span><span class="sxs-lookup"><span data-stu-id="f2fa0-103">Client/Server Communication</span></span>

<span data-ttu-id="f2fa0-104">Механизм [виневентс](winevents-overview.md) предоставляет серверам возможность легко обмениваться данными с клиентами Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="f2fa0-105">Клиенты часто собираются данные путем реагирования на Виневентс (например, следующий фокус), но они могут запрашивать информацию с сервера в любое время.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="f2fa0-106">Чтобы запросить сведения для объекта со специальными возможностями, создающего WinEvent, клиент должен обработать событие и установить соединение с соответствующим доступным объектом.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="f2fa0-107">Для этого клиент выполняет следующие шесть шагов:</span><span class="sxs-lookup"><span data-stu-id="f2fa0-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="f2fa0-108">Сервер вызывает [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , чтобы создать уведомление WinEvent для каждого изменения в своих элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="f2fa0-109">Код управления WinEvent в USER определяет, зарегистрировал ли клиентские приложения [*функцию-обработчик*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent с помощью [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) и вызывает зарегистрированную функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="f2fa0-110">В функции обратного вызова клиент запрашивает доступ к объекту, создавшему событие, путем вызова [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) или других функций получения доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="f2fa0-111">Дополнительные сведения см. в разделе [Получение объекта IAccessible](retrieving-an-iaccessible-object.md).</span><span class="sxs-lookup"><span data-stu-id="f2fa0-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="f2fa0-112">Этот API Microsoft Active Accessibility отправляет серверное приложение сообщение [**WM \_ GetObject**](wm-getobject.md) для получения доступного объекта.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="f2fa0-113">В ответ на функцию [**WM \_ GetObject**](wm-getobject.md)серверное приложение возвращает либо ноль, либо возвращает значение, которое выступает в качестве одноразовой ссылки на объект, создавший событие.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="f2fa0-114">Если сервер возвращает значение 0, Microsoft Active Accessibility создает прокси-объект и предоставляет клиенту свой адрес.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="f2fa0-115">В противном случае Microsoft Active Accessibility использует эту ссылку для получения адреса объектного интерфейса, такого как [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) или [**IDispatch**](idispatch-interface.md), и предоставляет клиенту этот адрес.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="f2fa0-116">После того как у клиента есть адрес интерфейса, он может вызывать свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и методы доступного объекта для получения информации.</span><span class="sxs-lookup"><span data-stu-id="f2fa0-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2fa0-117">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f2fa0-117">In this section</span></span>

-   [<span data-ttu-id="f2fa0-118">Виневентс и Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="f2fa0-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="f2fa0-119">Как \_ работает WM GetObject</span><span class="sxs-lookup"><span data-stu-id="f2fa0-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="f2fa0-120">Получение объекта IAccessible</span><span class="sxs-lookup"><span data-stu-id="f2fa0-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




