---
description: Дополнительные сведения о функции Жетжетдатабасеинфо
title: Функция JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264775"
---
# <a name="jetgetdatabaseinfo-function"></a>Функция JetGetDatabaseInfo


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetdatabaseinfo-function"></a>Функция JetGetDatabaseInfo

Функция **жетжетдатабасеинфо** извлекает различные типы сведений о базе данных. Этот API может вызываться, когда база данных подключена или находится в режиме «в сети» (с **жетжетдатабасеинфо**) либо база данных или ядро СУБД находятся в режиме «вне сети» (с [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*DBID*

[JET_DBID](./jet-dbid.md) для базы данных, из которой извлекаются сведения.

*пвресулт*

Указатель на буфер, который получит указанные сведения. Размер буфера в байтах передается в *кбмакс*.

При сбое содержимое *пвресулт* не определено.

Сведения, хранящиеся в *пвресулт* , зависят от *инфолевел*.

*кбмакс*

Размер (в байтах) буфера, переданного в *пвресулт*.

*инфолевел*

*Инфолевел* указывает, какой тип сведений следует получить о указанной базе данных. Это влияет на интерпретацию *пвресулт* . Некоторые *инфолевел* доступны только в автономной ([жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)) или интерактивной версии (**жетжетдатабасеинфо**) API.

Если предоставленный буфер *пвресулт* слишком мал, то в зависимости от *инфолевел* будет возвращаться либо JET_errInvalidBufferSize, либо JET_errBufferTooSmall.

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
<td><p>JET_DbInfoCollate</p></td>
<td><p>Пока не поддерживаются и не возвращают значения по умолчанию. Не используйте.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Эти <em>инфолевелс</em> являются устаревшими и сейчас не поддерживаются. Не используйте.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Пока не поддерживаются и не возвращают значения по умолчанию. Не используйте.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Пока не поддерживаются и не возвращают значения по умолчанию. Не используйте.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFilename</p></td>
<td><p><em>пвресулт</em> будет интерпретирован как строковый буфер (char *). Рекомендуется MAX_PATH буфер, но не требуется. Если буфер не достаточно длинный, будет возвращен JET_errBufferTooSmall. Строка будет заполнена путем к базе данных для этого DBID.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как DWORD (4 байта). Возвращает размер базы данных на страницах.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Эти <em>инфолевелс</em> являются устаревшими и сейчас не поддерживаются. Не используйте.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoLCID</p></td>
<td><p>(Windows XP и более поздние версии) Этот <em>инфолевел</em> был первоначально указан как JET_DbInfoLangid (Windows 2000).</p>
<p><em>пвресулт</em> будет интерпретироваться как длинное. Он возвращает код локали (LCID), связанный с этой базой данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>пвресулт</em> будет интерпретирован как <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. Структура <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> будет заполнена сведениями, относящимися к указанной базе данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoOptions</p></td>
<td><p><em>пвресулт</em> будет интерпретирован как <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Он возвращает значение, указывающее, открыта ли база данных в монопольном режиме. Если база данных находится в монопольном режиме JET_bitDbExclusive будет задана в предоставленном <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> , в противном случае устанавливается ноль. Обратите внимание, что другие параметры <em>грбит</em> базы данных для <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> и <a href="gg269299(v=exchg.10).md">жетопендатабасе</a> не возвращаются.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p>Доступно только в Windows XP и более поздних версиях. <em>пвресулт</em> будет интерпретироваться как длинное целое без знака. Это приведет к возврату размера страницы базы данных в байтах.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoSpaceAvailable</p></td>
<td><p><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как DWORD. Он возвращает доступное место для базы данных на страницах.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoSpaceOwned</p></td>
<td><p><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как DWORD. В результате будет возвращено пространство для базы данных на страницах.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoTransactions</p></td>
<td><p><em>пвресулт</em> будет интерпретироваться как длинное. Будет возвращено значение, превышающее максимальный уровень, до которого транзакции могут быть вложенными. Если <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a> вызывается (во вложенном режиме, то есть в том же сеансе без фиксации или отката), то при последнем вызове JET_errTransTooDeep будет возвращено из <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a>. Обратите внимание, что значение в Windows 2000, Windows XP и Windows Server 2003 — 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoVersion</p></td>
<td><p><em>пвресулт</em> будет интерпретироваться как длинное. Он возвращает собственный основной номер версии ядра СУБД. Это значение равно 0x620 для Windows 2000, Windows XP и Windows Server 2003.</p></td>
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
<td><p>Размер буфера, заданного в <em>кбмакс</em> , слишком мал (или неправильный) для хранения требуемой информации.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Запрошенный <em>инфолевел</em> был JET_DbInfoIsam. Такой способ связывания не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Размер буфера, заданного в <em>кбмакс</em> , слишком мал (или неправильный) для хранения требуемой информации.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Эта ошибка будет возвращена <strong>жетжетдатабасеинфо</strong> , если предоставленная <a href="gg269248(v=exchg.10).md">JET_DBID</a> не является допустимой (присоединенной) базой данных. Эта ошибка будет возвращена <a href="gg269239(v=exchg.10).md">жетжетдатабасефилеинфо</a> и <strong>жетжетдатабасеинфо</strong> , когда запрошенный <em>инфолевел</em> не поддерживается этой версией функции.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении запрошенные данные будут возвращены в выходной буфер.

В случае сбоя выходной буфер будет находиться в неопределенном состоянии.

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
<td><p>Реализуется как <strong>жетжетдатабасеинфов</strong> (Юникод) и <strong>жетжетдатабасеинфоа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md)
