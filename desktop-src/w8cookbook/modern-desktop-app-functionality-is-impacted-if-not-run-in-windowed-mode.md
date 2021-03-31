---
title: Функциональность классических приложений затрагивается, если не выполняется в оконном режиме
description: В Windows 10 приложения Windows больше не отображаются по умолчанию. вместо этого они становятся оконными и такими операциями, как минимизация, восстановление, увеличение размеров, изменение размера (и любые другие операции, которые всегда были доступны в любом другом классическом окне приложения Windows).
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411232"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="7841a-103">Функциональность классических приложений затрагивается, если не выполняется в оконном режиме</span><span class="sxs-lookup"><span data-stu-id="7841a-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="7841a-104">В Windows 10 приложения Windows больше не отображаются по умолчанию. вместо этого они становятся оконными и такими операциями, как минимизация, восстановление, увеличение размеров, изменение размера (и любые другие операции, которые всегда были доступны в любом другом классическом окне приложения Windows).</span><span class="sxs-lookup"><span data-stu-id="7841a-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="7841a-105">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="7841a-105">Manifestations</span></span>

<span data-ttu-id="7841a-106">Наиболее заметным изменением теперь является то, что можно получить произвольный размер, который не просто является размером экрана или высоты экрана.</span><span class="sxs-lookup"><span data-stu-id="7841a-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="7841a-107">Пользователь может постоянно изменять размер окна приложения (до минимального размера окна приложения).</span><span class="sxs-lookup"><span data-stu-id="7841a-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="7841a-108">Это отличается от Windows 8,0 или Windows 8.1, где изменение размера окна было дискретным действием (пользователи изменяют эскиз окна, что привело к изменению размера окна после того, как пользователь зафиксировал действие).</span><span class="sxs-lookup"><span data-stu-id="7841a-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="7841a-109">Сегодня вместо изменения размера, когда пользователь перетаскивает окно по нижнему углу (или другому положению границы), он становится непрерывным изменением размера, а приложение принимает сообщения в строке, а не изменяет размер.</span><span class="sxs-lookup"><span data-stu-id="7841a-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="7841a-110">Устранение проблем</span><span class="sxs-lookup"><span data-stu-id="7841a-110">Mitigations</span></span>

<span data-ttu-id="7841a-111">Чтобы устранить эту возможность для приложений Windows 8,0 и 8,1, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7841a-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="7841a-112">Если ожидаемая функция в функциональности приложения нарушена, то устранение проблем пользователя заключается в том, чтобы перевести приложение в полноэкранный режим (с помощью кнопки "переход во весь экран" в правом верхнем углу строки заголовка).</span><span class="sxs-lookup"><span data-stu-id="7841a-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="7841a-113">Если запуск приложения повлияет на то, что он не открывается должным образом, то пользователь по-прежнему должен иметь возможность переключиться в режим планшета, чтобы приложение запускалось в полноэкранном режиме без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="7841a-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="7841a-114">Для этого лучше всего изменить приложение таким образом, чтобы оно было известно о том, что его размер может быть не меньше размера монитора (т. е. у вас нет жестко зафиксированной таблицы высотой или ширины, и только для них, а также для ожидания жестко пропорций).</span><span class="sxs-lookup"><span data-stu-id="7841a-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="7841a-115">Разработчики приложений должны рассчитывать на то, что при изменении размера приложения другое сообщение об изменении размера может произойти сразу после доставки сообщения о текущем изменении размера. в результате, если приложение запускает анимацию во время изменения размера, возможно, приложение может получить другое сообщение об изменении размера после (поэтому важно убедиться, что этот тип ситуации не приводит к сбою приложения).</span><span class="sxs-lookup"><span data-stu-id="7841a-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




