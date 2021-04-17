---
title: Ивмпмедиаколлектион Жетаттрибутестрингколлектион, метод
description: Метод Жетаттрибутестрингколлектион возвращает интерфейс Ивмпстрингколлектион, представляющий набор всех значений для указанного атрибута в типе мультимедиа.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Жетаттрибутестрингколлектион метод Windows Media Player
- Жетаттрибутестрингколлектион метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жетаттрибутестрингколлектион
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669484"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a>Метод Ивмпмедиаколлектион:: Жетаттрибутестрингколлектион

Метод **жетаттрибутестрингколлектион** возвращает интерфейс **ивмпстрингколлектион** , представляющий набор всех значений для указанного атрибута в типе мультимедиа.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраттрибуте* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является атрибутом, для которого извлекаются значения.

</dd> <dt>

*бстрмедиатипе* \[ окне\]
</dt> <dd>

**Строка System. String** , представляющая тип носителя, для которого извлекаются значения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпстрингколлектион** для извлеченных значений.

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).

## <a name="examples"></a>Примеры

В следующем примере **жетаттрибутестрингколлектион** используется для вывода списка значений, соответствующих определенному атрибуту для звуковых элементов в коллекции мультимедиа. Поле со списком позволяет пользователю выбрать атрибут, например исполнитель, жанр или альбом, а также многострочное текстовое поле, в котором отображается результат. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

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

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпстрингколлектион (VB и C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





