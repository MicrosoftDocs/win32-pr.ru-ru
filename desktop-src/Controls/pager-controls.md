---
title: Сведения об элементах управления страничного навигатора
description: Элемент управления страничного навигатора — это контейнер окон, который используется с окном, у которого недостаточно отображаемой области для отображения всего содержимого.
ms.assetid: VS|Controls|~\controls\pager\pager.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d0b5aa01b72ca5feb8170d6d9fd218a433509b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774471"
---
# <a name="about-pager-controls"></a><span data-ttu-id="310f6-103">Сведения об элементах управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="310f6-103">About Pager Controls</span></span>

<span data-ttu-id="310f6-104">*Элемент управления страничного навигатора* — это контейнер окон, который используется с окном, у которого недостаточно отображаемой области для отображения всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="310f6-104">A *pager control* is a window container that is used with a window that does not have enough display area to show all of its content.</span></span> <span data-ttu-id="310f6-105">Элемент управления страничный навигатор позволяет пользователю выполнить прокрутку до области окна, которая в настоящий момент не находится в представлении.</span><span class="sxs-lookup"><span data-stu-id="310f6-105">The pager control allows the user to scroll to the area of the window that is not currently in view.</span></span>

-   [<span data-ttu-id="310f6-106">Сведения об элементах управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="310f6-106">About Pager Controls</span></span>](#about-pager-controls)

## <a name="about-pager-controls"></a><span data-ttu-id="310f6-107">Сведения об элементах управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="310f6-107">About Pager Controls</span></span>

<span data-ttu-id="310f6-108">В Microsoft Internet Explorer версии 4,0 (commctrl.dll версии 4,71) представлен элемент управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="310f6-108">Microsoft Internet Explorer Version 4.0 (commctrl.dll version 4.71) introduces the pager control.</span></span> <span data-ttu-id="310f6-109">Этот элемент управления полезен в ситуациях, когда окно не имеет достаточной области для вывода дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="310f6-109">This control is useful in situations where a window does not have enough area to display a child window.</span></span> <span data-ttu-id="310f6-110">Например, если приложение имеет недостаточную панель инструментов для отображения всех ее элементов, можно назначить панель инструментов элементу управления страничного навигатора, а пользователи смогут прокручиваться влево или вправо для доступа ко всем элементам.</span><span class="sxs-lookup"><span data-stu-id="310f6-110">For example, if your application has a toolbar that is not wide enough to show all of its items, you can assign the toolbar to a pager control and users will be able to scroll to the left or right to access all of the items.</span></span> <span data-ttu-id="310f6-111">Можно также создавать элементы управления страничного навигатора, которые прокручиваются вертикально.</span><span class="sxs-lookup"><span data-stu-id="310f6-111">You can also create pager controls that scroll vertically.</span></span>

<span data-ttu-id="310f6-112">Окно, назначенное элементу управления страничного навигатора, называется *автономным окном*.</span><span class="sxs-lookup"><span data-stu-id="310f6-112">A window assigned to the pager control is referred to as the *contained window*.</span></span>

<span data-ttu-id="310f6-113">На следующем снимке экрана показана панель инструментов, содержащаяся внутри элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="310f6-113">The following screen shot shows a toolbar contained inside a pager control.</span></span> <span data-ttu-id="310f6-114">Элемент управления страничный навигатор отображается красным цветом, чтобы показать, какие области элемента управления видимы.</span><span class="sxs-lookup"><span data-stu-id="310f6-114">The pager control is displayed in red to show what areas of the control are visible.</span></span>

![снимок экрана с небольшим окном с примером панели инструментов внутри элемента управления страничного навигатора](images/pager.jpg)

> [!Note]  
> <span data-ttu-id="310f6-116">Элемент управления страничного навигатора реализован в версии 4,71 и более поздних Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="310f6-116">The pager control is implemented in version 4.71 and later of Comctl32.dll.</span></span>

 

 

 




