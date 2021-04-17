---
title: Ивмперрор Ерроркаунт, свойство
description: Свойство Ерроркаунт возвращает количество ошибок в очереди ошибок.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Проигрыватель Windows Media для свойства Ерроркаунт
- Ерроркаунт свойство проигрывателя Windows Media Player, интерфейс Ивмперрор
- Интерфейс Ивмперрор Windows Media Player, свойство Ерроркаунт
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708536"
---
# <a name="iwmperrorerrorcount-property"></a>Свойство Ивмперрор:: Ерроркаунт

Свойство **ерроркаунт** возвращает количество ошибок в очереди ошибок.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>Значение свойства

Объект **System. Int32** , который является числом ошибок.

## <a name="remarks"></a>Комментарии

Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .

## <a name="examples"></a>Примеры

В следующем примере используется **ерроркаунт** в обработчике событий ошибки, чтобы предупредить пользователя о последней ошибке в очереди ошибок. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

[**Интерфейс Ивмперрор (VB и C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





