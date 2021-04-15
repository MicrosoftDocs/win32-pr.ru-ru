---
title: Метод Play Ивмпконтролс
description: Метод Play начинает воспроизведение текущего элемента мультимедиа или возобновляет воспроизведение приостановленного элемента.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- воспроизвести метод проигрыватель Windows Media
- метод Play проигрыватель Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689297"
---
# <a name="iwmpcontrolsplay-method"></a>Ивмпконтролс: метод макетирования:p

Метод **Play** начинает воспроизведение текущего элемента мультимедиа или возобновляет воспроизведение приостановленного элемента.

## <a name="syntax"></a>Синтаксис


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если этот метод вызывается во время быстрой пересылки или перемотки, скорость воспроизведения (значение **ивмпсеттингс. rate**) устанавливается равным 1,0.

## <a name="examples"></a>Примеры

В следующем примере функция **Play** используется для воспроизведения текущего элемента мультимедиа в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

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

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Плайитем (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. rate (VB и C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





