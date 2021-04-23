---
description: Диалоговое окно «Обзор» позволяет пользователю выбрать каталог. Каталог не обязательно должен существовать и может быть создан с помощью этого элемента управления.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Диалоговое окно обзора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423877"
---
# <a name="browse-dialog"></a><span data-ttu-id="6438e-104">Диалоговое окно обзора</span><span class="sxs-lookup"><span data-stu-id="6438e-104">Browse Dialog</span></span>

<span data-ttu-id="6438e-105">Диалоговое окно «Обзор» позволяет пользователю выбрать каталог.</span><span class="sxs-lookup"><span data-stu-id="6438e-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="6438e-106">Каталог не обязательно должен существовать и может быть создан с помощью этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6438e-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="6438e-107">Этот тип диалогового окна обычно содержит три следующих элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6438e-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="6438e-108">Эти элементы управления связаны с одним и тем же свойством.</span><span class="sxs-lookup"><span data-stu-id="6438e-108">These controls are connected to the same property.</span></span> <span data-ttu-id="6438e-109">Это свойство является выбранным путем.</span><span class="sxs-lookup"><span data-stu-id="6438e-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="6438e-110">[Элемент управления паседит](pathedit-control.md) для выбора заключительного фрагмента пути.</span><span class="sxs-lookup"><span data-stu-id="6438e-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="6438e-111">Этот элемент управления не может потерять фокус, если указанный хвост не является допустимым для текущего тома.</span><span class="sxs-lookup"><span data-stu-id="6438e-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="6438e-112">[Элемент управления директорикомбо](directorycombo-control.md) для отображения пути, выделенного в настоящий момент, который отображается элементом управления паседит.</span><span class="sxs-lookup"><span data-stu-id="6438e-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="6438e-113">Этот элемент управления не показывает последний сегмент пути.</span><span class="sxs-lookup"><span data-stu-id="6438e-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="6438e-114">[Элемент управления директорилист](directorylist-control.md) для отображения папок под каталогом, который в настоящее время отображается директорикомбо.</span><span class="sxs-lookup"><span data-stu-id="6438e-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="6438e-115">Кроме того, можно отобразить еще не созданную папку.</span><span class="sxs-lookup"><span data-stu-id="6438e-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="6438e-116">Диалоговое окно Обзор также обычно содержит [элемент управления директорикомбо](directorycombo-control.md) , указывающий типы отображаемых томов.</span><span class="sxs-lookup"><span data-stu-id="6438e-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="6438e-117">Обычно все типы томов отображаются в диалоговом окне Обзор.</span><span class="sxs-lookup"><span data-stu-id="6438e-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="6438e-118">Диалоговые окна обзора обычно содержат три [элемента управления "кнопка](pushbutton-control.md)".</span><span class="sxs-lookup"><span data-stu-id="6438e-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="6438e-119">Эти кнопки связаны с соответствующими Контролевентс в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="6438e-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="6438e-120">Эти кнопки используются для активации следующих параметров управления.</span><span class="sxs-lookup"><span data-stu-id="6438e-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="6438e-121">Control, параметр</span><span class="sxs-lookup"><span data-stu-id="6438e-121">Control option</span></span> | <span data-ttu-id="6438e-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="6438e-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="6438e-123">На один уровень вверх</span><span class="sxs-lookup"><span data-stu-id="6438e-123">Up One Level</span></span>   | [<span data-ttu-id="6438e-124">директорилиступ</span><span class="sxs-lookup"><span data-stu-id="6438e-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="6438e-125">Создать папку</span><span class="sxs-lookup"><span data-stu-id="6438e-125">New Folder</span></span>     | [<span data-ttu-id="6438e-126">директорилистнев</span><span class="sxs-lookup"><span data-stu-id="6438e-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="6438e-127">Открыть</span><span class="sxs-lookup"><span data-stu-id="6438e-127">Open</span></span>           | [<span data-ttu-id="6438e-128">директорилистопен</span><span class="sxs-lookup"><span data-stu-id="6438e-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="6438e-129">Чтобы команда Создать папку работала с именем папки, отличной от имени по умолчанию, путь к новой папке должен быть указан в [таблице уитекст](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="6438e-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="6438e-130">В строке пути должно использоваться имя файла "короткое имя файла \| длинное имя файла".</span><span class="sxs-lookup"><span data-stu-id="6438e-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="6438e-131">Например, используйте имя файла, например "Мипрод ~ 1 \| мой продукт невероятные".</span><span class="sxs-lookup"><span data-stu-id="6438e-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="6438e-132">Дополнительные сведения о формате имени файла см. в разделе Тип данных столбца [filename](filename.md) .</span><span class="sxs-lookup"><span data-stu-id="6438e-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="6438e-133">Если путь отсутствует в таблице Уитекст или для него задано недопустимое значение, по умолчанию для него задается значение "Fldr \| Новая папка".</span><span class="sxs-lookup"><span data-stu-id="6438e-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="6438e-134">Кнопка **создать папку** может быть пропущена, если диалоговое окно требуется только для поиска существующих папок.</span><span class="sxs-lookup"><span data-stu-id="6438e-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



