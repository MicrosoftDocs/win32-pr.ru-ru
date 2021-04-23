---
title: Создание стандартных элементов управления
description: В этом разделе описывается создание окна, принадлежащего классу окна, определенному в общей библиотеке элементов управления, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103987994"
---
# <a name="creating-common-controls"></a><span data-ttu-id="9478b-103">Создание стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="9478b-103">Creating Common Controls</span></span>

<span data-ttu-id="9478b-104">В этом разделе описывается создание окна, принадлежащего классу окна, определенному в общей библиотеке элементов управления, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="9478b-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="9478b-105">Большинство стандартных элементов управления принадлежат классу окна, определенному в библиотеке DLL общего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9478b-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="9478b-106">Класс Window и соответствующая процедура окна определяют свойства, внешний вид и поведение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9478b-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="9478b-107">Чтобы обеспечить загрузку библиотеки DLL Common Control, включите в приложение функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="9478b-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="9478b-108">Вы создаете общий элемент управления, указывая имя класса окна при вызове функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или указав соответствующее имя класса в шаблоне диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="9478b-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="9478b-109">Каждый тип общего элемента управления имеет набор стилей элементов управления, которые можно использовать для изменения внешнего вида и поведения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9478b-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="9478b-110">Общая библиотека элементов управления также включает набор стилей элементов управления, которые применяются к двум или более типам стандартных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="9478b-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="9478b-111">Общие стили элементов управления описаны в разделе [стили](common-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9478b-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9478b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9478b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9478b-113">Общие сведения об элементах управления</span><span class="sxs-lookup"><span data-stu-id="9478b-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 