---
title: таббингнотциклик
description: таббингнотциклик
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070227"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="fecf6-103">таббингнотциклик</span><span class="sxs-lookup"><span data-stu-id="fecf6-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="fecf6-104">Текст</span><span class="sxs-lookup"><span data-stu-id="fecf6-104">Text</span></span>

<span data-ttu-id="fecf6-105">Переход в этом приложении не является циклическим.</span><span class="sxs-lookup"><span data-stu-id="fecf6-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="fecf6-106">Переход вперед или назад {0} назад не возвращается к тому же элементу управления.</span><span class="sxs-lookup"><span data-stu-id="fecf6-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="fecf6-107">Тип</span><span class="sxs-lookup"><span data-stu-id="fecf6-107">Type</span></span>

<span data-ttu-id="fecf6-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="fecf6-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="fecf6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fecf6-109">Description</span></span>

<span data-ttu-id="fecf6-110">При использовании стандартной навигации с помощью клавиатуры (TAB или SHIFT + TAB) невозможно пройти по дереву элементов целевого объекта проверки, пока начальный элемент не станет конечным элементом (с использованием того же количества нажатий клавиш), отменив направление обхода.</span><span class="sxs-lookup"><span data-stu-id="fecf6-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="fecf6-111">Например, переход вперед (TAB) x раз от элемента A (0) к элементу A (x), а затем по нажатию клавиши TAB (Shift + Tab) x не приводит к тому, что элемент A (0) не восстанавливает фокус.</span><span class="sxs-lookup"><span data-stu-id="fecf6-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="fecf6-112">Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, так как нет предсказуемого способа вернуться к элементу управления после его посещения.</span><span class="sxs-lookup"><span data-stu-id="fecf6-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fecf6-113">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="fecf6-113">Possible causes</span></span>

-   <span data-ttu-id="fecf6-114">Элемент или его родитель является пользовательским элементом управления, который не реализует корректное выполнение вкладок.</span><span class="sxs-lookup"><span data-stu-id="fecf6-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="fecf6-115">Например, свойство состояния MSAA задано неправильно.</span><span class="sxs-lookup"><span data-stu-id="fecf6-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="fecf6-116">Некоторые приложения, например Блокнот, ведут себя иначе.</span><span class="sxs-lookup"><span data-stu-id="fecf6-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fecf6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="fecf6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fecf6-118">Рекомендации по проектированию пользовательского интерфейса клавиатуры</span><span class="sxs-lookup"><span data-stu-id="fecf6-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 