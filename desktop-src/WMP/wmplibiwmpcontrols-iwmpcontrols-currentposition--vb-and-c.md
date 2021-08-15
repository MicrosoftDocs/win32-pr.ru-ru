---
title: Ивмпконтролс currentPosition, свойство
description: Свойство currentPosition Возвращает или задает текущую позицию в элементе мультимедиа в секундах с начала.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- проигрыватель Windows Media свойства currentPosition
- проигрыватель Windows Media свойства currentPosition, интерфейс ивмпконтролс
- проигрыватель Windows Media интерфейса ивмпконтролс, свойство currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8eca861240256899fa19513fc1fb64cd540d47acb213f718674ebbda2d5f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053672"
---
# <a name="iwmpcontrolscurrentposition-property"></a>Свойство Ивмпконтролс:: currentPosition

Свойство **CurrentPosition** Возвращает или задает текущую позицию в элементе мультимедиа в секундах с начала.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Значение свойства

Значение **System. Double** , которое является текущей позицией.

## <a name="examples"></a>Примеры

В следующем примере **CurrentPosition** используется для поиска расположения, предоставленного пользователем. В ответ на нажатие кнопки **CurrentPosition** задается значение, указанное в текстовом поле с именем невпоситион. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

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

[**Ивмпконтролс. Куррентпоситионстринг (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





