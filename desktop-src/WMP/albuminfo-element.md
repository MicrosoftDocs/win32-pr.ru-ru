---
title: Албуминфо, элемент
description: Элемент Албуминфо указывает URL-адрес веб-страницы, отображаемой проигрывателем Windows Media, когда пользователь выбирает просмотр дополнительных сведений об определенном элементе мультимедиа.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Проигрыватель Windows Media, элемент Албуминфо
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695087"
---
# <a name="albuminfo-element"></a><span data-ttu-id="ab7fa-104">Албуминфо, элемент</span><span class="sxs-lookup"><span data-stu-id="ab7fa-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="ab7fa-105">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ab7fa-106">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ab7fa-107">Элемент **албуминфо** указывает URL-адрес веб-страницы, отображаемой проигрывателем Windows Media, когда пользователь выбирает просмотр дополнительных сведений об определенном элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="ab7fa-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ab7fa-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="ab7fa-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL-адрес** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ab7fa-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="ab7fa-110">URL-адрес веб-страницы, отображаемой проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="ab7fa-111">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ab7fa-111">Parent/Child Elements</span></span>



| <span data-ttu-id="ab7fa-112">Иерархия</span><span class="sxs-lookup"><span data-stu-id="ab7fa-112">Hierarchy</span></span>       | <span data-ttu-id="ab7fa-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="ab7fa-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="ab7fa-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ab7fa-114">Parent elements</span></span> | <span data-ttu-id="ab7fa-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ab7fa-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="ab7fa-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ab7fa-116">Child elements</span></span>  | <span data-ttu-id="ab7fa-117">Нет</span><span class="sxs-lookup"><span data-stu-id="ab7fa-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="ab7fa-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="ab7fa-118">Remarks</span></span>

<span data-ttu-id="ab7fa-119">Когда пользователь нажимает кнопку в проигрывателе Windows Media для просмотра дополнительных сведений об определенном элементе мультимедиа, проигрыватель отправляет запрос URL-адреса с параметрами, прикрепленными с помощью знака вопроса (?) разделитель строки запроса.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="ab7fa-120">В следующей таблице приведены параметры, отправленные с помощью запроса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="ab7fa-121">Другие могут присутствовать в целях совместимости с прежними версиями.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="ab7fa-122">Имя</span><span class="sxs-lookup"><span data-stu-id="ab7fa-122">Name</span></span>         | <span data-ttu-id="ab7fa-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ab7fa-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7fa-124">*Музыкальных*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-124">*Album*</span></span>      | <span data-ttu-id="ab7fa-125">Значение атрибута **WM/албумтитле** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="ab7fa-126">*Исполнител*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-126">*Artist*</span></span>     | <span data-ttu-id="ab7fa-127">Значение атрибута **WM/албумартист** , если оно существует, или значение атрибута **Author** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="ab7fa-128">*графическом*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-128">*geoid*</span></span>      | <span data-ttu-id="ab7fa-129">Идентификатор географического расположения Windows.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-129">Windows geographical location ID.</span></span> <span data-ttu-id="ab7fa-130">Идентификатор расположения задается пользователем в области **Расположение** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="ab7fa-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-131">*locale*</span></span>     | <span data-ttu-id="ab7fa-132">Идентификатор локали проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="ab7fa-133">*Title*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-133">*Title*</span></span>      | <span data-ttu-id="ab7fa-134">Значение атрибута **Title** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="ab7fa-135">*уфид*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-135">*UFID*</span></span>       | <span data-ttu-id="ab7fa-136">Значение атрибута **WM/уникуефилеидентифиер** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="ab7fa-137">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-137">*userlocale*</span></span> | <span data-ttu-id="ab7fa-138">Идентификатор локали Windows.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-138">Windows locale ID.</span></span> <span data-ttu-id="ab7fa-139">Языковой стандарт задается пользователем в области **стандарты и форматы** языковых и региональных параметров на панели управления.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="ab7fa-140">*version*</span><span class="sxs-lookup"><span data-stu-id="ab7fa-140">*version*</span></span>    | <span data-ttu-id="ab7fa-141">Номер версии проигрывателя Windows Media в следующем формате: 10.0. x. xxxx или 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="ab7fa-142">Требования</span><span class="sxs-lookup"><span data-stu-id="ab7fa-142">Requirements</span></span>



| <span data-ttu-id="ab7fa-143">Требование</span><span class="sxs-lookup"><span data-stu-id="ab7fa-143">Requirement</span></span> | <span data-ttu-id="ab7fa-144">Значение</span><span class="sxs-lookup"><span data-stu-id="ab7fa-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="ab7fa-145">Версия</span><span class="sxs-lookup"><span data-stu-id="ab7fa-145">Version</span></span><br/> | <span data-ttu-id="ab7fa-146">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab7fa-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab7fa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7fa-148">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="ab7fa-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="ab7fa-149">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="ab7fa-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="ab7fa-150">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ab7fa-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





