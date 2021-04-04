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
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999440"
---
# <a name="jetgettableinfo-function"></a>Функция JetGetTableInfo


_**Применимо к:** Windows | Windows Server_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_TblInfo</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> . Если метод выполняется правильно, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> структура заполняется соответствующими данными. В случае неудачи содержимое не определено.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoDbid</p></td>
<td><p><em>пвресулт</em> обрабатывается как массив из двух объектов <a href="gg269248(v=exchg.10).md">JET_DBID</a> . Идентификатор базы данных, владеющей таблицей, хранится в этом массиве дважды.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoDumpTable</p></td>
<td><p>JET_TblInfoDumpTable не рекомендуется к использованию. API возвратит JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoName</p></td>
<td><p>JET_TblInfoName извлекает имя таблицы и сохраняет ее в <em>пвресулт</em>. Если буфер слишком мал, поведение не определено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoMostMany</p></td>
<td><p>JET_TblInfoMostMany извлекает имя таблицы и сохраняет ее в <em>пвресулт</em>. Если буфер слишком мал, поведение не определено.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoOLC</p></td>
<td><p>JET_TblInfoOLC не рекомендуется к использованию. API возвратит JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoRvt</p></td>
<td><p>JET_TblInfoRvt не рекомендуется к использованию. API возвратит JET_errQueryNotSupported.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoResetOLC</p></td>
<td><p>JET_TblInfoResetOLC не рекомендуется к использованию. API возвратит JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceAlloc</p></td>
<td><p><em>пвресулт</em> интерпретируется как массив из двух ulong:</p>
<ul>
<li><p>Первый <strong>ulong</strong> — число страниц в таблице.</p></li>
<li><p>Второй <strong>ulong</strong> является целевой плотностью страниц для таблицы.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceAvailable</p></td>
<td><p><em>пвресулт</em> интерпретируется как <strong>ulong</strong>. <strong>Ulong</strong> — это сумма количества страниц, доступных в таблице, ее индексах и дереве значений long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceOwned</p></td>
<td><p><em>пвресулт</em> интерпретируется как <strong>ulong</strong>. <strong>Ulong</strong> представляет собой сумму количества страниц, принадлежащих таблице (включая ее индексы, а также дерево длинных значений и все доступные страницы).</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceUsage</p></td>
<td><p>Поведение API зависит от размера буфера, передаваемого в API. Два значения <em>кбмакс</em> должны быть не меньше (2 * sizeof (ulong)).</p>
<ul>
<li><p>Если <em>кбмакс</em> имеет значение (2 * sizeof (ulong)), <em>пвресулт</em> интерпретируется как массив из двух ulong:</p>
<ul>
<li><p>Первый <strong>ulong</strong> — число принадлежащих экстентов таблицы.</p></li>
<li><p>Второй <strong>ulong</strong> — число доступных экстентов таблицы.</p></li>
</ul></li>
<li><p><em>пвресулт</em> интерпретируется как массив:</p>
<ul>
<li><p>Первый <strong>ulong</strong> — число принадлежащих экстентов таблицы.</p></li>
<li><p>Второй <strong>ulong</strong> — число доступных экстентов таблицы.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoTemplateTableName</p></td>
<td><p><em>пвресулт</em> интерпретируется как строковый буфер. Буфер должен быть не менее JET_cbNameMost + 1, включая завершающее <strong>значение NULL</strong>. Если таблица является производной, буфер будет заполнен именем таблицы, из которой производные таблицы наследовали ее DDL. Если таблица не является производной, буфер будет пустой строкой.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Буфер слишком мал.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Указан устаревший <em>инфолевел</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Размер буфера не подходит.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Переданная таблица была временной таблицей, и запрошенный <em>инфолевел</em> не может быть получен для временной таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Переданная таблица была временной таблицей, и запрошенный <em>инфолевел</em> не может быть получен для временной таблицы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errQueryNotSupported</p></td>
<td><p><em>Инфолевел</em> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Таблица используется другой операцией базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>Таблица заблокирована другой операцией базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Таблица используется системой. Это предупреждение является неустранимым.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Некоторые части информации недопустимы для временных таблиц (см. [жетопентемптабле](./jetopentemptable-function.md)).

Статистика таблицы включает число записей и количество страниц в кластеризованном индексе (то есть индекс, содержащий данные записи). Доступ к статистике индекса осуществляется отдельно по имени с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>жетжеттаблеинфов</strong> (Юникод) и <strong>жетжеттаблеинфоа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
