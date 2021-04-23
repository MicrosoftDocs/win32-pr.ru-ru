---
description: Событие Валидатепродуктид задает для свойства ProductID полный идентификатор продукта. Если проверка завершается неудачно, это событие помещает сообщение об ошибке и модальное диалоговое окно для записи пользователя с ИДЕНТИФИКАТОРом продукта.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: Валидатепродуктид таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673364"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="0f0a5-104">Валидатепродуктид таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="0f0a5-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="0f0a5-105">Событие Валидатепродуктид задает для свойства [**ProductID**](productid.md) полный идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="0f0a5-106">Если проверка завершается неудачно, это событие помещает сообщение об ошибке и модальное диалоговое окно для записи пользователя с ИДЕНТИФИКАТОРом продукта.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="0f0a5-107">Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="0f0a5-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="0f0a5-108">Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f0a5-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="0f0a5-109">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0f0a5-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="0f0a5-110">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f0a5-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="0f0a5-111">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0f0a5-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="0f0a5-112">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="0f0a5-112">Published By</span></span>

<span data-ttu-id="0f0a5-113">Этот таблице ControlEvent событие публикуется установщиком.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="0f0a5-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="0f0a5-114">Argument</span></span>

<span data-ttu-id="0f0a5-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="0f0a5-116">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="0f0a5-116">Action on Subscribers</span></span>

<span data-ttu-id="0f0a5-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="0f0a5-118">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="0f0a5-118">Typical Use</span></span>

<span data-ttu-id="0f0a5-119">Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне привязан к этому событию и используется для проверки записи идентификатора продукта.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="0f0a5-120">Если запись пользователя является допустимой, откроется следующее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0f0a5-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



