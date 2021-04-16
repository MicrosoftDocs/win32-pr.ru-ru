---
description: Этот таблице ControlEvent событие можно использовать для включения или отключения возможностей отката установщика.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: Енаблероллбакк таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650643"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="4f426-103">Енаблероллбакк таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="4f426-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="4f426-104">Этот таблице ControlEvent событие можно использовать для включения или отключения возможностей отката установщика.</span><span class="sxs-lookup"><span data-stu-id="4f426-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="4f426-105">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="4f426-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="4f426-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f426-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="4f426-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4f426-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4f426-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4f426-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4f426-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4f426-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="4f426-110">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="4f426-110">Published By</span></span>

<span data-ttu-id="4f426-111">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="4f426-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="4f426-112">Аргумент</span><span class="sxs-lookup"><span data-stu-id="4f426-112">Argument</span></span>

<span data-ttu-id="4f426-113">Значение false отключает возможности отката установщика.</span><span class="sxs-lookup"><span data-stu-id="4f426-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="4f426-114">Значение true включает возможности отката установщика.</span><span class="sxs-lookup"><span data-stu-id="4f426-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4f426-115">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="4f426-115">Action on Subscribers</span></span>

<span data-ttu-id="4f426-116">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="4f426-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4f426-117">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="4f426-117">Typical Use</span></span>

<span data-ttu-id="4f426-118">Может использоваться для отключения возможностей отката, если установщик обнаруживает, что недостаточно места на диске для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="4f426-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="4f426-119">В этом случае таблице ControlEvent событие следует использовать с свойствами [**аутофдискспаце**](outofdiskspace.md), [**аутофнорбдискспаце**](outofnorbdiskspace.md)и [**промптроллбакккост**](promptrollbackcost.md) .</span><span class="sxs-lookup"><span data-stu-id="4f426-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



