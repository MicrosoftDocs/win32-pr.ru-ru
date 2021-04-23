---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Интернет-магазины проигрывателя Windows Media, listitem.csv
- Интернет-магазины, listitem.csv
- Введите 1 Интернет-магазины, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410815"
---
# <a name="listitemcsv"></a><span data-ttu-id="7cbfa-107">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="7cbfa-107">listitem.csv</span></span>

<span data-ttu-id="7cbfa-108">Этот файл содержит записи для каждого элемента, включенного в список.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-108">This file contains entries for each item that is included in a list.</span></span> <span data-ttu-id="7cbfa-109">Каждая запись представляет собой строку, состоящую из полей, разделенных табуляцией, описанных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="7cbfa-110">Поля должны присутствовать в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="7cbfa-111">Все поля обязательные.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-111">All fields are required.</span></span>

<span data-ttu-id="7cbfa-112">В столбце Format в следующей таблице описывается способ форматирования каждого текстового поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="7cbfa-113">Он не ссылается на тип данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="7cbfa-114">Например, если в столбце Format указано целое число, это означает, что поле содержит строку в Юникоде, представляющую целочисленное значение, а не фактическое целое число.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="7cbfa-115">Поле</span><span class="sxs-lookup"><span data-stu-id="7cbfa-115">Field</span></span>              | <span data-ttu-id="7cbfa-116">Формат</span><span class="sxs-lookup"><span data-stu-id="7cbfa-116">Format</span></span>                                          | <span data-ttu-id="7cbfa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7cbfa-117">Description</span></span>                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbfa-118">Связанный \_ ListID</span><span class="sxs-lookup"><span data-stu-id="7cbfa-118">Linked\_ListID</span></span>     | <span data-ttu-id="7cbfa-119">Неотрицательное целое число. Пример: 465</span><span class="sxs-lookup"><span data-stu-id="7cbfa-119">Non-negative integer.Example: 465</span></span><br/>    | <span data-ttu-id="7cbfa-120">Идентификатор списка, частью которого является этот элемент.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-120">The ID of the list this item is part of.</span></span>                                                                               |
| <span data-ttu-id="7cbfa-121">Связанный \_ ListItem</span><span class="sxs-lookup"><span data-stu-id="7cbfa-121">Linked\_ListItem</span></span>   | <span data-ttu-id="7cbfa-122">Неотрицательное целое число. Пример: 684793</span><span class="sxs-lookup"><span data-stu-id="7cbfa-122">Non-negative integer.Example: 684793</span></span><br/> | <span data-ttu-id="7cbfa-123">Идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-123">The ID of the item.</span></span> <span data-ttu-id="7cbfa-124">Может быть ИДЕНТИФИКАТОРом записи, альбома, исполнителя, жанра, субженре, канала радио или другого списка.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-124">Can be the ID of a track, an album, an artist, a genre, a subgenre, a radio feed, or another list.</span></span> |
| <span data-ttu-id="7cbfa-125">итемпоситионинлист</span><span class="sxs-lookup"><span data-stu-id="7cbfa-125">ItemPositionInList</span></span> | <span data-ttu-id="7cbfa-126">Неотрицательное целое число. Пример: 5</span><span class="sxs-lookup"><span data-stu-id="7cbfa-126">Non-negative integer.Example: 5</span></span><br/>      | <span data-ttu-id="7cbfa-127">Позиция элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-127">The position of the item within its list.</span></span> <span data-ttu-id="7cbfa-128">Первый элемент в списке находится в позиции 0.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-128">The first item in a list is at position 0.</span></span>                                   |



 

 

 





