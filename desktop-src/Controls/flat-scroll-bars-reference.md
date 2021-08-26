---
title: Плоская полоса прокрутки
description: В этом разделе содержатся сведения об элементах программирования, используемых для управления плоскими полосами прокрутки.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466601"
---
# <a name="flat-scroll-bar"></a>Плоская полоса прокрутки

В этом разделе содержатся сведения об элементах программирования, используемых для управления плоскими полосами прокрутки.

### <a name="overviews"></a>Разделы общих сведений



| Раздел                                    | Содержимое                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Плоские полосы прокрутки](flat-scroll-bars.md) | В Microsoft Internet Explorer 4,0 появилась новая визуальная технология, называемая плоскими полосами прокрутки. Функционально плоские полосы прокрутки ведут себя так же, как стандартные полосы прокрутки. Разница заключается в том, что их внешний вид можно изменить на более высокий, чем стандартные полосы прокрутки.<br/> |



 

### <a name="functions"></a>Функции




| Раздел | Содержимое | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | Включает или отключает одну или обе кнопки направления ориентации полосы прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>енаблескроллбар</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | Возвращает сведения для плоской полосы прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>жетскроллинфо</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | Возвращает расположение бегунка в плоской полосе прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>жетскроллпос</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | Возвращает свойства для плоской полосы прокрутки. Эта функция также может использоваться для определения того, была ли вызвана <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>инитиализефлатсб</strong></a> для этого окна. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | Возвращает свойства для плоской полосы прокрутки. Эта функция также может использоваться для определения того, была ли вызвана <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>инитиализефлатсб</strong></a> для этого окна.<blockquote>[!Note]<br />Это идентично <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | Возвращает диапазон прокрутки для плоской полосы прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>жетскроллранже</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | Задает сведения для плоской полосы прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>сетскроллинфо</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | Задает текущую точку бегунка в плоской полосе прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>сетскроллпос</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | Задает свойства для плоской полосы прокрутки. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | Задает диапазон прокрутки плоской полосы прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>сетскроллранже</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | Показывает или скрывает плоскую полосу прокрутки. Если плоские полосы прокрутки не инициализированы для окна, эта функция вызывает стандартную функцию <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>шовскроллбар</strong></a> . <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>инитиализефлатсб</strong></a> | Инициализирует плоские полосы прокрутки для определенного окна. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>унинитиализефлатсб</strong></a> | Отменяет инициализацию плоских полос прокрутки для конкретного окна. Указанное окно вернется к стандартным полосам прокрутки. <br /> | 




 

 

 





