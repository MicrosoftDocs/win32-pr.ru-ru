---
title: Ивмпмедиа Аттрибутекаунт, свойство
description: Свойство Аттрибутекаунт возвращает количество атрибутов, которые можно запрашивать или задавать для элемента мультимедиа.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- проигрыватель Windows Media свойства аттрибутекаунт
- проигрыватель Windows Media свойства аттрибутекаунт, интерфейс ивмпмедиа
- проигрыватель Windows Media интерфейса ивмпмедиа, свойство аттрибутекаунт
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c3139d076fd7d1cd1bad784e325c67da25b3e7dedf530a9634a2878fe3011a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746073"
---
# <a name="iwmpmediaattributecount-property"></a>Свойство Ивмпмедиа:: Аттрибутекаунт

Свойство **аттрибутекаунт** возвращает количество атрибутов, которые можно запрашивать или задавать для элемента мультимедиа.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является счетчиком.

## <a name="remarks"></a>Remarks

Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).

## <a name="examples"></a>Примеры

В следующем примере используется **аттрибутекаунт** для определения количества атрибутов, доступных в текущем элементе мультимедиа. Код использует это значение для вывода списка имен и значений атрибутов в текстовом поле. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





