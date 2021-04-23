---
title: Приложение б. Поддержка стандартного диспетчера диалоговых окон
description: Microsoft Active Accessibility обеспечивает полную поддержку стандартных элементов управления диалогового окна диспетчера диалоговых окон (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776403"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="4284e-103">Приложение б. Поддержка стандартного диспетчера диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="4284e-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="4284e-104">Microsoft Active Accessibility обеспечивает полную поддержку стандартных элементов управления диалогового окна диспетчера диалоговых окон (SDM).</span><span class="sxs-lookup"><span data-stu-id="4284e-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="4284e-105">Модель SDM — это внутренняя библиотека кода Майкрософт, которая предоставляет приложения Майкрософт со степенью независимости от различий между операционными системами Macintosh и Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4284e-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="4284e-106">Модель SDM в основном используется для диалоговых окон в Microsoft Excel и Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="4284e-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="4284e-107">В модели SDM представлены проблемы для вспомогательных функций, поскольку в ней используются нестандартные реализации диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="4284e-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="4284e-108">Например, кнопки диалогового окна модели SDM не используют оконные дескрипторы так же, как и стандартные элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4284e-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="4284e-109">Нельзя отправить сообщения кнопкам и кнопкам, не содержащимся в списке окон.</span><span class="sxs-lookup"><span data-stu-id="4284e-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="4284e-110">Приложение, использующее SDM, взаимодействует с элементом управления через частный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4284e-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="4284e-111">На следующем рисунке показан пример диалогового окна из Word.</span><span class="sxs-lookup"><span data-stu-id="4284e-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="4284e-112">Несмотря на то, что он выглядит как обычное диалоговое окно Windows, использующее элемент управления «вкладка», это действительно диалоговое окно SDM.</span><span class="sxs-lookup"><span data-stu-id="4284e-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![снимок экрана "диалоговое окно параметров с выбранной вкладкой" вид "](images/dialog.gif)

 

 




