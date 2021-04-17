---
title: Элемент Image (пакет SDK для WMP)
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Элемент Image (пакет SDK для WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Проигрыватель Windows Media, элемент Image
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698845"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="61c51-105">Элемент Image (пакет SDK для WMP)</span><span class="sxs-lookup"><span data-stu-id="61c51-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="61c51-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="61c51-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="61c51-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61c51-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="61c51-108">Элемент **Image** указывает изображения, которые проигрыватель Windows Media отображает пользователю для представления Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="61c51-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="61c51-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="61c51-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="61c51-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**Еулаурл** (требуется для хранилищ типа 1, игнорируется для типа 2)</span><span class="sxs-lookup"><span data-stu-id="61c51-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="61c51-111">URL-адрес эмблемы, отображаемой проигрывателем Windows Media в диалоговом окне лицензионного соглашения (EULA).</span><span class="sxs-lookup"><span data-stu-id="61c51-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="61c51-112">Это должен быть изображение PNG, 80 x 80 пикселей.</span><span class="sxs-lookup"><span data-stu-id="61c51-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="61c51-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**Менуурл** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="61c51-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="61c51-114">URL-адрес изображения, отображаемого проигрывателем Windows Media в меню "службы".</span><span class="sxs-lookup"><span data-stu-id="61c51-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="61c51-115">Этот образ должен иметь размер 15 x 15 пикселей.</span><span class="sxs-lookup"><span data-stu-id="61c51-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="61c51-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**Сервицеларжеурл** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="61c51-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="61c51-117">Для Интернет-магазина типа 1 это URL изображения, отображаемого проигрывателем Windows Media на вкладке **Интернет-магазины** . Для проигрывателя Windows Media 11 этот рисунок должен иметь размер 45 пикселей в ширину на 13 пикселей.</span><span class="sxs-lookup"><span data-stu-id="61c51-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="61c51-118">Для проигрывателя Windows Media 12 этот рисунок должен иметь размер 45 пикселей в ширину на 30 пикселей в высокий.</span><span class="sxs-lookup"><span data-stu-id="61c51-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="61c51-119">Для поддержки обеих версий проигрывателя Windows Media версии 11 и 12 необходимо предоставить два отдельных документа ServiceInfo.xml, каждый из которых указывает на изображение соответствующего размера для Сервицеларжеурл.</span><span class="sxs-lookup"><span data-stu-id="61c51-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="61c51-120">Для Интернет-магазина типа 2 это URL-адрес изображения, отображаемого проигрывателем Windows Media рядом с вкладкой **Интернет-магазины** или рядом с кнопками области задач.</span><span class="sxs-lookup"><span data-stu-id="61c51-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="61c51-121">Этот образ должен иметь 30 x 30 пикселей.</span><span class="sxs-lookup"><span data-stu-id="61c51-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="61c51-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**Сервицесмаллурл** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="61c51-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="61c51-123">URL-адрес логотипа, который отображается вместе с описанием маркетинга, указанным в элементе **Description** .</span><span class="sxs-lookup"><span data-stu-id="61c51-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="61c51-124">Если он не указан, он будет пустым.</span><span class="sxs-lookup"><span data-stu-id="61c51-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="61c51-125">(Все типы, необязательно) Это должен быть изображение PNG шириной 45 пикселей и высотой в 13 пикселей.</span><span class="sxs-lookup"><span data-stu-id="61c51-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="61c51-126">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="61c51-126">Parent/Child Elements</span></span>



| <span data-ttu-id="61c51-127">Иерархия</span><span class="sxs-lookup"><span data-stu-id="61c51-127">Hierarchy</span></span>       | <span data-ttu-id="61c51-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="61c51-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="61c51-129">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="61c51-129">Parent elements</span></span> | <span data-ttu-id="61c51-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="61c51-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="61c51-131">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="61c51-131">Child elements</span></span>  | <span data-ttu-id="61c51-132">Нет</span><span class="sxs-lookup"><span data-stu-id="61c51-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="61c51-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="61c51-133">Remarks</span></span>

<span data-ttu-id="61c51-134">Поддерживаются форматы изображений GIF, JPG, BMP и PNG (рекомендуемый формат).</span><span class="sxs-lookup"><span data-stu-id="61c51-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="61c51-135">Использование прозрачности веб-сайта поддерживается и рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="61c51-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="61c51-136">Анимированные GIF-файлы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="61c51-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="61c51-137">Если значение для **менуурл** не указано, проигрыватель Windows Media не отображает в меню Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="61c51-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="61c51-138">Вы можете предоставить анимированное изображение для Сервицеларжеурл.</span><span class="sxs-lookup"><span data-stu-id="61c51-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="61c51-139">В проигрывателе Windows Media 10 или 11 изображение анимировано.</span><span class="sxs-lookup"><span data-stu-id="61c51-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="61c51-140">В проигрывателе Windows Media 12 отображается только первый кадр изображения.</span><span class="sxs-lookup"><span data-stu-id="61c51-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="61c51-141">Чтобы предоставить анимированное изображение, создайте один файл изображения, содержащий последовательные кадры анимации.</span><span class="sxs-lookup"><span data-stu-id="61c51-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="61c51-142">Например, для изображения с шириной 30 пикселей и высотой в 30 пикселей можно предоставить 20 последовательных изображений параллельно в изображении шириной 600 пикселей и высотой в 30 пикселей.</span><span class="sxs-lookup"><span data-stu-id="61c51-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="61c51-143">Проигрыватель Windows Media автоматически анимирует такой образ, отображая 20 отдельных изображений один за другим.</span><span class="sxs-lookup"><span data-stu-id="61c51-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="61c51-144">Эта анимация возникает только один раз при открытии Интернет-магазина. Он не повторяется.</span><span class="sxs-lookup"><span data-stu-id="61c51-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c51-145">Требования</span><span class="sxs-lookup"><span data-stu-id="61c51-145">Requirements</span></span>



| <span data-ttu-id="61c51-146">Требование</span><span class="sxs-lookup"><span data-stu-id="61c51-146">Requirement</span></span> | <span data-ttu-id="61c51-147">Значение</span><span class="sxs-lookup"><span data-stu-id="61c51-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="61c51-148">Версия</span><span class="sxs-lookup"><span data-stu-id="61c51-148">Version</span></span><br/> | <span data-ttu-id="61c51-149">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="61c51-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61c51-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61c51-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c51-151">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="61c51-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="61c51-152">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="61c51-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="61c51-153">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="61c51-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





