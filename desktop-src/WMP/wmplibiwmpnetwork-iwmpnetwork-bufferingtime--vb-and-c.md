---
title: Ивмпнетворк Буфферингтиме, свойство
description: Свойство Буфферингтиме Возвращает или задает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- проигрыватель Windows Media свойства буфферингтиме
- проигрыватель Windows Media свойства буфферингтиме, интерфейс ивмпнетворк
- проигрыватель Windows Media интерфейса ивмпнетворк, свойство буфферингтиме
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d224e35dd9c87dad627e71f2ae07d3d0b9e24ee1b094cfa5dea549e86c69a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999994"
---
# <a name="iwmpnetworkbufferingtime-property"></a>Свойство Ивмпнетворк:: Буфферингтиме

Свойство **буфферингтиме** Возвращает или задает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является временем буферизации в миллисекундах, которое в диапазоне от нуля до 60 000 со значением по умолчанию 5 000.

## <a name="examples"></a>Примеры

В следующем примере кода используется **буфферингтиме** для указания количества секунд, выделенных для буферизации входящих данных. Текстовое поле позволяет пользователю ввести новое значение для **буфферингтиме**, а свойство обновляется в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





