---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Интернет-магазины проигрывателя Windows Media, artist.csv
- Интернет-магазины, artist.csv
- Введите 1 Интернет-магазины, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332427"
---
# <a name="artistcsv"></a><span data-ttu-id="3ce9c-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="3ce9c-107">artist.csv</span></span>

<span data-ttu-id="3ce9c-108">Этот файл содержит запись для каждого исполнителя в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="3ce9c-109">Каждая запись представляет собой строку, состоящую из полей, разделенных табуляцией, описанных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="3ce9c-110">Поля должны присутствовать в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="3ce9c-111">Все поля в artist.csv являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="3ce9c-112">В столбце Format в следующей таблице описывается способ форматирования каждого текстового поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="3ce9c-113">Он не ссылается на тип данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="3ce9c-114">Например, если в столбце Format указано целое число, это означает, что поле содержит строку в Юникоде, представляющую целочисленное значение, а не фактическое целое число.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="3ce9c-115">Поле</span><span class="sxs-lookup"><span data-stu-id="3ce9c-115">Field</span></span>                  | <span data-ttu-id="3ce9c-116">Формат</span><span class="sxs-lookup"><span data-stu-id="3ce9c-116">Format</span></span>                                            | <span data-ttu-id="3ce9c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3ce9c-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce9c-118">артистид</span><span class="sxs-lookup"><span data-stu-id="3ce9c-118">ArtistID</span></span>               | <span data-ttu-id="3ce9c-119">Неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-119">Non-negative integer.</span></span> <span data-ttu-id="3ce9c-120">Пример: 65832</span><span class="sxs-lookup"><span data-stu-id="3ce9c-120">Example: 65832</span></span>              | <span data-ttu-id="3ce9c-121">Уникальный идентификатор исполнителя, уникальный в пределах artist.csv.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="3ce9c-122">Должно быть меньше 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="3ce9c-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="3ce9c-123">ArtistName</span></span>             | <span data-ttu-id="3ce9c-124">Строка в Юникоде. Пример: Дон Функ</span><span class="sxs-lookup"><span data-stu-id="3ce9c-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="3ce9c-125">Отображаемое имя исполнителя.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="3ce9c-126">линкедженреид</span><span class="sxs-lookup"><span data-stu-id="3ce9c-126">LinkedGenreID</span></span>          | <span data-ttu-id="3ce9c-127">Неотрицательное целое число. Пример: 313</span><span class="sxs-lookup"><span data-stu-id="3ce9c-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="3ce9c-128">GenreID основного жанра исполнителя.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="3ce9c-129">Должен быть основным жанром, а не субженре.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="3ce9c-130">Допускается только одно значение.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="3ce9c-131">линкедсимиларартистидс</span><span class="sxs-lookup"><span data-stu-id="3ce9c-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="3ce9c-132">Н/Д</span><span class="sxs-lookup"><span data-stu-id="3ce9c-132">N/A</span></span>                                               | <span data-ttu-id="3ce9c-133">Не используется в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-133">Not used in this release.</span></span> <span data-ttu-id="3ce9c-134">Должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="3ce9c-135">Популярность</span><span class="sxs-lookup"><span data-stu-id="3ce9c-135">Popularity</span></span>             | <span data-ttu-id="3ce9c-136">Может быть целочисленным или десятичным значением.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-136">Can be integer or decimal value.</span></span> <span data-ttu-id="3ce9c-137">Пример: 1252,25</span><span class="sxs-lookup"><span data-stu-id="3ce9c-137">Example: 1252.25</span></span> | <span data-ttu-id="3ce9c-138">Ранжирование популярности.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-138">Popularity ranking.</span></span> <span data-ttu-id="3ce9c-139">Может быть позицией в списке при сортировке по популярности.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="3ce9c-140">фидсаваилабле</span><span class="sxs-lookup"><span data-stu-id="3ce9c-140">FeedsAvailable</span></span>         | <span data-ttu-id="3ce9c-141">Логическое.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-141">Boolean.</span></span> <span data-ttu-id="3ce9c-142">Формат: \[ 0 \| 1 \] Пример: 0</span><span class="sxs-lookup"><span data-stu-id="3ce9c-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="3ce9c-143">Не используется в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-143">Not used in this release.</span></span> <span data-ttu-id="3ce9c-144">Должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-144">Should be empty.</span></span>                                                                 |



 

 

 





