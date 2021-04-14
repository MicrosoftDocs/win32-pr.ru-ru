---
title: Использование элементов управления "Вкладка"
description: В этом разделе содержатся два примера использования элементов управления "Вкладка".
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488417"
---
# <a name="using-tab-controls"></a><span data-ttu-id="d2bb1-103">Использование элементов управления "Вкладка"</span><span class="sxs-lookup"><span data-stu-id="d2bb1-103">Using Tab Controls</span></span>

<span data-ttu-id="d2bb1-104">В этом разделе содержатся два примера использования элементов управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="d2bb1-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="d2bb1-105">В первом примере показано, как использовать элемент управления "Вкладка" для переключения между несколькими страницами текста в главном окне приложения.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="d2bb1-106">Во втором примере демонстрируется использование элемента управления "Вкладка" для переключения между несколькими страницами элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d2bb1-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d2bb1-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2bb1-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="d2bb1-108">Topic</span></span></th>
<th><span data-ttu-id="d2bb1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d2bb1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2bb1-110"><a href="create-a-tab-control-in-the-main-window.md">Создание элемента управления "Вкладка" в главном окне</a></span><span class="sxs-lookup"><span data-stu-id="d2bb1-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="d2bb1-111">В примере в этом разделе показано, как создать элемент управления "Вкладка" и отобразить его в клиентской области главного окна приложения.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="d2bb1-112">Приложение отображает третье окно (статический элемент управления) в области отображения элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="d2bb1-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="d2bb1-113">Родительское окно размещает и изменяет размеры элемента управления Tab и статического элемента управления при обработке сообщения <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2bb1-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="d2bb1-114">В этом примере есть семь вкладок, по одному на каждый день недели.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="d2bb1-115">Когда пользователь выбирает вкладку, приложение отображает имя соответствующего дня в статическом элементе управления.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2bb1-116"><a href="create-a-tabbed-dialog-box.md">Создание диалогового окна с вкладками</a></span><span class="sxs-lookup"><span data-stu-id="d2bb1-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="d2bb1-117">В примере в этом разделе показано, как создать диалоговое окно, в котором используются вкладки для предоставления нескольких страниц элементов управления.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="d2bb1-118">Главное диалоговое окно является модальным диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="d2bb1-119">Каждая страница элементов управления определяется шаблоном диалогового окна с <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> стилем.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="d2bb1-120">Если выбрана вкладка, то для страницы «входящие» создается немодальное диалоговое окно, и диалоговое окно для исходящей страницы уничтожается.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2bb1-121">Во многих случаях можно легко реализовать несколько диалоговых окон с помощью страниц свойств.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="d2bb1-122">Дополнительные сведения о страницах свойств см. в разделе <a href="property-sheets.md">сведения о страницах свойств</a>.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="d2bb1-123">Шаблон для главного диалогового окна просто определяет два элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="d2bb1-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="d2bb1-124">При обработке <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> сообщения процедура диалогового окна создает элемент управления «вкладка» и загружает ресурсы шаблона диалогового окна для каждого из дочерних диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="d2bb1-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

