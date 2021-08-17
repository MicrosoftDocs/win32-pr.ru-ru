---
title: Ивмпмедиа isMemberOf, метод
description: Метод isMemberOf возвращает значение, указывающее, является ли указанный элемент мультимедиа членом указанного списка воспроизведения.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- проигрыватель Windows Media метода isMemberOf
- проигрыватель Windows Media метода isMemberOf, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, метод isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485121f0ac9c4c441ff90e34b90ef5c9475c22995565b018d3f0e00dc5d94740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746019"
---
# <a name="iwmpmediaismemberof-method"></a>Метод Ивмпмедиа:: isMemberOf

Метод **isMemberOf** возвращает значение, указывающее, является ли указанный элемент мультимедиа членом указанного списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*пплайлист* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпплайлист** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , указывающее, является ли элемент мультимедиа членом списка воспроизведения.

## <a name="remarks"></a>Remarks

Этот метод не может проверять списки воспроизведения, полученные через интерфейс **ивмпмедиаколлектион** . Чтобы проверить, является ли элемент мультимедиа членом определенного списка воспроизведения, извлеките коллекцию списков воспроизведения с помощью свойства **аксвиндовсмедиаплайер. плайлистколлектион** . После получения коллекции Извлеките отдельный список воспроизведения, вызвав метод **ивмпплайлистколлектион. жетбинаме** .

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере **isMemberOf** используется для проверки того, является ли текущий элемент мультимедиа членом списка воспроизведения с именем вся музыка. Если это не так, текущий элемент мультимедиа добавляется к списку воспроизведения. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Аксвиндовсмедиаплайер. Плайлистколлектион (VB и C#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





