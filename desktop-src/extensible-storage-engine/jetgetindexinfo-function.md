---
description: Дополнительные сведения о функции Жетжетиндексинфо
title: Функция JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647497"
---
# <a name="jetgetindexinfo-function"></a>Функция JetGetIndexInfo


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>Функция JetGetIndexInfo

Функция **жетжетиндексинфо** получает сведения о индексе.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Идентификатор базы данных, используемый для вызова API.

*сзтабленаме*

Имя таблицы, содержащей индекс, с извлекаемыми данными.

*сзиндекснаме*

Имя индекса с извлекаемыми данными.

*пвресулт*

Указатель на буфер, который будет принимать нужные сведения. Буфер должен быть согласован, чтобы вместить требуемый тип. Тип буфера зависит от параметра *инфолевел* .

*кбресулт*

Размер (в байтах) буфера, переданного в качестве *пвресулт*.

*инфолевел*

Сведения, которые будут храниться в *пвресулт*. Для этого параметра можно использовать следующие параметры.

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе. При сбое содержимое <em>пвбуффер</em> не определено.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>пвресулт</em> интерпретируется как ULong. В случае успеха ULONG содержит количество индексов в указанной таблице. <em>сзиндекснаме</em> игнорируется. При сбое содержимое <em>пвбуффер</em> не определено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>пвресулт</em> интерпретируется как <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. При успешном выполнении структура <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> получает сведения об индексе. При сбое содержимое <em>пвбуффер</em> не определено.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid не рекомендуется к использованию. Вместо этого используйте JET_IdxInfoLCID и макрос <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">лангидфромлЦид</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>пвресулт</em> интерпретируется как LCID. При успешном выполнении код LCID содержит идентификатор локали индекса. При сбое содержимое <em>пвбуффер</em> не определено.</p>
<p><strong>Windows XP:  </strong> JET_IdxInfoLCID введен в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . При успешном выполнении структура <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> получает сведения об индексе. При сбое содержимое <em>пвбуффер</em> не определено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC устарел.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC устарел.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>пвресулт</em> интерпретируется как ULong. При успешном выполнении в ULONG содержится место использования индекса. При сбое содержимое <em>пвбуффер</em> не определено.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor устарел.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>пвресулт</em> интерпретируется как ushort. При успешном выполнении объект USHORT содержит значение <em>кбварсегмак</em> , используемое при создании индекса. Описание <em>кбварсегмак</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>пвресулт</em> интерпретируется как ushort. При успешном выполнении объект USHORT содержит значение <em>кбкэймост</em> , используемое при создании индекса. Описание <em>кбкэймост</em>см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p>
<p><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost введен в Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex введен в Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>пвресулт</em> интерпретируется как структура <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . При сбое содержимое <em>пвбуффер</em> не определено.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 введен в Windows 7.</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>Указанный индекс не найден в указанной таблице.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Буфер, переданный как <em>пвресулт</em> , слишком мал. Содержимое буфера не определено.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

**Жетжетиндексинфо** и [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) извлекают идентичные сведения о индексе. Разница заключается в том, как указана таблица. **Жетжетиндексинфо** ждет базу данных (*DBID*) и имя таблицы (*сзтабленаме*), а [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) — идентификатор таблицы (*TableID*).

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
<td><p>Реализуется как <strong>жетжетиндексинфов</strong> (Юникод) и <strong>жетжетиндексинфоа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)
