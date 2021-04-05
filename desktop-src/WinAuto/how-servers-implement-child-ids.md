---
title: Как серверы реализуют дочерние идентификаторы
description: Разработчики сервера могут назначить дочерние идентификаторы как для простых элементов, так и для объектов со специальными возможностями. Однако рекомендуемый подход заключается в поддержке стандартного интерфейса модели COM IEnumVARIANT в каждом доступном объекте, который имеет дочерние элементы.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987682"
---
# <a name="how-servers-implement-child-ids"></a><span data-ttu-id="24044-104">Как серверы реализуют дочерние идентификаторы</span><span class="sxs-lookup"><span data-stu-id="24044-104">How Servers Implement Child IDs</span></span>

<span data-ttu-id="24044-105">Разработчики сервера могут назначить дочерние идентификаторы как для простых элементов, так и для объектов со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="24044-105">Server developers can assign child IDs to both simple elements and accessible objects.</span></span> <span data-ttu-id="24044-106">Однако рекомендуемый подход заключается в поддержке стандартного интерфейса модели COM [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) в каждом доступном объекте, который имеет дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="24044-106">However, the recommended approach is to support the standard Component Object Model (COM) interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in every accessible object that has children.</span></span>

<span data-ttu-id="24044-107">При реализации [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="24044-107">If you implement [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must:</span></span>

-   <span data-ttu-id="24044-108">Перечисление всех дочерних элементов, как простых, так и доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="24044-108">Enumerate all children, both simple elements and accessible objects.</span></span> <span data-ttu-id="24044-109">Укажите дочерние идентификаторы для всех простых элементов и предоставьте [**IDispatch**](idispatch-interface.md) каждому доступному объекту.</span><span class="sxs-lookup"><span data-stu-id="24044-109">Provide child IDs for all simple elements and provide the [**IDispatch**](idispatch-interface.md) to each accessible object.</span></span>
-   <span data-ttu-id="24044-110">Для объектов со специальными возможностями  задайте для элемента VT [**в качестве значения**](variant-structure.md) параметра VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="24044-110">For accessible objects, set the **vt** member of the [**VARIANT**](variant-structure.md) to VT\_DISPATCH.</span></span> <span data-ttu-id="24044-111">Элемент **пдиспвал** должен содержать указатель на интерфейс [**IDispatch**](idispatch-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="24044-111">The **pdispVal** member must contain a pointer to the [**IDispatch**](idispatch-interface.md) interface.</span></span> <span data-ttu-id="24044-112">Обратите внимание, что **вариант** выделяется и освобождается клиентом.</span><span class="sxs-lookup"><span data-stu-id="24044-112">Note that the **VARIANT** is allocated and freed by the client.</span></span>
-   <span data-ttu-id="24044-113">Для простых элементов ИДЕНТИФИКАТОРом дочернего элемента является любое 32-разрядное положительное целое число.</span><span class="sxs-lookup"><span data-stu-id="24044-113">For simple elements, the child ID is any 32-bit positive integer.</span></span> <span data-ttu-id="24044-114">Обратите внимание, что ноль и отрицательные целые числа зарезервированы корпорацией Майкрософт Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="24044-114">Note that zero and negative integers are reserved by Microsoft Active Accessibility.</span></span> <span data-ttu-id="24044-115">Задайте для элемента **VT** структуры [**Variant**](variant-structure.md) значение VT \_ I4, а элемент **лвал** — идентификатор дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="24044-115">Set the [**VARIANT**](variant-structure.md) structure **vt** member to VT\_I4 and the **lVal** member to the child ID.</span></span>

<span data-ttu-id="24044-116">Если [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)не поддерживается, необходимо назначить дочерние идентификаторы и нумеровать дочерние объекты в каждом объекте последовательно, начиная с одного.</span><span class="sxs-lookup"><span data-stu-id="24044-116">If you do not support [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must assign child IDs and number the children in each object sequentially starting with one.</span></span>

<span data-ttu-id="24044-117">Рекомендуется, чтобы клиенты использовали функцию Microsoft Active Accessibility [**акцессиблечилдрен**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) , а не напрямую вызывать интерфейс [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) сервера.</span><span class="sxs-lookup"><span data-stu-id="24044-117">It is recommended that clients use the Microsoft Active Accessibility function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) rather than call the server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface directly.</span></span>

 

 