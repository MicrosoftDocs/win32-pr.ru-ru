---
description: Установщик использует это событие для публикации данных в последнем действии. Данные могут отображаться в диалоговом окне с помощью элемента управления "текст", который подписывается на этот таблице ControlEvent событие. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: Актиондата таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662967"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="9569a-105">Актиондата таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="9569a-105">ActionData ControlEvent</span></span>

<span data-ttu-id="9569a-106">Установщик использует это событие для публикации данных в последнем действии.</span><span class="sxs-lookup"><span data-stu-id="9569a-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="9569a-107">Данные могут отображаться в диалоговом окне с помощью [элемента управления "текст](text-control.md) ", который подписывается на этот таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="9569a-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="9569a-108">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="9569a-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="9569a-109">Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9569a-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="9569a-110">Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="9569a-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="9569a-111">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="9569a-111">Published By</span></span>

<span data-ttu-id="9569a-112">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="9569a-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="9569a-113">Аргумент</span><span class="sxs-lookup"><span data-stu-id="9569a-113">Argument</span></span>

<span data-ttu-id="9569a-114">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="9569a-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9569a-115">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="9569a-115">Action on Subscribers</span></span>

<span data-ttu-id="9569a-116">Подписчики скрыты при запуске нового действия и отображаются при поступлении данных о новых действиях из установщика.</span><span class="sxs-lookup"><span data-stu-id="9569a-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9569a-117">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="9569a-117">Typical Use</span></span>

<span data-ttu-id="9569a-118">[Элемент управления "текст](text-control.md) " в немодальном диалоговом окне подписывается на это событие через [таблицу таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="9569a-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="9569a-119">[Атрибут элемента управления Text](text-control-attribute.md) указан в поле Attributes этой таблицы для получения текущих данных действия.</span><span class="sxs-lookup"><span data-stu-id="9569a-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="9569a-120">Обычно используется для вывода имен файлов, копируемых во время копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="9569a-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



