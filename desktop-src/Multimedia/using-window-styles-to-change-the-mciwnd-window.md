---
title: Использование стилей окна для изменения окна МЦивнд
description: Использование стилей окна для изменения окна МЦивнд
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Функция МЦивндкреате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661697"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="5cc06-104">Использование стилей окна для изменения окна МЦивнд</span><span class="sxs-lookup"><span data-stu-id="5cc06-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="5cc06-105">Как и в любом окне, можно изменить внешний вид и поведение окна МЦивнд, выбрав стандартные стили окон, указанные с помощью функции [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="5cc06-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="5cc06-106">Кроме того, можно выбрать один из нескольких других стилей окна, относящихся к МЦивнд окнам.</span><span class="sxs-lookup"><span data-stu-id="5cc06-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="5cc06-107">С этими стилями приложение может изменить МЦивнд окна следующими способами:</span><span class="sxs-lookup"><span data-stu-id="5cc06-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="5cc06-108">Измените размер окна.</span><span class="sxs-lookup"><span data-stu-id="5cc06-108">Change window size.</span></span>
-   <span data-ttu-id="5cc06-109">Скрытие или отображение элементов управления.</span><span class="sxs-lookup"><span data-stu-id="5cc06-109">Hide or display controls.</span></span>
-   <span data-ttu-id="5cc06-110">Выдача сообщений об уведомлениях.</span><span class="sxs-lookup"><span data-stu-id="5cc06-110">Issue notification messages.</span></span>
-   <span data-ttu-id="5cc06-111">Отображение сведений в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="5cc06-111">Display information in the title bar.</span></span>

<span data-ttu-id="5cc06-112">Стили окна можно задать, указав их в функции [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) , или можно использовать макрос [**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) для изменения стиля существующего окна мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="5cc06-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="5cc06-113">Вы также можете запросить окно МЦивнд для его текущих стилей с помощью макроса [**мЦивнджетстилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="5cc06-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="5cc06-114">Список стилей окон, относящихся к МЦивнд, см. в разделе [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="5cc06-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 