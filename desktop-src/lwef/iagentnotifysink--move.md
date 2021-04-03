---
title: Иажентнотифисинк перемещение
description: Иажентнотифисинк перемещение
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986780"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="3de1c-103">Иажентнотифисинк:: Move</span><span class="sxs-lookup"><span data-stu-id="3de1c-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="3de1c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3de1c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="3de1c-105">Уведомляет клиентское приложение, когда символ был перемещен.</span><span class="sxs-lookup"><span data-stu-id="3de1c-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="3de1c-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3de1c-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="3de1c-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="3de1c-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="3de1c-108">Идентификатор перемещенного символа.</span><span class="sxs-lookup"><span data-stu-id="3de1c-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="3de1c-109"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="3de1c-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="3de1c-110">Координата по оси x нового положения в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="3de1c-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="3de1c-111">Расположение символа основано на левом верхнем углу фрейма анимации.</span><span class="sxs-lookup"><span data-stu-id="3de1c-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="3de1c-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="3de1c-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="3de1c-113">Координата по оси y нового положения в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="3de1c-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="3de1c-114">Расположение символа основано на левом верхнем углу фрейма анимации.</span><span class="sxs-lookup"><span data-stu-id="3de1c-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="3de1c-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*двкаусе*</span><span class="sxs-lookup"><span data-stu-id="3de1c-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="3de1c-116">Причина перемещения символа.</span><span class="sxs-lookup"><span data-stu-id="3de1c-116">The cause of the character move.</span></span> <span data-ttu-id="3de1c-117">Параметр может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="3de1c-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="3de1c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3de1c-118">Value</span></span>                                                          | <span data-ttu-id="3de1c-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3de1c-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3de1c-120">**const без знака Short** **невермовед = 0;**</span><span class="sxs-lookup"><span data-stu-id="3de1c-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="3de1c-121">Символ не был перемещен.</span><span class="sxs-lookup"><span data-stu-id="3de1c-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="3de1c-122">**const без знака Short** **усермовед = 1;**</span><span class="sxs-lookup"><span data-stu-id="3de1c-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="3de1c-123">Пользователь переместил символ.</span><span class="sxs-lookup"><span data-stu-id="3de1c-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="3de1c-124">**const без знака Short** **программовед = 2;**</span><span class="sxs-lookup"><span data-stu-id="3de1c-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="3de1c-125">Приложение переместило символ.</span><span class="sxs-lookup"><span data-stu-id="3de1c-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="3de1c-126">**const без знака Short** **осерпрограммовед = 3;**</span><span class="sxs-lookup"><span data-stu-id="3de1c-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="3de1c-127">Символ был перемещен другим приложением.</span><span class="sxs-lookup"><span data-stu-id="3de1c-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="3de1c-128">**const без знака Short** **системмовед = 4**</span><span class="sxs-lookup"><span data-stu-id="3de1c-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="3de1c-129">Сервер переместил символ, чтобы он оставался на экране после изменения разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="3de1c-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="3de1c-130">Это событие отправляется всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="3de1c-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="3de1c-131">См. также:</span><span class="sxs-lookup"><span data-stu-id="3de1c-131">See Also</span></span>

<span data-ttu-id="3de1c-132">[**Иажентчарактер:: жетмовекаусе**](iagentcharacter--getmovecause.md), [ **иажентчарактер:: MoveTo**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="3de1c-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 





