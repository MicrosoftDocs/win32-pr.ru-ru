---
title: Оконные станции
description: Оконная станция содержит буфер обмена, таблицу Atom и один или несколько объектов рабочего стола. Каждый объект "станция окна" является защищаемым объектом. При создании станции Windows она связывается с вызывающим процессом и назначается текущему сеансу.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- объекты оконной станции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070176"
---
# <a name="window-stations"></a><span data-ttu-id="7c92f-106">Оконные станции</span><span class="sxs-lookup"><span data-stu-id="7c92f-106">Window Stations</span></span>

<span data-ttu-id="7c92f-107">*Оконная станция* содержит буфер обмена, таблицу Atom и один или несколько объектов [рабочего стола](desktops.md) .</span><span class="sxs-lookup"><span data-stu-id="7c92f-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="7c92f-108">Каждый объект "станция окна" является защищаемым объектом.</span><span class="sxs-lookup"><span data-stu-id="7c92f-108">Each window station object is a securable object.</span></span> <span data-ttu-id="7c92f-109">При создании станции Windows она связывается с вызывающим процессом и назначается текущему сеансу.</span><span class="sxs-lookup"><span data-stu-id="7c92f-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="7c92f-110">*Интерактивная станция окна* — единственная Оконная станция, которая может отображать пользовательский интерфейс или принимать вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="7c92f-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="7c92f-111">Он назначается сеансу входа интерактивного пользователя и содержит клавиатуру, мышь и устройство вывода.</span><span class="sxs-lookup"><span data-stu-id="7c92f-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="7c92f-112">Всегда имеет имя «WinSta0».</span><span class="sxs-lookup"><span data-stu-id="7c92f-112">It is always named "WinSta0".</span></span> <span data-ttu-id="7c92f-113">Все остальные оконные станции являются неинтерактивными. Это означает, что они не могут отображать пользовательский интерфейс или принимать входные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c92f-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="7c92f-114">Когда пользователь входит в систему с помощью службы удаленных рабочих столов, для пользователя запускается сеанс.</span><span class="sxs-lookup"><span data-stu-id="7c92f-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="7c92f-115">Каждый сеанс связан со своей собственной интерактивной рабочей станцией с именем «WinSta0».</span><span class="sxs-lookup"><span data-stu-id="7c92f-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="7c92f-116">Дополнительные сведения см. в разделе [Удаленный рабочий стол Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span><span class="sxs-lookup"><span data-stu-id="7c92f-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="7c92f-117">Дополнительные сведения о станциях Windows см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7c92f-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="7c92f-118">Создание оконной станции и рабочего стола</span><span class="sxs-lookup"><span data-stu-id="7c92f-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="7c92f-119">Обработка подключения к оконной станции</span><span class="sxs-lookup"><span data-stu-id="7c92f-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="7c92f-120">Права доступа и безопасность оконной станции</span><span class="sxs-lookup"><span data-stu-id="7c92f-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 