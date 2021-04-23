---
description: Элемент управления Селектионтри использует событие Селектионбровсе для порождения диалогового окна обзора, что позволяет изменить путь выделенного элемента.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: Селектионбровсе таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350225"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="f5a94-103">Селектионбровсе таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="f5a94-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="f5a94-104">[Элемент управления селектионтри](selectiontree-control.md) использует событие селектионбровсе для порождения диалогового окна **обзора** , что позволяет изменить путь выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="f5a94-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="f5a94-105">Это событие должно быть опубликовано [элементом управления "кнопка](pushbutton-control.md) ", расположенным в том же диалоговом окне, что и элемент управления, подписавшийся на это событие.</span><span class="sxs-lookup"><span data-stu-id="f5a94-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="f5a94-106">Событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5a94-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="f5a94-107">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f5a94-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f5a94-108">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f5a94-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f5a94-109">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f5a94-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="f5a94-110">Все элементы управления, которые публикуют событие Селектионбровсе, становятся недоступными, если выбрана уже установленная, ненастраиваемая или не выбранная для локальной установки функция.</span><span class="sxs-lookup"><span data-stu-id="f5a94-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="f5a94-111">Для настройки функция должна иметь [открытое свойство](public-properties.md) , введенное в \_ поле Каталог [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5a94-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f5a94-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="f5a94-112">Published By</span></span>

[<span data-ttu-id="f5a94-113">селектионтри</span><span class="sxs-lookup"><span data-stu-id="f5a94-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="f5a94-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f5a94-114">Argument</span></span>

<span data-ttu-id="f5a94-115">Имя порождаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f5a94-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f5a94-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="f5a94-116">Action on Subscribers</span></span>

<span data-ttu-id="f5a94-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="f5a94-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f5a94-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="f5a94-118">Typical Use</span></span>

<span data-ttu-id="f5a94-119">Элемент управления " [кнопка](pushbutton-control.md) " в том же модальном диалоговом окне, что и селектионтри, использует это событие для запуска диалогового окна " **Обзор** ".</span><span class="sxs-lookup"><span data-stu-id="f5a94-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



