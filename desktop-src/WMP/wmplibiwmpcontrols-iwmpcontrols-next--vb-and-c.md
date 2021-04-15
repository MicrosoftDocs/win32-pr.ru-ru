---
title: Ивмпконтролс следующий метод
description: Следующий метод задает следующий элемент списка воспроизведения в качестве текущего элемента.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- Следующий метод проигрывателя Windows Media
- Следующий метод проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689299"
---
# <a name="iwmpcontrolsnext-method"></a>Метод Ивмпконтролс:: Next

**Следующий** метод задает следующий элемент списка воспроизведения в качестве текущего элемента.

## <a name="syntax"></a>Синтаксис


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если список воспроизведения находится в последней записи при вызове **Next** , первая запись списка воспроизведения станет текущей.

Для списков воспроизведения на стороне сервера этот метод пропускает следующий элемент в списке воспроизведения на стороне сервера, а не в списке воспроизведения клиента.

При воспроизведении DVD этот метод пропускает следующую логическую главу в последовательности воспроизведения, которая может не быть следующей главой в списке воспроизведения. При воспроизведении изображений DVD-образов этот метод переходит к следующему изображению.

## <a name="examples"></a>Примеры

В следующем примере функция **Next** используется для перехода к следующему элементу в текущем списке воспроизведения в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**Ивмпконтролс. Previous (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. останавливаться (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





