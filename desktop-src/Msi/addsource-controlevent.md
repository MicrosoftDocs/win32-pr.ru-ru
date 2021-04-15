---
description: Это событие уведомляет установщик, сохраняя выполнение текущего диалогового окна, что компонент или все компоненты должны запускаться из источника.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: Аддсаурце таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662958"
---
# <a name="addsource-controlevent"></a><span data-ttu-id="d4e6a-103">Аддсаурце таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="d4e6a-103">AddSource ControlEvent</span></span>

<span data-ttu-id="d4e6a-104">Это событие уведомляет установщик, сохраняя выполнение текущего диалогового окна, что компонент или все компоненты должны запускаться из источника.</span><span class="sxs-lookup"><span data-stu-id="d4e6a-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run from source.</span></span> <span data-ttu-id="d4e6a-105">Это событие может быть опубликовано [элементом управления "кнопка](pushbutton-control.md) [", элементом управления CheckBox](checkbox-control.md)или [элементом управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="d4e6a-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="d4e6a-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4e6a-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="d4e6a-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e6a-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d4e6a-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d4e6a-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d4e6a-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d4e6a-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d4e6a-110">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="d4e6a-110">Published By</span></span>

<span data-ttu-id="d4e6a-111">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="d4e6a-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d4e6a-112">Аргумент</span><span class="sxs-lookup"><span data-stu-id="d4e6a-112">Argument</span></span>

<span data-ttu-id="d4e6a-113">Строка, либо имя функции, либо "все".</span><span class="sxs-lookup"><span data-stu-id="d4e6a-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d4e6a-114">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="d4e6a-114">Action on Subscribers</span></span>

<span data-ttu-id="d4e6a-115">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="d4e6a-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d4e6a-116">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="d4e6a-116">Typical Use</span></span>

<span data-ttu-id="d4e6a-117">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне связан с этим событием и используется для уведомления установщика без остановки диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d4e6a-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



