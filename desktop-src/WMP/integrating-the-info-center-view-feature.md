---
title: Интеграция функции представления центра информации
description: Интеграция функции представления центра информации
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Интернет-магазины проигрывателя Windows Media, интеграция представления центра информации
- Интернет-магазины, интеграция представления центра информации
- Тип 1 Интернет-магазины, интеграция представления центра информации
- Тип 2 Интернет-магазинов, интеграция представления центра сведений
- Интернет-магазины проигрывателя Windows Media, представление информационной центра
- Интернет-магазины, представление информационной центра
- Тип 1 Интернет-магазины, представление информационной центра
- Тип 2 Интернет-магазинов, представление информационной центра
- Интеграция представления центра сведений
- Представление центра информации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681516"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="796d9-113">Интеграция функции представления центра информации</span><span class="sxs-lookup"><span data-stu-id="796d9-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="796d9-114">Проигрыватель Windows Media позволяет пользователям открывать и закрывать функцию просмотра центра информации.</span><span class="sxs-lookup"><span data-stu-id="796d9-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="796d9-115">Представление центра информации — это функция, в которой пользователи хотят найти обширную, расширенную информацию о конкретном цифровом содержимом.</span><span class="sxs-lookup"><span data-stu-id="796d9-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="796d9-116">Когда пользователь выбирает представление центра сведений, проигрыватель Windows Media вызывает в текущем музыкальном магазине, чтобы отобразить веб-страницу представления центра информации, заданную атрибутом **URL-адреса** элемента " **информационный** центр" документа serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="796d9-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="796d9-117">Чтобы получить сведения о текущем воспроизводимом цифровом содержимом, необходимо внедрить на веб-страницу экземпляр элемента управления проигрывателя Windows Media и использовать объектную модель проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="796d9-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="796d9-118">Например, чтобы получить заголовок, можно использовать следующий код JScript:</span><span class="sxs-lookup"><span data-stu-id="796d9-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="796d9-119">Рекомендации по представлению информационной центра</span><span class="sxs-lookup"><span data-stu-id="796d9-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="796d9-120">При создании веб-страницы **представления центра информации** используйте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="796d9-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="796d9-121">Страница должна четко определять Интернет-магазин, предоставляющий информацию.</span><span class="sxs-lookup"><span data-stu-id="796d9-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="796d9-122">Это можно сделать, например, с помощью наглядного отображения логотипа.</span><span class="sxs-lookup"><span data-stu-id="796d9-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="796d9-123">Страница должна содержать ссылку на заявление о конфиденциальности вашей компании.</span><span class="sxs-lookup"><span data-stu-id="796d9-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="796d9-124">Старайтесь не использовать навигацию по страницам в представлении центра информации, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="796d9-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="796d9-125">Для большинства действий следует переходить к вашему Интернет-магазину.</span><span class="sxs-lookup"><span data-stu-id="796d9-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="796d9-126">Рекомендуется предоставлять ценную информацию, не требуя от пользователя устанавливать программы или входить в Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="796d9-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="796d9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="796d9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="796d9-128">**External. Навигатетаскпанеурл**</span><span class="sxs-lookup"><span data-stu-id="796d9-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="796d9-129">**Элемент справочного центра**</span><span class="sxs-lookup"><span data-stu-id="796d9-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="796d9-130">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="796d9-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="796d9-131">**Использование элемента управления проигрывателя Windows Media на веб-странице**</span><span class="sxs-lookup"><span data-stu-id="796d9-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




