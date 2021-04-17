---
title: Ивмперроритем errorDescription, свойство
description: Свойство errorDescription Возвращает описание ошибки.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- Проигрыватель Windows Media для свойства errorDescription
- errorDescription свойство проигрывателя Windows Media Player, интерфейс Ивмперроритем
- Интерфейс Ивмперроритем Windows Media Player, свойство errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708530"
---
# <a name="iwmperroritemerrordescription-property"></a>Свойство Ивмперроритем:: errorDescription

Свойство **errorDescription** Возвращает описание ошибки.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является описанием ошибки.

## <a name="remarks"></a>Комментарии

Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .

## <a name="examples"></a>Примеры

В следующем примере для вывода описания ошибки пользователю используется **errorDescription** в обработчике событий ошибки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

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

[**Интерфейс Ивмперроритем (VB и C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





