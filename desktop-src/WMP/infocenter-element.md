---
title: Элемент справочного центра
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Элемент справочного центра
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Элемент справочного центра проигрыватель Windows Media
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694662"
---
# <a name="infocenter-element"></a><span data-ttu-id="4f394-105">Элемент справочного центра</span><span class="sxs-lookup"><span data-stu-id="4f394-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="4f394-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="4f394-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4f394-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4f394-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4f394-108">Элемент " **информационный центр** " указывает URL-адрес веб-страницы, которую проигрыватель Windows Media отображает в окне просмотра центра информации **, если Интернет** -магазин активен.</span><span class="sxs-lookup"><span data-stu-id="4f394-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="4f394-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f394-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="4f394-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL-адрес** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="4f394-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="4f394-111">URL-адрес веб-страницы, отображаемой проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4f394-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="4f394-112">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4f394-112">Parent/Child Elements</span></span>



| <span data-ttu-id="4f394-113">Иерархия</span><span class="sxs-lookup"><span data-stu-id="4f394-113">Hierarchy</span></span>       | <span data-ttu-id="4f394-114">Элемент</span><span class="sxs-lookup"><span data-stu-id="4f394-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="4f394-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4f394-115">Parent elements</span></span> | <span data-ttu-id="4f394-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="4f394-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="4f394-117">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4f394-117">Child elements</span></span>  | <span data-ttu-id="4f394-118">Нет</span><span class="sxs-lookup"><span data-stu-id="4f394-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="4f394-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f394-119">Remarks</span></span>

<span data-ttu-id="4f394-120">Пользователь управляет, когда представление центра сведений активно.</span><span class="sxs-lookup"><span data-stu-id="4f394-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="4f394-121">Чтобы получить сведения о воспроизводимом в данный момент элементе мультимедиа, необходимо внедрить на веб-страницу экземпляр элемента управления проигрывателя Windows Media и использовать объектную модель проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="4f394-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="4f394-122">В следующей таблице приведены параметры, отправленные с помощью запроса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="4f394-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="4f394-123">Другие могут присутствовать в целях совместимости с прежними версиями.</span><span class="sxs-lookup"><span data-stu-id="4f394-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="4f394-124">Имя</span><span class="sxs-lookup"><span data-stu-id="4f394-124">Name</span></span>         | <span data-ttu-id="4f394-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4f394-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f394-126">*графическом*</span><span class="sxs-lookup"><span data-stu-id="4f394-126">*geoid*</span></span>      | <span data-ttu-id="4f394-127">Идентификатор географического расположения Windows.</span><span class="sxs-lookup"><span data-stu-id="4f394-127">Windows geographical location ID.</span></span> <span data-ttu-id="4f394-128">Идентификатор расположения задается пользователем в области **Расположение** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="4f394-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="4f394-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="4f394-129">*locale*</span></span>     | <span data-ttu-id="4f394-130">Идентификатор локали проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4f394-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="4f394-131">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="4f394-131">*userlocale*</span></span> | <span data-ttu-id="4f394-132">Идентификатор локали Windows.</span><span class="sxs-lookup"><span data-stu-id="4f394-132">Windows locale ID.</span></span> <span data-ttu-id="4f394-133">Языковой стандарт задается пользователем в области **стандарты и форматы** языковых и региональных параметров на панели управления.</span><span class="sxs-lookup"><span data-stu-id="4f394-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="4f394-134">*version*</span><span class="sxs-lookup"><span data-stu-id="4f394-134">*version*</span></span>    | <span data-ttu-id="4f394-135">Номер версии проигрывателя Windows Media в следующем формате: 10.0. x. xxxx или 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="4f394-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="4f394-136">Требования</span><span class="sxs-lookup"><span data-stu-id="4f394-136">Requirements</span></span>



| <span data-ttu-id="4f394-137">Требование</span><span class="sxs-lookup"><span data-stu-id="4f394-137">Requirement</span></span> | <span data-ttu-id="4f394-138">Значение</span><span class="sxs-lookup"><span data-stu-id="4f394-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="4f394-139">Версия</span><span class="sxs-lookup"><span data-stu-id="4f394-139">Version</span></span><br/> | <span data-ttu-id="4f394-140">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4f394-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f394-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f394-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f394-142">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="4f394-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="4f394-143">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="4f394-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="4f394-144">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="4f394-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





