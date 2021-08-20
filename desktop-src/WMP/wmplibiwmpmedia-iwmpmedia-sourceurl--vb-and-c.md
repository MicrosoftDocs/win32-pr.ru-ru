---
title: Ивмпмедиа Саурцеурл, свойство
description: Свойство Саурцеурл получает URL-адрес элемента мультимедиа.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- проигрыватель Windows Media свойства саурцеурл
- проигрыватель Windows Media свойства саурцеурл, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, свойство саурцеурл
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5427dadcbc2b9dccc4156ff1c9b25e641298a3c7cd069900fa932b6e0803c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122604"
---
# <a name="iwmpmediasourceurl-property"></a>Свойство Ивмпмедиа:: Саурцеурл

Свойство **саурцеурл** получает URL-адрес элемента мультимедиа.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является URL-адресом источника.

## <a name="examples"></a>Примеры

В следующем примере **саурцеурл** используется для получения URL-адреса первого элемента мультимедиа в списке воспроизведения «все музыкальные файлы». затем URL-адрес элемента мультимедиа присваивается свойству URL-адрес объекта Player. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





