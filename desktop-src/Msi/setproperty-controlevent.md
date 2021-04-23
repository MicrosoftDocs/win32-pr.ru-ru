---
description: 'Синтаксис события SetProperty различается, чем для других Контролевентс вместо имени события. оно помещает свойство в квадратные скобки: \[ \_ имя свойства \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674052"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="71071-103">SetProperty таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="71071-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="71071-104">Синтаксис события SetProperty различается, чем для других Контролевентс вместо имени события. оно помещает свойство в квадратные скобки: \[ \_ имя свойства \] .</span><span class="sxs-lookup"><span data-stu-id="71071-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="71071-105">Аргумент — это новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="71071-105">The argument is the new value of the property.</span></span> <span data-ttu-id="71071-106">Чтобы отменить свойство, аргумент должен иметь значение {} .</span><span class="sxs-lookup"><span data-stu-id="71071-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="71071-107">Это необходимо, поскольку аргумент является первичным ключом в таблице и не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="71071-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="71071-108">Аргумент будет отформатирован с помощью метода Форматтекст, поэтому аргумент может содержать любое выражение, которое может обрабатывать метод Форматтекст.</span><span class="sxs-lookup"><span data-stu-id="71071-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="71071-109">Значения свойств оцениваются в момент таблице ControlEvent событие.</span><span class="sxs-lookup"><span data-stu-id="71071-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="71071-110">Это событие может быть опубликовано [элементом управления "кнопка](pushbutton-control.md) [", элементом управления CheckBox](checkbox-control.md)или [элементом управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="71071-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="71071-111">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="71071-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="71071-112">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="71071-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="71071-113">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="71071-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="71071-114">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="71071-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="71071-115">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="71071-115">Published By</span></span>

<span data-ttu-id="71071-116">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="71071-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="71071-117">Аргумент</span><span class="sxs-lookup"><span data-stu-id="71071-117">Argument</span></span>

<span data-ttu-id="71071-118">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="71071-118">The new value of the property.</span></span> <span data-ttu-id="71071-119">{} для NULL.</span><span class="sxs-lookup"><span data-stu-id="71071-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="71071-120">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="71071-120">Action on Subscribers</span></span>

<span data-ttu-id="71071-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="71071-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="71071-122">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="71071-122">Typical Use</span></span>

<span data-ttu-id="71071-123">Элемент управления " [кнопка](pushbutton-control.md) " в диалоговом окне, связанном с этим событием, поэтому он изменяет свойство при нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="71071-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



