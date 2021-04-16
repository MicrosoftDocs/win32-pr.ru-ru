---
description: Это событие уведомляет элемент управления Директорилист о том, что должна быть создана новая папка; Она создает новую папку и выбирает поле имени папки для редактирования.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: Директорилистнев таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664740"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="681f9-103">Директорилистнев таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="681f9-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="681f9-104">Это событие уведомляет [элемент управления директорилист](directorylist-control.md) о том, что должна быть создана новая папка; Она создает новую папку и выбирает поле имени папки для редактирования.</span><span class="sxs-lookup"><span data-stu-id="681f9-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="681f9-105">Имя новой папки по умолчанию может быть создано в [таблице уитекст](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="681f9-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="681f9-106">Введите "NewFolder" в ключевой столбец.</span><span class="sxs-lookup"><span data-stu-id="681f9-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="681f9-107">Введите значение имени по умолчанию для новой папки в текстовом столбце.</span><span class="sxs-lookup"><span data-stu-id="681f9-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="681f9-108">Это значение должно быть в виде типа данных столбца [filename](filename.md) и использовать \| синтаксис СФН лфн.</span><span class="sxs-lookup"><span data-stu-id="681f9-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="681f9-109">Если это значение отсутствует в таблице Уитекст или имеет недопустимое значение, установщик использует значение по умолчанию "Fldr \| New Folder".</span><span class="sxs-lookup"><span data-stu-id="681f9-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="681f9-110">Связанные сведения см. в разделе [диалоговое окно обзора](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="681f9-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="681f9-111">Это событие должно быть опубликовано [элементом управления "кнопка](pushbutton-control.md) ", расположенным в том же диалоговом окне, что и элемент управления, подписавшийся на это событие.</span><span class="sxs-lookup"><span data-stu-id="681f9-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="681f9-112">Событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="681f9-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="681f9-113">Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="681f9-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="681f9-114">Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="681f9-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="681f9-115">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="681f9-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="681f9-116">Обратите внимание, что если эта таблице ControlEvent событие вызывается снова, когда новая папка уже существует, вторая новая папка не будет создана.</span><span class="sxs-lookup"><span data-stu-id="681f9-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="681f9-117">В этом случае вызов Директорилистнев выбирает имя существующей новой папки для редактирования.</span><span class="sxs-lookup"><span data-stu-id="681f9-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="681f9-118">Кем опубликовано</span><span class="sxs-lookup"><span data-stu-id="681f9-118">Published By</span></span>

[<span data-ttu-id="681f9-119">директорилист</span><span class="sxs-lookup"><span data-stu-id="681f9-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="681f9-120">Аргумент</span><span class="sxs-lookup"><span data-stu-id="681f9-120">Argument</span></span>

<span data-ttu-id="681f9-121">В этом таблице ControlEvent событие не используется аргумент.</span><span class="sxs-lookup"><span data-stu-id="681f9-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="681f9-122">Действие на подписчиках</span><span class="sxs-lookup"><span data-stu-id="681f9-122">Action on Subscribers</span></span>

<span data-ttu-id="681f9-123">Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.</span><span class="sxs-lookup"><span data-stu-id="681f9-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="681f9-124">Типичные случаи использования</span><span class="sxs-lookup"><span data-stu-id="681f9-124">Typical Use</span></span>

<span data-ttu-id="681f9-125">Для запуска создания новой папки используется элемент управления " [кнопка](pushbutton-control.md) " в том же модальном диалоговом окне, что и директорилист.</span><span class="sxs-lookup"><span data-stu-id="681f9-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



