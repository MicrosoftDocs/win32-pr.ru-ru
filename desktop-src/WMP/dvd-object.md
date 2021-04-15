---
title: Объект DVD
description: Объект DVD предоставляет свойства и методы для работы с DVD-дисками.
ms.assetid: 953f6ba5-637b-4f70-aeea-dfe9f52d8675
keywords:
- Проигрыватель Windows Media, объект DVD
topic_type:
- apiref
api_name:
- DVD Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 656b08f90f3b6878cfde2a526ddf682a82dd8498
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104412017"
---
# <a name="dvd-object"></a><span data-ttu-id="4b996-104">Объект DVD</span><span class="sxs-lookup"><span data-stu-id="4b996-104">DVD Object</span></span>

<span data-ttu-id="4b996-105">Объект **DVD** предоставляет свойства и методы для работы с DVD-дисками.</span><span class="sxs-lookup"><span data-stu-id="4b996-105">The **DVD** object provides properties and methods for working with DVDs.</span></span>

<span data-ttu-id="4b996-106">Объект **DVD** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b996-106">The **DVD** object supports the following properties.</span></span>



| <span data-ttu-id="4b996-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="4b996-107">Property</span></span>                           | <span data-ttu-id="4b996-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4b996-108">Description</span></span>                                                                                        |
|------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b996-109">поддомен</span><span class="sxs-lookup"><span data-stu-id="4b996-109">domain</span></span>](dvd-domain.md)           | <span data-ttu-id="4b996-110">Возвращает текущий домен DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="4b996-110">Retrieves the current domain of the DVD.</span></span>                                                           |
| [<span data-ttu-id="4b996-111">isAvailable</span><span class="sxs-lookup"><span data-stu-id="4b996-111">isAvailable</span></span>](dvd-isavailable.md) | <span data-ttu-id="4b996-112">Получает сведения о доступности указанного типа сведений или о том, что может быть выполнено данное действие.</span><span class="sxs-lookup"><span data-stu-id="4b996-112">Retrieves whether a specified type of information is available or a given action can be performed.</span></span> |



 

<span data-ttu-id="4b996-113">Объект **DVD** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4b996-113">The **DVD** object supports the following methods.</span></span>



| <span data-ttu-id="4b996-114">Метод</span><span class="sxs-lookup"><span data-stu-id="4b996-114">Method</span></span>                         | <span data-ttu-id="4b996-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4b996-115">Description</span></span>                                                                                          |
|--------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b996-116">Назад</span><span class="sxs-lookup"><span data-stu-id="4b996-116">back</span></span>](dvd-back.md)           | <span data-ttu-id="4b996-117">Изменяет отображение из подменю на его родительское меню.</span><span class="sxs-lookup"><span data-stu-id="4b996-117">Changes the display from a submenu to its parent menu.</span></span>                                               |
| [<span data-ttu-id="4b996-118">выход</span><span class="sxs-lookup"><span data-stu-id="4b996-118">resume</span></span>](dvd-resume.md)       | <span data-ttu-id="4b996-119">Изменение режима воспроизведения из режима меню с возобновлением в той же позиции, что и при вызове меню.</span><span class="sxs-lookup"><span data-stu-id="4b996-119">Changes to playback mode from menu mode, resuming at the same position as when the menu was invoked.</span></span> |
| [<span data-ttu-id="4b996-120">титлемену</span><span class="sxs-lookup"><span data-stu-id="4b996-120">titleMenu</span></span>](dvd-titlemenu.md) | <span data-ttu-id="4b996-121">Останавливает воспроизведение и отображает меню заголовка.</span><span class="sxs-lookup"><span data-stu-id="4b996-121">Stops playback and displays the title menu.</span></span>                                                          |
| [<span data-ttu-id="4b996-122">топмену</span><span class="sxs-lookup"><span data-stu-id="4b996-122">topMenu</span></span>](dvd-topmenu.md)     | <span data-ttu-id="4b996-123">Останавливает воспроизведение и отображает корневое меню.</span><span class="sxs-lookup"><span data-stu-id="4b996-123">Stops playback and displays the root menu.</span></span>                                                           |



 

<span data-ttu-id="4b996-124">Доступ к объекту **DVD** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="4b996-124">The **DVD** object is accessed through the following property.</span></span>



| <span data-ttu-id="4b996-125">Объект</span><span class="sxs-lookup"><span data-stu-id="4b996-125">Object</span></span>                      | <span data-ttu-id="4b996-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="4b996-126">Property</span></span>              |
|-----------------------------|-----------------------|
| [<span data-ttu-id="4b996-127">Игрок</span><span class="sxs-lookup"><span data-stu-id="4b996-127">Player</span></span>](player-object.md) | [<span data-ttu-id="4b996-128">оптически</span><span class="sxs-lookup"><span data-stu-id="4b996-128">dvd</span></span>](player-dvd.md) |



 

## <a name="see-also"></a><span data-ttu-id="4b996-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b996-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b996-130">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="4b996-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




