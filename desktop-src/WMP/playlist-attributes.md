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
# <a name="playlist-attributes"></a>Атрибуты списка воспроизведения

Списки воспроизведения содержат метаданные, которые называются атрибутами, так же как элементы мультимедиа имеют атрибуты. Можно извлекать имена и значения атрибутов списка воспроизведения, а также отображать их в пользовательском интерфейсе, или код может выполнять действия на основе значения атрибута.

Списки воспроизведения определяются в файлах, организованных в формате XML, а определенные элементы в файле определяют атрибуты списка воспроизведения. Некоторые элементы атрибутов хорошо известны; Автор метафайла также может определять произвольные атрибуты. Дополнительные сведения об элементах атрибутов в файлах списков воспроизведения см. в разделе [Получение метаданных](retrieving-metadata.md).

Библиотека может предоставлять дополнительные атрибуты списка воспроизведения, например **саурцеурл** или **усерластплайедтиме**. Дополнительные сведения об атрибутах списка воспроизведения библиотеки см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

*Список воспроизведения*. Свойство **аттрибутекаунт** извлекает количество атрибутов, связанных с списком воспроизведения. *Список воспроизведения*. Свойство **attributeName** извлекает имя атрибута на основе его индекса и *списка воспроизведения*. метод **getItemInfo** извлекает значение атрибута на основе его имени.

Значение атрибута текущего списка воспроизведения можно изменить с помощью *списка воспроизведения*. метод **сетитеминфо** .

Особое использование метода **сетитеминфо** заключается в сортировке элементов списка воспроизведения с помощью атрибута **SortAttribute** . В следующем примере C# список воспроизведения сортируется по значениям атрибута **усерластплайедтиме** . *Список воспроизведения* переменных является ссылкой на объект **списка воспроизведения** .


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



В этом разделе объект **Player** был определен следующим образом:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



В следующем примере кода C# демонстрируется получение атрибутов списка воспроизведения. Первая функция, Шовплайлистс, заполняет элемент управления ListBox именами доступных списков воспроизведения. Вторая часть — обработчик событий окна списка. Когда пользователь щелкает имя списка воспроизведения, этот код извлекает атрибуты для этого списка воспроизведения и отображает эти атрибуты во втором поле списка.


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



Событие в элементе управления ListBox вызывается каждый раз, когда пользователь выбирает имя списка воспроизведения. Следующий обработчик событий заполняет второе окно списка именами атрибутов и значениями, соответствующими выбору пользователя.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Управление списками воспроизведения**](managing-playlists.md)
</dt> <dt>

[**Атрибуты элемента мультимедиа**](media-item-attributes.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> </dl>

 

 




