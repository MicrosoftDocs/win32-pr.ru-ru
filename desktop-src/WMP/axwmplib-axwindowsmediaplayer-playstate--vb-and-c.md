---
title: Аксвиндовсмедиаплайер. Плайстате, свойство
description: Свойство Плайстате возвращает значение перечисления, указывающее состояние операции проигрывателя Windows Media.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Проигрыватель Windows Media для свойства Плайстате
- Плайстате свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Плайстате
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699076"
---
# <a name="axwindowsmediaplayerplaystate-property"></a>Аксвиндовсмедиаплайер. Плайстате, свойство

Свойство Плайстате возвращает значение перечисления, указывающее состояние операции проигрывателя Windows Media.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a>Значение свойства

Значение перечисления Вмплиб. Вмпплайстате.

## <a name="remarks"></a>Комментарии

Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке. Кроме того, не все состояния должны происходить во время последовательности событий. Не следует писать код, зависящий от порядка состояний.

## <a name="examples"></a>Примеры

В следующем примере свойство Плайстате используется для вывода текущего состояния воспроизведения проигрывателя в метке. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
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

[**Событие Аксвиндовсмедиаплайер. Плайстатечанже (VB и C#)**](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[**вмпплайстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





