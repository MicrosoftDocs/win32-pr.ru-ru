---
title: Плоская полоса прокрутки
description: В этом разделе содержатся сведения об элементах программирования, используемых для управления плоскими полосами прокрутки.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887951"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="24821-103">Плоская полоса прокрутки</span><span class="sxs-lookup"><span data-stu-id="24821-103">Flat Scroll Bar</span></span>

<span data-ttu-id="24821-104">В этом разделе содержатся сведения об элементах программирования, используемых для управления плоскими полосами прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="24821-105">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="24821-105">Overviews</span></span>



| <span data-ttu-id="24821-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="24821-106">Topic</span></span>                                    | <span data-ttu-id="24821-107">Содержимое</span><span class="sxs-lookup"><span data-stu-id="24821-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24821-108">Плоские полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="24821-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="24821-109">В Microsoft Internet Explorer 4,0 появилась новая визуальная технология, называемая плоскими полосами прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="24821-110">Функционально плоские полосы прокрутки ведут себя так же, как стандартные полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="24821-111">Разница заключается в том, что их внешний вид можно изменить на более высокий, чем стандартные полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="24821-112">Функции</span><span class="sxs-lookup"><span data-stu-id="24821-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24821-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="24821-113">Topic</span></span></th>
<th><span data-ttu-id="24821-114">Содержимое</span><span class="sxs-lookup"><span data-stu-id="24821-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24821-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="24821-116">Включает или отключает одну или обе кнопки направления ориентации полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="24821-117">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>енаблескроллбар</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24821-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="24821-119">Возвращает сведения для плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="24821-120">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>жетскроллинфо</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24821-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="24821-122">Возвращает расположение бегунка в плоской полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="24821-123">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>жетскроллпос</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24821-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="24821-125">Возвращает свойства для плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="24821-126">Эта функция также может использоваться для определения того, была ли вызвана <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>инитиализефлатсб</strong></a> для этого окна.</span><span class="sxs-lookup"><span data-stu-id="24821-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24821-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="24821-128">Возвращает свойства для плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="24821-129">Эта функция также может использоваться для определения того, была ли вызвана <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>инитиализефлатсб</strong></a> для этого окна.</span><span class="sxs-lookup"><span data-stu-id="24821-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="24821-130">Это идентично <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="24821-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24821-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="24821-132">Возвращает диапазон прокрутки для плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="24821-133">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>жетскроллранже</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24821-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="24821-135">Задает сведения для плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="24821-136">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>сетскроллинфо</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24821-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="24821-138">Задает текущую точку бегунка в плоской полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="24821-139">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>сетскроллпос</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24821-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="24821-141">Задает свойства для плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24821-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="24821-143">Задает диапазон прокрутки плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="24821-144">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>сетскроллранже</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24821-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="24821-146">Показывает или скрывает плоскую полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="24821-147">Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>шовскроллбар</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="24821-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24821-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>инитиализефлатсб</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="24821-149">Инициализирует плоские полосы прокрутки для определенного окна.</span><span class="sxs-lookup"><span data-stu-id="24821-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24821-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>унинитиализефлатсб</strong></a></span><span class="sxs-lookup"><span data-stu-id="24821-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="24821-151">Отменяет инициализацию плоских полос прокрутки для конкретного окна.</span><span class="sxs-lookup"><span data-stu-id="24821-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="24821-152">Указанное окно вернется к стандартным полосам прокрутки.</span><span class="sxs-lookup"><span data-stu-id="24821-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 





