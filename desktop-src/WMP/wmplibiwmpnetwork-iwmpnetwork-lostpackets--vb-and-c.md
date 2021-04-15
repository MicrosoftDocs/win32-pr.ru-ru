---
title: Ивмпнетворк Лостпаккетс, свойство
description: Свойство Лостпаккетс возвращает число потерянных пакетов.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Проигрыватель Windows Media для свойства Лостпаккетс
- Лостпаккетс свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Лостпаккетс
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668849"
---
# <a name="iwmpnetworklostpackets-property"></a>Свойство Ивмпнетворк:: Лостпаккетс

Свойство **лостпаккетс** возвращает число потерянных пакетов.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , равное количеству потерянных пакетов.

## <a name="remarks"></a>Комментарии

Это свойство включает только пакеты потокового мультимедиа и возвращает нуль при использовании протокола HTTP, который не учитывается.

Пакеты могут быть потеряны по ряду причин, таким как тип и качество сетевого подключения.

Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля. Значение не сбрасывается, если воспроизведение приостановлено. Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .

## <a name="examples"></a>Примеры

В следующем примере кода используется **лостпаккетс** для вывода общего числа потерянных пакетов во время воспроизведения. Сведения отображаются в метке, когда пользователь нажимает кнопку. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





