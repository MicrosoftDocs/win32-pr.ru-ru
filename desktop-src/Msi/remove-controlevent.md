---
description: Установщик уведомляется по этому событию при выборе компонента или всех компонентов для удаления при сохранении работоспособного диалогового окна.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Удалить таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663377"
---
# <a name="remove-controlevent"></a><span data-ttu-id="d0d76-103">Удалить таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="d0d76-103">Remove ControlEvent</span></span>

<span data-ttu-id="d0d76-104">Установщик уведомляется по этому событию при выборе компонента или всех компонентов для удаления при сохранении работоспособного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d0d76-104">The installer is notified through this event when a feature or all features are selected for removal while keeping the present dialog box running.</span></span>

<span data-ttu-id="d0d76-105">Это событие может быть опубликовано [элементом управления "кнопка](pushbutton-control.md) [", элементом управления CheckBox](checkbox-control.md)или [элементом управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="d0d76-105">This event can be published by a [PushButton control](pushbutton-control.md), [CheckBox control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="d0d76-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0d76-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="d0d76-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d76-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d0d76-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d0d76-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d0d76-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d0d76-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d0d76-110">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="d0d76-110">Published By</span></span>

<span data-ttu-id="d0d76-111">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="d0d76-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d0d76-112">Аргумент</span><span class="sxs-lookup"><span data-stu-id="d0d76-112">Argument</span></span>

<span data-ttu-id="d0d76-113">Строка, которая является либо именем функции, либо "ALL".</span><span class="sxs-lookup"><span data-stu-id="d0d76-113">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d0d76-114">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="d0d76-114">Action on Subscribers</span></span>

<span data-ttu-id="d0d76-115">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="d0d76-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="action-by-publisher-when-subscriber-activated"></a><span data-ttu-id="d0d76-116">Действие издателя при активации подписчика</span><span class="sxs-lookup"><span data-stu-id="d0d76-116">Action by Publisher When Subscriber Activated</span></span>

<span data-ttu-id="d0d76-117">Установщик сохраняет текущее диалоговое окно и уведомляет установщик.</span><span class="sxs-lookup"><span data-stu-id="d0d76-117">The installer keeps the present dialog box running and notifies the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d0d76-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="d0d76-118">Typical Use</span></span>

<span data-ttu-id="d0d76-119">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне, привязанном к этому событию.</span><span class="sxs-lookup"><span data-stu-id="d0d76-119">A [PushButton](pushbutton-control.md) control on a modal dialog box tied to this event.</span></span>

 

 



