---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Интернет-магазины проигрывателя Windows Media, subgenre.csv
- Интернет-магазины, subgenre.csv
- Введите 1 Интернет-магазины, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710126"
---
# <a name="subgenrecsv"></a><span data-ttu-id="3febb-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="3febb-107">subgenre.csv</span></span>

<span data-ttu-id="3febb-108">Этот файл содержит запись для каждого субженре, представленного в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3febb-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="3febb-109">Каждая запись представляет собой строку, состоящую из полей, разделенных табуляцией, описанных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="3febb-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="3febb-110">Поля должны присутствовать в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="3febb-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="3febb-111">В столбце Format в следующей таблице описывается способ форматирования каждого текстового поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3febb-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="3febb-112">Он не ссылается на тип данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="3febb-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="3febb-113">Например, если в столбце Format указано целое число, это означает, что поле содержит строку в Юникоде, представляющую целочисленное значение, а не фактическое целое число.</span><span class="sxs-lookup"><span data-stu-id="3febb-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="3febb-114">Поле</span><span class="sxs-lookup"><span data-stu-id="3febb-114">Field</span></span>             | <span data-ttu-id="3febb-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3febb-115">Required</span></span> | <span data-ttu-id="3febb-116">Формат</span><span class="sxs-lookup"><span data-stu-id="3febb-116">Format</span></span>                                                                                            | <span data-ttu-id="3febb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3febb-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3febb-118">субженреид</span><span class="sxs-lookup"><span data-stu-id="3febb-118">SubGenreID</span></span>        | <span data-ttu-id="3febb-119">Да</span><span class="sxs-lookup"><span data-stu-id="3febb-119">Yes</span></span>      | <span data-ttu-id="3febb-120">Неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="3febb-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="3febb-121">Идентификатор субженре (ID), уникальный в пределах subgenre.csv.</span><span class="sxs-lookup"><span data-stu-id="3febb-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="3febb-122">Разрешено до 1024 поджанров.</span><span class="sxs-lookup"><span data-stu-id="3febb-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="3febb-123">субженретитле</span><span class="sxs-lookup"><span data-stu-id="3febb-123">SubGenreTitle</span></span>     | <span data-ttu-id="3febb-124">Да</span><span class="sxs-lookup"><span data-stu-id="3febb-124">Yes</span></span>      | <span data-ttu-id="3febb-125">Строка в Юникоде. Пример: Интеллектуальная Dance музыка (IDM)</span><span class="sxs-lookup"><span data-stu-id="3febb-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="3febb-126">Отображаемое имя субженре.</span><span class="sxs-lookup"><span data-stu-id="3febb-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="3febb-127">субженресубтитле</span><span class="sxs-lookup"><span data-stu-id="3febb-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="3febb-128">Нет</span><span class="sxs-lookup"><span data-stu-id="3febb-128">No</span></span>       | <span data-ttu-id="3febb-129">Строка в Юникоде. Пример. Новая, перкуссиве электронная музыка, не очень чистая Technology.</span><span class="sxs-lookup"><span data-stu-id="3febb-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="3febb-130">Опишите значение отображаемого имени субженре.</span><span class="sxs-lookup"><span data-stu-id="3febb-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="3febb-131">Длина должна быть меньше 64 символов.</span><span class="sxs-lookup"><span data-stu-id="3febb-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="3febb-132">фидсареаваилабле</span><span class="sxs-lookup"><span data-stu-id="3febb-132">FeedsAreAvailable</span></span> | <span data-ttu-id="3febb-133">Да</span><span class="sxs-lookup"><span data-stu-id="3febb-133">Yes</span></span>      | <span data-ttu-id="3febb-134">Логический. формат: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="3febb-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="3febb-135">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="3febb-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="3febb-136">Указывает, возможно ли воспроизведение радио путем перехода к веб-каналу.</span><span class="sxs-lookup"><span data-stu-id="3febb-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="3febb-137">Связанный \_ GenreID</span><span class="sxs-lookup"><span data-stu-id="3febb-137">Linked\_GenreID</span></span>   | <span data-ttu-id="3febb-138">Да</span><span class="sxs-lookup"><span data-stu-id="3febb-138">Yes</span></span>      | <span data-ttu-id="3febb-139">Неотрицательное целое число (GenreID). Пример: 12</span><span class="sxs-lookup"><span data-stu-id="3febb-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="3febb-140">GenreID родительского жанра.</span><span class="sxs-lookup"><span data-stu-id="3febb-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="3febb-141">Допускается только один родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="3febb-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="3febb-142">сортордерранк</span><span class="sxs-lookup"><span data-stu-id="3febb-142">SortOrderRank</span></span>     | <span data-ttu-id="3febb-143">Да</span><span class="sxs-lookup"><span data-stu-id="3febb-143">Yes</span></span>      | <span data-ttu-id="3febb-144">Неотрицательное целое число. Пример: 23</span><span class="sxs-lookup"><span data-stu-id="3febb-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="3febb-145">Ранжирование, идеально уникальное, используемое для сортировки поджанров в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3febb-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="3febb-146">Если у родительского жанра есть 10 поджанров, это может быть целое число от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="3febb-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





