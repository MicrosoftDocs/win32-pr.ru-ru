---
title: Сопоставление RSS-каналов со свойствами диспетчер устройств Windows Media
description: Сопоставление RSS-каналов со свойствами диспетчер устройств Windows Media
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Диспетчер устройств Windows Media, RSS-каналы
- Диспетчер устройств, RSS-каналы
- инструкции по программированию, RSS-каналы
- Классические приложения, RSS-каналы
- Создание приложений диспетчер устройств Windows Media, RSS-каналов
- RSS-каналы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887808"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="fa07f-109">Сопоставление RSS-каналов со свойствами диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="fa07f-110">Проигрыватель Windows Media 11 предоставляет функцию агрегатора RSS, которая позволяет пользователям хранить содержимое, полученное из подкастов, на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="fa07f-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="fa07f-111">В этом разделе описаны элементы XML, найденные в RSS-канале.</span><span class="sxs-lookup"><span data-stu-id="fa07f-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="fa07f-112">Кроме того, он сопоставляет эти элементы RSS со свойствами диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fa07f-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="fa07f-113">Элементы в RSS-канале имеют следующие иерархию и атрибуты:</span><span class="sxs-lookup"><span data-stu-id="fa07f-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="fa07f-114">В следующей таблице перечислены элементы канала в RSS-канале и соответствующие свойства Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="fa07f-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="fa07f-115">Элемент Channel</span><span class="sxs-lookup"><span data-stu-id="fa07f-115">Channel element</span></span> | <span data-ttu-id="fa07f-116">Состояние</span><span class="sxs-lookup"><span data-stu-id="fa07f-116">Status</span></span>         | <span data-ttu-id="fa07f-117">Соответствующее свойство диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="fa07f-118">категория</span><span class="sxs-lookup"><span data-stu-id="fa07f-118">category</span></span>        | <span data-ttu-id="fa07f-119">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-119">Optional</span></span>       | [<span data-ttu-id="fa07f-120">g \_ всзвмдмженре</span><span class="sxs-lookup"><span data-stu-id="fa07f-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="fa07f-121">cloud</span><span class="sxs-lookup"><span data-stu-id="fa07f-121">cloud</span></span>           | <span data-ttu-id="fa07f-122">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-122">Not applicable</span></span> | <span data-ttu-id="fa07f-123">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-123">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-124">авторские права</span><span class="sxs-lookup"><span data-stu-id="fa07f-124">copyright</span></span>       | <span data-ttu-id="fa07f-125">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-125">Optional</span></span>       | [<span data-ttu-id="fa07f-126">g \_ всзвмдмпровидеркопиригхт</span><span class="sxs-lookup"><span data-stu-id="fa07f-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="fa07f-127">description;</span><span class="sxs-lookup"><span data-stu-id="fa07f-127">description</span></span>     | <span data-ttu-id="fa07f-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-128">Required</span></span>       | [<span data-ttu-id="fa07f-129">g \_ всзвмдмдескриптион</span><span class="sxs-lookup"><span data-stu-id="fa07f-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="fa07f-130">Документы</span><span class="sxs-lookup"><span data-stu-id="fa07f-130">docs</span></span>            | <span data-ttu-id="fa07f-131">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-131">Not applicable</span></span> | <span data-ttu-id="fa07f-132">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-132">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-133">генератор</span><span class="sxs-lookup"><span data-stu-id="fa07f-133">generator</span></span>       | <span data-ttu-id="fa07f-134">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-134">Not applicable</span></span> | <span data-ttu-id="fa07f-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-135">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-136">Язык</span><span class="sxs-lookup"><span data-stu-id="fa07f-136">language</span></span>        | <span data-ttu-id="fa07f-137">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-137">Not applicable</span></span> | <span data-ttu-id="fa07f-138">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-138">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-139">ластбуилддате</span><span class="sxs-lookup"><span data-stu-id="fa07f-139">lastBuildDate</span></span>   | <span data-ttu-id="fa07f-140">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-140">Optional</span></span>       | [<span data-ttu-id="fa07f-141">g \_ всзвмдмластмодифиеддате</span><span class="sxs-lookup"><span data-stu-id="fa07f-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="fa07f-142">link</span><span class="sxs-lookup"><span data-stu-id="fa07f-142">link</span></span>            | <span data-ttu-id="fa07f-143">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-143">Required</span></span>       | [<span data-ttu-id="fa07f-144">g \_ всзвмдмдестинатионурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="fa07f-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="fa07f-145">managingEditor</span></span>  | <span data-ttu-id="fa07f-146">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-146">Optional</span></span>       | [<span data-ttu-id="fa07f-147">g \_ всзвмдмедитор</span><span class="sxs-lookup"><span data-stu-id="fa07f-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="fa07f-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="fa07f-148">pubDate</span></span>         | <span data-ttu-id="fa07f-149">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-149">Optional</span></span>       | [<span data-ttu-id="fa07f-150">g \_ всзвмдмеар</span><span class="sxs-lookup"><span data-stu-id="fa07f-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="fa07f-151">рейтинг</span><span class="sxs-lookup"><span data-stu-id="fa07f-151">rating</span></span>          | <span data-ttu-id="fa07f-152">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-152">Not applicable</span></span> | <span data-ttu-id="fa07f-153">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-153">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-154">скипдайс</span><span class="sxs-lookup"><span data-stu-id="fa07f-154">skipDays</span></span>        | <span data-ttu-id="fa07f-155">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-155">Not applicable</span></span> | <span data-ttu-id="fa07f-156">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-156">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-157">скифаурс</span><span class="sxs-lookup"><span data-stu-id="fa07f-157">skipHours</span></span>       | <span data-ttu-id="fa07f-158">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-158">Not applicable</span></span> | <span data-ttu-id="fa07f-159">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-159">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-160">textInput</span><span class="sxs-lookup"><span data-stu-id="fa07f-160">textInput</span></span>       | <span data-ttu-id="fa07f-161">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-161">Not applicable</span></span> | <span data-ttu-id="fa07f-162">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-162">Not applicable</span></span>                                        |
| <span data-ttu-id="fa07f-163">title</span><span class="sxs-lookup"><span data-stu-id="fa07f-163">title</span></span>           | <span data-ttu-id="fa07f-164">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-164">Required</span></span>       | [<span data-ttu-id="fa07f-165">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="fa07f-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="fa07f-166">ttl</span><span class="sxs-lookup"><span data-stu-id="fa07f-166">ttl</span></span>             | <span data-ttu-id="fa07f-167">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-167">Optional</span></span>       | [<span data-ttu-id="fa07f-168">g \_ всзвмдмтиметоливе</span><span class="sxs-lookup"><span data-stu-id="fa07f-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="fa07f-169">webMaster</span><span class="sxs-lookup"><span data-stu-id="fa07f-169">webMaster</span></span>       | <span data-ttu-id="fa07f-170">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-170">Optional</span></span>       | [<span data-ttu-id="fa07f-171">g \_ всзвмдмвебмастер</span><span class="sxs-lookup"><span data-stu-id="fa07f-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="fa07f-172">В следующей таблице перечислены элементы Image в RSS-канале и соответствующие свойства ВМДМ.</span><span class="sxs-lookup"><span data-stu-id="fa07f-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="fa07f-173">Элемент Image</span><span class="sxs-lookup"><span data-stu-id="fa07f-173">Image element</span></span> | <span data-ttu-id="fa07f-174">Состояние</span><span class="sxs-lookup"><span data-stu-id="fa07f-174">Status</span></span>   | <span data-ttu-id="fa07f-175">Соответствующее свойство диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="fa07f-176">description;</span><span class="sxs-lookup"><span data-stu-id="fa07f-176">description</span></span>   | <span data-ttu-id="fa07f-177">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-177">Optional</span></span> | [<span data-ttu-id="fa07f-178">g \_ всзвмдмдескриптион</span><span class="sxs-lookup"><span data-stu-id="fa07f-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="fa07f-179">рост</span><span class="sxs-lookup"><span data-stu-id="fa07f-179">height</span></span>        | <span data-ttu-id="fa07f-180">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-180">Optional</span></span> | [<span data-ttu-id="fa07f-181">g \_ всзвмдмхеигхт</span><span class="sxs-lookup"><span data-stu-id="fa07f-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="fa07f-182">link</span><span class="sxs-lookup"><span data-stu-id="fa07f-182">link</span></span>          | <span data-ttu-id="fa07f-183">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-183">Optional</span></span> | [<span data-ttu-id="fa07f-184">g \_ всзвмдмдестинатионурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="fa07f-185">title</span><span class="sxs-lookup"><span data-stu-id="fa07f-185">title</span></span>         | <span data-ttu-id="fa07f-186">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-186">Optional</span></span> | [<span data-ttu-id="fa07f-187">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="fa07f-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="fa07f-188">url</span><span class="sxs-lookup"><span data-stu-id="fa07f-188">url</span></span>           | <span data-ttu-id="fa07f-189">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-189">Optional</span></span> | [<span data-ttu-id="fa07f-190">g \_ всзвмдмсаурцеурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="fa07f-191">width</span><span class="sxs-lookup"><span data-stu-id="fa07f-191">width</span></span>         | <span data-ttu-id="fa07f-192">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-192">Optional</span></span> | [<span data-ttu-id="fa07f-193">g \_ всзвмдмвидс</span><span class="sxs-lookup"><span data-stu-id="fa07f-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="fa07f-194">В следующей таблице перечислены элементы элементов в RSS-канале и соответствующие свойства Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="fa07f-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="fa07f-195">Элемент Item</span><span class="sxs-lookup"><span data-stu-id="fa07f-195">Item element</span></span> | <span data-ttu-id="fa07f-196">attribute</span><span class="sxs-lookup"><span data-stu-id="fa07f-196">Attribute</span></span>   | <span data-ttu-id="fa07f-197">Состояние</span><span class="sxs-lookup"><span data-stu-id="fa07f-197">Status</span></span>         | <span data-ttu-id="fa07f-198">Соответствующее свойство диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="fa07f-199">автор</span><span class="sxs-lookup"><span data-stu-id="fa07f-199">author</span></span>       |             | <span data-ttu-id="fa07f-200">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-200">Optional</span></span>       | [<span data-ttu-id="fa07f-201">g \_ всзвмдмаусор</span><span class="sxs-lookup"><span data-stu-id="fa07f-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="fa07f-202">категория</span><span class="sxs-lookup"><span data-stu-id="fa07f-202">category</span></span>     |             | <span data-ttu-id="fa07f-203">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-203">Optional</span></span>       | [<span data-ttu-id="fa07f-204">g \_ всзвмдмженре</span><span class="sxs-lookup"><span data-stu-id="fa07f-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="fa07f-205">домен</span><span class="sxs-lookup"><span data-stu-id="fa07f-205">domain</span></span>      | <span data-ttu-id="fa07f-206">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-206">Not applicable</span></span> | <span data-ttu-id="fa07f-207">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="fa07f-208">description;</span><span class="sxs-lookup"><span data-stu-id="fa07f-208">description</span></span>  |             | <span data-ttu-id="fa07f-209">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-209">Optional</span></span>       | [<span data-ttu-id="fa07f-210">g \_ всзвмдмдескриптион</span><span class="sxs-lookup"><span data-stu-id="fa07f-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="fa07f-211">корпуса</span><span class="sxs-lookup"><span data-stu-id="fa07f-211">enclosure</span></span>    |             | <span data-ttu-id="fa07f-212">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-212">Optional</span></span>       | <span data-ttu-id="fa07f-213">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="fa07f-214">length</span><span class="sxs-lookup"><span data-stu-id="fa07f-214">length</span></span>      | <span data-ttu-id="fa07f-215">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-215">Required</span></span>       | [<span data-ttu-id="fa07f-216">g \_ всзвмдмфилесизе</span><span class="sxs-lookup"><span data-stu-id="fa07f-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="fa07f-217">type</span><span class="sxs-lookup"><span data-stu-id="fa07f-217">type</span></span>        | <span data-ttu-id="fa07f-218">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-218">Required</span></span>       | <span data-ttu-id="fa07f-219">(Тип MIME должен быть сопоставлен с типом содержимого свойства.)</span><span class="sxs-lookup"><span data-stu-id="fa07f-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="fa07f-220">url</span><span class="sxs-lookup"><span data-stu-id="fa07f-220">url</span></span>         | <span data-ttu-id="fa07f-221">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-221">Required</span></span>       | [<span data-ttu-id="fa07f-222">g \_ всзвмдмсаурцеурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="fa07f-223">guid</span><span class="sxs-lookup"><span data-stu-id="fa07f-223">guid</span></span>         |             | <span data-ttu-id="fa07f-224">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-224">Optional</span></span>       | [<span data-ttu-id="fa07f-225">g \_ всзвмдмедиагуид</span><span class="sxs-lookup"><span data-stu-id="fa07f-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="fa07f-226">подпостоянная</span><span class="sxs-lookup"><span data-stu-id="fa07f-226">isPermaLink</span></span> | <span data-ttu-id="fa07f-227">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-227">Not applicable</span></span> | <span data-ttu-id="fa07f-228">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="fa07f-229">link</span><span class="sxs-lookup"><span data-stu-id="fa07f-229">link</span></span>         |             | <span data-ttu-id="fa07f-230">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-230">Optional</span></span>       | [<span data-ttu-id="fa07f-231">g \_ всзвмдмдестинатионурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="fa07f-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="fa07f-232">pubDate</span></span>      |             | <span data-ttu-id="fa07f-233">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-233">Optional</span></span>       | [<span data-ttu-id="fa07f-234">g \_ всзвмдмеар</span><span class="sxs-lookup"><span data-stu-id="fa07f-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="fa07f-235">source</span><span class="sxs-lookup"><span data-stu-id="fa07f-235">source</span></span>       |             | <span data-ttu-id="fa07f-236">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-236">Not applicable</span></span> | <span data-ttu-id="fa07f-237">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fa07f-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="fa07f-238">title</span><span class="sxs-lookup"><span data-stu-id="fa07f-238">title</span></span>        |             | <span data-ttu-id="fa07f-239">Необязательно</span><span class="sxs-lookup"><span data-stu-id="fa07f-239">Optional</span></span>       | [<span data-ttu-id="fa07f-240">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="fa07f-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="fa07f-241">Пример</span><span class="sxs-lookup"><span data-stu-id="fa07f-241">Example</span></span>

<span data-ttu-id="fa07f-242">В следующем примере показан полный RSS-канал для вымышленной подкаста, предоставляемого Генеральным директором компании для публикации.</span><span class="sxs-lookup"><span data-stu-id="fa07f-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



<span data-ttu-id="fa07f-243">Сопоставление элементов RSS-канала со значениями свойств диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="fa07f-244">В следующей таблице показано, как значения в элементах RSS-канала в предыдущем примере сопоставляются с определенными свойствами Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="fa07f-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="fa07f-245">Свойство диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="fa07f-246">Значение</span><span class="sxs-lookup"><span data-stu-id="fa07f-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa07f-247">g \_ всзвмдмаусордате</span><span class="sxs-lookup"><span data-stu-id="fa07f-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="fa07f-248">Пятница, 9 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="fa07f-249">g \_ всзвмдмдескриптион</span><span class="sxs-lookup"><span data-stu-id="fa07f-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="fa07f-250">Исполнительный директор по компании Lucerne Питер банков, который просматривает последние тенденции в онлайн-публикациях.</span><span class="sxs-lookup"><span data-stu-id="fa07f-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="fa07f-251">\_ \_ URL-адрес всзвмдмдестинатион g</span><span class="sxs-lookup"><span data-stu-id="fa07f-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="fa07f-252">g \_ всзвмдмедитор</span><span class="sxs-lookup"><span data-stu-id="fa07f-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="fa07f-253">g \_ всзвмдмфилекреатиондате</span><span class="sxs-lookup"><span data-stu-id="fa07f-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="fa07f-254">Пятница, 9 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="fa07f-255">g \_ всзвмдмфиленаме</span><span class="sxs-lookup"><span data-stu-id="fa07f-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="fa07f-256">Цифровая публикация</span><span class="sxs-lookup"><span data-stu-id="fa07f-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="fa07f-257">g \_ всзвмдмфилесизе</span><span class="sxs-lookup"><span data-stu-id="fa07f-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="fa07f-258">13 790</span><span class="sxs-lookup"><span data-stu-id="fa07f-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="fa07f-259">g \_ всзвмдмформаткоде</span><span class="sxs-lookup"><span data-stu-id="fa07f-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="fa07f-260">ВМДМ \_ форматкоде \_ мультимедиа \_ -приведение</span><span class="sxs-lookup"><span data-stu-id="fa07f-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="fa07f-261">g \_ всзвмдмженре</span><span class="sxs-lookup"><span data-stu-id="fa07f-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="fa07f-262">Новости</span><span class="sxs-lookup"><span data-stu-id="fa07f-262">News</span></span>                                                                                          |
| [<span data-ttu-id="fa07f-263">\_ \_ Дата изменения всзвмдмласт \_</span><span class="sxs-lookup"><span data-stu-id="fa07f-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="fa07f-264">Пятница, 9 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="fa07f-265">g \_ всзвмдмластмодифиеддате</span><span class="sxs-lookup"><span data-stu-id="fa07f-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="fa07f-266">Пятница, 9 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="fa07f-267">g \_ всзвмдмпровидеркопиригхт</span><span class="sxs-lookup"><span data-stu-id="fa07f-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="fa07f-268">2006. Публикация LP ЛЛЛП для компании Lucerne.</span><span class="sxs-lookup"><span data-stu-id="fa07f-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="fa07f-269">All Rights Reserved.</span><span class="sxs-lookup"><span data-stu-id="fa07f-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="fa07f-270">g \_ всзвмдмтиметоливе</span><span class="sxs-lookup"><span data-stu-id="fa07f-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="fa07f-271">240</span><span class="sxs-lookup"><span data-stu-id="fa07f-271">240</span></span>                                                                                           |
| [<span data-ttu-id="fa07f-272">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="fa07f-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="fa07f-273">Цифровая публикация</span><span class="sxs-lookup"><span data-stu-id="fa07f-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="fa07f-274">g \_ всзвмдмвебмастер</span><span class="sxs-lookup"><span data-stu-id="fa07f-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="fa07f-275">g \_ всзвмдмеар</span><span class="sxs-lookup"><span data-stu-id="fa07f-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="fa07f-276">Пятница, 9 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="fa07f-277">Сопоставление элементов изображения RSS со значениями свойств диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="fa07f-278">В следующей таблице показано, как значения в элементах изображения RSS в предыдущем примере сопоставляются с определенными свойствами Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="fa07f-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="fa07f-279">Свойство диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="fa07f-280">Значение</span><span class="sxs-lookup"><span data-stu-id="fa07f-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="fa07f-281">g \_ всзвмдмалбумковерформат</span><span class="sxs-lookup"><span data-stu-id="fa07f-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="fa07f-282">\_Формат объекта \_ WPD \_ GIF</span><span class="sxs-lookup"><span data-stu-id="fa07f-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="fa07f-283">g \_ всзвмдмалбумковерсизе</span><span class="sxs-lookup"><span data-stu-id="fa07f-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="fa07f-284">512</span><span class="sxs-lookup"><span data-stu-id="fa07f-284">512</span></span>                                              |
| [<span data-ttu-id="fa07f-285">g \_ всзвмдмдескриптион</span><span class="sxs-lookup"><span data-stu-id="fa07f-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="fa07f-286">Логотип компании Lucerne</span><span class="sxs-lookup"><span data-stu-id="fa07f-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="fa07f-287">g \_ всзвмдмдестинатионурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="fa07f-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="fa07f-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="fa07f-289">g \_ всзвмдмхеигхт</span><span class="sxs-lookup"><span data-stu-id="fa07f-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="fa07f-290">300</span><span class="sxs-lookup"><span data-stu-id="fa07f-290">300</span></span>                                              |
| [<span data-ttu-id="fa07f-291">g \_ всзвмдмсаурцеурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="fa07f-292">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="fa07f-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="fa07f-293">Публикация в компании Lucerne</span><span class="sxs-lookup"><span data-stu-id="fa07f-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="fa07f-294">g \_ всзвмдмвидс</span><span class="sxs-lookup"><span data-stu-id="fa07f-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="fa07f-295">300</span><span class="sxs-lookup"><span data-stu-id="fa07f-295">300</span></span>                                              |



 

<span data-ttu-id="fa07f-296">Сопоставление элементов RSS-элемента со значениями свойств диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="fa07f-297">В следующей таблице описано, как значения в элементах элементов RSS в предыдущем примере сопоставляются с определенными свойствами Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="fa07f-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="fa07f-298">Свойство диспетчер устройств Windows Media</span><span class="sxs-lookup"><span data-stu-id="fa07f-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="fa07f-299">Значение</span><span class="sxs-lookup"><span data-stu-id="fa07f-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa07f-300">g \_ всзвмдмаусор</span><span class="sxs-lookup"><span data-stu-id="fa07f-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="fa07f-301">Компания</span><span class="sxs-lookup"><span data-stu-id="fa07f-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="fa07f-302">g \_ всзвмдмаусордате</span><span class="sxs-lookup"><span data-stu-id="fa07f-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="fa07f-303">"Чт, 1 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="fa07f-304">g \_ всзвмдмдескриптион</span><span class="sxs-lookup"><span data-stu-id="fa07f-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="fa07f-305">Оперативные публикации быстро меняются.</span><span class="sxs-lookup"><span data-stu-id="fa07f-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="fa07f-306">Генеральный директор по публикации изучает тенденции за последние пять лет и их последствия.</span><span class="sxs-lookup"><span data-stu-id="fa07f-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="fa07f-307">g \_ всзвмдмдестинатионурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="fa07f-308">g \_ всзвмдмдуратион</span><span class="sxs-lookup"><span data-stu-id="fa07f-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="fa07f-309">120325445</span><span class="sxs-lookup"><span data-stu-id="fa07f-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="fa07f-310">g \_ всзвмдмфилекреатиондате</span><span class="sxs-lookup"><span data-stu-id="fa07f-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="fa07f-311">"Чт, 1 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="fa07f-312">g \_ всзвмдмфилесизе</span><span class="sxs-lookup"><span data-stu-id="fa07f-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="fa07f-313">10329011</span><span class="sxs-lookup"><span data-stu-id="fa07f-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="fa07f-314">g \_ всзвмдмформаткоде</span><span class="sxs-lookup"><span data-stu-id="fa07f-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="fa07f-315">ВМДМ \_ форматкоде \_ MP3</span><span class="sxs-lookup"><span data-stu-id="fa07f-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="fa07f-316">g \_ всзвмдмженре</span><span class="sxs-lookup"><span data-stu-id="fa07f-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="fa07f-317">Новости</span><span class="sxs-lookup"><span data-stu-id="fa07f-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="fa07f-318">g \_ всзвмдмластмодифиеддате</span><span class="sxs-lookup"><span data-stu-id="fa07f-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="fa07f-319">"Чт, 1 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="fa07f-320">g \_ всзвмдммедиагуид</span><span class="sxs-lookup"><span data-stu-id="fa07f-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="fa07f-321">g \_ всзвмдмсаурцеурл</span><span class="sxs-lookup"><span data-stu-id="fa07f-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="fa07f-322">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="fa07f-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="fa07f-323">Цифровая публикация</span><span class="sxs-lookup"><span data-stu-id="fa07f-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="fa07f-324">g \_ всзвмдмеар</span><span class="sxs-lookup"><span data-stu-id="fa07f-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="fa07f-325">"Чт, 1 июня 2006 14:00:28, EDT</span><span class="sxs-lookup"><span data-stu-id="fa07f-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="fa07f-326">См. также</span><span class="sxs-lookup"><span data-stu-id="fa07f-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa07f-327">**Константы метаданных**</span><span class="sxs-lookup"><span data-stu-id="fa07f-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




