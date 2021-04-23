---
description: Позволяет автору указать режим проверки или режимы во время повторной установки, а также пока работает текущее диалоговое окно.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650778"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="c13fe-103">ReinstallMode таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="c13fe-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="c13fe-104">ReinstallMode Контролевенталловс автора, чтобы указать режим или режимы проверки во время повторной установки, а также пока работает текущее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c13fe-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="c13fe-105">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md) " или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="c13fe-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="c13fe-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md)и требует запуска пользовательского интерфейса на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c13fe-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c13fe-107">Это событие не работает с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c13fe-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c13fe-108">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c13fe-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c13fe-109">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="c13fe-109">Published By</span></span>

<span data-ttu-id="c13fe-110">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="c13fe-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="c13fe-111">Аргумент</span><span class="sxs-lookup"><span data-stu-id="c13fe-111">Argument</span></span>

<span data-ttu-id="c13fe-112">Строка.</span><span class="sxs-lookup"><span data-stu-id="c13fe-112">A string.</span></span> <span data-ttu-id="c13fe-113">Список возможных значений см. в разделе свойство [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c13fe-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c13fe-114">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="c13fe-114">Action on Subscribers</span></span>

<span data-ttu-id="c13fe-115">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="c13fe-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c13fe-116">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="c13fe-116">Typical Use</span></span>

<span data-ttu-id="c13fe-117">Это событие связано с элементом управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="c13fe-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="c13fe-118">Один и тот же элемент управления " [кнопка](pushbutton-control.md) " также должен быть связан с [переустановкой](reinstall-controlevent.md) таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="c13fe-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



