---
description: Игноречанже таблице ControlEvent событие публикуется элементом управления Директорилист, когда выбранная папка изменяется из одного каталога в другой в элементе управления. Это событие должно быть создано в таблице таблица eventmapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: Игноречанже таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650699"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="aa09d-104">Игноречанже таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="aa09d-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="aa09d-105">Игноречанже таблице ControlEvent событие публикуется [элементом управления директорилист](directorylist-control.md) , когда выбранная папка изменяется из одного каталога в другой в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="aa09d-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="aa09d-106">Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa09d-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="aa09d-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="aa09d-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="aa09d-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aa09d-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="aa09d-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="aa09d-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="aa09d-110">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="aa09d-110">Published By</span></span>

[<span data-ttu-id="aa09d-111">директорилист</span><span class="sxs-lookup"><span data-stu-id="aa09d-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="aa09d-112">Аргумент</span><span class="sxs-lookup"><span data-stu-id="aa09d-112">Argument</span></span>

<span data-ttu-id="aa09d-113">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="aa09d-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="aa09d-114">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="aa09d-114">Action on Subscribers</span></span>

<span data-ttu-id="aa09d-115">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="aa09d-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="aa09d-116">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="aa09d-116">Typical Use</span></span>

<span data-ttu-id="aa09d-117">[Элемент управления директорикомбо](directorycombo-control.md) обычно использует игноречанже таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="aa09d-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



