---
title: Атрибуты списка воспроизведения
description: Атрибуты списка воспроизведения
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Проигрыватель Windows Media, списки воспроизведения
- Объектная модель проигрывателя Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- Проигрыватель Windows Media Mobile, списки воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, списки воспроизведения
- Элементы управления ActiveX, списки воспроизведения
- списки воспроизведения, атрибуты
- списки воспроизведения метафайлов, атрибуты
- Списки воспроизведения метафайлов Windows Media, атрибуты
- атрибуты, списки воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986346"
---
# <a name="playlist-attributes"></a><span data-ttu-id="d38fb-114">Атрибуты списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="d38fb-114">Playlist Attributes</span></span>

<span data-ttu-id="d38fb-115">Списки воспроизведения содержат метаданные, которые называются атрибутами, так же как элементы мультимедиа имеют атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d38fb-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="d38fb-116">Можно извлекать имена и значения атрибутов списка воспроизведения, а также отображать их в пользовательском интерфейсе, или код может выполнять действия на основе значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="d38fb-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="d38fb-117">Списки воспроизведения определяются в файлах, организованных в формате XML, а определенные элементы в файле определяют атрибуты списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d38fb-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="d38fb-118">Некоторые элементы атрибутов хорошо известны; Автор метафайла также может определять произвольные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d38fb-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="d38fb-119">Дополнительные сведения об элементах атрибутов в файлах списков воспроизведения см. в разделе [Получение метаданных](retrieving-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="d38fb-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="d38fb-120">Библиотека может предоставлять дополнительные атрибуты списка воспроизведения, например **саурцеурл** или **усерластплайедтиме**.</span><span class="sxs-lookup"><span data-stu-id="d38fb-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="d38fb-121">Дополнительные сведения об атрибутах списка воспроизведения библиотеки см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d38fb-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="d38fb-122">*Список воспроизведения*. Свойство **аттрибутекаунт** извлекает количество атрибутов, связанных с списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d38fb-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="d38fb-123">*Список воспроизведения*. Свойство **attributeName** извлекает имя атрибута на основе его индекса и *списка воспроизведения*. метод **getItemInfo** извлекает значение атрибута на основе его имени.</span><span class="sxs-lookup"><span data-stu-id="d38fb-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="d38fb-124">Значение атрибута текущего списка воспроизведения можно изменить с помощью *списка воспроизведения*. метод **сетитеминфо** .</span><span class="sxs-lookup"><span data-stu-id="d38fb-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="d38fb-125">Особое использование метода **сетитеминфо** заключается в сортировке элементов списка воспроизведения с помощью атрибута **SortAttribute** .</span><span class="sxs-lookup"><span data-stu-id="d38fb-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="d38fb-126">В следующем примере C# список воспроизведения сортируется по значениям атрибута **усерластплайедтиме** .</span><span class="sxs-lookup"><span data-stu-id="d38fb-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="d38fb-127">*Список воспроизведения* переменных является ссылкой на объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="d38fb-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="d38fb-128">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d38fb-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="d38fb-129">В следующем примере кода C# демонстрируется получение атрибутов списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d38fb-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="d38fb-130">Первая функция, Шовплайлистс, заполняет элемент управления ListBox именами доступных списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d38fb-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="d38fb-131">Вторая часть — обработчик событий окна списка.</span><span class="sxs-lookup"><span data-stu-id="d38fb-131">The second part is the list box event handler.</span></span> <span data-ttu-id="d38fb-132">Когда пользователь щелкает имя списка воспроизведения, этот код извлекает атрибуты для этого списка воспроизведения и отображает эти атрибуты во втором поле списка.</span><span class="sxs-lookup"><span data-stu-id="d38fb-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



<span data-ttu-id="d38fb-133">Событие в элементе управления ListBox вызывается каждый раз, когда пользователь выбирает имя списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d38fb-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="d38fb-134">Следующий обработчик событий заполняет второе окно списка именами атрибутов и значениями, соответствующими выбору пользователя.</span><span class="sxs-lookup"><span data-stu-id="d38fb-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="d38fb-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d38fb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d38fb-136">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="d38fb-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="d38fb-137">**Атрибуты элемента мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="d38fb-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="d38fb-138">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="d38fb-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




