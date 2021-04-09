---
title: Иажентчарактерекс Шовпопупмену
description: Иажентчарактерекс Шовпопупмену
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888715"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="04a2b-103">Иажентчарактерекс:: Шовпопупмену</span><span class="sxs-lookup"><span data-stu-id="04a2b-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="04a2b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04a2b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="04a2b-105">Отображает всплывающее меню для символа.</span><span class="sxs-lookup"><span data-stu-id="04a2b-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="04a2b-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="04a2b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="04a2b-107"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="04a2b-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="04a2b-108">Координата x всплывающего меню символа в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="04a2b-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="04a2b-109"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="04a2b-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="04a2b-110">Координата y всплывающего меню символа (в пикселях) относительно начала координат экрана (вверху слева).</span><span class="sxs-lookup"><span data-stu-id="04a2b-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="04a2b-111">При установке [**иажентчарактерекс:: сетаутопопупмену**](iagentcharacterex--setautopopupmenu.md) в **значение false** сервер больше не будет автоматически отображать меню при щелчке символа или его значка на панели задач.</span><span class="sxs-lookup"><span data-stu-id="04a2b-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="04a2b-112">Этот метод можно использовать для вывода меню.</span><span class="sxs-lookup"><span data-stu-id="04a2b-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="04a2b-113">Меню отображается до тех пор, пока пользователь не выберет команду или не отобразит другое меню.</span><span class="sxs-lookup"><span data-stu-id="04a2b-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="04a2b-114">В каждый момент времени может отображаться только одно всплывающее меню; Поэтому вызовы этого метода будут отменяться (удалить) из предыдущего меню.</span><span class="sxs-lookup"><span data-stu-id="04a2b-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="04a2b-115">Этот метод следует вызывать только в том случае, если клиентское приложение является активным клиентом символа. в противном случае произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="04a2b-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="04a2b-116">**Иажентчарактерекс:: Сетаутопопупмену**</span><span class="sxs-lookup"><span data-stu-id="04a2b-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 




