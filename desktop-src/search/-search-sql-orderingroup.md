---
description: Предложение ORDER IN GROUP используется в сочетании с инструкцией GROUP ON, которая возвращает результирующие наборы в группах.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER в предложении GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342952"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="c95b0-103">ORDER в предложении GROUP</span><span class="sxs-lookup"><span data-stu-id="c95b0-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="c95b0-104">Предложение ORDER IN GROUP используется в сочетании с инструкцией [Group on](-search-sql-group-on-over.md) , которая возвращает результирующие наборы в группах.</span><span class="sxs-lookup"><span data-stu-id="c95b0-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="c95b0-105">Предложение ORDER IN GROUP позволяет сортировать каждую возвращаемую группу по-другому.</span><span class="sxs-lookup"><span data-stu-id="c95b0-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="c95b0-106">Например, если вы выполняете группировку по System. Kind, можно сортировать все документы по System.Docумент. Ластаусор, все музыкальные файлы по System. Music. Албумартист и все сообщения электронной почты с помощью System. Message. Фромнаме.</span><span class="sxs-lookup"><span data-stu-id="c95b0-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="c95b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c95b0-107">Syntax</span></span>

<span data-ttu-id="c95b0-108">Ниже приведен синтаксис предложения ORDER IN GROUP:</span><span class="sxs-lookup"><span data-stu-id="c95b0-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="c95b0-109">Описатель имени группы — это диапазон или известное значение из столбца Group, как указано в инструкции GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="c95b0-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="c95b0-110">Например, известные значения для System. photo. Исоспид будут содержать "ISO-100", "ISO-200" и т. д.</span><span class="sxs-lookup"><span data-stu-id="c95b0-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="c95b0-111">Диапазон для System. photo. Датетакен будет включать "2006-1-1" и "2007-1-1" для инструкции, такой как GROUP ON System. Итемдате \[ ' 2006-1-1 ', ' 2007-1-1 ' \] .</span><span class="sxs-lookup"><span data-stu-id="c95b0-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="c95b0-112">Спецификатор столбца должен быть допустимым столбцом, указанным в инструкции GROUP ON или SELECT.</span><span class="sxs-lookup"><span data-stu-id="c95b0-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="c95b0-113">Можно включить несколько столбцов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="c95b0-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="c95b0-114">Например, если вы выполняете группировку по System. photo. Исоспид, вы можете сортировать все фотографии ISO-100 сначала по System. photo. Шуттерспид, а затем по System. photo. апертуры.</span><span class="sxs-lookup"><span data-stu-id="c95b0-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="c95b0-115">Необязательный спецификатор направления может быть либо ASC для возрастания (от низкого до высокого), либо DESC для нисходящей (от высокого до низкого).</span><span class="sxs-lookup"><span data-stu-id="c95b0-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="c95b0-116">Если не указать описатель направления, используется значение по умолчанию (по возрастанию).</span><span class="sxs-lookup"><span data-stu-id="c95b0-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="c95b0-117">Если указать более одного столбца, но не указывать все направления, то направление, заданное последним, применяется к каждому последовательному столбцу до тех пор, пока не будет явно изменено направление.</span><span class="sxs-lookup"><span data-stu-id="c95b0-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="c95b0-118">Диапазоны или значения, которые явно не указаны в предложении GROUP ORDER, сортируются в возрастающем порядке по значениям в столбце GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="c95b0-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="c95b0-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="c95b0-119">Examples</span></span>

<span data-ttu-id="c95b0-120">В следующем примере результаты группируются по свойству System. Kind.</span><span class="sxs-lookup"><span data-stu-id="c95b0-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="c95b0-121">Запрос упорядочивает группу "Program" по имени приложения и группе "Музыка" по названию альбома и номеру отслеживания.</span><span class="sxs-lookup"><span data-stu-id="c95b0-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="c95b0-122">Группа **со значением NULL** будет упорядочена по имени элемента.</span><span class="sxs-lookup"><span data-stu-id="c95b0-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="c95b0-123">Все остальные группы будут упорядочены по дате элемента.</span><span class="sxs-lookup"><span data-stu-id="c95b0-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="c95b0-124">Следующий пример группирует результаты по свойству System. Итемдате, а затем сортирует каждую группу по URL-адресу элемента, виду или имени.</span><span class="sxs-lookup"><span data-stu-id="c95b0-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="c95b0-125">Результаты предыдущего запроса будут возвращены в пяти группах и отсортированы, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c95b0-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="c95b0-126">Группа</span><span class="sxs-lookup"><span data-stu-id="c95b0-126">Group</span></span>    | <span data-ttu-id="c95b0-127">Описание</span><span class="sxs-lookup"><span data-stu-id="c95b0-127">Description</span></span>                                               | <span data-ttu-id="c95b0-128">Отсортировано по</span><span class="sxs-lookup"><span data-stu-id="c95b0-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="c95b0-129">MINVALUE</span><span class="sxs-lookup"><span data-stu-id="c95b0-129">MINVALUE</span></span> | <span data-ttu-id="c95b0-130">Элементы с датами до 2006-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="c95b0-131">Сортировка по URL-адресу элемента в порядке возрастания</span><span class="sxs-lookup"><span data-stu-id="c95b0-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="c95b0-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-132">2006-1-1</span></span> | <span data-ttu-id="c95b0-133">Элементы с датами от 2006-1-1 до 2007-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="c95b0-134">Сортировка по дате элемента в возрастающем порядке</span><span class="sxs-lookup"><span data-stu-id="c95b0-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="c95b0-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-135">2007-1-1</span></span> | <span data-ttu-id="c95b0-136">Элементы с датами от 2007-1-1 до 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="c95b0-137">Сортировка по значению типа в возрастающем порядке</span><span class="sxs-lookup"><span data-stu-id="c95b0-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="c95b0-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-138">2008-1-1</span></span> | <span data-ttu-id="c95b0-139">Элементы с датами в или после 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="c95b0-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="c95b0-140">Сортировка по дате элемента в возрастающем порядке</span><span class="sxs-lookup"><span data-stu-id="c95b0-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="c95b0-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="c95b0-141">**NULL**</span></span> | <span data-ttu-id="c95b0-142">Элементы, не имеющие значения в столбце System. Итемдате</span><span class="sxs-lookup"><span data-stu-id="c95b0-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="c95b0-143">Сортировка по имени элемента в возрастающем порядке</span><span class="sxs-lookup"><span data-stu-id="c95b0-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="c95b0-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c95b0-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c95b0-145">**Reference**</span><span class="sxs-lookup"><span data-stu-id="c95b0-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c95b0-146">ГРУППИРОВАТЬ ПО... Поверх... Баланс</span><span class="sxs-lookup"><span data-stu-id="c95b0-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="c95b0-147">Предложение ORDER BY</span><span class="sxs-lookup"><span data-stu-id="c95b0-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



