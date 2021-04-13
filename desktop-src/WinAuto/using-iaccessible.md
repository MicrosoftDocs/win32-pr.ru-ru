---
title: Использование интерфейса IAccessible
description: Интерфейс IAccessible — это коллекция методов, которые предоставляют наиболее распространенные атрибуты и поведение для широкого спектра элементов пользовательского интерфейса.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330427"
---
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="f6e9a-103">Использование интерфейса IAccessible</span><span class="sxs-lookup"><span data-stu-id="f6e9a-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="f6e9a-104">Интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) — это коллекция методов, которые предоставляют наиболее распространенные атрибуты и поведение для широкого спектра элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="f6e9a-105">Элемент пользовательского интерфейса — это элемент управления, например меню или кнопка "Отправить", который является частью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="f6e9a-106">Доступный объект — это элемент пользовательского интерфейса, имеющий осмысленный интерфейс **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="f6e9a-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="f6e9a-107">Некоторые свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) неприменимы к каждому типу элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="f6e9a-108">Кроме того, реализация **IAccessible** отличается от приложения к приложению.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="f6e9a-109">Хотя параметры и возвращаемые значения для свойств и методов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) заданы полностью, то, как клиент должен использовать свойство или как сервер должен реализовать свойство, иногда подлежит интерпретации.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="f6e9a-110">В этом разделе приводятся рекомендации, рекомендации и примеры, позволяющие клиентским приложениям получать сведения об элементах пользовательского интерфейса и помочь серверным приложениям предоставлять соответствующую информацию.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6e9a-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f6e9a-111">In this section</span></span>

-   [<span data-ttu-id="f6e9a-112">Содержимое описательных свойств</span><span class="sxs-lookup"><span data-stu-id="f6e9a-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="f6e9a-113">Свойства и методы выбора и фокуса</span><span class="sxs-lookup"><span data-stu-id="f6e9a-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="f6e9a-114">Свойства и методы навигации по объектам</span><span class="sxs-lookup"><span data-stu-id="f6e9a-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




