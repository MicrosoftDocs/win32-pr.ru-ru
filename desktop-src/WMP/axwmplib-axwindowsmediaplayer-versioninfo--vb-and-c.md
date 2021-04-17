---
title: Аксвиндовсмедиаплайер. versionInfo, свойство
description: Свойство versionInfo возвращает значение, указывающее версию проигрывателя Windows Media.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- Проигрыватель Windows Media для свойства versionInfo
- versionInfo свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698848"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>Аксвиндовсмедиаплайер. versionInfo, свойство

Свойство versionInfo возвращает значение, указывающее версию проигрывателя Windows Media.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a>Значение свойства

Строка System. String, которая является сведениями о версии в следующем формате: "*X*. 0,0. *Yyyy*"где *X* представляет основной номер версии, а *yyyy* — номер сборки.

## <a name="examples"></a>Примеры

В следующем примере создается кнопка, которая при нажатии отображает окно сообщения, содержащее сведения о версии проигрывателя Windows Media. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
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
</dt> </dl>

 

 





