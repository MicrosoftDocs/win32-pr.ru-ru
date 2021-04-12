---
title: Управление элементами мультимедиа
description: Управление элементами мультимедиа
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Проигрыватель Windows Media, Библиотека
- Объектная модель проигрывателя Windows Media, Библиотека
- Объектная модель, Библиотека
- Проигрыватель Windows Media Mobile, Библиотека для объектной модели
- Элемент управления ActiveX проигрывателя Windows Media, Библиотека для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, Библиотека для объектной модели
- Элемент управления ActiveX, Библиотека для объектной модели
- Библиотека проигрывателя Windows Media, Управление элементами мультимедиа
- Библиотека, Управление элементами мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133042"
---
# <a name="managing-media-items"></a><span data-ttu-id="1d5ee-112">Управление элементами мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1d5ee-112">Managing Media Items</span></span>

<span data-ttu-id="1d5ee-113">Объект **мультимедиа** представляет один элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="1d5ee-114">Он содержит свойства и методы, которые можно использовать для получения сведений и их вывода пользователю, а также для выполнения различных действий в зависимости от полученного значения.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="1d5ee-115">Большая часть работы с объектами **мультимедиа** включает метаданные о содержимом элемента мультимедиа, называемые атрибутами.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="1d5ee-116">В разделе [атрибуты элемента мультимедиа](media-item-attributes.md) описывается чтение и изменение значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="1d5ee-117">Кроме этого раздела, ознакомьтесь с [рекомендациями по использованию метаданных Windows Media](/previous-versions/ms867702(v=msdn.10)) на веб-сайте Майкрософт, чтобы получить дополнительные сведения об атрибутах и их использовании.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="1d5ee-118">Объект **мультимедиа** имеет свойства и методы, которые извлекают некоторые атрибуты напрямую, например имя или длительность элемента.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="1d5ee-119">Для элементов видео можно получить высоту и ширину изображения, а также получить сведения о маркере на основе имени или индекса маркера.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="1d5ee-120">Можно также определить, включен ли определенный элемент мультимедиа в конкретный список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="1d5ee-121">Получение объекта мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1d5ee-121">Retrieving a Media Object</span></span>

<span data-ttu-id="1d5ee-122">С помощью *проигрывателя* можно быстро получить доступ к текущему элементу мультимедиа. Свойство **куррентмедиа** .</span><span class="sxs-lookup"><span data-stu-id="1d5ee-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="1d5ee-123">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1d5ee-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="1d5ee-124">В следующем примере кода C# извлекается объект **мультимедиа** , представляющий текущий элемент.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="1d5ee-125">С помощью *проигрывателя* можно создать новый элемент мультимедиа из цифрового файла мультимедиа. метод **невмедиа** .</span><span class="sxs-lookup"><span data-stu-id="1d5ee-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="1d5ee-126">Вы передаете методу URL-путь к файлу цифрового мультимедиа и возвращаете ссылку на новый объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1d5ee-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="1d5ee-127">Метод не добавляет новый объект непосредственно в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="1d5ee-128">Однако объект можно передать в *список воспроизведения*. метод **аппендитем** или *список воспроизведения*. метод **insertItem** .</span><span class="sxs-lookup"><span data-stu-id="1d5ee-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="1d5ee-129">В следующем примере кода C# создается объект **мультимедиа** на основе одного из примеров цифровых носителей, установленных вместе с пакетом SDK для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="1d5ee-130">\)Для представления одного действительного символа обратной косой черты в строке необходимо указать две обратные косые черты (или символ @ в C#).</span><span class="sxs-lookup"><span data-stu-id="1d5ee-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="1d5ee-131">Это происходит потому, что C# использует один символ обратной косой черты для определения escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="1d5ee-132">Вы можете создать новый элемент мультимедиа из цифрового файла мультимедиа и добавить его в библиотеку за один шаг с помощью *медиаколлектион*. **добавьте** метод.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="1d5ee-133">Как и *проигрыватель*. метод **невмедиа** , метод **Add** принимает путь к цифровому файлу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="1d5ee-134">В следующем примере кода C# создается объект **мультимедиа** на основе одного из примеров файлов пакета SDK и добавляется в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="1d5ee-135">Объект **мультимедиа** , представляющий элемент мультимедиа в списке воспроизведения, можно получить с помощью *списка воспроизведения*. **Item** , метод.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="1d5ee-136">В следующем примере на C# извлекается шестой элемент мультимедиа из текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1d5ee-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="1d5ee-137">См. также</span><span class="sxs-lookup"><span data-stu-id="1d5ee-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5ee-138">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-139">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-140">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-141">**Медиаколлектион. Add**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-142">**Player. Куррентмедиа**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-143">**Player. Невмедиа**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-144">**Список воспроизведения. элемент**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="1d5ee-145">**Работа с библиотекой**</span><span class="sxs-lookup"><span data-stu-id="1d5ee-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




