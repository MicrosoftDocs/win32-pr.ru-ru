---
title: Получение объекта IAccessible
description: Microsoft Active Accessibility предоставляет такие функции, как Акцессиблеобжектфромвиндов и Акцессиблеобжектфромпоинт, которые позволяют клиентам получать доступные объекты.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328792"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="0ab03-103">Получение объекта IAccessible</span><span class="sxs-lookup"><span data-stu-id="0ab03-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="0ab03-104">Microsoft Active Accessibility предоставляет такие функции, как [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) и [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) , которые позволяют клиентам получать доступные объекты.</span><span class="sxs-lookup"><span data-stu-id="0ab03-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="0ab03-105">Эти функции возвращают указатель на интерфейс [**IDispatch**](idispatch-interface.md) или [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , через который клиенты получают сведения о доступном объекте.</span><span class="sxs-lookup"><span data-stu-id="0ab03-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="0ab03-106">Когда клиент вызывает [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) или любую другую функцию \**акцессиблеобжектфром \* \* \* X* , которая получает интерфейс к объекту, Microsoft Active Accessibility отправляет сообщение в окне [**WM \_ GetObject**](wm-getobject.md) в соответствующую процедуру в соответствующем приложении.</span><span class="sxs-lookup"><span data-stu-id="0ab03-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="0ab03-107">Чтобы предоставить сведения клиентам, серверы должны отвечать на сообщение **WM \_ GetObject** .</span><span class="sxs-lookup"><span data-stu-id="0ab03-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="0ab03-108">Чтобы получить конкретные сведения об элементе пользовательского интерфейса, клиенты должны сначала получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента.</span><span class="sxs-lookup"><span data-stu-id="0ab03-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="0ab03-109">Чтобы получить объект **IAccessible** элемента, клиенты могут использовать одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="0ab03-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="0ab03-110">**акцессиблеобжектфромпоинт**</span><span class="sxs-lookup"><span data-stu-id="0ab03-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="0ab03-111">**акцессиблеобжектфромвиндов**</span><span class="sxs-lookup"><span data-stu-id="0ab03-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="0ab03-112">**акцессиблеобжектфромевент**</span><span class="sxs-lookup"><span data-stu-id="0ab03-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="0ab03-113">**Получение указателя на интерфейс IAccessible**</span><span class="sxs-lookup"><span data-stu-id="0ab03-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="0ab03-114">Клиент вызывает одну из функций \**акцессиблеобжектфром \* \* \* X* .</span><span class="sxs-lookup"><span data-stu-id="0ab03-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="0ab03-115">Oleacc.dll отправляет сообщение [**WM \_ GetObject**](wm-getobject.md) на сервер.</span><span class="sxs-lookup"><span data-stu-id="0ab03-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="0ab03-116">Сервер определяет, какой элемент пользовательского интерфейса соответствует запросу.</span><span class="sxs-lookup"><span data-stu-id="0ab03-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="0ab03-117">Сервер либо возвращает нуль, чтобы запросить Oleacc.dll прокси-сервер,</span><span class="sxs-lookup"><span data-stu-id="0ab03-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="0ab03-118">либо</span><span class="sxs-lookup"><span data-stu-id="0ab03-118">Or</span></span>

    <span data-ttu-id="0ab03-119">Возвращает объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (собственная реализация).</span><span class="sxs-lookup"><span data-stu-id="0ab03-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="0ab03-120">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0ab03-120">To do this, it:</span></span>

    -   <span data-ttu-id="0ab03-121">Конструирует объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента.</span><span class="sxs-lookup"><span data-stu-id="0ab03-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="0ab03-122">Вызывает [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) для маршалирования указателя объекта.</span><span class="sxs-lookup"><span data-stu-id="0ab03-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="0ab03-123">Возвращает LRESULT для Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="0ab03-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="0ab03-124">Oleacc.dll проверяет возвращаемое значение из [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="0ab03-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="0ab03-125">Если он равен нулю, Oleacc.dll конструирует прокси-объект и возвращает его клиенту.</span><span class="sxs-lookup"><span data-stu-id="0ab03-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="0ab03-126">либо</span><span class="sxs-lookup"><span data-stu-id="0ab03-126">Or</span></span>

    <span data-ttu-id="0ab03-127">Если значение не равно нулю, Oleacc.dll вызывает метод [**обжектфромлресулт**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) для распаковки указателя на собственный объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и возвращает его клиенту.</span><span class="sxs-lookup"><span data-stu-id="0ab03-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




