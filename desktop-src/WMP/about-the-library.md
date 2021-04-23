---
title: Сведения о библиотеке
description: Сведения о библиотеке
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Проигрыватель Windows Media, Библиотека
- Объектная модель проигрывателя Windows Media, Библиотека
- Объектная модель, Библиотека
- Элемент управления ActiveX проигрывателя Windows Media, Библиотека для объектной модели
- Элемент управления ActiveX, Библиотека для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, Библиотека для объектной модели
- Проигрыватель Windows Media Mobile, Библиотека для объектной модели
- Библиотека проигрывателя Windows Media, сведения
- Библиотека, сведения
- метаданные, Библиотека проигрывателя Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691138"
---
# <a name="about-the-library"></a><span data-ttu-id="1d5b0-113">Сведения о библиотеке</span><span class="sxs-lookup"><span data-stu-id="1d5b0-113">About the Library</span></span>

<span data-ttu-id="1d5b0-114">Библиотека представляет собой базу данных сведений или *метаданных* о мультимедийном содержимом, доступном для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="1d5b0-115">Некоторые сведения отображаются в области **Библиотека** в проигрывателе; его больше можно получить с помощью кода.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="1d5b0-116">(В серии проигрывателя Windows Media 9 и более ранних версий эта функция называется **библиотекой мультимедиа**.)</span><span class="sxs-lookup"><span data-stu-id="1d5b0-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="1d5b0-117">Библиотека предоставляет пользователям простой способ организации и доступа к цифровому содержимому мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="1d5b0-118">Например, пользователи могут просматривать музыку по альбому, исполнителям, жанрам или просто списку всех музыкальных файлов.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="1d5b0-119">Можно использовать объектную модель пакета SDK проигрывателя Windows Media для доступа к библиотеке для воспроизведения содержимого, извлечения списков воспроизведения, добавления содержимого, удаления содержимого и изменения связанных метаданных.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="1d5b0-120">Проигрыватель Windows Media защищает конфиденциальность пользователей, запрещая доступ к библиотеке из кода при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="1d5b0-121">Дополнительные сведения о правах доступа см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1d5b0-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1d5b0-122">Библиотека хранит метаданные о двух основных типах цифрового мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="1d5b0-123">Первый тип, цифровые мультимедийные элементы, являются отдельными файлами содержимого, например музыкальной дорожкой или фотографией.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="1d5b0-124">Второй тип, списки воспроизведения — это файлы, представляющие группу цифровых мультимедийных элементов, которые обычно предназначены для воспроизведения в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="1d5b0-125">Метаданные, связанные с цифровым содержимым мультимедиа, хранятся в виде пар «имя-значение».</span><span class="sxs-lookup"><span data-stu-id="1d5b0-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="1d5b0-126">Например, метаданные, описывающие пользователя, выполнившего песню, называются "исполнителем", а связанное с ним значение обычно представляет собой текстовую строку, содержащую имя исполнителя.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="1d5b0-127">Каждое уникальное имя метаданных называется *атрибутом*.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="1d5b0-128">Список поддерживаемых атрибутов см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1d5b0-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="1d5b0-129">Сведения об использовании атрибутов в коде см. в разделе [атрибуты элементов мультимедиа](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1d5b0-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="1d5b0-130">В следующих разделах приведены дополнительные сведения о работе с библиотекой.</span><span class="sxs-lookup"><span data-stu-id="1d5b0-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="1d5b0-131">Программный доступ к библиотеке</span><span class="sxs-lookup"><span data-stu-id="1d5b0-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="1d5b0-132">Сведения о службах библиотек</span><span class="sxs-lookup"><span data-stu-id="1d5b0-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="1d5b0-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1d5b0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5b0-134">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="1d5b0-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




