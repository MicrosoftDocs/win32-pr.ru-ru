---
title: Выбор свойств для поддержки
description: Свойства IAccessible предоставляют разработчикам сервера возможность описывать разнообразные элементы пользовательского интерфейса.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330920"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="8dd69-103">Выбор свойств для поддержки</span><span class="sxs-lookup"><span data-stu-id="8dd69-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="8dd69-104">Свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляют разработчикам сервера возможность описывать разнообразные элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8dd69-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="8dd69-105">Но не все свойства применимы для каждого вида элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8dd69-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="8dd69-106">Кроме того, некоторые свойства предоставляют описательные сведения, которые полезны, но не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="8dd69-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="8dd69-107">Серверы должны поддерживать следующие свойства и методы для каждого объекта:</span><span class="sxs-lookup"><span data-stu-id="8dd69-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="8dd69-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8dd69-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="8dd69-109">**Role**</span><span class="sxs-lookup"><span data-stu-id="8dd69-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="8dd69-110">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8dd69-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="8dd69-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) и [ **IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="8dd69-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="8dd69-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) и [ **IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="8dd69-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="8dd69-113">Следующие свойства и метод должны поддерживаться, если они применимы к объекту:</span><span class="sxs-lookup"><span data-stu-id="8dd69-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="8dd69-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="8dd69-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="8dd69-115">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8dd69-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="8dd69-116">Если у объекта есть дочерние элементы, необходимо поддерживать следующие свойства и метод.</span><span class="sxs-lookup"><span data-stu-id="8dd69-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="8dd69-117">[**Дочерний элемент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) и [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="8dd69-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="8dd69-118">[**Фокус, выбор**](selection-and-focus-properties-and-methods.md)и [ **IAccessible:: аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="8dd69-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="8dd69-119">Следующие свойства являются необязательными, но предоставляют полезные описательные сведения об объекте.</span><span class="sxs-lookup"><span data-stu-id="8dd69-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="8dd69-120">Свойство [**Description**](description-property.md) реализуется для описания точечных рисунков и других изображений.</span><span class="sxs-lookup"><span data-stu-id="8dd69-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="8dd69-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8dd69-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="8dd69-122">[**DefaultAction**](defaultaction-property.md) и [ **IAccessible:: аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="8dd69-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="8dd69-123">**Справка**</span><span class="sxs-lookup"><span data-stu-id="8dd69-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="8dd69-124">**хелптопик**</span><span class="sxs-lookup"><span data-stu-id="8dd69-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




