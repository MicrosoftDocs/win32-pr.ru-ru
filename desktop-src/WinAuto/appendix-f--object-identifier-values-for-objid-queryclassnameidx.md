---
title: Приложение F значения идентификатора объекта для OBJID_QUERYCLASSNAMEIDX
description: Когда ОЛЕАКК отправляет сообщение WM \_ GetObject с параметром lParam, установленным в значение обжидкуерикласснамеидкс, многие стандартные пользовательские или стандартные элементы управления (комктл) возвращают одно из следующих значений.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691612"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="c585f-103">Приложение F. значения идентификаторов объектов для OBJID \_ куерикласснамеидкс</span><span class="sxs-lookup"><span data-stu-id="c585f-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="c585f-104">Когда ОЛЕАКК отправляет сообщение [**WM \_ GetObject**](wm-getobject.md) с параметром *lParam* , установленным в значение обжидкуерикласснамеидкс, многие стандартные пользовательские или стандартные элементы управления (комктл) возвращают одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c585f-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="c585f-105">ПОЛЬЗОВАТЕЛЬ или общий элемент управления</span><span class="sxs-lookup"><span data-stu-id="c585f-105">USER or common control</span></span> | <span data-ttu-id="c585f-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c585f-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c585f-107">Listbox</span><span class="sxs-lookup"><span data-stu-id="c585f-107">Listbox</span></span>                | <span data-ttu-id="c585f-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="c585f-108">65536+0</span></span>      |
| <span data-ttu-id="c585f-109">Кнопка</span><span class="sxs-lookup"><span data-stu-id="c585f-109">Button</span></span>                 | <span data-ttu-id="c585f-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="c585f-110">65536+2</span></span>      |
| <span data-ttu-id="c585f-111">Статические</span><span class="sxs-lookup"><span data-stu-id="c585f-111">Static</span></span>                 | <span data-ttu-id="c585f-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="c585f-112">65536+3</span></span>      |
| <span data-ttu-id="c585f-113">Изменить</span><span class="sxs-lookup"><span data-stu-id="c585f-113">Edit</span></span>                   | <span data-ttu-id="c585f-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="c585f-114">65536+4</span></span>      |
| <span data-ttu-id="c585f-115">Combobox</span><span class="sxs-lookup"><span data-stu-id="c585f-115">Combobox</span></span>               | <span data-ttu-id="c585f-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="c585f-116">65536+5</span></span>      |
| <span data-ttu-id="c585f-117">Полоса прокрутки</span><span class="sxs-lookup"><span data-stu-id="c585f-117">Scrollbar</span></span>              | <span data-ttu-id="c585f-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="c585f-118">65536+10</span></span>     |
| <span data-ttu-id="c585f-119">Состояние</span><span class="sxs-lookup"><span data-stu-id="c585f-119">Status</span></span>                 | <span data-ttu-id="c585f-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="c585f-120">65536+11</span></span>     |
| <span data-ttu-id="c585f-121">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="c585f-121">Toolbar</span></span>                | <span data-ttu-id="c585f-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="c585f-122">65536+12</span></span>     |
| <span data-ttu-id="c585f-123">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="c585f-123">Progress</span></span>               | <span data-ttu-id="c585f-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="c585f-124">65536+13</span></span>     |
| <span data-ttu-id="c585f-125">Анимируемого</span><span class="sxs-lookup"><span data-stu-id="c585f-125">Animate</span></span>                | <span data-ttu-id="c585f-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="c585f-126">65536+14</span></span>     |
| <span data-ttu-id="c585f-127">Вкладка</span><span class="sxs-lookup"><span data-stu-id="c585f-127">Tab</span></span>                    | <span data-ttu-id="c585f-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="c585f-128">65536+15</span></span>     |
| <span data-ttu-id="c585f-129">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="c585f-129">Hotkey</span></span>                 | <span data-ttu-id="c585f-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="c585f-130">65536+16</span></span>     |
| <span data-ttu-id="c585f-131">Header</span><span class="sxs-lookup"><span data-stu-id="c585f-131">Header</span></span>                 | <span data-ttu-id="c585f-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="c585f-132">65536+17</span></span>     |
| <span data-ttu-id="c585f-133">TrackBar</span><span class="sxs-lookup"><span data-stu-id="c585f-133">Trackbar</span></span>               | <span data-ttu-id="c585f-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="c585f-134">65536+18</span></span>     |
| <span data-ttu-id="c585f-135">Элементе</span><span class="sxs-lookup"><span data-stu-id="c585f-135">Listview</span></span>               | <span data-ttu-id="c585f-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="c585f-136">65536+19</span></span>     |
| <span data-ttu-id="c585f-137">-Координаты центра</span><span class="sxs-lookup"><span data-stu-id="c585f-137">Updown</span></span>                 | <span data-ttu-id="c585f-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="c585f-138">65536+22</span></span>     |
| <span data-ttu-id="c585f-139">Подсказки</span><span class="sxs-lookup"><span data-stu-id="c585f-139">ToolTips</span></span>               | <span data-ttu-id="c585f-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="c585f-140">65536+24</span></span>     |
| <span data-ttu-id="c585f-141">Дерева</span><span class="sxs-lookup"><span data-stu-id="c585f-141">Treeview</span></span>               | <span data-ttu-id="c585f-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="c585f-142">65536+25</span></span>     |
| <span data-ttu-id="c585f-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="c585f-143">RichEdit</span></span>               | <span data-ttu-id="c585f-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="c585f-144">65536+28</span></span>     |



 

<span data-ttu-id="c585f-145">Только пользовательские и обычные элементы управления Windows (КОМКТЛ) будут возвращать одно из значений из таблицы.</span><span class="sxs-lookup"><span data-stu-id="c585f-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="c585f-146">Если окно возвращает 0 в ответ на это сообщение, окно может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="c585f-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="c585f-147">Пользовательский элемент управления</span><span class="sxs-lookup"><span data-stu-id="c585f-147">A custom control</span></span>
-   <span data-ttu-id="c585f-148">Элемент управления, отличный от одного из элементов управления в предыдущей таблице</span><span class="sxs-lookup"><span data-stu-id="c585f-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="c585f-149">Старая версия элемента управления системы, не распознающая сообщение [**WM \_ GetObject**](wm-getobject.md)</span><span class="sxs-lookup"><span data-stu-id="c585f-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="c585f-150">Если окно возвращает значение 0, то клиентам может потребоваться использовать [**реалжетвиндовкласс**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) или [**className**](/windows/win32/api/winuser/nf-winuser-getclassname).</span><span class="sxs-lookup"><span data-stu-id="c585f-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="c585f-151">Эти функции можно использовать для определения типа элемента управления на основе имени класса.</span><span class="sxs-lookup"><span data-stu-id="c585f-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="c585f-152">Как правило, клиенты могут использовать сведения, предоставляемые ОЛЕАКК.</span><span class="sxs-lookup"><span data-stu-id="c585f-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 