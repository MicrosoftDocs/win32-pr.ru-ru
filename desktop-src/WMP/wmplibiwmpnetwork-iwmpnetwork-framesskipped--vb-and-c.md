---
title: Ивмпнетворк Фрамесскиппед, свойство
description: Свойство Фрамесскиппед возвращает общее число кадров, пропущенных во время воспроизведения.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- проигрыватель Windows Media свойства фрамесскиппед
- проигрыватель Windows Media свойства фрамесскиппед, интерфейс ивмпнетворк
- проигрыватель Windows Media интерфейса ивмпнетворк, свойство фрамесскиппед
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3640ff73eeadd1bf59eecc29045b0434f0885b7dc1eef319d6e6ee040442abdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999984"
---
# <a name="iwmpnetworkframesskipped-property"></a>Свойство Ивмпнетворк:: Фрамесскиппед

Свойство **фрамесскиппед** возвращает общее число кадров, пропущенных во время воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , равное количеству пропущенных кадров.

## <a name="examples"></a>Примеры

В следующем примере кода используется **фрамесскиппед** для вывода общего числа кадров, пропущенных во время воспроизведения. Сведения отображаются в метке, когда пользователь нажимает кнопку. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

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

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





