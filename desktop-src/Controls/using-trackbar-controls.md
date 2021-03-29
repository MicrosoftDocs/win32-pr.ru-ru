---
title: Использование элементов управления TrackBar
description: В этом разделе содержатся сведения о реализации и примеры элементов управления TrackBar.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775557"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="35758-103">Использование элементов управления TrackBar</span><span class="sxs-lookup"><span data-stu-id="35758-103">Using Trackbar Controls</span></span>

<span data-ttu-id="35758-104">В этом разделе содержатся сведения о реализации и примеры элементов управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="35758-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35758-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="35758-105">In this section</span></span>



| <span data-ttu-id="35758-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="35758-106">Topic</span></span>                                                                                                  | <span data-ttu-id="35758-107">Описание</span><span class="sxs-lookup"><span data-stu-id="35758-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35758-108">Создание линейки значений</span><span class="sxs-lookup"><span data-stu-id="35758-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="35758-109">При создании значения TrackBar инициализируются и его диапазон, и диапазон выбора.</span><span class="sxs-lookup"><span data-stu-id="35758-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="35758-110">Размер страницы также задается в данный момент.</span><span class="sxs-lookup"><span data-stu-id="35758-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="35758-111">Обработка сообщений с уведомлениями TrackBar</span><span class="sxs-lookup"><span data-stu-id="35758-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="35758-112">Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="35758-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="35758-113">Ограничение перемещения ползунка</span><span class="sxs-lookup"><span data-stu-id="35758-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="35758-114">Как описано в разделе [о элементах управления TrackBar](trackbar-controls.md), можно отключить часть диапазона TrackBar в качестве диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="35758-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="35758-115">Одной из целей диапазона выбора может быть ограничение перемещения ползунка, что делает некоторые части ограничений полного диапазона.</span><span class="sxs-lookup"><span data-stu-id="35758-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="35758-116">Использование дружественных окон</span><span class="sxs-lookup"><span data-stu-id="35758-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="35758-117">Настроив другие элементы управления как дружественные окна для TrackBar, можно автоматически размещать эти элементы управления на концах TrackBar в виде меток.</span><span class="sxs-lookup"><span data-stu-id="35758-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





