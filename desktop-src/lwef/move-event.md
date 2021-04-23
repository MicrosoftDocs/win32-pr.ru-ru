---
title: Переместить событие
description: Переместить событие
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888444"
---
# <a name="move-event"></a><span data-ttu-id="c425e-103">Переместить событие</span><span class="sxs-lookup"><span data-stu-id="c425e-103">Move Event</span></span>

<span data-ttu-id="c425e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c425e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c425e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="c425e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c425e-106">Происходит при перемещении символа.</span><span class="sxs-lookup"><span data-stu-id="c425e-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="c425e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c425e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c425e-108">Перемещение агента в **подсистеме**  \_ **(ByVal** *чарактерид*, **ByVal** *X*, **ByVal** *Y*, **ByVal** , *Причина \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="c425e-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="c425e-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="c425e-109">Part</span></span>          | <span data-ttu-id="c425e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c425e-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c425e-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="c425e-111">*CharacterID*</span></span> | <span data-ttu-id="c425e-112">Возвращает идентификатор перемещаемого символа.</span><span class="sxs-lookup"><span data-stu-id="c425e-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c425e-113">*X*</span><span class="sxs-lookup"><span data-stu-id="c425e-113">*X*</span></span>           | <span data-ttu-id="c425e-114">Возвращает координату по оси x (в пикселях) верхнего края нового расположения символьного кадра в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="c425e-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="c425e-115">*да*</span><span class="sxs-lookup"><span data-stu-id="c425e-115">*Y*</span></span>           | <span data-ttu-id="c425e-116">Возвращает координату по оси y (в пикселях) левого края нового расположения символьного кадра в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="c425e-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="c425e-117">*Причина*</span><span class="sxs-lookup"><span data-stu-id="c425e-117">*Cause*</span></span>       | <span data-ttu-id="c425e-118">Возвращает значение, указывающее, что привело к перемещению символа.</span><span class="sxs-lookup"><span data-stu-id="c425e-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="c425e-119">1 Пользователь переместил символ.</span><span class="sxs-lookup"><span data-stu-id="c425e-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="c425e-120">2 клиентское приложение переместило символ.</span><span class="sxs-lookup"><span data-stu-id="c425e-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="c425e-121">3 другое клиентское приложение переместило этот символ.</span><span class="sxs-lookup"><span data-stu-id="c425e-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="c425e-122">4 сервер агента переместил символ, чтобы он оставался на экране после изменения разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="c425e-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="c425e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c425e-123">Remarks</span></span>

<span data-ttu-id="c425e-124">Это событие возникает, когда пользователь или приложение изменяет расположение символа.</span><span class="sxs-lookup"><span data-stu-id="c425e-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="c425e-125">Координаты имеют отношение к левому верхнему углу экрана.</span><span class="sxs-lookup"><span data-stu-id="c425e-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="c425e-126">Это событие отправляется только клиентам символа (приложения, которые загрузили символ).</span><span class="sxs-lookup"><span data-stu-id="c425e-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="c425e-127">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="c425e-127">**See Also**</span></span>

<span data-ttu-id="c425e-128">[**Свойство мовекаусе**](movecause-property.md), [ **событие size**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="c425e-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 





