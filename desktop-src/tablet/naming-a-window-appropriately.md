---
description: Общие сведения о правильном именовании окна и настройке заголовка окна для планшетных ПК.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Правильное именование окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656653"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="18f64-103">Правильное именование окна</span><span class="sxs-lookup"><span data-stu-id="18f64-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="18f64-104">Присвойте каждому окну заголовку, понятному пользователю, даже если окно или его заголовок невидимы.</span><span class="sxs-lookup"><span data-stu-id="18f64-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="18f64-105">Это позволяет функции распознавания речи обнаруживать окно и иерархию окон.</span><span class="sxs-lookup"><span data-stu-id="18f64-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="18f64-106">Эта рекомендация относится ко всем окнам окон верхнего уровня с видимыми кадрами. дочерние окна, например плавающие палитры; пользовательские элементы управления; Toolbar и панели в окне, реализованные как дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="18f64-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="18f64-107">Существует три способа задать заголовок окна:</span><span class="sxs-lookup"><span data-stu-id="18f64-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="18f64-108">Задайте строку в скрипте ресурса при вызове [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или связанных функций.</span><span class="sxs-lookup"><span data-stu-id="18f64-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="18f64-109">Вызовите функцию [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="18f64-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="18f64-110">Определение имен элементов управления в диалоговых окнах с помощью методов, описанных в разделе [элементы управления именованием в диалоговых окнах](naming-controls-in-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="18f64-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="18f64-111">Это единственный метод для добавления метки к элементу управления "поле ввода", так как установка встроенной метки элементов управления изменяет содержимое элементов управления.</span><span class="sxs-lookup"><span data-stu-id="18f64-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="18f64-112">Вы можете запросить заголовок, используя либо Microsoft Active Accessibility, либо сообщение WM \_ gettext.</span><span class="sxs-lookup"><span data-stu-id="18f64-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="18f64-113">Дополнительные сведения о запросе заголовка с помощью Active Accessibility см. в разделе " [Специальные возможности](/windows/desktop/accessibility) ".</span><span class="sxs-lookup"><span data-stu-id="18f64-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
