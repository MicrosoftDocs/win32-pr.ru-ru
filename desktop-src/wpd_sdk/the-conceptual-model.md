---
description: Концептуальная модель
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Концептуальная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265984"
---
# <a name="the-conceptual-model"></a><span data-ttu-id="81538-103">Концептуальная модель</span><span class="sxs-lookup"><span data-stu-id="81538-103">The Conceptual Model</span></span>

<span data-ttu-id="81538-104">В этом разделе описываются объекты, свойства и ресурсы, составляющие концептуальную модель WPD.</span><span class="sxs-lookup"><span data-stu-id="81538-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="81538-105">Объекты</span><span class="sxs-lookup"><span data-stu-id="81538-105">Objects</span></span>

<span data-ttu-id="81538-106">В WPD логические сущности на устройствах называются объектами.</span><span class="sxs-lookup"><span data-stu-id="81538-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="81538-107">Обычно, но не всегда, они представляют данные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="81538-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="81538-108">Объекты имеют свойства и на них ссылаются идентификаторы объектов.</span><span class="sxs-lookup"><span data-stu-id="81538-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="81538-109">К примерам объектов относятся изображения и папки на камере, песни и списки воспроизведения на проигрывателе мультимедиа, контакты на мобильном телефоне и т. д.</span><span class="sxs-lookup"><span data-stu-id="81538-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="81538-110">Объекты также могут представлять функциональные или информационные части устройства.</span><span class="sxs-lookup"><span data-stu-id="81538-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="81538-111">К таким примерам относятся элементы управления проигрывателя (воспроизведение/запись/пауза), параметры камеры, возможности SMS на мобильном телефоне и т. д.</span><span class="sxs-lookup"><span data-stu-id="81538-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="81538-112">В двух следующих разделах приведены примеры и иллюстрации двух типов объектов: объект Image и объект Медиакаст.</span><span class="sxs-lookup"><span data-stu-id="81538-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="81538-113">Объект Image</span><span class="sxs-lookup"><span data-stu-id="81538-113">Image Object</span></span>

<span data-ttu-id="81538-114">Объект Image представляет изображение по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="81538-114">An image object represents a still image.</span></span> <span data-ttu-id="81538-115">На следующей диаграмме показаны связи между объектом Image, его свойствами и ресурсами.</span><span class="sxs-lookup"><span data-stu-id="81538-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![Схема, показывающая объект WPD и его связь со свойствами и ресурсами](images/wpd-overview-figure2.gif)

<span data-ttu-id="81538-117">Дополнительные сведения об объекте Image и его свойствах см. в разделе [**о \_ \_ типе содержимого \_ WPD**](wpd-content-type-image.md) .</span><span class="sxs-lookup"><span data-stu-id="81538-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="81538-118">Объект медиакаст</span><span class="sxs-lookup"><span data-stu-id="81538-118">Mediacast Object</span></span>

<span data-ttu-id="81538-119">Объект Медиакаст можно рассматривать как объект-контейнер, группирующий связанное содержимое, как и список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="81538-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="81538-120">Часто объект Медиакаст используется для группировки мультимедийного содержимого, опубликованного в сети.</span><span class="sxs-lookup"><span data-stu-id="81538-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="81538-121">Например, RSS-канал может быть представлен как объект Медиакаст, объект которого ссылается на объекты содержимого, представляющие каждый элемент в канале.</span><span class="sxs-lookup"><span data-stu-id="81538-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="81538-122">На следующей схеме показана связь между объектом Медиакаст и тремя звуковыми объектами, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="81538-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![Схема, показывающая иерархическую структуру объекта медикаст и трех содержащихся в нем объектов](images/mediacast1.gif)

<span data-ttu-id="81538-124">Ссылки на объект Audio указываются в свойстве " [ \_ \_ ссылки на объект WPD](object-properties.md) " для объекта медиакаст.</span><span class="sxs-lookup"><span data-stu-id="81538-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="81538-125">Дополнительные сведения о свойствах, поддерживаемых объектом Медиакаст, см. в статье [**о \_ типе содержимого WPD \_ \_ Media \_ Cast**](wpd-content-type-media-cast.md) .</span><span class="sxs-lookup"><span data-stu-id="81538-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="81538-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="81538-126">Properties</span></span>

<span data-ttu-id="81538-127">Свойства объекта предоставляют механизм для обмена метаданными, описывающими объект.</span><span class="sxs-lookup"><span data-stu-id="81538-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="81538-128">Например, объект Image может содержать свойства, описывающие его имя, размер, формат, ширину в пикселях и т. д.</span><span class="sxs-lookup"><span data-stu-id="81538-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="81538-129">Свойства имеют текущее значение, а также атрибуты.</span><span class="sxs-lookup"><span data-stu-id="81538-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="81538-130">WPD определяет набор стандартных свойств, составляющих определения API и DDI.</span><span class="sxs-lookup"><span data-stu-id="81538-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="81538-131">Поставщики не ограничиваются стандартными свойствами WPD и могут добавлять свои собственные.</span><span class="sxs-lookup"><span data-stu-id="81538-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="81538-132">Атрибуты свойства</span><span class="sxs-lookup"><span data-stu-id="81538-132">Property Attributes</span></span>

<span data-ttu-id="81538-133">Атрибуты свойств описывают права доступа, допустимые значения и другие сведения, связанные со свойством.</span><span class="sxs-lookup"><span data-stu-id="81538-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="81538-134">Например, свойство, представляющее битовую скорость, может быть в диапазоне от 8 килобит в секунду (кбит/с) до 20 кбит/с с шагом в 1 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="81538-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="81538-135">Права доступа указывают, могут ли вызывающие объекты читать, записывать и (или) удалять свойство.</span><span class="sxs-lookup"><span data-stu-id="81538-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="81538-136">Допустимые значения указывают на ограничения для значений свойств.</span><span class="sxs-lookup"><span data-stu-id="81538-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="81538-137">Считается, что допустимые значения относятся к определенной форме.</span><span class="sxs-lookup"><span data-stu-id="81538-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="81538-138">Допустимые формы значений включают диапазон (то есть свойство может принимать значение от min до max с указанным шагом), перечисление (то есть значение свойства является одним из значений в указанном списке) и None (т. е. нет определенных допустимых значений).</span><span class="sxs-lookup"><span data-stu-id="81538-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="81538-139">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="81538-139">Resources</span></span>

<span data-ttu-id="81538-140">Ресурсы — это заполнители для двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="81538-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="81538-141">Объект может иметь более одного ресурса.</span><span class="sxs-lookup"><span data-stu-id="81538-141">An object can have more than one resource.</span></span> <span data-ttu-id="81538-142">Например, если объект представляет файл изображения с звуковой заметкой, то ресурсы для этого объекта могут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="81538-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="81538-143">Ресурс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81538-143">A default resource.</span></span> <span data-ttu-id="81538-144">Этот ресурс представляет весь файл изображения.</span><span class="sxs-lookup"><span data-stu-id="81538-144">This resource represents the entire image file.</span></span> <span data-ttu-id="81538-145">(Сюда входят все внедренные данные, такие как звуковые заметки, эскизы и т. д.)</span><span class="sxs-lookup"><span data-stu-id="81538-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="81538-146">Ресурс эскиза.</span><span class="sxs-lookup"><span data-stu-id="81538-146">A thumbnail resource.</span></span> <span data-ttu-id="81538-147">Этот ресурс представляет данные эскиза для изображения.</span><span class="sxs-lookup"><span data-stu-id="81538-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="81538-148">Ресурс заметки в звуковой заметке.</span><span class="sxs-lookup"><span data-stu-id="81538-148">An audio annotation resource.</span></span> <span data-ttu-id="81538-149">Этот ресурс представляет звуковые данные, связанные с изображением.</span><span class="sxs-lookup"><span data-stu-id="81538-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="81538-150">Атрибуты ресурсов</span><span class="sxs-lookup"><span data-stu-id="81538-150">Resource Attributes</span></span>

<span data-ttu-id="81538-151">Как и атрибуты свойств, атрибуты ресурсов описывают права доступа, размер, формат и другие сведения, связанные с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="81538-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="81538-152">Например, атрибуты для ресурса «Звуковая заметка» на объекте Image могут указывать скорость потока, число каналов и формат данных звука.</span><span class="sxs-lookup"><span data-stu-id="81538-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="81538-153">Подготовка профилей и атрибутов ресурсов</span><span class="sxs-lookup"><span data-stu-id="81538-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="81538-154">Профиль подготовки отчетов — это один из методов, используемых приложениями для обнаружения допустимых атрибутов для данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="81538-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="81538-155">Например, мобильный телефон может поддерживать точечные рисунки с определенными ограничениями по минимальным и максимальным значениям ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="81538-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="81538-156">При запросе профилей подготовки к просмотру для объекта Bitmap приложение может получить эти точные значения.</span><span class="sxs-lookup"><span data-stu-id="81538-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="81538-157">Следующий пример выходных данных определяет сведения о профиле отрисовки, возвращаемые устройством, если оно поддерживало точечные рисунки с минимальной высотой в 10 пикселей, минимальной шириной 20 пикселей, максимальной высотой 1000 пикселей и максимальной шириной 2000 пикселей.</span><span class="sxs-lookup"><span data-stu-id="81538-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



<span data-ttu-id="81538-158">Описание того, как приложение может извлечь профиль подготовки к просмотру (и связанные атрибуты ресурса), см. в разделе Получение сведений о возможностях [отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md) в руководстве по программированию.</span><span class="sxs-lookup"><span data-stu-id="81538-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81538-159">См. также</span><span class="sxs-lookup"><span data-stu-id="81538-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81538-160">**Общие сведения о приложении**</span><span class="sxs-lookup"><span data-stu-id="81538-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



