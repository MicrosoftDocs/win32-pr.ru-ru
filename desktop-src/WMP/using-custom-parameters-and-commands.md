---
title: Использование пользовательских параметров и команд
description: Использование пользовательских параметров и команд
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Списки воспроизведения метафайлов Windows Media, пользовательские параметры
- списки воспроизведения, пользовательские параметры
- списки воспроизведения метафайлов, пользовательские параметры
- Списки воспроизведения метафайлов Windows Media, пользовательские команды
- списки воспроизведения, пользовательские команды
- списки воспроизведения метафайлов, пользовательские команды
- Списки воспроизведения метафайлов Windows Media, параметры
- списки воспроизведения, параметры
- списки воспроизведения метафайлов, параметры
- пользовательские параметры
- пользовательские команды
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888563"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="ecba2-114">Использование пользовательских параметров и команд</span><span class="sxs-lookup"><span data-stu-id="ecba2-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="ecba2-115">Можно создать пользовательские параметры для передачи дополнительных метаданных в список воспроизведения метафайлов с помощью элемента **param** .</span><span class="sxs-lookup"><span data-stu-id="ecba2-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="ecba2-116">Используйте атрибут **Name** элемента **param** , чтобы определить имя настраиваемого параметра.</span><span class="sxs-lookup"><span data-stu-id="ecba2-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="ecba2-117">Используйте атрибут **value** , чтобы определить значение для именованного настраиваемого параметра.</span><span class="sxs-lookup"><span data-stu-id="ecba2-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="ecba2-118">Получите метаданные **param** с помощью методов **getItemInfo** объектов **мультимедиа** и **списков воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="ecba2-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="ecba2-119">Пример использования этих методов для получения метаданных см. в описании метода [аттрибутекаунт](playlist-attributecount.md) объекта **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="ecba2-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="ecba2-120">В следующем примере списка воспроизведения метафайла показано использование элемента **param** для определения пользовательских параметров.</span><span class="sxs-lookup"><span data-stu-id="ecba2-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="ecba2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ecba2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecba2-122">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="ecba2-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




