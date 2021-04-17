---
title: Свойство списка воспроизведения Ивмпкдром
description: Свойство списка воспроизведения получает интерфейс Ивмпплайлист, представляющий дорожки на компакт-диске в данный момент в дисководе компакт-дисков или записи заголовка корневого уровня для DVD-диска.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Проигрыватель Windows Media, свойство списка воспроизведения
- Свойство списка воспроизведения проигрыватель Windows Media Player, интерфейс Ивмпкдром
- Интерфейс Ивмпкдром Windows Media Player, свойство списка воспроизведения
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717995"
---
# <a name="iwmpcdromplaylist-property"></a>Ивмпкдром: свойство лайлист:P

Свойство **списка воспроизведения** получает интерфейс **ивмпплайлист** , представляющий дорожки на компакт-диске в данный момент в дисководе компакт-дисков или записи заголовка КОРНЕВого уровня для DVD-диска.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Значение свойства

Интерфейс **вмплиб. ивмпплайлист** .

## <a name="remarks"></a>Комментарии

Как правило, содержимое на DVD-диске организовано в заголовки. Каждое название содержит одну или несколько глав. Каждый DVD-диск создан по-разному, поэтому использование заголовков и глав имеет автор содержимого.

Для DVD это свойство получает список воспроизведения, который содержит как первый элемент интерфейса **ивмпмедиа** с именем "DVD". Этот интерфейс представляет DVD-носитель. Воспроизведение элемента приводит к тому, что DVD-диск воспроизводится с начала, если он впервые воспроизводится после вставки нового DVD-диска, или возобновляется воспроизведение, если DVD-диск совпадает с последним просмотренным DVD-диском. При установке этого элемента в качестве текущего элемента во время воспроизведения DVD-диск воспроизводится с самого начала.

Дополнительные элементы (представленные интерфейсами **ивмпмедиа** ) в списке воспроизведения — это заголовки DVD, представленные вложенными списками воспроизведения. Если **ивмпконтролс. currentItem** устанавливается равным одному из этих вложенных элементов списка воспроизведения, проигрыватель Windows Media автоматически устанавливает вложенный список воспроизведения в качестве текущего списка воспроизведения после начала воспроизведения главы. Затем можно использовать свойства интерфейса **ивмпплайлист** , методы и связанные события для работы с главами DVD, которые также являются элементами списка воспроизведения.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере используется **список воспроизведения** для заполнения многострочного текстового поля с именем myText с списком дорожек аудио компакт-диска, находящегося в данный момент на первом компакт-диске. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдром (VB и C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. currentItem (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





