---
description: Позволяет автору инициировать переустановку некоторых или всех компонентов, пока работает текущее диалоговое окно.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Повторная установка таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663056"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="ac216-103">Повторная установка таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="ac216-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="ac216-104">Переустановите Контролевенталловс автора, чтобы запустить переустановку некоторых или всех компонентов, пока работает текущее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ac216-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="ac216-105">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md) " или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="ac216-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="ac216-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md)и требует запуска пользовательского интерфейса на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ac216-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ac216-107">Это событие не работает с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ac216-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ac216-108">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ac216-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ac216-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="ac216-109">Published By</span></span>

<span data-ttu-id="ac216-110">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="ac216-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="ac216-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="ac216-111">Argument</span></span>

<span data-ttu-id="ac216-112">Строка, которая является либо именем функции, либо "ALL".</span><span class="sxs-lookup"><span data-stu-id="ac216-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ac216-113">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="ac216-113">Action on Subscribers</span></span>

<span data-ttu-id="ac216-114">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="ac216-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ac216-115">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="ac216-115">Typical Use</span></span>

<span data-ttu-id="ac216-116">Это событие связано с элементом управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ac216-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="ac216-117">Один и тот же элемент управления " [кнопка](pushbutton-control.md) " также должен быть привязан к [ReinstallMode](reinstallmode-controlevent.md) таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="ac216-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



