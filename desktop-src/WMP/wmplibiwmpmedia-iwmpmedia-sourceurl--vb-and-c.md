---
title: Ивмпмедиа Саурцеурл, свойство
description: Свойство Саурцеурл получает URL-адрес элемента мультимедиа.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Проигрыватель Windows Media для свойства Саурцеурл
- Саурцеурл свойство проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Саурцеурл
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
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668585"
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
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





