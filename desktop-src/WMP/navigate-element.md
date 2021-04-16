---
title: Элемент Navigate
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент Navigate указывает URL-адрес, используемый вызовами метода external. Навигатетаскпанеурл.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Навигация по элементу проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648737"
---
# <a name="navigate-element"></a><span data-ttu-id="811c7-106">Элемент Navigate</span><span class="sxs-lookup"><span data-stu-id="811c7-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="811c7-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="811c7-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="811c7-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="811c7-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="811c7-109">Элемент **navigate** указывает URL-адрес, используемый вызовами метода **External. навигатетаскпанеурл**.</span><span class="sxs-lookup"><span data-stu-id="811c7-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="811c7-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="811c7-110">Attributes</span></span>



| <span data-ttu-id="811c7-111">Термин</span><span class="sxs-lookup"><span data-stu-id="811c7-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="811c7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="811c7-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="811c7-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="811c7-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="811c7-114">Полный URL-адрес веб-страницы, к которой осуществляется переход.</span><span class="sxs-lookup"><span data-stu-id="811c7-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="811c7-115">**Навигатетаскпанеурл** может добавлять строку запроса к этому URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="811c7-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="811c7-116">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="811c7-116">Parent/Child Elements</span></span>



| <span data-ttu-id="811c7-117">Иерархия</span><span class="sxs-lookup"><span data-stu-id="811c7-117">Hierarchy</span></span>       | <span data-ttu-id="811c7-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="811c7-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="811c7-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="811c7-119">Parent elements</span></span> | <span data-ttu-id="811c7-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="811c7-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="811c7-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="811c7-121">Child elements</span></span>  | <span data-ttu-id="811c7-122">Нет</span><span class="sxs-lookup"><span data-stu-id="811c7-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="811c7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="811c7-123">Requirements</span></span>



| <span data-ttu-id="811c7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="811c7-124">Requirement</span></span> | <span data-ttu-id="811c7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="811c7-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="811c7-126">Версия</span><span class="sxs-lookup"><span data-stu-id="811c7-126">Version</span></span><br/> | <span data-ttu-id="811c7-127">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="811c7-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="811c7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="811c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811c7-129">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="811c7-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="811c7-130">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="811c7-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="811c7-131">**External. Навигатетаскпанеурл**</span><span class="sxs-lookup"><span data-stu-id="811c7-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="811c7-132">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="811c7-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





