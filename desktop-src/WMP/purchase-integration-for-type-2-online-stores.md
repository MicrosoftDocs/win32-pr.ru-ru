---
title: Интеграция покупки для типа 2 Online Stores
description: Интеграция покупки для типа 2 Online Stores
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Интернет-магазины проигрывателя Windows Media, приобретение интеграции
- Интернет-магазины, приобретение интеграции
- Тип 2 Интернет-магазинов, интеграция с покупкой
- Интернет-магазины проигрывателя Windows Media, интеграция покупок
- Интернет-магазины, интеграция покупок
- Тип 2 Интернет-магазинов, интеграция покупок
- Windows Media Player, интеграция с покупкой
- Проигрыватель Windows Media, интеграция покупок
- Интеграция с покупкой
- Интеграция покупок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700625"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="c501b-113">Интеграция покупки для типа 2 Online Stores</span><span class="sxs-lookup"><span data-stu-id="c501b-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="c501b-114">Когда проигрыватель Windows Media воспроизводит мультимедийное содержимое или пользователь выбирает **сведения об альбоме**, проигрыватель предоставляет пользователю ссылку на покупку компакт-диска или DVD, с которого поступило содержимое, если такая ссылка доступна.</span><span class="sxs-lookup"><span data-stu-id="c501b-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="c501b-115">Когда пользователь щелкнет ссылку, проигрыватель Windows Media 10 или более поздней версии вызывает в текущем музыкальном магазине, чтобы справиться с запросом на покупку.</span><span class="sxs-lookup"><span data-stu-id="c501b-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="c501b-116">В этом случае игрок переходит к первой области задач службы (в проигрывателе Windows Media 10) или вкладке Интернет-магазины (в проигрывателе Windows Media 11) и отображает веб-страницу, заданную атрибутом **медиаплайерурл** элемента **буйкд** документа serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="c501b-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="c501b-117">(Атрибуты **медиацентерурл** и **бровсерурл** используются аналогичным образом для обработки вызовов из Windows xp Media Center Edition 2004 и Windows XP с пакетом обновления 2 (SP2)).</span><span class="sxs-lookup"><span data-stu-id="c501b-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="c501b-118">Проигрыватель Windows Media добавляет строку запроса в URL-адрес для предоставления информации в Интернет-магазине о содержимом, которое пользователь выбрал для покупки.</span><span class="sxs-lookup"><span data-stu-id="c501b-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="c501b-119">Строка запроса содержит такие атрибуты, как **Title**, **альбом** и **исполнитель**, которые Интернет-магазин может использовать для определения нужного альбома для продажи.</span><span class="sxs-lookup"><span data-stu-id="c501b-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="c501b-120">Справочная документация по элементу **буйкд** содержит полный список атрибутов строки запроса и их описания.</span><span class="sxs-lookup"><span data-stu-id="c501b-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="c501b-121">Рекомендации для страницы Буйкд</span><span class="sxs-lookup"><span data-stu-id="c501b-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="c501b-122">При создании веб-страницы Буйкд используйте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="c501b-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="c501b-123">Страница должна четко определять Интернет-магазин, предоставляющий информацию.</span><span class="sxs-lookup"><span data-stu-id="c501b-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="c501b-124">Это можно сделать, например, с помощью наглядного отображения логотипа.</span><span class="sxs-lookup"><span data-stu-id="c501b-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="c501b-125">Страница должна содержать ссылку на заявление о конфиденциальности вашей компании.</span><span class="sxs-lookup"><span data-stu-id="c501b-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="c501b-126">Рекомендуется предоставлять первоначальную информацию о приобретении, не требуя от пользователя устанавливать программы или входить в Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="c501b-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c501b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c501b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c501b-128">**Сведения о типе 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="c501b-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c501b-129">**Буйкд, элемент**</span><span class="sxs-lookup"><span data-stu-id="c501b-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 




