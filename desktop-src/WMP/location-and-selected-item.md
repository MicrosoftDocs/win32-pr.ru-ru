---
title: Расположение и выбранный элемент
description: Расположение и выбранный элемент
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Интернет-магазины проигрывателя Windows Media, расположения
- Интернет-магазины, расположения
- Тип 1 Интернет-магазины, расположения
- Интернет-магазины проигрывателя Windows Media, расположения библиотек
- Интернет-магазины, расположения библиотек
- Тип 1 Интернет-магазины, расположения библиотек
- Интернет-магазины проигрывателя Windows Media, выбранные элементы
- Интернет-магазины, выбранные элементы
- Тип 1 Интернет-магазины, выбранные элементы
- Библиотека проигрывателя Windows Media, расположения
- Библиотека проигрывателя Windows Media, выбранные элементы
- Библиотека, расположения
- Библиотека, выбранные элементы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253186"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="20dc6-116">Расположение и выбранный элемент</span><span class="sxs-lookup"><span data-stu-id="20dc6-116">Location and Selected Item</span></span>

<span data-ttu-id="20dc6-117">Проигрыватель Windows Media использует следующие пять элементов для обхарактеризующее текущее представление содержимого Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="20dc6-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="20dc6-118">задача</span><span class="sxs-lookup"><span data-stu-id="20dc6-118">task</span></span>
-   <span data-ttu-id="20dc6-119">Тип расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-119">library location type</span></span>
-   <span data-ttu-id="20dc6-120">Идентификатор расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-120">library location ID</span></span>
-   <span data-ttu-id="20dc6-121">Тип выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-121">selected item type</span></span>
-   <span data-ttu-id="20dc6-122">Идентификатор выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-122">selected item ID</span></span>

<span data-ttu-id="20dc6-123">Как правило, представление в проигрывателе Windows Media можно представить как контейнер элементов.</span><span class="sxs-lookup"><span data-stu-id="20dc6-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="20dc6-124">Контейнер имеет тип, а элемент имеет тип.</span><span class="sxs-lookup"><span data-stu-id="20dc6-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="20dc6-125">Все элементы в контейнере имеют одинаковый тип.</span><span class="sxs-lookup"><span data-stu-id="20dc6-125">All the items in a container have the same type.</span></span> <span data-ttu-id="20dc6-126">Типы расположения и типы элементов задаются [константами расположения библиотеки](library-location-constants.md).</span><span class="sxs-lookup"><span data-stu-id="20dc6-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="20dc6-127">Например, если в текущем представлении отображается отдельный альбом, то тип расположения библиотеки — Кпалбумид, а, так как альбом содержит дорожки, выбранный тип элемента — Кптраккид.</span><span class="sxs-lookup"><span data-stu-id="20dc6-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="20dc6-128">В следующей таблице показано расположение и типы элементов для нескольких контейнеров.</span><span class="sxs-lookup"><span data-stu-id="20dc6-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="20dc6-129">Описание контейнера</span><span class="sxs-lookup"><span data-stu-id="20dc6-129">Description of container</span></span>                              | <span data-ttu-id="20dc6-130">Тип расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-130">Library location type</span></span> | <span data-ttu-id="20dc6-131">Тип выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="20dc6-132">Альбом, который является контейнером дорожек</span><span class="sxs-lookup"><span data-stu-id="20dc6-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="20dc6-133">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="20dc6-133">CPAlbumID</span></span>             | <span data-ttu-id="20dc6-134">кптраккид</span><span class="sxs-lookup"><span data-stu-id="20dc6-134">CPTrackID</span></span>          |
| <span data-ttu-id="20dc6-135">Список, который является контейнером дорожек</span><span class="sxs-lookup"><span data-stu-id="20dc6-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="20dc6-136">кплистид</span><span class="sxs-lookup"><span data-stu-id="20dc6-136">CPListID</span></span>              | <span data-ttu-id="20dc6-137">кптраккид</span><span class="sxs-lookup"><span data-stu-id="20dc6-137">CPTrackID</span></span>          |
| <span data-ttu-id="20dc6-138">Список, который является контейнером альбомов</span><span class="sxs-lookup"><span data-stu-id="20dc6-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="20dc6-139">кплистид</span><span class="sxs-lookup"><span data-stu-id="20dc6-139">CPListID</span></span>              | <span data-ttu-id="20dc6-140">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="20dc6-140">CPAlbumID</span></span>          |
| <span data-ttu-id="20dc6-141">Радиостанция, являющийся контейнером списков</span><span class="sxs-lookup"><span data-stu-id="20dc6-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="20dc6-142">кпрадиоид</span><span class="sxs-lookup"><span data-stu-id="20dc6-142">CPRadioID</span></span>             | <span data-ttu-id="20dc6-143">кплистид</span><span class="sxs-lookup"><span data-stu-id="20dc6-143">CPListID</span></span>           |
| <span data-ttu-id="20dc6-144">Набор всех альбомов, который является контейнером альбомов</span><span class="sxs-lookup"><span data-stu-id="20dc6-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="20dc6-145">аллкпалбумидс</span><span class="sxs-lookup"><span data-stu-id="20dc6-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="20dc6-146">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="20dc6-146">CPAlbumID</span></span>          |
| <span data-ttu-id="20dc6-147">Набор всех жанров, которые являются контейнером жанров</span><span class="sxs-lookup"><span data-stu-id="20dc6-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="20dc6-148">аллкпженреидс</span><span class="sxs-lookup"><span data-stu-id="20dc6-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="20dc6-149">кпженреид</span><span class="sxs-lookup"><span data-stu-id="20dc6-149">CPGenreID</span></span>          |



 

<span data-ttu-id="20dc6-150">Вкладки в проигрывателе Windows Media представляют разные задачи.</span><span class="sxs-lookup"><span data-stu-id="20dc6-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="20dc6-151">Проигрыватель отображает содержимое Интернет-магазина в трех разных областях задач: **Библиотека**, **запись** и **Синхронизация**. Область задач Библиотека также называется областью задач **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="20dc6-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="20dc6-152">Иногда область задач называется *компонентом*, поэтому в этой документации могут отображаться такие термины, как *запись функций* и *синхронизации* .</span><span class="sxs-lookup"><span data-stu-id="20dc6-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="20dc6-153">В следующих примерах показано, как проигрыватель Windows Media использует пять фрагментов информации (задача, тип расположения библиотеки, идентификатор расположения библиотеки, выбранный тип элемента, выбранный идентификатор элемента) для определения различных представлений.</span><span class="sxs-lookup"><span data-stu-id="20dc6-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="20dc6-154">В области задач **запись** в проигрывателе отображается альбом в виде контейнера дорожек.</span><span class="sxs-lookup"><span data-stu-id="20dc6-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="20dc6-155">У альбома есть идентификатор 250.</span><span class="sxs-lookup"><span data-stu-id="20dc6-155">The album has an ID of 250.</span></span> <span data-ttu-id="20dc6-156">В представлении выбранный элемент является записью с ИДЕНТИФИКАТОРом 800.</span><span class="sxs-lookup"><span data-stu-id="20dc6-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="20dc6-157">Обратите внимание, что 800 — это идентификатор записи в каталоге интернет-магазина, а не номер записи в альбоме.</span><span class="sxs-lookup"><span data-stu-id="20dc6-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="20dc6-158">Элемент</span><span class="sxs-lookup"><span data-stu-id="20dc6-158">Item</span></span>                  | <span data-ttu-id="20dc6-159">Значение</span><span class="sxs-lookup"><span data-stu-id="20dc6-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="20dc6-160">задача</span><span class="sxs-lookup"><span data-stu-id="20dc6-160">task</span></span>                  | <span data-ttu-id="20dc6-161">Записать</span><span class="sxs-lookup"><span data-stu-id="20dc6-161">Burn</span></span>      |
| <span data-ttu-id="20dc6-162">Тип расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-162">library location type</span></span> | <span data-ttu-id="20dc6-163">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="20dc6-163">CPAlbumID</span></span> |
| <span data-ttu-id="20dc6-164">Идентификатор расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-164">library location ID</span></span>   | <span data-ttu-id="20dc6-165">250</span><span class="sxs-lookup"><span data-stu-id="20dc6-165">250</span></span>       |
| <span data-ttu-id="20dc6-166">Тип выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-166">selected item type</span></span>    | <span data-ttu-id="20dc6-167">кптраккид</span><span class="sxs-lookup"><span data-stu-id="20dc6-167">CPTrackID</span></span> |
| <span data-ttu-id="20dc6-168">Идентификатор выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-168">selected item ID</span></span>      | <span data-ttu-id="20dc6-169">800</span><span class="sxs-lookup"><span data-stu-id="20dc6-169">800</span></span>       |



 

<span data-ttu-id="20dc6-170">В области задач **Синхронизация** в проигрывателе отображается набор всех альбомов, который является контейнером альбомов.</span><span class="sxs-lookup"><span data-stu-id="20dc6-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="20dc6-171">В представлении выбранный элемент является альбомом с ИДЕНТИФИКАТОРом 300.</span><span class="sxs-lookup"><span data-stu-id="20dc6-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="20dc6-172">Обратите внимание, что идентификатор расположения библиотеки неприменим к этому представлению.</span><span class="sxs-lookup"><span data-stu-id="20dc6-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="20dc6-173">Элемент</span><span class="sxs-lookup"><span data-stu-id="20dc6-173">Item</span></span>                  | <span data-ttu-id="20dc6-174">Значение</span><span class="sxs-lookup"><span data-stu-id="20dc6-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="20dc6-175">задача</span><span class="sxs-lookup"><span data-stu-id="20dc6-175">task</span></span>                  | <span data-ttu-id="20dc6-176">Синхронизация</span><span class="sxs-lookup"><span data-stu-id="20dc6-176">Sync</span></span>          |
| <span data-ttu-id="20dc6-177">Тип расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-177">library location type</span></span> | <span data-ttu-id="20dc6-178">аллкпалбумидс</span><span class="sxs-lookup"><span data-stu-id="20dc6-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="20dc6-179">Идентификатор расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-179">library location ID</span></span>   | <span data-ttu-id="20dc6-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20dc6-180">N/A</span></span>           |
| <span data-ttu-id="20dc6-181">Тип выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-181">selected item type</span></span>    | <span data-ttu-id="20dc6-182">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="20dc6-182">CPAlbumID</span></span>     |
| <span data-ttu-id="20dc6-183">Идентификатор выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-183">selected item ID</span></span>      | <span data-ttu-id="20dc6-184">300</span><span class="sxs-lookup"><span data-stu-id="20dc6-184">300</span></span>           |



 

<span data-ttu-id="20dc6-185">В элементе управления иерархического представления выбран корневой узел для Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="20dc6-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="20dc6-186">В этом случае нет контейнера и, следовательно, нет элементов.</span><span class="sxs-lookup"><span data-stu-id="20dc6-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="20dc6-187">В области задач « **Библиотека** » отображается страница «обнаружение».</span><span class="sxs-lookup"><span data-stu-id="20dc6-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="20dc6-188">Элемент</span><span class="sxs-lookup"><span data-stu-id="20dc6-188">Item</span></span>                  | <span data-ttu-id="20dc6-189">Значение</span><span class="sxs-lookup"><span data-stu-id="20dc6-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="20dc6-190">задача</span><span class="sxs-lookup"><span data-stu-id="20dc6-190">task</span></span>                  | <span data-ttu-id="20dc6-191">Просмотреть</span><span class="sxs-lookup"><span data-stu-id="20dc6-191">Browse</span></span>          |
| <span data-ttu-id="20dc6-192">Тип расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-192">library location type</span></span> | <span data-ttu-id="20dc6-193">рутлокатион</span><span class="sxs-lookup"><span data-stu-id="20dc6-193">RootLocation</span></span>    |
| <span data-ttu-id="20dc6-194">Идентификатор расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-194">library location ID</span></span>   | <span data-ttu-id="20dc6-195">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20dc6-195">N/A</span></span>             |
| <span data-ttu-id="20dc6-196">Тип выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-196">selected item type</span></span>    | <span data-ttu-id="20dc6-197">ункновнлокатион</span><span class="sxs-lookup"><span data-stu-id="20dc6-197">UnknownLocation</span></span> |
| <span data-ttu-id="20dc6-198">Идентификатор выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-198">selected item ID</span></span>      | <span data-ttu-id="20dc6-199">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20dc6-199">N/A</span></span>             |



 

<span data-ttu-id="20dc6-200">В области задач **Синхронизация** игрок отображает 2002 год в качестве контейнера дорожек.</span><span class="sxs-lookup"><span data-stu-id="20dc6-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="20dc6-201">В представлении выбранный элемент является записью с ИДЕНТИФИКАТОРом 450.</span><span class="sxs-lookup"><span data-stu-id="20dc6-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="20dc6-202">Элемент</span><span class="sxs-lookup"><span data-stu-id="20dc6-202">Item</span></span>                  | <span data-ttu-id="20dc6-203">Значение</span><span class="sxs-lookup"><span data-stu-id="20dc6-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="20dc6-204">задача</span><span class="sxs-lookup"><span data-stu-id="20dc6-204">task</span></span>                  | <span data-ttu-id="20dc6-205">Синхронизация</span><span class="sxs-lookup"><span data-stu-id="20dc6-205">Sync</span></span>            |
| <span data-ttu-id="20dc6-206">Тип расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-206">library location type</span></span> | <span data-ttu-id="20dc6-207">релеаседатэйеар</span><span class="sxs-lookup"><span data-stu-id="20dc6-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="20dc6-208">Идентификатор расположения библиотеки</span><span class="sxs-lookup"><span data-stu-id="20dc6-208">library location ID</span></span>   | <span data-ttu-id="20dc6-209">2002</span><span class="sxs-lookup"><span data-stu-id="20dc6-209">2002</span></span>            |
| <span data-ttu-id="20dc6-210">Тип выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-210">selected item type</span></span>    | <span data-ttu-id="20dc6-211">кптраккид</span><span class="sxs-lookup"><span data-stu-id="20dc6-211">CPTrackID</span></span>       |
| <span data-ttu-id="20dc6-212">Идентификатор выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="20dc6-212">selected item ID</span></span>      | <span data-ttu-id="20dc6-213">450</span><span class="sxs-lookup"><span data-stu-id="20dc6-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="20dc6-214">См. также</span><span class="sxs-lookup"><span data-stu-id="20dc6-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20dc6-215">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="20dc6-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="20dc6-216">**Страницы обнаружения**</span><span class="sxs-lookup"><span data-stu-id="20dc6-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 




