---
description: Установщик использует событие TimeRemaining для публикации приблизительного оставшегося времени в секундах для текущей последовательности хода выполнения.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081440"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="be700-103">TimeRemaining таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="be700-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="be700-104">Установщик использует событие TimeRemaining для публикации приблизительного оставшегося времени в секундах для текущей последовательности хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="be700-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="be700-105">Оставшееся время может отображаться в диалоговом окне с помощью [элемента управления "текст](text-control.md) ", который подписывается на этот таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="be700-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="be700-106">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="be700-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="be700-107">Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="be700-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="be700-108">Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="be700-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="be700-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="be700-109">Published By</span></span>

<span data-ttu-id="be700-110">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="be700-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="be700-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="be700-111">Argument</span></span>

<span data-ttu-id="be700-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="be700-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="be700-113">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="be700-113">Action on Subscribers</span></span>

<span data-ttu-id="be700-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="be700-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="be700-115">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="be700-115">Typical Use</span></span>

<span data-ttu-id="be700-116">[Элемент управления "текст](text-control.md) " в немодальном диалоговом окне подписывается на это событие через [таблицу таблица eventmapping](eventmapping-table.md) и использует [атрибут TimeRemaining](timeremaining-control-attribute.md) для просмотра оставшегося времени.</span><span class="sxs-lookup"><span data-stu-id="be700-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="be700-117">Тот же элемент управления текстом, который подписывается на TimeRemaining таблице ControlEvent событие, может также подписываться на [Скриптинпрогресс таблице ControlEvent событие](scriptinprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="be700-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="be700-118">В этом случае в качестве предварительной строки сообщения Скриптинпрогресс она заменяется строкой "оставшееся время: XX минут".</span><span class="sxs-lookup"><span data-stu-id="be700-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



