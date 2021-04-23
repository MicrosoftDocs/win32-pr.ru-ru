---
title: Висибилитикаусе, свойство
description: Висибилитикаусе, свойство
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410986"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="ef381-103">Висибилитикаусе, свойство</span><span class="sxs-lookup"><span data-stu-id="ef381-103">VisibilityCause Property</span></span>

<span data-ttu-id="ef381-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef381-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ef381-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="ef381-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ef381-106">Возвращает целочисленное значение, указывающее, что привело к видимому состоянию символа.</span><span class="sxs-lookup"><span data-stu-id="ef381-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="ef381-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ef381-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ef381-108">*Агент*. **Символы ("***чарактерид***"). Висибилитикаусе**</span><span class="sxs-lookup"><span data-stu-id="ef381-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="ef381-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ef381-109">Value</span></span> | <span data-ttu-id="ef381-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ef381-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef381-111">0</span><span class="sxs-lookup"><span data-stu-id="ef381-111">0</span></span>     | <span data-ttu-id="ef381-112">Символ не был показан.</span><span class="sxs-lookup"><span data-stu-id="ef381-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="ef381-113">1</span><span class="sxs-lookup"><span data-stu-id="ef381-113">1</span></span>     | <span data-ttu-id="ef381-114">Пользователь скрыл символ с помощью команды во всплывающем меню значка символа на панели задач или с помощью речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="ef381-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="ef381-115">2</span><span class="sxs-lookup"><span data-stu-id="ef381-115">2</span></span>     | <span data-ttu-id="ef381-116">Пользователь показал символ.</span><span class="sxs-lookup"><span data-stu-id="ef381-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="ef381-117">3</span><span class="sxs-lookup"><span data-stu-id="ef381-117">3</span></span>     | <span data-ttu-id="ef381-118">Приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="ef381-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="ef381-119">4</span><span class="sxs-lookup"><span data-stu-id="ef381-119">4</span></span>     | <span data-ttu-id="ef381-120">Приложение показало этот символ.</span><span class="sxs-lookup"><span data-stu-id="ef381-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="ef381-121">5</span><span class="sxs-lookup"><span data-stu-id="ef381-121">5</span></span>     | <span data-ttu-id="ef381-122">Другое клиентское приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="ef381-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="ef381-123">6</span><span class="sxs-lookup"><span data-stu-id="ef381-123">6</span></span>     | <span data-ttu-id="ef381-124">Этот символ был показан в другом клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="ef381-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="ef381-125">7</span><span class="sxs-lookup"><span data-stu-id="ef381-125">7</span></span>     | <span data-ttu-id="ef381-126">Пользователь скрыл символ, используя команду во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="ef381-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef381-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef381-127">Remarks</span></span>

<span data-ttu-id="ef381-128">Это свойство можно использовать для определения того, что привело к перемещению символа, когда несколько приложений совместно используют один и тот же символ.</span><span class="sxs-lookup"><span data-stu-id="ef381-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="ef381-129">Эти значения совпадают со значениями, возвращаемыми событиями [**Показать**](show-event.md) и [**Скрыть**](hide-event.md) .</span><span class="sxs-lookup"><span data-stu-id="ef381-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef381-130">См. также:</span><span class="sxs-lookup"><span data-stu-id="ef381-130">See Also</span></span>

<span data-ttu-id="ef381-131">[**Скрыть событие**](hide-event.md), [**Показать событие**](show-event.md), [**метод Hide**](hide-method.md), [**Показать метод**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="ef381-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 




