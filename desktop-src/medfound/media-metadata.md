---
description: Метаданные мультимедиа
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Метаданные мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713282"
---
# <a name="media-metadata"></a><span data-ttu-id="9fecd-103">Метаданные мультимедиа</span><span class="sxs-lookup"><span data-stu-id="9fecd-103">Media Metadata</span></span>

<span data-ttu-id="9fecd-104">Файлы мультимедиа содержат свойства, описывающие содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="9fecd-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="9fecd-105">В Microsoft Media Foundation эти свойства можно классифицировать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9fecd-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="9fecd-106">**Атрибуты типа мультимедиа** определяют параметры кодировки, такие как алгоритм кодирования (подтип носителя), размер видеокадра, частота кадров видео, скорость звуковых битов и частота дискретизации.</span><span class="sxs-lookup"><span data-stu-id="9fecd-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="9fecd-107">Дополнительные сведения об атрибутах типа носителя см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="9fecd-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="9fecd-108">**Метаданные** содержат описательные сведения для мультимедийного содержимого, такие как Title, исполнителя, composer и жанр.</span><span class="sxs-lookup"><span data-stu-id="9fecd-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="9fecd-109">Метаданные также могут описывать параметры кодирования.</span><span class="sxs-lookup"><span data-stu-id="9fecd-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="9fecd-110">Доступ к этим сведениям через метаданные можно ускорить, чем с помощью атрибутов типа носителя.</span><span class="sxs-lookup"><span data-stu-id="9fecd-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="9fecd-111">**Свойства DRM** содержат сведения об ограничениях использования.</span><span class="sxs-lookup"><span data-stu-id="9fecd-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="9fecd-112">В настоящее время Media Foundation не поддерживает свойства DRM с помощью метаданных, за исключением свойства " **\_ \_ незащищенное управление цифровыми правами** ".</span><span class="sxs-lookup"><span data-stu-id="9fecd-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="9fecd-113">Существует два способа чтения метаданных в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9fecd-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="9fecd-114">Интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation метаданных версии 1).</span><span class="sxs-lookup"><span data-stu-id="9fecd-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="9fecd-115">Интерфейс [**Ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) оболочки Windows (метаданные оболочки).</span><span class="sxs-lookup"><span data-stu-id="9fecd-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="9fecd-116">Метаданные оболочки относятся не только к файлам мультимедиа, но и к более широкому спектру файлов в системе.</span><span class="sxs-lookup"><span data-stu-id="9fecd-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="9fecd-117">В следующей таблице сравниваются функции и ограничения каждого API метаданных.</span><span class="sxs-lookup"><span data-stu-id="9fecd-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fecd-118">Метаданные Media Foundation v1</span><span class="sxs-lookup"><span data-stu-id="9fecd-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="9fecd-119">Метаданные оболочки</span><span class="sxs-lookup"><span data-stu-id="9fecd-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9fecd-120">Требуется Windows Vista или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="9fecd-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="9fecd-121">Требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9fecd-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9fecd-122">Метаданные оболочки в целом не нуждаются в Windows 7, но Media Foundation не поддерживали метаданные оболочки до Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9fecd-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9fecd-123">Свойства несовместимы с системой свойств оболочки.</span><span class="sxs-lookup"><span data-stu-id="9fecd-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="9fecd-124">Свойства совместимы с системой свойств оболочки.</span><span class="sxs-lookup"><span data-stu-id="9fecd-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9fecd-125">Свойства могут применяться ко всему файлу или на уровне потока.</span><span class="sxs-lookup"><span data-stu-id="9fecd-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="9fecd-126">Поддерживаются только свойства уровня файла.</span><span class="sxs-lookup"><span data-stu-id="9fecd-126">Only file-level properties are supported.</span></span> <span data-ttu-id="9fecd-127">Свойства уровня потока не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9fecd-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9fecd-128">Свойства могут иметь значения на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="9fecd-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="9fecd-129">Значения на нескольких языках не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9fecd-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9fecd-130">Ключи свойств — это строки расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="9fecd-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="9fecd-131">Ключи свойств — это <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> значения.</span><span class="sxs-lookup"><span data-stu-id="9fecd-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9fecd-132">Значения свойств — это <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>пропвариант</strong></a> значения.</span><span class="sxs-lookup"><span data-stu-id="9fecd-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="9fecd-133">Значения свойств — это <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>пропвариант</strong></a> значения.</span><span class="sxs-lookup"><span data-stu-id="9fecd-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="9fecd-134">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9fecd-134">In this section</span></span>



| <span data-ttu-id="9fecd-135">Раздел</span><span class="sxs-lookup"><span data-stu-id="9fecd-135">Topic</span></span>                                                                                     | <span data-ttu-id="9fecd-136">Описание</span><span class="sxs-lookup"><span data-stu-id="9fecd-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fecd-137">Поставщики метаданных оболочки</span><span class="sxs-lookup"><span data-stu-id="9fecd-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="9fecd-138">Начиная с Windows 7 Media Foundation предоставляет метаданные через интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="9fecd-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="9fecd-139">Свойства метаданных для файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="9fecd-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="9fecd-140">В этом разделе перечислены наиболее распространенные свойства метаданных для файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9fecd-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="9fecd-141">Поставщики метаданных в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fecd-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="9fecd-142">В Windows Vista Media Foundation предоставляет метаданные через интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="9fecd-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="9fecd-143">Если вы реализуете пользовательский источник мультимедиа и хотите предоставить метаданные оболочки, см. раздел [пользовательские поставщики метаданных для файлов мультимедиа](custom-metadata-providers-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="9fecd-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fecd-144">См. также</span><span class="sxs-lookup"><span data-stu-id="9fecd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fecd-145">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="9fecd-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
