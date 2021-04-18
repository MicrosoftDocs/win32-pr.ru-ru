---
description: Дополнительные сведения о функции Жетжетдатабасефилеинфо
title: Функция Жетжетдатабасефилеинфо
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656713"
---
# <a name="jetgetdatabasefileinfo-function"></a>Функция Жетжетдатабасефилеинфо


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetdatabasefileinfo-function"></a>Функция Жетжетдатабасефилеинфо

Функция **жетжетдатабасефилеинфо** извлекает различные типы сведений о базе данных. Этот API может вызываться, когда база данных подключена или находится в режиме «в сети» (с [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)) либо база данных или ядро СУБД находятся в режиме «вне сети» (с **жетжетдатабасефилеинфо**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сздатабасенаме*

Путь к базе данных, из которой извлекаются сведения.

*пвресулт*

Указатель на буфер, который будет принимать указанные сведения. Размер буфера в байтах передается в *кбмакс*.

Если эта функция завершается ошибкой, содержимое *пвресулт* не определено.

Сведения, хранящиеся в *пвресулт* , зависят от *инфолевел*.

*кбмакс*

Размер буфера (в байтах), переданного в *пвресулт*.

*инфолевел*

*Инфолевел* указывает, какой тип сведений следует получить о указанной базе данных. Это влияет на интерпретацию *пвресулт* . Некоторые объекты *инфолевел* доступны только в автономной (**жетжетдатабасефилеинфо**) или интерактивной версии ([жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)) API.

Если предоставленный буфер *пвресулт* слишком мал, возвращается либо JET_errInvalidBufferSize, либо JET_errBufferTooSmall, в зависимости от *инфолевел*.

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
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как QWORD (8 байт). Возвращает размер базы данных в байтах.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>пвресулт</em> будет интерпретирован как <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>. Структура <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> будет заполнена сведениями, относящимися к указанной базе данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>пвресулт</em> будет интерпретирован как <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. Структура <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> будет заполнена сведениями, относящимися к указанной базе данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>пвресулт</em> будет ИНТЕРПРЕТИРОВАН как bool (4 байта). Это приведет к возвращению наличия открытых или подключенных баз данных в настоящий момент в ядре СУБД.</p>
<p><strong>Windows XP:  </strong> Это значение вводится в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>пвресулт</em> будет интерпретироваться как длинное целое без знака. Это приведет к возврату размера страницы базы данных в байтах.</p>
<p><strong>Windows XP:  </strong> Это значение вводится в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Эти <em>инфолевелс</em> пока не поддерживаются и возвращают значения по умолчанию. Не используйте эти <em>инфолевелс</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Эти <em>инфолевелс</em> пока не поддерживаются и возвращают значения по умолчанию. Не используйте эти <em>инфолевелс</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>То же, что и JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Эти <em>инфолевелс</em> являются устаревшими и сейчас не поддерживаются. Не используйте эти <em>инфолевелс</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>То же, что и JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:  </strong> Это значение <em>инфолевел</em> введено в Windows Vista.</p>
<p><em>пвресулт</em> будет рассматриваться как указатель на DWORD. Возвращает значение перечисления, указывающее тип файла, который подсистема считает этим средством. Типы файлов перечислены в следующей таблице. Дополнительные сведения об этих типах файлов и их использовании в подсистеме см. в разделе <a href="gg294069(v=exchg.10).md">Расширенные файлы подсистемы хранилища</a>.</p>
<div class="tableSection">
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
<td><p>JET_filetypeUnknown</p></td>
<td><p>Тип файла неизвестен или не является типом файла ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>Файл является файлом базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>Файл является файлом журнала транзакций.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>Файл является файлом контрольных точек.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>Файл является временным файлом базы данных.</p></td>
</tr>
</tbody>
</table>

</div></td>
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
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Запрошенный <em>инфолевел</em> был JET_DbInfoIsam. Такой способ связывания не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Буфер, указанный в <em>кбмакс</em> , слишком мал для получения требуемой информации.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Буфер, указанный в <em>кбмакс</em> , имеет неправильный размер для требуемой информации.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из предоставленных параметров содержит непредвиденное значение, или сочетание нескольких значений параметров привело к непредвиденному результату. Эта ошибка будет возвращена <a href="gg294076(v=exchg.10).md">жетжетдатабасеинфо</a> , если предоставленный DBID не является допустимой (присоединенной) базой данных. Эта ошибка будет возвращена <strong>жетжетдатабасефилеинфо</strong> и <a href="gg294076(v=exchg.10).md">жетжетдатабасеинфо</a> , когда запрошенный <em>инфолевел</em> не поддерживается этой версией функции.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, запрошенные данные будут возвращены в выходной буфер.

Если эта функция завершается ошибкой, выходной буфер будет находиться в неопределенном состоянии.

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
<td><p>Реализуется как <strong>жетжетдатабасефилеинфов</strong> (Юникод) и <strong>жетжетдатабасефилеинфоа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md)
