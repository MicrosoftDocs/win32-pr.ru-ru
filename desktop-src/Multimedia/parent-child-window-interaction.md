---
title: Взаимодействие с окном Parent-Child
description: Взаимодействие с окном Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790548"
---
# <a name="parent-child-window-interaction"></a><span data-ttu-id="bb702-103">Взаимодействие с окном Parent-Child</span><span class="sxs-lookup"><span data-stu-id="bb702-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="bb702-104">Некоторые сообщения на уровне системы, такие как [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette), отправляются только в окна верхнего уровня и перекрывающихся окон.</span><span class="sxs-lookup"><span data-stu-id="bb702-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="bb702-105">Если окно записи является дочерним окном, его родительский элемент должен пересылать эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="bb702-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="bb702-106">Аналогично, если размер родительского окна изменится, может потребоваться отправить сообщения уведомления в окно Capture (захват).</span><span class="sxs-lookup"><span data-stu-id="bb702-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="bb702-107">И наоборот, при изменении размера записанного видео в окне Capture может потребоваться отправить уведомления родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="bb702-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="bb702-108">Самый простой способ управления этим — всегда сохранять размеры окна захвата равными размеру захваченного видеопотока, уведомляя родительский элемент при изменении этих измерений.</span><span class="sxs-lookup"><span data-stu-id="bb702-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb702-109">См. также</span><span class="sxs-lookup"><span data-stu-id="bb702-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb702-110">Окна захвата</span><span class="sxs-lookup"><span data-stu-id="bb702-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 