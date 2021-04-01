---
title: Тестовые и производственные ключи для Интернет-магазина типа 2
description: Тестовые и производственные ключи для Интернет-магазина типа 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Интернет-магазины проигрывателя Windows Media, тестовые ключи
- Интернет-магазины, тестовые ключи
- Тип 2 Интернет-магазинов, тестовые ключи
- Интернет-магазины проигрывателя Windows Media, рабочие ключи
- Интернет-магазины, производственные ключи
- Тип 2 Интернет-магазинов, производственные ключи
- Интернет-магазины проигрывателя Windows Media, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 2 Интернет-магазинов, документ ServiceInfo
- тестовые ключи
- производственные ключи
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986749"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a><span data-ttu-id="1e9bb-115">Тестовые и производственные ключи для Интернет-магазина типа 2</span><span class="sxs-lookup"><span data-stu-id="1e9bb-115">Test and Production Keys for a Type 2 Online Store</span></span>

<span data-ttu-id="1e9bb-116">После начала разработки Интернет-магазина Корпорация Майкрософт предоставляет два числовых ключа: тестовый ключ и рабочий ключ.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="1e9bb-117">В то же время необходимо предоставить корпорации Майкрософт два URL-адреса: один из них указывает на документ Test ServiceInfo и один, который указывает на рабочий документ ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="1e9bb-118">На этапе разработки и тестирования Интернет-магазин отображается в проигрывателе Windows Media только в том случае, если ваш тестовый ключ или рабочий ключ находится в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="1e9bb-119">Если тестовый ключ находится в реестре, проигрыватель Windows Media извлекает документ Test ServiceInfo, который указывает на подключаемый модуль, веб-страницы и изображения, принадлежащие хранилищу тестов.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="1e9bb-120">Если рабочий ключ находится в реестре, проигрыватель Windows Media извлекает рабочий документ ServiceInfo, который указывает на подключаемый модуль, веб-страницы и изображения, принадлежащие рабочему магазину.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="1e9bb-121">Вы можете использовать хранилища тестов и рабочих хранилищ любым удобным для вас способом.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-121">You can use your test and production stores in any way you find useful.</span></span> <span data-ttu-id="1e9bb-122">Однако, как правило, это различие выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1e9bb-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="1e9bb-123">Хранилище тестов — это место, где вы вносите ежедневные изменения в подключаемый модуль, веб-страницы, изображения и другие компоненты службы.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="1e9bb-124">Рабочее хранилище — это место, где хранится стабильный выпуск службы, включающий подключаемый модуль, веб-страницы, изображения и другие компоненты.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="1e9bb-125">Прежде чем Интернет-магазин можно будет опубликовать в проигрывателе Windows Media, корпорация Майкрософт должна проверить, правильно ли работает служба.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="1e9bb-126">На этапе проверки Корпорация Майкрософт использует ваш рабочий ключ.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="1e9bb-127">Корпорация Майкрософт не использует ваш тестовый ключ на этапе проверки.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="1e9bb-128">Когда рабочий Интернет-магазин успешно завершает процесс проверки, корпорация Майкрософт публикует магазин. Это означает, что рабочее хранилище отображается в проигрывателе Windows Media для всех пользователей, а не только тех, у кого есть рабочий ключ в реестре.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="1e9bb-129">После публикации хранилища ключи тестирования и производства больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="1e9bb-130">Пользователи могут иметь возможность угадать тестовый или рабочий ключ для Интернет-магазина и просматривать магазин во время его разработки.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="1e9bb-131">Вы должны быть внимательны в предоставлении функций, которые вы хотите хранить в секрете до выхода общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="1e9bb-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="1e9bb-132">Подробные сведения о том, где можно разместить рабочие и тестовые ключи в реестре пользователя, см. в разделе [разделы реестра и записи для Интернет-магазина типа 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="1e9bb-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e9bb-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1e9bb-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e9bb-134">**Сведения о типе 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="1e9bb-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="1e9bb-135">**Тип 2 Примеры Интернет-магазина**</span><span class="sxs-lookup"><span data-stu-id="1e9bb-135">**Type 2 Online Store Samples**</span></span>](type-2-online-store-samples.md)
</dt> </dl>

 

 




