---
description: Дополнительные сведения о функции Жетжетколумнинфо
title: Функция JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97b6dfc76de520249880314ecd32769951c7b927
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479110"
---
# <a name="jetgetcolumninfo-function"></a>Функция JetGetColumnInfo


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetcolumninfo-function"></a>Функция JetGetColumnInfo

Функция **жетжетколумнинфо** извлекает сведения о столбце.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Определяет, а также *сзтабленаме* таблицу, содержащую столбец, из которого извлекаются данные.

*сзтабленаме*

Определяет, вместе с *DBID*— таблицу, содержащую столбец, из которого извлекаются данные.

*сзколумннаме*

Имя столбца, для которого извлекается информация.

*пвресулт*

Указатель на буфер, который будет принимать сведения. Тип буфера зависит от *инфолевел*. Вызывающий объект должен быть настроен для правильного согласования буфера.

*кбмакс*

Размер буфера (в байтах), переданного в *пвресулт*.

*инфолевел*

Тип извлекаемых данных для столбца, заданного параметром *сзколумннаме*. Формат данных, хранящихся в *пвресулт* , зависит от этого параметра. Сведения о схеме временной таблицы см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).

Эти *инфолевелс* отличаются следующими:

  - JET_ColInfoListSortColumnid будет сортировать временную таблицу по *columnid*.

  - JET_ColInfoListCompact будет сжимать выходные данные. Дополнительные сведения о компактном выходе см. в разделе [JET_COLUMNLIST](./jet-columnlist-structure.md).

Для использования с этим параметром доступны следующие параметры.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p>JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения. <em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, а поля структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> заполняются соответствующим образом.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Это похоже на структуру <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p> | 
| <p>JET_ColInfoByColid</p> | <p>Как и JET_ColInfo, <em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является именем столбца строк, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p> | 
| <p>JET_ColInfoList</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Открывается временная таблица, которая определяется элементом <strong>tableid</strong> структуры <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p> | 
| <p>JET_ColInfoListCompact</p> | <p>То же, что и JET_ColInfoList.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>То же, что и JET_ColInfoList; Однако результирующая таблица сортируется по columnid, а не к имени столбца.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor не рекомендуется, и его использование будет возвращать JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Как и JET_ColInfoBase, <em>пвресулт</em> интерпретируется как <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является именем столбца строк, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> это значение вводится в Windows Vista.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Возвращать только столбцы, не являющиеся производными (если таблица является производной от шаблона).</p><p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> это значение введено Windows Vista.</p> | 
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

[Жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) и **жетжетколумнинфо** извлекают сведения о столбце. Различие между ними заключается в том, как определяется таблица:

  - [Жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) определяет таблицу по *TableID*.

  - **Жетжетколумнинфо** определяет таблицу, используя сочетание *DBID* и *сзтабленаме* .

При получении данных с помощью JET_ColInfoList, JET_ColInfoListSortColumnid или JET_ColInfoListCompact будет открыта временная таблица. Временная таблица содержит данные, а структура [JET_COLUMNLIST](./jet-columnlist-structure.md) содержит достаточно сведений для прохода по временной таблице. Временная таблица должна быть закрыта с помощью [жетклосетабле](./jetclosetable-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетжетколумнинфов</strong> (Юникод) и <strong>жетжетколумнинфоа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[Параметры обработки ошибок](./error-handling-parameters.md)  
[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md)
