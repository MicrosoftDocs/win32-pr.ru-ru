---
description: Дополнительные сведения о функции Жетжеттаблеинфо
title: Функция JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c17e1c5aa23e8e2fe77aaa07f98fee1b2df0c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465801"
---
# <a name="jetgettableinfo-function"></a>Функция JetGetTableInfo


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgettableinfo-function"></a>Функция JetGetTableInfo

Функция **жетжеттаблеинфо** извлекает различные фрагменты информации о таблице в базе данных.

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, к которой применяются сведения.

*пвресулт*

Указатель на буфер, который будет принимать сведения. Тип буфера зависит от *инфолевел*. Вызывающий объект отвечает за то, чтобы правильно согласовать буфер.

*кбмакс*

Размер (в байтах) буфера, переданного в *пвресулт*.

*инфолевел*

Тип сведений, которые будут получены для таблицы, заданной *tableid*. Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.

Для этого параметра можно задать следующие параметры:


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_TblInfo</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> . Если метод выполняется правильно, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> структура заполняется соответствующими данными. В случае неудачи содержимое не определено.</p> | 
| <p>JET_TblInfoDbid</p> | <p><em>пвресулт</em> обрабатывается как массив из двух объектов <a href="gg269248(v=exchg.10).md">JET_DBID</a> . Идентификатор базы данных, владеющей таблицей, хранится в этом массиве дважды.</p> | 
| <p>JET_TblInfoDumpTable</p> | <p>JET_TblInfoDumpTable не рекомендуется к использованию. API возвратит JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoName</p> | <p>JET_TblInfoName извлекает имя таблицы и сохраняет ее в <em>пвресулт</em>. Если буфер слишком мал, поведение не определено.</p> | 
| <p>JET_TblInfoMostMany</p> | <p>JET_TblInfoMostMany извлекает имя таблицы и сохраняет ее в <em>пвресулт</em>. Если буфер слишком мал, поведение не определено.</p> | 
| <p>JET_TblInfoOLC</p> | <p>JET_TblInfoOLC не рекомендуется к использованию. API возвратит JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoRvt</p> | <p>JET_TblInfoRvt не рекомендуется к использованию. API возвратит JET_errQueryNotSupported.</p> | 
| <p>JET_TblInfoResetOLC</p> | <p>JET_TblInfoResetOLC не рекомендуется к использованию. API возвратит JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoSpaceAlloc</p> | <p><em>пвресулт</em> интерпретируется как массив из двух ulong:</p><ul><li><p>Первый <strong>ulong</strong> — число страниц в таблице.</p></li><li><p>Второй <strong>ulong</strong> является целевой плотностью страниц для таблицы.</p></li></ul> | 
| <p>JET_TblInfoSpaceAvailable</p> | <p><em>пвресулт</em> интерпретируется как <strong>ulong</strong>. <strong>Ulong</strong> — это сумма количества страниц, доступных в таблице, ее индексах и дереве значений long.</p> | 
| <p>JET_TblInfoSpaceOwned</p> | <p><em>пвресулт</em> интерпретируется как <strong>ulong</strong>. <strong>Ulong</strong> представляет собой сумму количества страниц, принадлежащих таблице (включая ее индексы, а также дерево длинных значений и все доступные страницы).</p> | 
| <p>JET_TblInfoSpaceUsage</p> | <p>Поведение API зависит от размера буфера, передаваемого в API. Два значения <em>кбмакс</em> должны быть не меньше (2 * sizeof (ulong)).</p><ul><li><p>Если <em>кбмакс</em> имеет значение (2 * sizeof (ulong)), <em>пвресулт</em> интерпретируется как массив из двух ulong:</p><ul><li><p>Первый <strong>ulong</strong> — число принадлежащих экстентов таблицы.</p></li><li><p>Второй <strong>ulong</strong> — число доступных экстентов таблицы.</p></li></ul></li><li><p><em>пвресулт</em> интерпретируется как массив:</p><ul><li><p>Первый <strong>ulong</strong> — число принадлежащих экстентов таблицы.</p></li><li><p>Второй <strong>ulong</strong> — число доступных экстентов таблицы.</p></li></ul></li></ul> | 
| <p>JET_TblInfoTemplateTableName</p> | <p><em>пвресулт</em> интерпретируется как строковый буфер. Буфер должен быть не менее JET_cbNameMost + 1, включая завершающее <strong>значение NULL</strong>. Если таблица является производной, буфер будет заполнен именем таблицы, из которой производные таблицы наследовали ее DDL. Если таблица не является производной, буфер будет пустой строкой.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Буфер слишком мал.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Указан устаревший <em>инфолевел</em> .</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Размер буфера не подходит.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Переданная таблица была временной таблицей, и запрошенный <em>инфолевел</em> не может быть получен для временной таблицы.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Переданная таблица была временной таблицей, и запрошенный <em>инфолевел</em> не может быть получен для временной таблицы.</p> | 
| <p>JET_errQueryNotSupported</p> | <p><em>Инфолевел</em> не поддерживается.</p> | 
| <p>JET_errTableInUse</p> | <p>Таблица используется другой операцией базы данных.</p> | 
| <p>JET_errTableLocked</p> | <p>Таблица заблокирована другой операцией базы данных.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Таблица используется системой. Это предупреждение является неустранимым.</p> | 



#### <a name="remarks"></a>Комментарии

Некоторые части информации недопустимы для временных таблиц (см. [жетопентемптабле](./jetopentemptable-function.md)).

Статистика таблицы включает число записей и количество страниц в кластеризованном индексе (то есть индекс, содержащий данные записи). Доступ к статистике индекса осуществляется отдельно по имени с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетжеттаблеинфов</strong> (Юникод) и <strong>жетжеттаблеинфоа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[жетжетиндексинфо](./jetgetindexinfo-function.md)  
[жетжетобжектинфо](./jetgetobjectinfo-function.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)  
[жетопентемптабле](./jetopentemptable-function.md)
