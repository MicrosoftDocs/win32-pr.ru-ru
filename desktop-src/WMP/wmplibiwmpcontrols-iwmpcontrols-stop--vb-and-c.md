---
title: Метод завершения Ивмпконтролс
description: Метод Stop останавливает воспроизведение элемента мультимедиа. | Метод завершения Ивмпконтролс
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- проигрыватель Windows Media метода завершения
- проигрыватель Windows Media метода завершения, интерфейс ивмпконтролс
- интерфейс ивмпконтролс проигрыватель Windows Media, метод завершения
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f941ac90fa86cdd16dedf5349c0a6d614c57f49bc91009f5d62c56bb83144bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332079"
---
# <a name="iwmpcontrolsstop-method"></a>Метод Ивмпконтролс:: останавливаться

Метод **Stop** останавливает воспроизведение элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

этот метод заставляет проигрыватель Windows Media освобождать какие-либо системные ресурсы, которые он использует, например звуковое устройство. Однако текущий элемент мультимедиа не освобожден.

при остановке проигрыватель Windows Media текущая позиция воспроизведения в элементе мультимедиа сбрасывается до начала элемента. При последующем вызове **ивмпконтролс. Play** начнет воспроизведение с начала элемента мультимедиа. Чтобы остановить операцию воспроизведения без изменения текущей позицией, используйте метод **ивмпконтролс. Pause** .

## <a name="examples"></a>Примеры

В следующем примере используется функция " **Отключить** " для завершения текущего элемента мультимедиа в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Next (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Pause (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Play (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Previous (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





