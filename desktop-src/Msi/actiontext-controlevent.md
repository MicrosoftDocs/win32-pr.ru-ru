---
description: Установщик использует это событие для публикации имени текущего действия. Имя может отображаться в диалоговом окне с помощью элемента управления "текст", который подписывается на этот таблице ControlEvent событие. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: Актионтекст таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998311"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="1ad2b-105">Актионтекст таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="1ad2b-105">ActionText ControlEvent</span></span>

<span data-ttu-id="1ad2b-106">Установщик использует это событие для публикации имени текущего действия.</span><span class="sxs-lookup"><span data-stu-id="1ad2b-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="1ad2b-107">Имя может отображаться в диалоговом окне с помощью [элемента управления "текст](text-control.md) ", который подписывается на этот таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="1ad2b-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="1ad2b-108">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ad2b-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="1ad2b-109">Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad2b-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="1ad2b-110">Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1ad2b-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="1ad2b-111">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="1ad2b-111">Published By</span></span>

<span data-ttu-id="1ad2b-112">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="1ad2b-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1ad2b-113">Аргумент</span><span class="sxs-lookup"><span data-stu-id="1ad2b-113">Argument</span></span>

<span data-ttu-id="1ad2b-114">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="1ad2b-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1ad2b-115">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="1ad2b-115">Action on Subscribers</span></span>

<span data-ttu-id="1ad2b-116">Подписчики отображаются, когда из установщика поступают новые данные о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="1ad2b-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1ad2b-117">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="1ad2b-117">Typical Use</span></span>

<span data-ttu-id="1ad2b-118">[Элемент управления "текст](text-control.md) " в немодальном диалоговом окне подписывается на это событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ad2b-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="1ad2b-119">[Атрибут элемента управления Text](text-control-attribute.md) должен быть указан в поле Attributes этой таблицы для получения имени текущего действия.</span><span class="sxs-lookup"><span data-stu-id="1ad2b-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



