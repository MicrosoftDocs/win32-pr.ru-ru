---
description: Событие Сеттаржетпас уведомляет установщик о необходимости проверки и установки выбранного пути. Если путь не является допустимым для занесения, установщик блокирует дополнительные Контролевентс, связанные с элементом управления.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: Сеттаржетпас таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265412"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="19ee4-104">Сеттаржетпас таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="19ee4-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="19ee4-105">Событие Сеттаржетпас уведомляет установщик о необходимости проверки и установки выбранного пути.</span><span class="sxs-lookup"><span data-stu-id="19ee4-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="19ee4-106">Если путь не является допустимым для занесения, установщик блокирует дополнительные Контролевентс, связанные с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="19ee4-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="19ee4-107">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="19ee4-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="19ee4-108">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="19ee4-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="19ee4-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="19ee4-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="19ee4-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="19ee4-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="19ee4-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="19ee4-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="19ee4-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="19ee4-112">Published By</span></span>

<span data-ttu-id="19ee4-113">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="19ee4-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="19ee4-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="19ee4-114">Argument</span></span>

<span data-ttu-id="19ee4-115">Имя свойства, содержащего путь.</span><span class="sxs-lookup"><span data-stu-id="19ee4-115">The name of the property containing the path.</span></span> <span data-ttu-id="19ee4-116">Если свойство является косвенным, имя свойства заключено в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="19ee4-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="19ee4-117">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="19ee4-117">Action on Subscribers</span></span>

<span data-ttu-id="19ee4-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="19ee4-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="19ee4-119">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="19ee4-119">Typical Use</span></span>

<span data-ttu-id="19ee4-120">Элемент управления " [кнопка](pushbutton-control.md) " в диалоговом окне обзора связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) , чтобы проверить выбранный путь перед возвратом в диалоговое окно выбора.</span><span class="sxs-lookup"><span data-stu-id="19ee4-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ee4-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19ee4-121">Remarks</span></span>

<span data-ttu-id="19ee4-122">Не пытайтесь настроить целевой путь, если компоненты, использующие эти пути, уже установлены для текущего пользователя или для другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="19ee4-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="19ee4-123">Проверьте свойство [**продуктстате**](productstate.md) перед публикацией сеттаржетпас таблице ControlEvent событие, чтобы определить, установлен ли продукт, содержащий компонент.</span><span class="sxs-lookup"><span data-stu-id="19ee4-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



