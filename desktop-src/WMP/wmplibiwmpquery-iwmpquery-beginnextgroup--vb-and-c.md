---
title: Ивмпкуери Бегиннекстграуп, метод
description: Метод Бегиннекстграуп начинает новую группу условий. | Ивмпкуери Бегиннекстграуп, метод
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- Бегиннекстграуп метод Windows Media Player
- Бегиннекстграуп метод проигрывателя Windows Media Player, интерфейс Ивмпкуери
- Интерфейс Ивмпкуери Windows Media Player, метод Бегиннекстграуп
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718031"
---
# <a name="iwmpquerybeginnextgroup-method"></a>Метод Ивмпкуери:: Бегиннекстграуп

Метод **бегиннекстграуп** начинает новую группу условий.

## <a name="syntax"></a>Синтаксис


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Начало новой группы условий означает, что вы завершили текущую группу условий. Новая группа условий всегда объединяется с предыдущей группой условий с помощью логики **или** .

## <a name="examples"></a>Примеры

В следующем примере создается сложный запрос с объединением двух групп, каждая из которых содержит условие. Результаты запроса извлекаются в виде коллекции строк и отображаются в окне списка. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IWMPMediaCollection2. createQuery (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. Жетплайлистбикуери (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. Жетстрингколлектионбикуери (VB и C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкуери (VB и C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





