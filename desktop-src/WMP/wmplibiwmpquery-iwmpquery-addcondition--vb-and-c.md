---
title: Ивмпкуери Аддкондитион, метод
description: Метод Аддкондитион добавляет условие в составной запрос с помощью логики и.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- проигрыватель Windows Media метода аддкондитион
- проигрыватель Windows Media метода аддкондитион, интерфейс ивмпкуери
- проигрыватель Windows Media интерфейса ивмпкуери, метод аддкондитион
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe85999c60364827d483f81d14ff88602c9b2831c16e7cff8a3e17076b77671d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745709"
---
# <a name="iwmpqueryaddcondition-method"></a>Метод Ивмпкуери:: Аддкондитион

Метод **аддкондитион** добавляет условие в составной запрос с помощью логики **и** .

## <a name="syntax"></a>Синтаксис


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраттрибуте* \[ окне\]
</dt> <dd>

**Строка System. String** , которая представляет собой имя атрибута, добавляемого в запрос.

</dd> <dt>

*бстроператор* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является оператором. Поддерживаемые значения см. в разделе Примечания.

</dd> <dt>

*бстрвалуе* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является значением атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Условия, содержащиеся в составном запросе, организованы в группы условий. Несколько условий в группе условий всегда объединяются с помощью логики **и** . Группы условий всегда объединяются друг с другом с помощью логики **или** . Чтобы запустить новую группу условий, вызовите метод [ивмпкуери. бегиннекстграуп](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).

В составных запросах, использующих **ивмпкуери** , регистр не учитывается.

Список значений для параметра *бстраттрибуте* можно найти в [алфавитном справочнике по атрибутам](alphabetical-attribute-reference.md).

В следующей таблице перечислены поддерживаемые значения для *бстроператор*.



| Строковый тип              | Применяется к     |
|---------------------|----------------|
| BeginsWith          | Строки        |
| Содержит            | Строки        |
| Равно              | Все типы      |
| GreaterThan         | Числа, даты |
| GreaterThanOrEquals | Числа, даты |
| LessThan;            | Числа, даты |
| LessThanOrEquals    | Числа, даты |
| нотбегинсвис       | Строки        |
| NotContains         | Строки        |
| NotEquals           | Все типы      |



 

## <a name="examples"></a>Примеры

Следующий пример создает запрос, добавляет к нему два условия и использует этот запрос для извлечения результатов запроса в виде коллекции строк. Затем результаты отображаются в окне списка. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Алфавитный справочник по атрибутам**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2. createQuery (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. Жетплайлистбикуери (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. Жетстрингколлектионбикуери (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкуери**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





