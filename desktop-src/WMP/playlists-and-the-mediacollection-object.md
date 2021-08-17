---
title: Списки воспроизведения и объект Медиаколлектион
description: Списки воспроизведения и объект Медиаколлектион
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- проигрыватель Windows Media, списки воспроизведения
- объектная модель проигрыватель Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- проигрыватель Windows Media Мобильные устройства, списки воспроизведения
- проигрыватель Windows Media ActiveX элемент управления, списки воспроизведения
- проигрыватель Windows Media управление мобильными ActiveXми, списки воспроизведения
- элемент управления ActiveX, списки воспроизведения
- списки воспроизведения, объект Медиаколлектион
- списки воспроизведения метафайлов, объект Медиаколлектион
- Windows Списки воспроизведения метафайлов мультимедиа, объект Медиаколлектион
- Объект Медиаколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a0bba2e966e51523dc24965c2f2a066767b059f26a08fde9ee5856a1694df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334457"
---
# <a name="playlists-and-the-mediacollection-object"></a>Списки воспроизведения и объект Медиаколлектион

Объект **медиаколлектион** предоставляет доступ к разнообразным спискам воспроизведения и включает метод для создания нового списка воспроизведения из метафайла.

Следующие методы получают специальные списки воспроизведения:

-   **жеталл**
-   **жетбялбум**
-   **жетбяттрибуте**
-   **жетбяусор**
-   **жетбиженре**
-   **жетбинаме**

Как следует из своих имен, эти методы извлекают списки воспроизведения, содержащие все элементы мультимедиа в библиотеке, соответствующие определенным критериям.

Будьте внимательны, чтобы не путать *медиаколлектион*. метод **жетбинаме** с параметром *плайлистколлектион*. метод **жетбинаме** . Метод **медиаколлектион** возвращает объект **списка воспроизведения** , содержащий все элементы мультимедиа с указанным именем. Метод **плайлистколлектион** возвращает объект **плайлистаррай** , содержащий все списки воспроизведения с указанным именем.

Можно использовать *медиаколлектион*. **добавьте** метод для добавления списков воспроизведения, а также элементов мультимедиа в библиотеку. Чтобы добавить список воспроизведения, необходимо передать методу путь к метафайлу, который определяет список воспроизведения. Метод всегда возвращает объект **мультимедиа** . Невозможно выполнить приведение между объектами **мультимедиа** и **списками воспроизведения** . Для работы с добавленным списком воспроизведения извлеките объект **списка воспроизведения** , имя которого совпадает с именем объекта **мультимедиа** .

В следующем примере C# показано, как получить мультимедиа по типу с помощью **медиаколлектион**. метод **жетбяттрибуте** . Этот код извлекает имена всех атрибутов, связанных с данным типом, а также состояние этих атрибутов для чтения и записи или только для чтения. Он создает один файл, содержащий списки атрибутов для аудио, видео, Радио, списков воспроизведения, других, музыкальных и фотографий.


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



В следующем примере кода C# показано, как добавить список воспроизведения из метафайла в библиотеку.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



К статическим спискам воспроизведения относятся определенные элементы мультимедиа. Автоматические списки воспроизведения выполняют поиск в библиотеке при каждом открытии и могут содержать разные элементы мультимедиа в разные моменты времени. В библиотеку можно добавить как статические, так и автоматические списки воспроизведения с помощью *медиаколлектион*. **добавьте** метод. Также можно добавить статические списки воспроизведения с помощью *плайлистколлектион*. метод **импортплайлист** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Управление списками воспроизведения**](managing-playlists.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> <dt>

[**Списки воспроизведения и объект Плайлистколлектион**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Статические и автоматические списки воспроизведения**](static-and-auto-playlists.md)
</dt> </dl>

 

 




