---
title: Мовекаусе, свойство
description: Мовекаусе, свойство
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888447"
---
# <a name="movecause-property"></a><span data-ttu-id="533b3-103">Мовекаусе, свойство</span><span class="sxs-lookup"><span data-stu-id="533b3-103">MoveCause Property</span></span>

<span data-ttu-id="533b3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="533b3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="533b3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="533b3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="533b3-106">Возвращает целочисленное значение, указывающее, что привело к последнему перемещению символа.</span><span class="sxs-lookup"><span data-stu-id="533b3-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="533b3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="533b3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="533b3-108">*Агент*. **Символы ("***чарактерид***"). Мовекаусе**</span><span class="sxs-lookup"><span data-stu-id="533b3-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="533b3-109">Значение</span><span class="sxs-lookup"><span data-stu-id="533b3-109">Value</span></span> | <span data-ttu-id="533b3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="533b3-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="533b3-111">0</span><span class="sxs-lookup"><span data-stu-id="533b3-111">0</span></span>     | <span data-ttu-id="533b3-112">Символ не был перемещен.</span><span class="sxs-lookup"><span data-stu-id="533b3-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="533b3-113">1</span><span class="sxs-lookup"><span data-stu-id="533b3-113">1</span></span>     | <span data-ttu-id="533b3-114">Пользователь переместил символ.</span><span class="sxs-lookup"><span data-stu-id="533b3-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="533b3-115">2</span><span class="sxs-lookup"><span data-stu-id="533b3-115">2</span></span>     | <span data-ttu-id="533b3-116">Приложение переместило символ.</span><span class="sxs-lookup"><span data-stu-id="533b3-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="533b3-117">3</span><span class="sxs-lookup"><span data-stu-id="533b3-117">3</span></span>     | <span data-ttu-id="533b3-118">Символ был перемещен другим клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="533b3-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="533b3-119">4</span><span class="sxs-lookup"><span data-stu-id="533b3-119">4</span></span>     | <span data-ttu-id="533b3-120">Сервер агента переместил символ, чтобы он оставался на экране после изменения разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="533b3-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="533b3-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="533b3-121">Remarks</span></span>

<span data-ttu-id="533b3-122">Это свойство можно использовать для определения того, что привело к перемещению символа, когда несколько приложений совместно используют один и тот же символ.</span><span class="sxs-lookup"><span data-stu-id="533b3-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="533b3-123">Эти значения совпадают с значениями, возвращаемыми событием [**Move**](move-event.md) .</span><span class="sxs-lookup"><span data-stu-id="533b3-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="533b3-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="533b3-124">See Also</span></span>

<span data-ttu-id="533b3-125">[**Событие перемещения**](move-event.md), [ **метод moveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="533b3-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




