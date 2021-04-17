---
title: Аксвиндовсмедиаплайер. полноэкранное свойство
description: Свойство «во весь экран» получает или задает значение, указывающее, воспроизводится ли видео в полноэкранном режиме.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Полноэкранное свойство проигрывателя Windows Media Player
- свойство "Полноэкранный" проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство полноэкранного режима
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694449"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>Аксвиндовсмедиаплайер. полноэкранное свойство

Свойство «во весь экран» получает или задает значение, указывающее, воспроизводится ли видео в полноэкранном режиме.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение System. Boolean, указывающее, воспроизводится ли содержимое в полноэкранном режиме. Значением по умолчанию является false.

## <a name="remarks"></a>Комментарии

Чтобы полноэкранный режим работал правильно при внедрении элемента управления проигрывателя Windows Media, область отображения видео должна иметь высоту и ширину по крайней мере на один пиксель. Если для **uiMode** задано значение "Mini" или "Full", то высота самого элемента управления должна быть 65 или больше для размещения видеообласти в дополнение к пользовательскому интерфейсу.

Если для **uiMode** задано значение "Невидимый", то установка этого свойства в значение true вызовет ошибку и не влияет на поведение элемента управления.

Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда [енаблеконтекстмену](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) равняется false, а **uiMode** равно «None».

Если для **uiMode** задано значение Full или Mini, проигрыватель Windows Media отображает элементы управления движением в полноэкранном режиме при перемещении курсора мыши. По истечении короткого интервала перемещения мыши элементы управления транспорта скрываются. Если для **uiMode** задано значение "нет", никакие элементы управления не отображаются в полноэкранном режиме.

> [!Note]  
> Для отображения элементов управления транспорта в полноэкранном режиме требуется операционная система Windows XP.

 

Если элементы управления передачей не отображаются в полноэкранном режиме, проигрыватель Windows Media автоматически выходит из полноэкранного режима при остановке воспроизведения.

## <a name="examples"></a>Примеры

В следующем примере создается кнопка, которая использует свойство "полноэкранное" для переключения внедренного объекта проигрывателя в полноэкранный режим. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                  |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                            |
| Сборка<br/>  | <dl> <dt>Аксинтероп. Вмплиб (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. uiMode (VB и C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





