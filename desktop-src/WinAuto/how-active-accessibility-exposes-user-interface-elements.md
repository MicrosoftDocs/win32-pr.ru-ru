---
title: Как Active Accessibility предоставляет элементы пользовательского интерфейса
description: Microsoft Active Accessibility создает прокси-объект для каждого элемента пользовательского интерфейса, который он предоставляет.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253260"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="deacd-103">Как Active Accessibility предоставляет элементы пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="deacd-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="deacd-104">Microsoft Active Accessibility создает *прокси-* объект для каждого элемента пользовательского интерфейса, который он предоставляет.</span><span class="sxs-lookup"><span data-stu-id="deacd-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="deacd-105">Прокси-объект выступает в качестве посредника между клиентской программой и элементом пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="deacd-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="deacd-106">Цель прокси-объекта заключается в мониторинге жизненного цикла элемента пользовательского интерфейса и реализации свойств и методов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) от имени элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="deacd-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="deacd-107">Разработчики сервера, создающие настраиваемые элементы управления или другие настраиваемые элементы пользовательского интерфейса, также должны создавать прокси-объекты.</span><span class="sxs-lookup"><span data-stu-id="deacd-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="deacd-108">Дополнительные сведения см. в разделе [Создание прокси-объектов](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="deacd-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="deacd-109">Когда Microsoft Active Accessibility создает объект для предоставления предопределенного или общего элемента управления, он на самом деле создает по крайней мере два объекта: один для элемента управления и один для окна, охватывающего элемент управления.</span><span class="sxs-lookup"><span data-stu-id="deacd-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="deacd-110">В большинстве случаев эти родительские окна имеют [свойство Role](role-property.md) [**\_ системного \_ окна Role**](object-roles.md) и имеют то же имя [Свойства](name-property.md) и класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="deacd-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="deacd-111">Сведения об элементе управления, который клиенты передают конечным пользователям, содержатся в объекте, создаваемом Microsoft Active Accessibility для предоставления элемента управления, а не на родительском объекте, который предоставляет окно, охватывающее элемент управления.</span><span class="sxs-lookup"><span data-stu-id="deacd-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="deacd-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="deacd-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="deacd-113">Блокировка ненужных объектов</span><span class="sxs-lookup"><span data-stu-id="deacd-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="deacd-114">Предоставление свойства Name</span><span class="sxs-lookup"><span data-stu-id="deacd-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="deacd-115">Проверка правильности имен элементов пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="deacd-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="deacd-116">Неподдерживаемые элементы пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="deacd-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




