---
title: Метод Query. Аддкондитион
description: Метод Аддкондитион добавляет условие в объект запроса с помощью логики и.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Аддкондитион метод Windows Media Player
- метод Аддкондитион Windows Media Player, класс запроса
- Класс запроса проигрыватель Windows Media Player, метод Аддкондитион
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704184"
---
# <a name="queryaddcondition-method"></a>Метод Query. Аддкондитион

Метод **аддкондитион** добавляет условие в объект **запроса** с помощью логики и.

## <a name="syntax"></a>Синтаксис


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута.

</dd> <dt>

*оператор* \[ окне\]
</dt> <dd>

**Строка** , содержащая оператор. Поддерживаемые значения см. в разделе Примечания.

</dd> <dt>

*значение* \[ окне\]
</dt> <dd>

**Строка** , содержащая значение атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

В составных запросах, использующих **запрос** , регистр не учитывается.

Список значений для параметра *Attribute* можно найти в [алфавитном разделе Справочник по атрибутам](alphabetical-attribute-reference.md) .

Условия, содержащиеся в объекте **запроса** , организованы в группы условий. Несколько условий в группе условий всегда объединяются с помощью логики и. Группы условий всегда объединяются друг с другом с помощью логики или. Чтобы запустить новую группу условий, вызовите **Query. бегиннекстграуп**.

В следующей таблице перечислены поддерживаемые значения для *оператора*.



| Оператор            | Применяется к     |
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

В следующем примере JScript для выполнения примера запроса используется **Query. аддкондитион** и **Query. бегиннекстграуп** .


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Медиаколлектион. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**Медиаколлектион. Жетплайлистбикуери**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Медиаколлектион. Жетстрингколлектионбикуери**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Объект запроса**](query-object.md)
</dt> <dt>

[**Query. Бегиннекстграуп**](query-beginnextgroup.md)
</dt> </dl>

 

 





