---
title: Предыдущий метод Ивмпконтролс
description: Предыдущий метод устанавливает предыдущий элемент списка воспроизведения в качестве текущего элемента.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- Предыдущий метод проигрывателя Windows Media
- Предыдущий метод проигрыватель Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, предыдущий метод
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689295"
---
# <a name="iwmpcontrolsprevious-method"></a>Ивмпконтролс: метод:p Предыдущая

**Предыдущий** метод устанавливает предыдущий элемент списка воспроизведения в качестве текущего элемента.

## <a name="syntax"></a>Синтаксис


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если список воспроизведения находится в первой записи при вызове **предыдущего** , последняя запись списка воспроизведения станет текущей.

## <a name="examples"></a>Примеры

В следующем примере функция **Previous** используется для перехода к предыдущему элементу в текущем списке воспроизведения в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

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

[**Ивмпконтролс. Next (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. останавливаться (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





