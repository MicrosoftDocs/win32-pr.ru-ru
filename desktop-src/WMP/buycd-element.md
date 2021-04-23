---
title: Буйкд, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Буйкд, элемент
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Проигрыватель Windows Media, элемент Буйкд
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694961"
---
# <a name="buycd-element"></a><span data-ttu-id="e6222-105">Буйкд, элемент</span><span class="sxs-lookup"><span data-stu-id="e6222-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="e6222-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="e6222-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e6222-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e6222-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e6222-108">Элемент **буйкд** указывает URL-адреса для веб-страниц, отображаемых проигрывателем Windows Media, когда пользователь решает выполнить покупку.</span><span class="sxs-lookup"><span data-stu-id="e6222-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="e6222-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e6222-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="e6222-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**Медиаплайерурл** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="e6222-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="e6222-111">URL-адрес веб-страницы, отображаемой Интернет-магазином для приобретения компакт-диска или DVD-диска в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e6222-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="e6222-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**медиацентерурл**</span><span class="sxs-lookup"><span data-stu-id="e6222-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="e6222-113">URL-адрес веб-страницы. в Интернет-магазине появится компакт-диск или DVD-диск для приобретения в обновлении Windows XP Media Center Edition 2004.</span><span class="sxs-lookup"><span data-stu-id="e6222-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="e6222-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**бровсерурл**</span><span class="sxs-lookup"><span data-stu-id="e6222-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="e6222-115">URL-адрес веб-страницы, отображаемой Интернет-магазином для приобретения компакт-диска или DVD-диска в отдельном окне браузера.</span><span class="sxs-lookup"><span data-stu-id="e6222-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="e6222-116">Этот URL-адрес также используется в Windows XP с пакетом обновления 2 (SP2) или более поздней версии для компонента " **магазин для музыки** " в Интернете.</span><span class="sxs-lookup"><span data-stu-id="e6222-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="e6222-117">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e6222-117">Parent/Child Elements</span></span>



| <span data-ttu-id="e6222-118">Иерархия</span><span class="sxs-lookup"><span data-stu-id="e6222-118">Hierarchy</span></span>       | <span data-ttu-id="e6222-119">Элемент</span><span class="sxs-lookup"><span data-stu-id="e6222-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="e6222-120">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e6222-120">Parent elements</span></span> | <span data-ttu-id="e6222-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e6222-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="e6222-122">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e6222-122">Child elements</span></span>  | <span data-ttu-id="e6222-123">Нет</span><span class="sxs-lookup"><span data-stu-id="e6222-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="e6222-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6222-124">Remarks</span></span>

<span data-ttu-id="e6222-125">Когда пользователь нажимает кнопку или ссылку в проигрывателе Windows Media для приобретения компакт-диска или DVD, проигрыватель отправляет запрос URL-адреса в ServiceTask1 с параметрами, вложенными с помощью разделителя строк запроса (?).</span><span class="sxs-lookup"><span data-stu-id="e6222-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="e6222-126">В следующей таблице приведены параметры, отправленные с помощью запроса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e6222-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="e6222-127">Другие могут присутствовать в целях совместимости с прежними версиями.</span><span class="sxs-lookup"><span data-stu-id="e6222-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="e6222-128">Имя</span><span class="sxs-lookup"><span data-stu-id="e6222-128">Name</span></span>         | <span data-ttu-id="e6222-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e6222-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6222-130">*Музыкальных*</span><span class="sxs-lookup"><span data-stu-id="e6222-130">*Album*</span></span>      | <span data-ttu-id="e6222-131">Значение атрибута **WM/албумтитле** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e6222-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="e6222-132">*Исполнител*</span><span class="sxs-lookup"><span data-stu-id="e6222-132">*Artist*</span></span>     | <span data-ttu-id="e6222-133">Значение атрибута **WM/албумартист** , если оно существует, или значение атрибута **Author** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e6222-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="e6222-134">*графическом*</span><span class="sxs-lookup"><span data-stu-id="e6222-134">*geoid*</span></span>      | <span data-ttu-id="e6222-135">Идентификатор географического расположения Windows.</span><span class="sxs-lookup"><span data-stu-id="e6222-135">Windows geographical location ID.</span></span> <span data-ttu-id="e6222-136">Идентификатор расположения задается пользователем в области **Расположение** в разделе региональные и языковые параметры панели управления.</span><span class="sxs-lookup"><span data-stu-id="e6222-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="e6222-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="e6222-137">*locale*</span></span>     | <span data-ttu-id="e6222-138">Идентификатор локали проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e6222-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="e6222-139">*Title*</span><span class="sxs-lookup"><span data-stu-id="e6222-139">*Title*</span></span>      | <span data-ttu-id="e6222-140">Значение атрибута **Title** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e6222-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="e6222-141">*уфид*</span><span class="sxs-lookup"><span data-stu-id="e6222-141">*UFID*</span></span>       | <span data-ttu-id="e6222-142">Значение атрибута **WM/уникуефилеидентифиер** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e6222-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="e6222-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="e6222-143">*userlocale*</span></span> | <span data-ttu-id="e6222-144">Идентификатор локали Windows.</span><span class="sxs-lookup"><span data-stu-id="e6222-144">Windows locale ID.</span></span> <span data-ttu-id="e6222-145">Языковой стандарт задается пользователем в области **стандарты и форматы** языковых и региональных параметров на панели управления.</span><span class="sxs-lookup"><span data-stu-id="e6222-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="e6222-146">*version*</span><span class="sxs-lookup"><span data-stu-id="e6222-146">*version*</span></span>    | <span data-ttu-id="e6222-147">Номер версии проигрывателя Windows Media в следующем формате: 10.0. x. xxxx или 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="e6222-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="e6222-148">Windows XP Media Center Edition 2004 предоставляет пользователям пользовательский интерфейс, предназначенный для просмотра на расстоянии.</span><span class="sxs-lookup"><span data-stu-id="e6222-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="e6222-149">Необходимо создать веб-страницы, чтобы параметр *медиацентерурл* можно было просматривать на больших экранах.</span><span class="sxs-lookup"><span data-stu-id="e6222-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6222-150">Требования</span><span class="sxs-lookup"><span data-stu-id="e6222-150">Requirements</span></span>



| <span data-ttu-id="e6222-151">Требование</span><span class="sxs-lookup"><span data-stu-id="e6222-151">Requirement</span></span> | <span data-ttu-id="e6222-152">Значение</span><span class="sxs-lookup"><span data-stu-id="e6222-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="e6222-153">Версия</span><span class="sxs-lookup"><span data-stu-id="e6222-153">Version</span></span><br/> | <span data-ttu-id="e6222-154">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e6222-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6222-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6222-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6222-156">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="e6222-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e6222-157">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="e6222-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e6222-158">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e6222-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





