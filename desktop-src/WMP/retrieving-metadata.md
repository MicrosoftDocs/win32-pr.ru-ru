---
title: Извлечение метаданных
description: Извлечение метаданных
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Списки воспроизведения метафайлов Windows Media, получение метаданных
- списки воспроизведения, получение метаданных
- списки воспроизведения метафайлов, получение метаданных
- Списки воспроизведения метафайлов Windows Media, получение метаданных
- списки воспроизведения, получение метаданных
- списки воспроизведения метафайлов, получение метаданных
- метаданные, извлечение
- получение метаданных
- Проигрыватель Windows Media, получение метаданных
- Проигрыватель Windows Media, получение метаданных
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986616"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="ed37d-113">Извлечение метаданных</span><span class="sxs-lookup"><span data-stu-id="ed37d-113">Retrieving Metadata</span></span>

<span data-ttu-id="ed37d-114">Во время воспроизведения или клипа сценарий может извлекать метаданные, такие как Title и Author, с помощью методов **getItemInfo** объектов **мультимедиа** и **списков воспроизведения** проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ed37d-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="ed37d-115">Метаданные из области ASX можно получить с помощью методов объектов **списков воспроизведения** и из области записи с помощью методов объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="ed37d-116">Например, чтобы получить значения автор, ABSTRACT и PARAM в следующем файле, используйте метод **getItemInfo** объекта **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="ed37d-117">Для этого метода требуется имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="ed37d-117">The attribute name is required for this method.</span></span> <span data-ttu-id="ed37d-118">Имена атрибутов можно получить, предоставив номер индекса свойству **attributeName** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="ed37d-119">Доступные индексы для объекта **списка воспроизведения** можно получить с помощью свойства **аттрибутекаунт** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="ed37d-120">Пример кода</span><span class="sxs-lookup"><span data-stu-id="ed37d-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="ed37d-121">Чтобы получить значения текущего объекта **мультимедиа** в области записи для ref, Title, Copyright и param ("три"), используйте свойство **куррентмедиа** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="ed37d-122">Используйте свойство **аттрибутекаунт** объекта **мультимедиа** , чтобы определить количество атрибутов, доступных для указанного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="ed37d-123">Используйте индексные номера с помощью метода **жетитеминфобятом** для получения значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ed37d-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="ed37d-124">Используйте индексные номера с помощью метода **жетаттрибутенаме** объекта **мультимедиа** , чтобы определить имена доступных атрибутов, а затем используйте результаты с помощью метода **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="ed37d-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="ed37d-125">Пример использования методов объектов проигрывателя Windows Media для получения метаданных см. в разделе [список воспроизведения. аттрибутекаунт](playlist-attributecount.md).</span><span class="sxs-lookup"><span data-stu-id="ed37d-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed37d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ed37d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed37d-127">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="ed37d-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ed37d-128">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="ed37d-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ed37d-129">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ed37d-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




