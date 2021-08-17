---
title: Метод Query. Аддкондитион
description: Метод Аддкондитион добавляет условие в объект запроса с помощью логики и.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- проигрыватель Windows Media метода аддкондитион
- метод аддкондитион проигрыватель Windows Media, класс запроса
- класс запроса проигрыватель Windows Media, метод аддкондитион
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
ms.openlocfilehash: 53a3eed0a7923b93861eabc30d115a7726046d0595b7c57625d9a9afaf9c7523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746593"
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

## <a name="remarks"></a>Remarks

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

в следующем примере JScript используется **query. аддкондитион** и **query. бегиннекстграуп** для выполнения примера запроса.


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
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
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

 

 





