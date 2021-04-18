---
title: Ивмпплайлист. Item (VB и C)
description: Свойство Item ( \_ метод Get Item в C \) получает интерфейс для элемента мультимедиа по указанному индексу.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- Проигрыватель Windows Media Ивмпплайлист. Item (VB и C)
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685074"
---
# <a name="iwmpplaylistitem-vb-and-c"></a>Ивмпплайлист. Item (VB и C#)

Свойство **Item** (метод **Get \_ Item** в C#) получает интерфейс для элемента мультимедиа по указанному индексу.


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a>Параметры

*линдекс*

Объект **System. Int32** , который является индексом элемента мультимедиа в списке воспроизведения.

## <a name="property-value"></a>Значение свойства

Интерфейс **вмплиб. ивмпмедиа** , предоставляющий доступ к элементу мультимедиа по указанному индексу.

## <a name="remarks"></a>Комментарии

**Ивмпплайлист. Item** — это свойство, доступное только для чтения, в Visual Basic, которое принимает параметр, а в C# называется методом **ивмпплайлист. Get \_ Item** .

## <a name="examples"></a>Примеры

В следующем примере свойство **Item** (метод **Get \_ Item** в C#) используется для извлечения элемента мультимедиа из списка воспроизведения на основе выбора пользователя. Список был создан с именем "список" и заполняется заголовками из списка воспроизведения с именем Аудиоплайлист. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. insertItem (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. removeItem (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





