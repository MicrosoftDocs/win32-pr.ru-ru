---
title: Интеграция сведений о альбоме
description: Интеграция сведений о альбоме
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Интернет-магазины проигрывателя Windows Media, интеграция сведений о альбоме
- Интернет-магазины, интеграция сведений о альбоме
- Тип 2 Интернет-магазинов, интеграция сведений о альбоме
- Интернет-магазины проигрывателя Windows Media, интеграция сведений о альбоме
- Интернет-магазины, интеграция сведений о альбоме
- Тип 2 Интернет-магазинов, интеграция сведений о альбоме
- Проигрыватель Windows Media, интеграция сведений о альбоме
- Проигрыватель Windows Media, интеграция сведений о альбоме
- интеграция сведений о альбоме
- интеграция сведений о альбоме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067893"
---
# <a name="album-info-integration"></a><span data-ttu-id="139f6-113">Интеграция сведений о альбоме</span><span class="sxs-lookup"><span data-stu-id="139f6-113">Album Info Integration</span></span>

<span data-ttu-id="139f6-114">Проигрыватель Windows Media позволяет пользователям запрашивать подробные сведения о компакт-диске или DVD-диске, с которого поступило мультимедийное содержимое, нажав кнопку, например, **Дополнительные сведения**.</span><span class="sxs-lookup"><span data-stu-id="139f6-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="139f6-115">Когда пользователь нажимает кнопку, проигрыватель Windows Media 10 или более поздней версии вызывает в текущем музыкальном магазине, чтобы отобразить сведения об альбоме.</span><span class="sxs-lookup"><span data-stu-id="139f6-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="139f6-116">В этом случае проигрыватель открывает панель сведения о альбоме и отображает веб-страницу, указанную атрибутом **URL-адреса** элемента **албуминфо** документа serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="139f6-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="139f6-117">Проигрыватель Windows Media добавляет строку запроса в URL-адрес, чтобы предоставить сведения о содержимом, запрошенном пользователем, в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="139f6-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="139f6-118">Строка запроса содержит такие атрибуты, как **Title**, **альбом** и **исполнитель**, которые Интернет-магазин может использовать для определения правильного отображаемого альбома.</span><span class="sxs-lookup"><span data-stu-id="139f6-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="139f6-119">Справочная документация по элементу **албуминфо** содержит полный список атрибутов строки запроса и их описания.</span><span class="sxs-lookup"><span data-stu-id="139f6-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="139f6-120">Рекомендации по использованию сведений об альбоме</span><span class="sxs-lookup"><span data-stu-id="139f6-120">Guidelines for Album Info</span></span>

<span data-ttu-id="139f6-121">При создании веб-страницы сведений о диске используйте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="139f6-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="139f6-122">Страница должна четко определять Интернет-магазин, предоставляющий информацию.</span><span class="sxs-lookup"><span data-stu-id="139f6-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="139f6-123">Это можно сделать, например, с помощью наглядного отображения логотипа.</span><span class="sxs-lookup"><span data-stu-id="139f6-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="139f6-124">Страница должна содержать ссылку на заявление о конфиденциальности вашей компании.</span><span class="sxs-lookup"><span data-stu-id="139f6-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="139f6-125">По возможности избегайте перехода по страницам в компоненте «сведения о диске».</span><span class="sxs-lookup"><span data-stu-id="139f6-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="139f6-126">Для большинства действий следует переходить к вашему Интернет-магазину.</span><span class="sxs-lookup"><span data-stu-id="139f6-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="139f6-127">Рекомендуется предоставлять ценную информацию, не требуя от пользователя устанавливать программы или входить в Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="139f6-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="139f6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="139f6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="139f6-129">**Сведения о типе 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="139f6-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="139f6-130">**Албуминфо, элемент**</span><span class="sxs-lookup"><span data-stu-id="139f6-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 




