---
title: Работа с WM_GETOBJECT
description: При получении \_ сообщения WM GetObject, содержащего \_ клиент OBJID, сервер должен вернуть указатель на объект, реализующий IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777252"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="2118b-103">Как работать с WM \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="2118b-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="2118b-104">При получении сообщения [**WM \_ GetObject**](wm-getobject.md) , содержащего [**\_ клиент OBJID**](object-identifiers.md), сервер должен вернуть указатель на объект, реализующий [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="2118b-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="2118b-105">Этот указатель является LRESULT, полученным путем вызова [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="2118b-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="2118b-106">Microsoft Active Accessibility, в сочетании с библиотекой COM, выполняет соответствующий маршалирование и передает указатель интерфейса **IAccessible** с сервера клиенту.</span><span class="sxs-lookup"><span data-stu-id="2118b-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="2118b-107">Серверы должны правильно выполнять подсчет ссылок на доступном объекте.</span><span class="sxs-lookup"><span data-stu-id="2118b-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="2118b-108">Помните, что при создании COM-объекта счетчик ссылок равен 1.</span><span class="sxs-lookup"><span data-stu-id="2118b-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="2118b-109">Затем [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) несколько раз увеличивает число ссылок.</span><span class="sxs-lookup"><span data-stu-id="2118b-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="2118b-110">Все ссылки, созданные с помощью **функции lresultfromobject** , автоматически освобождаются, когда объект больше не нужен, но сервер отвечает за освобождение начальной ссылки, и если это не так, то объект никогда не будет уничтожен.</span><span class="sxs-lookup"><span data-stu-id="2118b-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="2118b-111">В примерах в следующих разделах показано, как освободить ссылки на доступные объекты.</span><span class="sxs-lookup"><span data-stu-id="2118b-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="2118b-112">Обычно серверы обрабатывали [**WM \_ GetObject**](wm-getobject.md) одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="2118b-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="2118b-113">Создание новых объектов со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="2118b-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="2118b-114">Повторное использование существующих указателей на объекты</span><span class="sxs-lookup"><span data-stu-id="2118b-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="2118b-115">Создание новых интерфейсов для одного и того же объекта</span><span class="sxs-lookup"><span data-stu-id="2118b-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="2118b-116">В этом разделе, как и в оставшейся части документации, при обсуждении указателя на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) этот указатель может фактически быть указателем на прокси-объект, который заключает в оболочку интерфейс **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="2118b-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="2118b-117">Дополнительные сведения об объектах прокси см. в разделе [Создание прокси-объектов](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2118b-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="2118b-118">Общие сведения о [**WM \_ GetObject**](wm-getobject.md)см. в статье [как \_ работает WM GetObject](how-wm-getobject-works.md).</span><span class="sxs-lookup"><span data-stu-id="2118b-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




