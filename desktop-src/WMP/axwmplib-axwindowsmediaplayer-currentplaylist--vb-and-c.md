---
title: Аксвиндовсмедиаплайер. Куррентплайлист, свойство
description: Свойство Куррентплайлист Возвращает или задает текущий интерфейс Ивмпплайлист, предоставляющий простой способ организации и управления мультимедийными элементами в списке.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- проигрыватель Windows Media свойства куррентплайлист
- проигрыватель Windows Media свойства куррентплайлист, класс аксвиндовсмедиаплайер
- проигрыватель Windows Media класса аксвиндовсмедиаплайер, свойство куррентплайлист
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
ms.openlocfilehash: f976084773a333e40c0a278878e9a35ed913e5911ec732c0dccfe6525e5f45a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765265"
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

## <a name="remarks"></a>Remarks

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





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 





