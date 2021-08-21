---
title: Аксвиндовсмедиаплайер. versionInfo, свойство
description: свойство versionInfo возвращает значение, указывающее версию проигрыватель Windows Media.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- проигрыватель Windows Media свойства versionInfo
- проигрыватель Windows Media свойства versionInfo, класс аксвиндовсмедиаплайер
- проигрыватель Windows Media класса аксвиндовсмедиаплайер, свойство versionInfo
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
ms.openlocfilehash: 2fd7491af0fc102f03da9855b78ecef79ac0a09ca9b3ab8b49f9bf6b948f0d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841165"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a>Аксвиндовсмедиаплайер. versionInfo, свойство

свойство versionInfo возвращает значение, указывающее версию проигрыватель Windows Media.

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

в следующем примере создается кнопка, которая при нажатии отображает окно сообщения, содержащее сведения о версии для проигрыватель Windows Media. Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.


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





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





