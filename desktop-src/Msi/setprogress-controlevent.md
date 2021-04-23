---
description: Установщик использует событие Сетпрогресс для публикации информации о ходе установки.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: Сетпрогресс таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998912"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="23c01-103">Сетпрогресс таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="23c01-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="23c01-104">Установщик использует событие Сетпрогресс для публикации информации о ходе установки.</span><span class="sxs-lookup"><span data-stu-id="23c01-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="23c01-105">[Элемент управления ProgressBar](progressbar-control.md) или [элемент управления "объявление](billboard-control.md) " должен подписываться на событие через [таблицу таблица eventmapping](eventmapping-table.md) , присваивая имя действия, ход выполнения которого указывается.</span><span class="sxs-lookup"><span data-stu-id="23c01-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="23c01-106">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="23c01-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="23c01-107">Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="23c01-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="23c01-108">Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="23c01-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="23c01-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="23c01-109">Published By</span></span>

<span data-ttu-id="23c01-110">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="23c01-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="23c01-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="23c01-111">Argument</span></span>

<span data-ttu-id="23c01-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="23c01-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="23c01-113">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="23c01-113">Action on Subscribers</span></span>

<span data-ttu-id="23c01-114">Нет.</span><span class="sxs-lookup"><span data-stu-id="23c01-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="23c01-115">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="23c01-115">Typical Use</span></span>

<span data-ttu-id="23c01-116">Элемент управления [ProgressBar](progressbar-control.md) в немодальном диалоговом окне подписывается на это событие с помощью атрибута [Progress](progress-control-attribute.md) для получения сведений о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="23c01-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



