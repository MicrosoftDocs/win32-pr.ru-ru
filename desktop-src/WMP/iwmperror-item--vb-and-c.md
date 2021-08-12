---
title: Ивмперрор. Item (VB и C)
description: Свойство Item ( \_ метод Get Item в C \) получает интерфейс ивмперроритем по указанному индексу в очереди ошибок.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- ивмперрор. Item (VB и C) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be8d212eca9e9e54770e7e2751df345d80bbfb6bfc1b12714e811c7795990725
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575636"
---
# <a name="iwmperroritem-vb-and-c"></a>Ивмперрор. Item (VB и C#)

Свойство **Item** (метод **Get \_ Item** в C#) получает интерфейс **ивмперроритем** по указанному индексу в очереди ошибок.


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a>Параметры

*двиндекс*

Объект **System. Int32** , который является начинающимся с нуля индексом интерфейса **ивмперроритем** в очереди ошибок.

## <a name="property-value"></a>Значение свойства

Интерфейс **вмплиб. ивмперроритем** .

## <a name="remarks"></a>Remarks

проигрыватель Windows Media может создать ряд ошибок в ответ на состояние ошибки. Это свойство возвращает определенную ошибку в очереди с помощью номера индекса. Номера индексов для очереди ошибок начинаются с нуля.

Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .

## <a name="examples"></a>Примеры

В следующем примере свойство **Item** (метод **Get \_ Item** в C#) используется в обработчике событий ошибок для получения и вывода сведений о последней ошибке в очереди ошибок. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

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

[**Интерфейс Ивмперрор (VB и C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмперроритем (VB и C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





