---
title: REF, элемент
description: Элемент REF указывает URL-адрес для мультимедийного содержимого.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Проигрыватель Windows Media, элемент REF
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704376"
---
# <a name="ref-element"></a><span data-ttu-id="7a115-104">REF, элемент</span><span class="sxs-lookup"><span data-stu-id="7a115-104">REF Element</span></span>

<span data-ttu-id="7a115-105">Элемент **ref** указывает URL-адрес для мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="7a115-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="7a115-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7a115-106">Attributes</span></span>

<span data-ttu-id="7a115-107">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7a115-107">**HREF** (required)</span></span>

<span data-ttu-id="7a115-108">URL-адрес любого фрагмента мультимедийного содержимого, поддерживаемого проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7a115-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7a115-109">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7a115-109">Parent/Child Elements</span></span>



| <span data-ttu-id="7a115-110">Иерархия</span><span class="sxs-lookup"><span data-stu-id="7a115-110">Hierarchy</span></span>       | <span data-ttu-id="7a115-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="7a115-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a115-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7a115-112">Parent elements</span></span> | <span data-ttu-id="7a115-113">**ОПЕРАЦИИ**</span><span class="sxs-lookup"><span data-stu-id="7a115-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="7a115-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7a115-114">Child elements</span></span>  | <span data-ttu-id="7a115-115">**DURATION**, **ендмаркер**, **превиевдуратион**, **стартмаркер**, **StartTime**</span><span class="sxs-lookup"><span data-stu-id="7a115-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7a115-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a115-116">Remarks</span></span>

<span data-ttu-id="7a115-117">Этот элемент задает URL-адрес для фрагмента мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="7a115-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="7a115-118">URL-адрес может указывать на любой поддерживаемый тип носителя, используя любой протокол, поддерживаемый проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7a115-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="7a115-119">Поддерживаемые типы мультимедиа включают изображения в формате GIF и JPG, а также файлы Flash с расширением. SWF.</span><span class="sxs-lookup"><span data-stu-id="7a115-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="7a115-120">Эти типы носителей полезны для включения рекламного содержимого в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7a115-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="7a115-121">При использовании файлов изображений и Flash-файлов, которые воспроизводятся в цикле, необходимо также указать количество времени для вывода элемента мультимедиа, включив элемент **DURATION** в элемент **ref** .</span><span class="sxs-lookup"><span data-stu-id="7a115-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="7a115-122">Если вы хотите, чтобы изображение продолжалось отображать во время буферизации следующей записи в списке воспроизведения, включите элемент **param** в элемент **entry** , задайте для его атрибута **Name** значение шоввхилебуфферинг и установите для атрибута **value значения** true.</span><span class="sxs-lookup"><span data-stu-id="7a115-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="7a115-123">Для ссылки на содержимое компакт-диска или DVD-диска, который допускает его, предоставляются протоколы вмпкд и вмпдвд.</span><span class="sxs-lookup"><span data-stu-id="7a115-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="7a115-124">Например, если задать для атрибута **href** значение «wmpdvd://f/5/3», будет воспроизводится глава 3 из заголовка 5 на DVD, но только в том случае, если DVD-диск был создан для разрешения.</span><span class="sxs-lookup"><span data-stu-id="7a115-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="7a115-125">Приложения, которые открывают цифровые мультимедиа из защищенного брандмауэра, будут иметь лучшую производительность при открытии элементов мультимедиа, если адрес указан с использованием имени сервера доменных имен (DNS) вместо IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7a115-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="7a115-126">Наиболее часто этот элемент используется для смены URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7a115-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="7a115-127">Если проигрывателю Windows Media не удается открыть часть носителя, определенную в элементе **ref** , он пытается получить URL-адрес в следующем элементе **ref** .</span><span class="sxs-lookup"><span data-stu-id="7a115-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="7a115-128">Когда проигрыватель Windows Media открывает мультимедийное содержимое из URL-адреса, определенного в области одного элемента **entry** , он игнорирует последующие теги **ref** внутри этого элемента **entry** .</span><span class="sxs-lookup"><span data-stu-id="7a115-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="7a115-129">После завершения воспроизведения части содержимого проигрыватель Windows Media переходит к следующему элементу **entry** , если он есть.</span><span class="sxs-lookup"><span data-stu-id="7a115-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="7a115-130">**Важно!** Когда проигрыватель Windows Media устанавливает соединение с фрагментом содержимого, на который ссылается ссылка, он игнорирует все остальные элементы **ref** в этой **записи**, независимо от того, завершается ли соединение нормально или аварийно.</span><span class="sxs-lookup"><span data-stu-id="7a115-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="7a115-131">Если элемент мультимедиа, на который указывает ссылка, является файлом изображения, то для указания времени показа изображения должен использоваться элемент **DURATION** .</span><span class="sxs-lookup"><span data-stu-id="7a115-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="7a115-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7a115-132">**Note**</span></span>

<span data-ttu-id="7a115-133">Попытка воспроизведения Flash-носителя, который содержит звук с первым кадром, может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="7a115-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="7a115-134">Содержимое Flash следует создавать, чтобы воспроизводить звук, начинающийся не раньше, чем второй кадр.</span><span class="sxs-lookup"><span data-stu-id="7a115-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="7a115-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="7a115-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="7a115-136">Требования</span><span class="sxs-lookup"><span data-stu-id="7a115-136">Requirements</span></span>



| <span data-ttu-id="7a115-137">Требование</span><span class="sxs-lookup"><span data-stu-id="7a115-137">Requirement</span></span> | <span data-ttu-id="7a115-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7a115-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7a115-139">Версия</span><span class="sxs-lookup"><span data-stu-id="7a115-139">Version</span></span><br/> | <span data-ttu-id="7a115-140">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="7a115-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a115-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a115-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a115-142">**Поддерживаемые протоколы и типы файлов**</span><span class="sxs-lookup"><span data-stu-id="7a115-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="7a115-143">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7a115-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7a115-144">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7a115-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





