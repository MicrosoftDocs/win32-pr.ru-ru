---
title: Свойства и методы выбора и фокуса
description: Как и многие элементы в приложениях, работающих в операционных системах Microsoft Windows, доступные объекты — выбор и получение фокуса клавиатуры. Эти атрибуты позволяют пользователям взаимодействовать с элементами приложения, изменять значения и иным образом манипулировать ими.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792474"
---
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="e485e-104">Свойства и методы выбора и фокуса</span><span class="sxs-lookup"><span data-stu-id="e485e-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="e485e-105">Как и многие элементы в приложениях, работающих в операционных системах Microsoft Windows, доступные объекты — *Выбор* и получение *фокуса* клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="e485e-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="e485e-106">Эти атрибуты позволяют пользователям взаимодействовать с элементами приложения, изменять значения и иным образом манипулировать ими.</span><span class="sxs-lookup"><span data-stu-id="e485e-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="e485e-107">Между выделением объектов и фокусом объектов связаны некоторые ключевые различия.</span><span class="sxs-lookup"><span data-stu-id="e485e-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="e485e-108">Объект с фокусом — это один объект во всей операционной системе, принимающий ввод с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="e485e-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="e485e-109">Объект с фокусом клавиатуры — это либо активное окно, либо дочерний объект активного окна.</span><span class="sxs-lookup"><span data-stu-id="e485e-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="e485e-110">Выбранный объект помечен для участия в некоторой операции группы.</span><span class="sxs-lookup"><span data-stu-id="e485e-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="e485e-111">Например, пользователь может выбрать несколько элементов в элементе управления "представление списка", но в каждый момент времени фокус передается только на один объект в системе.</span><span class="sxs-lookup"><span data-stu-id="e485e-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="e485e-112">Обратите внимание, что элементы с сортировкой связаны с выбором элементов.</span><span class="sxs-lookup"><span data-stu-id="e485e-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="e485e-113">Клиенты определяют, имеет ли определенный доступный объект или дочерний элемент фокус, вызывая метод [**IAccessible:: Get \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span><span class="sxs-lookup"><span data-stu-id="e485e-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="e485e-114">Клиенты определяют, выбран ли объект, или какие потомки в доступном объекте выбираются путем вызова метода [**IAccessible:: Get \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span><span class="sxs-lookup"><span data-stu-id="e485e-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="e485e-115">Для объектов, таких как элементы управления "представление списка", в которых выбрано несколько дочерних объектов, родительский объект должен поддерживать интерфейс [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , который позволяет клиентам перечислять выбранные дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="e485e-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="e485e-116">События, активируемые в меню</span><span class="sxs-lookup"><span data-stu-id="e485e-116">Events Triggered in Menus</span></span>

<span data-ttu-id="e485e-117">Microsoft Active Accessibility предоставляет стандартные меню, созданные с помощью API меню Microsoft Win32 и файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e485e-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="e485e-118">Чтобы обеспечить соответствие стандартным меню, серверы с пользовательскими меню активируют [**\_ \_ фокус объекта событий**](event-constants.md), а [**не \_ \_ Выбор объектов событий**](event-constants.md), когда пользователь выделяет пункт меню.</span><span class="sxs-lookup"><span data-stu-id="e485e-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="e485e-119">Microsoft Active Accessibility не поддерживает выбор текста, содержащегося в элементах управления Edit и Rich Edit, поскольку текст представлен в свойстве [**value**](value-property.md) для этих элементов управления в виде одной строки.</span><span class="sxs-lookup"><span data-stu-id="e485e-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e485e-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="e485e-120">In this section</span></span>

-   [<span data-ttu-id="e485e-121">Выбор дочерних объектов</span><span class="sxs-lookup"><span data-stu-id="e485e-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 