---
description: Спавндиалог таблице ControlEvent событие уведомляет установщик о необходимости создания дочернего элемента модального диалогового окна, сохраняя выполнение текущего диалогового окна.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: Спавндиалог таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673207"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="05a5e-103">Спавндиалог таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="05a5e-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="05a5e-104">Спавндиалог таблице ControlEvent событие уведомляет установщик о необходимости создания дочернего элемента модального диалогового окна, сохраняя выполнение текущего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05a5e-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="05a5e-105">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="05a5e-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="05a5e-106">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="05a5e-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="05a5e-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="05a5e-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="05a5e-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="05a5e-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="05a5e-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="05a5e-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="05a5e-110">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="05a5e-110">Published By</span></span>

<span data-ttu-id="05a5e-111">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="05a5e-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="05a5e-112">Аргумент</span><span class="sxs-lookup"><span data-stu-id="05a5e-112">Argument</span></span>

<span data-ttu-id="05a5e-113">Строка, которая является именем нового диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="05a5e-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="05a5e-114">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="05a5e-114">Action on Subscribers</span></span>

<span data-ttu-id="05a5e-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="05a5e-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="05a5e-116">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="05a5e-116">Typical Use</span></span>

<span data-ttu-id="05a5e-117">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) для создания дочернего диалогового окна, такого как "вы действительно хотите отменить?"</span><span class="sxs-lookup"><span data-stu-id="05a5e-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="05a5e-118">приложения для управления доступом.</span><span class="sxs-lookup"><span data-stu-id="05a5e-118">dialog box.</span></span>

 

 



