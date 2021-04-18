---
title: ServiceInfo, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент ServiceInfo является основным элементом для ServiceInfo.xml документа.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Проигрыватель Windows Media, элемент ServiceInfo
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648736"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="9a5c2-106">ServiceInfo, элемент</span><span class="sxs-lookup"><span data-stu-id="9a5c2-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="9a5c2-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9a5c2-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9a5c2-109">Элемент **serviceInfo** является основным элементом для ServiceInfo.xml документа.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="9a5c2-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a5c2-110">Attributes</span></span>



| <span data-ttu-id="9a5c2-111">Термин</span><span class="sxs-lookup"><span data-stu-id="9a5c2-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="9a5c2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9a5c2-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5c2-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Версия** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="9a5c2-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="9a5c2-114">Версия файла ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="9a5c2-115">Версия 1,00 поддерживается для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="9a5c2-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Ключ** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="9a5c2-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="9a5c2-117">Строка ключа службы, однозначно определяющая Интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="9a5c2-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**контентпартнер**</span><span class="sxs-lookup"><span data-stu-id="9a5c2-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="9a5c2-119">Указывает, является ли Интернет-магазин хранилищем типа 1.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="9a5c2-120">Значение "true" указывает, что хранилищем является хранилище типа 1.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="9a5c2-121">Значение "false" указывает, что хранилище не является хранилищем типа 1; то есть, это хранилище типа 2.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="9a5c2-122">Значение по умолчанию — «false».</span><span class="sxs-lookup"><span data-stu-id="9a5c2-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="9a5c2-123">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a5c2-123">Parent/Child Elements</span></span>



| <span data-ttu-id="9a5c2-124">Иерархия</span><span class="sxs-lookup"><span data-stu-id="9a5c2-124">Hierarchy</span></span>       | <span data-ttu-id="9a5c2-125">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a5c2-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5c2-126">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9a5c2-126">Parent elements</span></span> | <span data-ttu-id="9a5c2-127">None</span><span class="sxs-lookup"><span data-stu-id="9a5c2-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="9a5c2-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a5c2-128">Child elements</span></span>  | <span data-ttu-id="9a5c2-129">**Албуминфо**, **буйкд**, **Цвет**, **Описание**, **FriendlyName**, **хтмлвиев**, **изображение**, **Справочный центр**, **Установка**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="9a5c2-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9a5c2-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a5c2-130">Remarks</span></span>

<span data-ttu-id="9a5c2-131">В следующей таблице приведены параметры, отправленные с помощью запроса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="9a5c2-132">Другие могут присутствовать в целях совместимости с прежними версиями.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="9a5c2-133">Запрос также будет включать все параметры, указанные с помощью параметра командной строки Сервицеекстра программы установки проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="9a5c2-134">Имя</span><span class="sxs-lookup"><span data-stu-id="9a5c2-134">Name</span></span>         | <span data-ttu-id="9a5c2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9a5c2-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5c2-136">*графическом*</span><span class="sxs-lookup"><span data-stu-id="9a5c2-136">*geoid*</span></span>      | <span data-ttu-id="9a5c2-137">Идентификатор географического расположения Windows.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-137">Windows geographical location ID.</span></span> <span data-ttu-id="9a5c2-138">Идентификатор расположения задается пользователем в области **Расположение** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="9a5c2-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="9a5c2-139">*locale*</span></span>     | <span data-ttu-id="9a5c2-140">Идентификатор локали проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="9a5c2-141">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="9a5c2-141">*userlocale*</span></span> | <span data-ttu-id="9a5c2-142">Идентификатор локали Windows.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-142">Windows locale ID.</span></span> <span data-ttu-id="9a5c2-143">Языковой стандарт задается пользователем в области **стандарты и форматы** языковых и региональных параметров на панели управления.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="9a5c2-144">*version*</span><span class="sxs-lookup"><span data-stu-id="9a5c2-144">*version*</span></span>    | <span data-ttu-id="9a5c2-145">Номер версии проигрывателя Windows Media в следующем формате: 10.0. x. xxxx или 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="9a5c2-146">Требования</span><span class="sxs-lookup"><span data-stu-id="9a5c2-146">Requirements</span></span>



| <span data-ttu-id="9a5c2-147">Требование</span><span class="sxs-lookup"><span data-stu-id="9a5c2-147">Requirement</span></span> | <span data-ttu-id="9a5c2-148">Значение</span><span class="sxs-lookup"><span data-stu-id="9a5c2-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="9a5c2-149">Версия</span><span class="sxs-lookup"><span data-stu-id="9a5c2-149">Version</span></span><br/> | <span data-ttu-id="9a5c2-150">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9a5c2-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a5c2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a5c2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5c2-152">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="9a5c2-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="9a5c2-153">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="9a5c2-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="9a5c2-154">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9a5c2-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





