---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Интернет-магазины проигрывателя Windows Media, genre.csv
- Интернет-магазины, genre.csv
- Введите 1 Интернет-магазины, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986686"
---
# <a name="genrecsv"></a><span data-ttu-id="f7ad5-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="f7ad5-107">genre.csv</span></span>

<span data-ttu-id="f7ad5-108">Этот файл содержит запись для каждого жанра, представленного в каталоге.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="f7ad5-109">Каждая запись представляет собой строку, состоящую из полей, разделенных табуляцией, описанных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="f7ad5-110">Поля должны присутствовать в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="f7ad5-111">Все поля в genre.csv являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="f7ad5-112">В столбце Format в следующей таблице описывается способ форматирования каждого текстового поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="f7ad5-113">Он не ссылается на тип данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="f7ad5-114">Например, если в столбце Format указано целое число, это означает, что поле содержит строку в Юникоде, представляющую целочисленное значение, а не фактическое целое число.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="f7ad5-115">Поле</span><span class="sxs-lookup"><span data-stu-id="f7ad5-115">Field</span></span>             | <span data-ttu-id="f7ad5-116">Формат</span><span class="sxs-lookup"><span data-stu-id="f7ad5-116">Format</span></span>                                                    | <span data-ttu-id="f7ad5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f7ad5-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ad5-118">Идентификатор жанра \_</span><span class="sxs-lookup"><span data-stu-id="f7ad5-118">Genre\_ID</span></span>         | <span data-ttu-id="f7ad5-119">Неотрицательное целое число. Пример: 22</span><span class="sxs-lookup"><span data-stu-id="f7ad5-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="f7ad5-120">Идентификатор жанра, уникальный в пределах genre.csv.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="f7ad5-121">Должно быть меньше 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-121">Must be less than 2^32.</span></span> <span data-ttu-id="f7ad5-122">Допускается не более 64 жанров.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="f7ad5-123">женретитле</span><span class="sxs-lookup"><span data-stu-id="f7ad5-123">GenreTitle</span></span>        | <span data-ttu-id="f7ad5-124">Строка в Юникоде. Пример: рок</span><span class="sxs-lookup"><span data-stu-id="f7ad5-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="f7ad5-125">Отображаемое имя жанра.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="f7ad5-126">фидсареаваилабле</span><span class="sxs-lookup"><span data-stu-id="f7ad5-126">FeedsAreAvailable</span></span> | <span data-ttu-id="f7ad5-127">Логический. формат: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="f7ad5-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="f7ad5-128">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="f7ad5-128">Example: 0</span></span><br/> | <span data-ttu-id="f7ad5-129">Указывает, возможно ли поведение "Радио Play", переходя к каналу.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="f7ad5-130">хаскомпосер</span><span class="sxs-lookup"><span data-stu-id="f7ad5-130">HasComposer</span></span>       | <span data-ttu-id="f7ad5-131">Логический. формат: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="f7ad5-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="f7ad5-132">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="f7ad5-132">Example: 1</span></span><br/> | <span data-ttu-id="f7ad5-133">Значение true, если этот жанр должен сохранять сведения о Composer в каталоге.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="f7ad5-134">Если значение не задано, сведения Composer игнорируются и не компилируются в каталог.</span><span class="sxs-lookup"><span data-stu-id="f7ad5-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





