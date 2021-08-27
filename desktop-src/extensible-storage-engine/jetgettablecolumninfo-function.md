---
description: Дополнительные сведения о функции Жетжеттаблеколумнинфо
title: Функция Жетжеттаблеколумнинфо
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3940c07cc641d8c8d077c420f8c492ab5122b3f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984737"
---
# <a name="jetgettablecolumninfo-function"></a>Функция Жетжеттаблеколумнинфо


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgettablecolumninfo-function"></a>Функция Жетжеттаблеколумнинфо

Функция **жетжеттаблеколумнинфо** извлекает сведения о столбце таблицы.

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, содержащая столбец, для которого необходимо получить сведения.

*сзколумннаме*

Имя столбца, для которого необходимо получить сведения.

*пвресулт*

Указатель на буфер, который будет принимать сведения. Тип буфера зависит от *инфолевел*. Вызывающий объект должен быть настроен для правильного согласования буфера.

*кбмакс*

Размер (в байтах) буфера, переданного в *пвресулт*.

*инфолевел*

Тип данных, которые будут получены для столбца, заданного параметром *сзколумннаме*. Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*. Сведения о схеме временной таблицы см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid будет сортировать временную таблицу по *columnid*.

  - JET_ColInfoListCompact будет сжимать выходные данные. Дополнительные сведения о компактном выходе см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).

Для этого параметра можно задать следующие параметры:


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, а поля структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> заполняются соответствующим образом. JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Это похоже на структуру <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p> | 
| <p>JET_ColInfoByColid</p> | <p><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является строковым именем столбца, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</p> | 
| <p>JET_ColInfoList</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Открывается временная таблица, которая определяется элементом <em>tableid</em> <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p> | 
| <p>JET_ColInfoListCompact</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Открывается временная таблица, которая определяется элементом <em>tableid</em> <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>То же, что и JET_ColInfoList, однако результирующая таблица сортируется по <em>columnid</em>, а не по имени столбца.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor не рекомендуется, и его использование будет возвращать JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>То же, что и JET_ColInfoBase, <em>пвресулт</em> интерпретируется как <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является строковым именем столбца, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> он доступен в Windows Vista и более поздних версиях.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Возвращать только столбцы, не являющиеся производными (если таблица является производной от шаблона).</p><p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> это значение вводится в Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Возвращать только имя столбца и значение columnid для каждого столбца.</p><p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> это значение вводится в Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Сортировать возвращенный список столбцов по columnid (по умолчанию сортировка списка по имени столбца).</p><p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> это значение вводится в Windows Vista.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Столбец с именем <em>сзколумннаме</em> не найден в таблице.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Указан недопустимый <em>инфолевел</em> .</p> | 
| <p>JET_errInvalidName</p> | <p>Эта ошибка может быть возвращена, если:</p><ul><li><p>Задано неправильное имя для <em>сзтабленаме</em> .</p></li><li><p>Задано неправильное имя для <em>сзколумннаме</em> .</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Эта ошибка может быть возвращена, если:</p><ul><li><p>Указан недопустимый <em>инфолевел</em> .</p></li><li><p>Передан <em>СЗТАБЛЕНАМЕ</em> null.</p></li><li><p>Буфер слишком мал.</p></li></ul> | 



#### <a name="remarks"></a>Комментарии

**Жетжеттаблеколумнинфо** и [жетжетколумнинфо](./jetgetcolumninfo-function.md) извлекают сведения о столбце. Различие между ними заключается в том, как определяется таблица:

  - **Жетжеттаблеколумнинфо** определяет таблицу по *TableID*.

  - [Жетжетколумнинфо](./jetgetcolumninfo-function.md) определяет таблицу, используя сочетание *DBID* и *сзтабленаме* .

При получении данных с помощью JET_ColInfoList, JET_ColInfoListSortColumnid или JET_ColInfoListCompact будет открыта временная таблица. Временная таблица содержит данные, а структура [JET_COLUMNLIST](./jet-columnlist-structure.md) содержит достаточно сведений для прохода по временной таблице. Временная таблица должна быть закрыта с помощью [жетклосетабле](./jetclosetable-function.md).

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетжеттаблеколумнинфов</strong> (Юникод) и <strong>жетжеттаблеколумнинфоа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[Параметры обработки ошибок](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетжетколумнинфо](./jetgetcolumninfo-function.md)  
[жетжеттаблеколумнинфо]()
