---
title: Рекомендации для международных рынков
description: Рекомендации для международных рынков
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Интернет-магазины проигрывателя Windows Media, международные рынки
- Интернет-магазины, международные рынки
- Тип 1 Интернет-магазины, международные рынки
- Тип 2 Интернет-магазинов, международные рынки
- международные рынки
- Интернет-магазины проигрывателя Windows Media, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 1 Интернет-магазины, документ ServiceInfo
- Тип 2 Интернет-магазинов, документ ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691274"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="8a568-113">Рекомендации для международных рынков</span><span class="sxs-lookup"><span data-stu-id="8a568-113">Considerations for International Markets</span></span>

<span data-ttu-id="8a568-114">Если ваша компания создает Интернет-магазины для нескольких рынков, для каждого рынка необходимо предоставить корпорации Майкрософт адрес URL документа ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="8a568-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="8a568-115">Это можно сделать одним из следующих двух способов:</span><span class="sxs-lookup"><span data-stu-id="8a568-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="8a568-116">Создайте отдельный документ ServiceInfo для каждого рынка.</span><span class="sxs-lookup"><span data-stu-id="8a568-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="8a568-117">В этом случае вы предоставляете корпорации Майкрософт URL-адреса, указывающие на отдельные документы ServiceInfo для каждого из Интернет-магазинов на каждом рынке.</span><span class="sxs-lookup"><span data-stu-id="8a568-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="8a568-118">Создайте отдельный документ ServiceInfo для всех рынков.</span><span class="sxs-lookup"><span data-stu-id="8a568-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="8a568-119">При этом вы предоставляете корпорации Майкрософт один и тот же URL-адрес для каждого рынка.</span><span class="sxs-lookup"><span data-stu-id="8a568-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="8a568-120">Документ ServiceInfo, созданный в виде ASP-страницы, может динамически определять расположение пользователя на основе параметров строки запроса.</span><span class="sxs-lookup"><span data-stu-id="8a568-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="8a568-121">Проигрыватель Windows Media добавляет строку запроса в запрос URL-адреса ServiceInfo, который предоставляет сведения о локали и параметрах расположения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8a568-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="8a568-122">Если Интернет-магазин использует эти сведения для определения отображаемого содержимого, следует динамически добавлять эти значения к своим URL-адресам в документе ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="8a568-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="8a568-123">Это лучший способ гарантировать, что URL-адреса веб-страниц всегда будут содержать нужные параметры.</span><span class="sxs-lookup"><span data-stu-id="8a568-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="8a568-124">Определив расположение пользователя и предпочитаемый язык, вы можете сохранить эти сведения для будущих сеансов.</span><span class="sxs-lookup"><span data-stu-id="8a568-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="8a568-125">Это можно сделать с помощью любого из методов, обычно используемых на веб-странице, таких как файлы cookie, или с помощью COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="8a568-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a568-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8a568-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a568-127">**Динамическое создание документа ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="8a568-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="8a568-128">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="8a568-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8a568-129">**ServiceInfo, элемент**</span><span class="sxs-lookup"><span data-stu-id="8a568-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 




