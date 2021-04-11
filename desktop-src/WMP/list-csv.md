---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Интернет-магазины проигрывателя Windows Media, list.csv
- Интернет-магазины, list.csv
- Введите 1 Интернет-магазины, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133471"
---
# <a name="listcsv"></a><span data-ttu-id="2c4df-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="2c4df-107">list.csv</span></span>

<span data-ttu-id="2c4df-108">Этот файл содержит запись для каждого из списков, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="2c4df-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="2c4df-109">Списки могут быть списками дорожек, альбомов, исполнителей, жанров, поджанров или веб-каналов. или они могут быть списками других списков.</span><span class="sxs-lookup"><span data-stu-id="2c4df-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="2c4df-110">Каждая запись списка представляет собой строку, состоящую из полей, разделенных табуляцией, описанных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="2c4df-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="2c4df-111">Поля должны присутствовать в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="2c4df-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="2c4df-112">В столбце Format в следующей таблице описывается способ форматирования каждого текстового поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="2c4df-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="2c4df-113">Он не ссылается на тип данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="2c4df-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="2c4df-114">Например, если в столбце Format указано целое число, это означает, что поле содержит строку в Юникоде, представляющую целочисленное значение, а не фактическое целое число.</span><span class="sxs-lookup"><span data-stu-id="2c4df-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c4df-115">Поле</span><span class="sxs-lookup"><span data-stu-id="2c4df-115">Field</span></span></th>
<th><span data-ttu-id="2c4df-116">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2c4df-116">Required</span></span></th>
<th><span data-ttu-id="2c4df-117">Формат</span><span class="sxs-lookup"><span data-stu-id="2c4df-117">Format</span></span></th>
<th><span data-ttu-id="2c4df-118">Описание</span><span class="sxs-lookup"><span data-stu-id="2c4df-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c4df-119">ListID</span><span class="sxs-lookup"><span data-stu-id="2c4df-119">ListID</span></span></td>
<td><span data-ttu-id="2c4df-120">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-120">Yes</span></span></td>
<td><span data-ttu-id="2c4df-121">Неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="2c4df-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="2c4df-122">Идентификатор списка, уникальный в пределах list.csv.</span><span class="sxs-lookup"><span data-stu-id="2c4df-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="2c4df-123">Значение должно быть неотрицательным и меньше 2 ^ 32. <strong>Отображение узла списка в элементе управления представлением в виде дерева:</strong> Если ListID имеет значение 0, 1, 2, 3, 4, 5, 6 или 7, список будет отображаться как пользовательский узел в узле верхнего уровня Интернет-магазина в элементе управления древовидного представления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="2c4df-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="2c4df-124">Пользовательские узлы отображаются перед стандартными узлами в узле верхнего уровня Интернет-магазина и располагаются в возрастающем порядке по ListID.</span><span class="sxs-lookup"><span data-stu-id="2c4df-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="2c4df-125">Например, если имеется три настраиваемых узла с Листидс 1, 3 и 5, они будут показаны первыми, вторым и третьи в узле верхнего уровня Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="2c4df-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-126">листтитле</span><span class="sxs-lookup"><span data-stu-id="2c4df-126">ListTitle</span></span></td>
<td><span data-ttu-id="2c4df-127">Нет</span><span class="sxs-lookup"><span data-stu-id="2c4df-127">No</span></span></td>
<td><span data-ttu-id="2c4df-128">Строка в Юникоде. Пример: десять основных попаданий</span><span class="sxs-lookup"><span data-stu-id="2c4df-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="2c4df-129">Заголовок списка.</span><span class="sxs-lookup"><span data-stu-id="2c4df-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c4df-130">листсубтитле</span><span class="sxs-lookup"><span data-stu-id="2c4df-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="2c4df-131">Нет</span><span class="sxs-lookup"><span data-stu-id="2c4df-131">No</span></span></td>
<td><span data-ttu-id="2c4df-132">Строка Юникода</span><span class="sxs-lookup"><span data-stu-id="2c4df-132">Unicode string</span></span></td>
<td><span data-ttu-id="2c4df-133">Список альтернативного заголовка, отображаемый во второй строке мозаичного представления.</span><span class="sxs-lookup"><span data-stu-id="2c4df-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-134">листдескриптион</span><span class="sxs-lookup"><span data-stu-id="2c4df-134">ListDescription</span></span></td>
<td><span data-ttu-id="2c4df-135">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-135">Yes</span></span></td>
<td><span data-ttu-id="2c4df-136">Строка Юникода</span><span class="sxs-lookup"><span data-stu-id="2c4df-136">Unicode string</span></span></td>
<td><span data-ttu-id="2c4df-137">Список понятный отображаемый текст (отображается на страницах свойств).</span><span class="sxs-lookup"><span data-stu-id="2c4df-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c4df-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="2c4df-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="2c4df-139">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-139">Yes</span></span></td>
<td><span data-ttu-id="2c4df-140">Строка в Юникоде. Формат: [T | P | A | L | G | S | Cерверный</span><span class="sxs-lookup"><span data-stu-id="2c4df-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="2c4df-141">Пример: T</span><span class="sxs-lookup"><span data-stu-id="2c4df-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="2c4df-142">Указывает тип связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="2c4df-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="2c4df-143">T = отслеживание</span><span class="sxs-lookup"><span data-stu-id="2c4df-143">T= Track</span></span></li>
<li><span data-ttu-id="2c4df-144">P = исполнитель</span><span class="sxs-lookup"><span data-stu-id="2c4df-144">P = Performer</span></span></li>
<li><span data-ttu-id="2c4df-145">A = альбом</span><span class="sxs-lookup"><span data-stu-id="2c4df-145">A = Album</span></span></li>
<li><span data-ttu-id="2c4df-146">L = список</span><span class="sxs-lookup"><span data-stu-id="2c4df-146">L = List</span></span></li>
<li><span data-ttu-id="2c4df-147">G = жанр</span><span class="sxs-lookup"><span data-stu-id="2c4df-147">G = Genre</span></span></li>
<li><span data-ttu-id="2c4df-148">S = Субженре</span><span class="sxs-lookup"><span data-stu-id="2c4df-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="2c4df-149">R = Радио</span><span class="sxs-lookup"><span data-stu-id="2c4df-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="2c4df-150">ListPrice</span></span></td>
<td><span data-ttu-id="2c4df-151">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-151">Yes</span></span></td>
<td><span data-ttu-id="2c4df-152">Строка в Юникоде. Пример: $9,99</span><span class="sxs-lookup"><span data-stu-id="2c4df-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="2c4df-153">Цена списка.</span><span class="sxs-lookup"><span data-stu-id="2c4df-153">Price of the list.</span></span> <span data-ttu-id="2c4df-154">Необходимо добавить символ валюты. Ноль означает, что список свободен.</span><span class="sxs-lookup"><span data-stu-id="2c4df-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="2c4df-155">Отсутствие значения означает, что цена неизвестна.</span><span class="sxs-lookup"><span data-stu-id="2c4df-155">No value means the price is unknown.</span></span> <span data-ttu-id="2c4df-156">Дефис означает, что список не может быть приобретен.</span><span class="sxs-lookup"><span data-stu-id="2c4df-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c4df-157">Популярность</span><span class="sxs-lookup"><span data-stu-id="2c4df-157">Popularity</span></span></td>
<td><span data-ttu-id="2c4df-158">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-158">Yes</span></span></td>
<td><span data-ttu-id="2c4df-159">Целочисленное или десятичное значение. Пример: 1259,3</span><span class="sxs-lookup"><span data-stu-id="2c4df-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="2c4df-160">Указывает ранжирование популярности при появлении этого списка в других списках.</span><span class="sxs-lookup"><span data-stu-id="2c4df-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="2c4df-161">Может быть равно нулю, если неприменимо.</span><span class="sxs-lookup"><span data-stu-id="2c4df-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-162">исрецентляддед</span><span class="sxs-lookup"><span data-stu-id="2c4df-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="2c4df-163">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-163">Yes</span></span></td>
<td><span data-ttu-id="2c4df-164">Логический. формат: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2c4df-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="2c4df-165">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="2c4df-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="2c4df-166">Указывает, был ли список недавно добавлен.</span><span class="sxs-lookup"><span data-stu-id="2c4df-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c4df-167">По функциям</span><span class="sxs-lookup"><span data-stu-id="2c4df-167">IsFeatured</span></span></td>
<td><span data-ttu-id="2c4df-168">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-168">Yes</span></span></td>
<td><span data-ttu-id="2c4df-169">Логический. формат: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="2c4df-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="2c4df-170">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="2c4df-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="2c4df-171">Указывает, является ли список избранным.</span><span class="sxs-lookup"><span data-stu-id="2c4df-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="2c4df-172">Может использоваться в определении порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="2c4df-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-173">едиториалглиф</span><span class="sxs-lookup"><span data-stu-id="2c4df-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="2c4df-174">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-174">Yes</span></span></td>
<td><span data-ttu-id="2c4df-175">Неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="2c4df-175">Non-negative integer.</span></span> <span data-ttu-id="2c4df-176">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="2c4df-176">Should be 0.</span></span></td>
<td><span data-ttu-id="2c4df-177">Не используется в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="2c4df-177">Not used in this release.</span></span> <span data-ttu-id="2c4df-178">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="2c4df-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c4df-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="2c4df-179">ViewType</span></span></td>
<td><span data-ttu-id="2c4df-180">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-180">Yes</span></span></td>
<td><span data-ttu-id="2c4df-181">Строка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="2c4df-181">Unicode string.</span></span> <span data-ttu-id="2c4df-182">Формат: [I | T | R | L | O] пример: T</span><span class="sxs-lookup"><span data-stu-id="2c4df-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="2c4df-183">Указывает тип представления для использования в списке.</span><span class="sxs-lookup"><span data-stu-id="2c4df-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="2c4df-184">I = значок</span><span class="sxs-lookup"><span data-stu-id="2c4df-184">I = Icon</span></span></li>
<li><span data-ttu-id="2c4df-185">T = плитка</span><span class="sxs-lookup"><span data-stu-id="2c4df-185">T = Tile</span></span></li>
<li><span data-ttu-id="2c4df-186">R = отчет</span><span class="sxs-lookup"><span data-stu-id="2c4df-186">R = Report</span></span></li>
<li><span data-ttu-id="2c4df-187">L = список</span><span class="sxs-lookup"><span data-stu-id="2c4df-187">L = List</span></span></li>
<li><span data-ttu-id="2c4df-188">O = упорядоченный список</span><span class="sxs-lookup"><span data-stu-id="2c4df-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-189">виевимажесизе</span><span class="sxs-lookup"><span data-stu-id="2c4df-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="2c4df-190">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-190">Yes</span></span></td>
<td><span data-ttu-id="2c4df-191">Неотрицательное целое число. Пример: 180</span><span class="sxs-lookup"><span data-stu-id="2c4df-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="2c4df-192">Размер, в котором отображается изображение списка.</span><span class="sxs-lookup"><span data-stu-id="2c4df-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="2c4df-193">Если значение равно 0, размер определяется автоматически.</span><span class="sxs-lookup"><span data-stu-id="2c4df-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c4df-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="2c4df-194">GroupBy</span></span></td>
<td><span data-ttu-id="2c4df-195">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-195">Yes</span></span></td>
<td><span data-ttu-id="2c4df-196">Строка в Юникоде. Формат: [-| P | A | C | R | Четырехмерного</span><span class="sxs-lookup"><span data-stu-id="2c4df-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="2c4df-197">Пример: P</span><span class="sxs-lookup"><span data-stu-id="2c4df-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="2c4df-198">Указывает, какое поле используется для группирования элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="2c4df-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="2c4df-199">- = Автоматический</span><span class="sxs-lookup"><span data-stu-id="2c4df-199">- = Automatic</span></span></li>
<li><span data-ttu-id="2c4df-200">P = исполнитель</span><span class="sxs-lookup"><span data-stu-id="2c4df-200">P = Performer</span></span></li>
<li><span data-ttu-id="2c4df-201">A = альбом</span><span class="sxs-lookup"><span data-stu-id="2c4df-201">A = Album</span></span></li>
<li><span data-ttu-id="2c4df-202">C = Composer</span><span class="sxs-lookup"><span data-stu-id="2c4df-202">C = Composer</span></span></li>
<li><span data-ttu-id="2c4df-203">R = Оценка</span><span class="sxs-lookup"><span data-stu-id="2c4df-203">R = Rating</span></span></li>
<li><span data-ttu-id="2c4df-204">D = Дата</span><span class="sxs-lookup"><span data-stu-id="2c4df-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c4df-205">листитемсарединамик</span><span class="sxs-lookup"><span data-stu-id="2c4df-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="2c4df-206">Да</span><span class="sxs-lookup"><span data-stu-id="2c4df-206">Yes</span></span></td>
<td><span data-ttu-id="2c4df-207">Логическое.</span><span class="sxs-lookup"><span data-stu-id="2c4df-207">Boolean.</span></span> <span data-ttu-id="2c4df-208">Может иметь значение 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="2c4df-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="2c4df-209">Указывает, создается ли список динамически.</span><span class="sxs-lookup"><span data-stu-id="2c4df-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="2c4df-210">Динамические списки не содержат элементов в listitem.csv.</span><span class="sxs-lookup"><span data-stu-id="2c4df-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="2c4df-211">Если список помечен как динамический, его элементы предоставляются <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">ивмпконтентпартнер:: жетлистконтентс</a></span><span class="sxs-lookup"><span data-stu-id="2c4df-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





