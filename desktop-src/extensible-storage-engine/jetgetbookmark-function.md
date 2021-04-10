---
description: Дополнительные сведения о функции Жетжетбукмарк
title: Функция Жетжетбукмарк
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156807"
---
# <a name="jetgetbookmark-function"></a>Функция Жетжетбукмарк


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>Функция Жетжетбукмарк

Функция **жетжетбукмарк** извлекает закладку для записи, связанной с элементом индекса, в текущем положении курсора. Эту закладку можно использовать для перемещения курсора обратно в ту же запись с помощью [жетготобукмарк](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*пвбукмарк*

Выходной буфер, получающий закладку.

*кбмакс*

Максимальный размер выходного буфера в байтах.

*пкбактуал*

Фактический размер закладки в байтах.

Если этот параметр имеет **значение NULL** , фактический размер закладки не будет возвращен.

Если выходной буфер слишком мал, фактический размер закладки все равно будет возвращен. Это означает, что это число будет больше, чем размер выходного буфера.

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
<td><p>Операция успешно завершена, но выходной буфер слишком мал для получения всей закладки. Выходной буфер заполнен объемом заданной закладки. При запросе также возвращается фактический размер закладки.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:  </strong> Эти возвращаемые значения появились в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Курсор не располагается на записи. Это может произойти по различным причинам. Например, это произойдет, если курсор помещается после последней записи текущего индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, закладка для записи, связанной с записью индекса в текущей позиции курсора, будет возвращена в выходной буфер. Изменение состояния базы данных не выполняется.

Если эта функция завершается ошибкой, состояние выходного буфера и фактический размер закладки будут неопределенными, если не была возвращена JET_errBufferTooSmall. В случае, если возвращается JET_errBufferTooSmall, выходной буфер будет содержать столько закладок, сколько будет помещаться в предоставленное пространство, и фактический размер закладки будет неточным. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Закладки обычно должны рассматриваться как непрозрачные фрагменты данных. Для использования внутренней структуры этих данных не нужно предпринимать никаких попыток. Однако для всех закладок ESENT справедливы следующие условия:

  - Закладка однозначно определяет запись в заданной таблице.

  - Закладка записи не изменится в течение времени существования этой записи.

  - Закладка записи совпадает с ключом записи на первичном индексе таблицы, содержащей эту запись. Если в этой таблице не определен первичный индекс, ядро СУБД создаст собственную закладку для записи.

  - Закладки можно сравнить друг с другом с помощью функции [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) , чтобы установить их относительное упорядочение в первичном индексе по таблице исходных записей. Если для этой таблицы не определен первичный индекс, не имеет смысла использовать относительный порядок закладок из этой таблицы.

  - Нет смысла сравнивать закладки записей из разных таблиц друг с другом.

  - Длина закладки всегда меньше или равна JET_cbBookmarkMost (256) байт до Windows Vista.
    
**Windows Vista:** В Windows Vista и более поздних выпусках закладки могут быть больше JET_cbBookmarkMost (256) байт. Максимальный размер закладки равен текущему значению JET_paramKeyMost + 1.

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
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетготобукмарк](./jetgotobookmark-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
