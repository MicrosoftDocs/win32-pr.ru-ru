---
title: Хтмлвиев, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент Хтмлвиев указывает базовый URL-адрес веб-страницы Хтмлвиев.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Проигрыватель Windows Media, элемент Хтмлвиев
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695014"
---
# <a name="htmlview-element"></a><span data-ttu-id="d561f-106">Хтмлвиев, элемент</span><span class="sxs-lookup"><span data-stu-id="d561f-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="d561f-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="d561f-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d561f-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d561f-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d561f-109">Элемент **хтмлвиев** указывает базовый URL-адрес веб-страницы хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="d561f-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="d561f-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d561f-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="d561f-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="d561f-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="d561f-112">Базовый URL-адрес веб-страницы Хтмлвиев, отображаемой проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d561f-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="d561f-113">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d561f-113">Parent/Child Elements</span></span>



| <span data-ttu-id="d561f-114">Иерархия</span><span class="sxs-lookup"><span data-stu-id="d561f-114">Hierarchy</span></span>       | <span data-ttu-id="d561f-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="d561f-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="d561f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d561f-116">Parent elements</span></span> | <span data-ttu-id="d561f-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="d561f-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="d561f-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d561f-118">Child elements</span></span>  | <span data-ttu-id="d561f-119">Нет</span><span class="sxs-lookup"><span data-stu-id="d561f-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="d561f-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="d561f-120">Remarks</span></span>

<span data-ttu-id="d561f-121">Этот элемент можно использовать для интеграции функции Хтмлвиев с вашим Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="d561f-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="d561f-122">Если домен URL-адреса, указанного в текущем интернет-магазине, соответствует одному для веб-страницы Хтмлвиев, переключиться на **Воспроизведение выполняется** без вмешательства пользователя и отображения содержимого хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="d561f-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="d561f-123">В противном случае проигрыватель Windows Media запрашивает у пользователя разрешение на отображение содержимого Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="d561f-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="d561f-124">Например, если URL-адрес веб-страницы Хтмлвиев имеет значение https://www.proseware.com/html/HTMLView.htm , а URL-адрес для атрибута **BaseURL** указан как https://www.proseware.com , то веб-страница хтмлвиев отображается без запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="d561f-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="d561f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d561f-125">Requirements</span></span>



| <span data-ttu-id="d561f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d561f-126">Requirement</span></span> | <span data-ttu-id="d561f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d561f-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="d561f-128">Версия</span><span class="sxs-lookup"><span data-stu-id="d561f-128">Version</span></span><br/> | <span data-ttu-id="d561f-129">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d561f-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d561f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d561f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d561f-131">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d561f-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="d561f-132">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="d561f-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="d561f-133">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="d561f-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="d561f-134">**PARAM, элемент**</span><span class="sxs-lookup"><span data-stu-id="d561f-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="d561f-135">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="d561f-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





