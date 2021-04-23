---
description: Следующие функции обеспечивают поддержку нескольких мониторов.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Функции нескольких мониторов экрана
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984928"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="3f5dc-103">Функции нескольких мониторов экрана</span><span class="sxs-lookup"><span data-stu-id="3f5dc-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="3f5dc-104">Следующие функции обеспечивают поддержку нескольких мониторов.</span><span class="sxs-lookup"><span data-stu-id="3f5dc-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="3f5dc-105">Функция</span><span class="sxs-lookup"><span data-stu-id="3f5dc-105">Function</span></span>                                           | <span data-ttu-id="3f5dc-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3f5dc-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f5dc-107">**енумдисплаймониторс**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="3f5dc-108">Перечисляет мониторы, пересекающие регион, образованный пересечением указанного прямоугольника обрезки и видимой области контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="3f5dc-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="3f5dc-109">**жетмониторинфо**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="3f5dc-110">Извлекает сведения о мониторе отображения.</span><span class="sxs-lookup"><span data-stu-id="3f5dc-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="3f5dc-111">**мониторенумпрок**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="3f5dc-112">Определяемая приложением функция обратного вызова, вызываемая функцией [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="3f5dc-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="3f5dc-113">**мониторфромпоинт**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="3f5dc-114">Извлекает маркер монитора, который содержит указанную точку.</span><span class="sxs-lookup"><span data-stu-id="3f5dc-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="3f5dc-115">**мониторфромрект**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="3f5dc-116">Извлекает маркер монитора, который имеет большую часть пересечения с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="3f5dc-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="3f5dc-117">**мониторфромвиндов**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="3f5dc-118">Извлекает маркер монитора, который имеет большую часть пересечения с ограничивающим прямоугольником заданного окна.</span><span class="sxs-lookup"><span data-stu-id="3f5dc-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



