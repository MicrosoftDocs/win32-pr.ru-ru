---
title: Ивмпмедиа Сетитеминфо, метод
description: Метод Сетитеминфо задает значение указанного атрибута для элемента мультимедиа.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- проигрыватель Windows Media метода сетитеминфо
- проигрыватель Windows Media метода сетитеминфо, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, метод сетитеминфо
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24265e94880899df96aa954f2df30ca6e4f5ae1e5b4fc20c419085e3f9f0ab14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053642"
---
# <a name="iwmpmediasetiteminfo-method"></a>Метод Ивмпмедиа:: Сетитеминфо

Метод **сетитеминфо** задает значение указанного атрибута для элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстритемнаме* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута.

</dd> <dt>

*бстрвал* \[ окне\]
</dt> <dd>

Значение **System. String** , которое является новым значением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Свойство **аттрибутекаунт** возвращает количество атрибутов, доступных для данного элемента мультимедиа. Номера индексов можно использовать с методом **жетаттрибутенаме** для определения имен встроенных атрибутов, которые могут использоваться с этим методом.

Перед использованием этого метода используйте метод **исреадонлитем** , чтобы определить, можно ли задать определенный атрибут.

Перед вызовом этого метода необходимо иметь полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Примечание

при внедрении элемента управления проигрыватель Windows Media в приложение измененные атрибуты файла не будут записываться в файл мультимедиа до тех пор, пока пользователь не выполнит проигрыватель Windows Media.

## <a name="examples"></a>Примеры

В следующем примере **сетитеминфо** используется для изменения значения атрибута жанра для текущего элемента мультимедиа. Текстовое поле позволяет пользователю ввести строку, которая затем используется для изменения сведений об атрибуте в ответ на событие щелчка кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

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

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Аттрибутекаунт (VB и C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Жетаттрибутенаме (VB и C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Исреадонлитем (VB и C#)**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





