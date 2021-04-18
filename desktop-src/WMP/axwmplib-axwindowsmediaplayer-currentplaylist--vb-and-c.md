---
title: Аксвиндовсмедиаплайер. Куррентплайлист, свойство
description: Свойство Куррентплайлист Возвращает или задает текущий интерфейс Ивмпплайлист, предоставляющий простой способ организации и управления мультимедийными элементами в списке.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Проигрыватель Windows Media для свойства Куррентплайлист
- Куррентплайлист свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Куррентплайлист
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698800"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>Аксвиндовсмедиаплайер. Куррентплайлист, свойство

Свойство Куррентплайлист Возвращает или задает текущий интерфейс **ивмпплайлист** , предоставляющий простой способ организации и управления мультимедийными элементами в списке.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Значение свойства

Интерфейс Вмплиб. Ивмпплайлист, предоставляющий доступ к текущему списку воспроизведения.

## <a name="remarks"></a>Комментарии

Значение, если свойство Ивмпсеттингс. Автозапуск (также доступно через Аксвиндовсмедиаплайер. Settings **). Автозапуск**) имеет значение true, воспроизведение начинается автоматически при установке **куррентплайлист**.

Это свойство принимает интерфейс Ивмпплайлист, который может быть получен несколькими способами, например путем получения значения из *ивмпплайлистаррай*. **Item** или *ивмпплайлистколлектион*. свойства **невплайлист** . Чтобы загрузить элемент **списка воспроизведения** с помощью имени файла, задайте свойство URL-адреса или используйте аксвиндовсмедиаплайер. **невплайлист**.

## <a name="examples"></a>Примеры

В следующем примере извлекается первый список воспроизведения в библиотеке и используется свойство Куррентплайлист для задания полученного списка воспроизведения в качестве текущего списка воспроизведения и вывода его имени. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Невплайлист (VB и C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Settings (VB и C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистаррай. Item (VB и C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Невплайлист (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Автозапуск (VB и C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





