---
title: Ивмпконтролс Фастреверсе, метод
description: Метод Фастреверсе запускает быстрое воспроизведение элемента мультимедиа в обратном направлении.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- проигрыватель Windows Media метода фастреверсе
- проигрыватель Windows Media метода фастреверсе, интерфейс ивмпконтролс
- проигрыватель Windows Media интерфейса ивмпконтролс, метод фастреверсе
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bbc1442ca223765b498560d078879c9a7033011117b7f663d4d40ff26bdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761084"
---
# <a name="iwmpcontrolsfastreverse-method"></a>Метод Ивмпконтролс:: Фастреверсе

Метод **фастреверсе** запускает быстрое воспроизведение элемента мультимедиа в обратном направлении.

## <a name="syntax"></a>Синтаксис


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод **фастреверсе** просматривает клип в обратную, в пять раз превышающую нормальную скорость, отображая только ключевые кадры, если это видеофайл. Вызов **фастреверсе** эквивалентен указанию-5,0 для ставки путем установки свойства **ивмпсеттингс. rate** . если частота впоследствии изменилась или если вызывается **ивмпконтролс. play** или **ивмпконтролс. останавливаться** , проигрыватель Windows Media прекращается на обратный.

Если элемент является частью списка воспроизведения, **фастреверсе** останавливается в начале текущей записи. например, если для параметра track 3 задано значение **фастреверсе**, то при достижении начала track 3 проигрыватель Windows Media не будет переходить к дорожке 2. При вызове **фастреверсе** Счетчик воспроизведения не увеличивается.

При вызове **ивмпконтролс. фастфорвард** во время выполнения **фастреверсе** **фастреверсе** будет остановлен и **ивмпконтролс. фастфорвард** начнется.

Этот метод не работает для широковещательных трансляций и определенных типов цифровых носителей. Чтобы определить, можно ли использовать параметр "Быстрый обратный" в картинке, передайте значение **System. String** "фастреверсе" в свойство **ивмпконтролс. Available** (метод **ивмпконтролс. Get, \_ доступный** в C#).

## <a name="examples"></a>Примеры

В следующем примере **фастреверсе** используется для отмены текущего элемента мультимедиа в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

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

[**Ивмпконтролс. Фастфорвард (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. доступ (VB и C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Play (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. останавливаться (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. rate (VB и C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





