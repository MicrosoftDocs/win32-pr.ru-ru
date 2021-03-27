---
description: Почти все приложения используют экран для отображения данных, которыми они управляют.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: О рисовании и рисовании
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997298"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="a6d7d-103">О рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="a6d7d-103">About Painting and Drawing</span></span>

<span data-ttu-id="a6d7d-104">Почти все приложения используют экран для отображения данных, которыми они управляют.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="a6d7d-105">Приложение рисует изображения, отображает рисунки и записывает текст, чтобы пользователь мог просматривать данные по мере их создания, изменения и печати.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="a6d7d-106">В Microsoft Windows предусмотрена широкая поддержка рисования и рисования, но из-за природы многозадачных операционных систем приложения должны взаимодействовать друг с другом при доступе к экрану.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="a6d7d-107">Чтобы обеспечить бесперебойную работу всех приложений, система управляет всем выводом на экран.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="a6d7d-108">Приложения используют Windows в качестве основного выходного устройства, а не самого экрана.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="a6d7d-109">Система предоставляет контексты устройств, которые уникально соответствуют Windows.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="a6d7d-110">Приложения используют контексты устройств для направления выходных данных в указанные окна.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="a6d7d-111">Рисование в окне (направление вывода в него) не позволяет приложению противоречить выходным данным других приложений и позволяет приложениям сосуществовать друг с другом, одновременно используя все возможности графики системы.</span><span class="sxs-lookup"><span data-stu-id="a6d7d-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="a6d7d-112">Когда следует рисовать в окне</span><span class="sxs-lookup"><span data-stu-id="a6d7d-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="a6d7d-113">Сообщение WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="a6d7d-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="a6d7d-114">Рисование без сообщения WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="a6d7d-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="a6d7d-115">Система координат окна</span><span class="sxs-lookup"><span data-stu-id="a6d7d-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="a6d7d-116">Области окна</span><span class="sxs-lookup"><span data-stu-id="a6d7d-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="a6d7d-117">Фон окна</span><span class="sxs-lookup"><span data-stu-id="a6d7d-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="a6d7d-118">Уменьшенные окна</span><span class="sxs-lookup"><span data-stu-id="a6d7d-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="a6d7d-119">Измененные размеры окон</span><span class="sxs-lookup"><span data-stu-id="a6d7d-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="a6d7d-120">Неклиентская область</span><span class="sxs-lookup"><span data-stu-id="a6d7d-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="a6d7d-121">Регион обновления дочернего окна</span><span class="sxs-lookup"><span data-stu-id="a6d7d-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="a6d7d-122">Отображение устройств</span><span class="sxs-lookup"><span data-stu-id="a6d7d-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="a6d7d-123">Блокировка обновления окна</span><span class="sxs-lookup"><span data-stu-id="a6d7d-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="a6d7d-124">Накопленный ограничивающий прямоугольник</span><span class="sxs-lookup"><span data-stu-id="a6d7d-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



