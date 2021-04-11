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
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104274003"
---
# <a name="jetgettablecolumninfo-function"></a>Функция Жетжеттаблеколумнинфо


_**Применимо к:** Windows | Windows Server_

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
<td><p>JET_ColInfo</p></td>
<td><p><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, а поля структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> заполняются соответствующим образом. JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Это похоже на структуру <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p><em>пвресулт</em> интерпретируется как <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является строковым именем столбца, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo и JET_ColInfoByColid получают одни и те же сведения.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Открывается временная таблица, которая определяется элементом <em>tableid</em> <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Если эта функция выполнена, структура заполняется соответствующими значениями. Открывается временная таблица, которая определяется элементом <em>tableid</em> <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. Таблица должна быть закрыта с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>. Если эта функция завершается ошибкой, структура содержит неопределенные данные.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>То же, что и JET_ColInfoList, однако результирующая таблица сортируется по <em>columnid</em>, а не по имени столбца.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor не рекомендуется, и его использование будет возвращать JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>То же, что и JET_ColInfoBase, <em>пвресулт</em> интерпретируется как <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, за исключением того, что этот <em>инфолевел</em> указывает, что запрашиваемый столбец (<em>сзколумнаме</em>) не является строковым именем столбца, а указатель на <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p>
<p><strong>Windows Vista:  </strong> Он доступен в Windows Vista и более поздних версиях.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Возвращать только столбцы, не являющиеся производными (если таблица является производной от шаблона).</p>
<p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Возвращать только имя столбца и значение columnid для каждого столбца.</p>
<p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Сортировать возвращенный список столбцов по columnid (по умолчанию сортировка списка по имени столбца).</p>
<p>Это значение может быть логически или в <em>инфолевел</em>, когда базовый <em>инфолевел</em> JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Это значение представлено в Windows Vista.</p></td>
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
<td><p>JET_errColumnNotFound</p></td>
<td><p>Столбец с именем <em>сзколумннаме</em> не найден в таблице.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Указан недопустимый <em>инфолевел</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Эта ошибка может быть возвращена, если:</p>
<ul>
<li><p>Задано неправильное имя для <em>сзтабленаме</em> .</p></li>
<li><p>Задано неправильное имя для <em>сзколумннаме</em> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Эта ошибка может быть возвращена, если:</p>
<ul>
<li><p>Указан недопустимый <em>инфолевел</em> .</p></li>
<li><p>Передан <em>СЗТАБЛЕНАМЕ</em> null.</p></li>
<li><p>Буфер слишком мал.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

**Жетжеттаблеколумнинфо** и [жетжетколумнинфо](./jetgetcolumninfo-function.md) извлекают сведения о столбце. Различие между ними заключается в том, как определяется таблица:

  - **Жетжеттаблеколумнинфо** определяет таблицу по *TableID*.

  - [Жетжетколумнинфо](./jetgetcolumninfo-function.md) определяет таблицу, используя сочетание *DBID* и *сзтабленаме* .

При получении данных с помощью JET_ColInfoList, JET_ColInfoListSortColumnid или JET_ColInfoListCompact будет открыта временная таблица. Временная таблица содержит данные, а структура [JET_COLUMNLIST](./jet-columnlist-structure.md) содержит достаточно сведений для прохода по временной таблице. Временная таблица должна быть закрыта с помощью [жетклосетабле](./jetclosetable-function.md).

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
<td><p>Реализуется как <strong>жетжеттаблеколумнинфов</strong> (Юникод) и <strong>жетжеттаблеколумнинфоа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[Ошибки расширяемого подсистемы хранилища](./extensible-storage-engine-errors.md)  
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
