---
description: Дополнительные сведения о функции Жетендекстерналбаккуп
title: Функция JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703341"
---
# <a name="jetendexternalbackup-function"></a>Функция JetEndExternalBackup


_**Применимо к:** Windows | Windows Server_

## <a name="jetendexternalbackup-function"></a>Функция JetEndExternalBackup

Функция **жетендекстерналбаккуп** завершает внешний сеанс резервного копирования. Эта функция является последним элементом API в серии элементов API, которые необходимо вызвать для выполнения успешной резервной копии (на основе не VSS).

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a>Параметры

У этой функции нет параметров.

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
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP</p>
<p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, для которой необходимо отозвать доступ ко всем данным, чтобы защитить целостность этих данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Не удалось выполнить операцию, так как не выполняется внешняя архивация.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003:  </strong> Это возвращаемое значение представлено в Windows Server 2003.</p>
<p>Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</p></td>
</tr>
<tr class="odd">
<td><p>еррбаккупабортбикаллер</p></td>
<td><p><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</p>
<p>Вызывающий объект прервал резервную копию в середине последовательности резервного копирования, не указывая намерения <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>. Эта ошибка возникает в результате ошибки в клиенте резервного копирования в Windows Server 2003 и более поздних версиях. В Windows XP эта ошибка возвращается для преднамеренного завершения внешней последовательности резервного копирования.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, когда в действительности несколько экземпляров уже существуют.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается успешно, Внешняя резервная копия была успешно выполнена. Успешное завершение означает, что все файлы (например, базы данных и журналы), подходящие для типа резервной копии (указанной в [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)), были получены из модуля резервного копирования. Резервные копии файлов можно восстановить с помощью жесткого восстановления ([жетекстерналресторе](./jetexternalrestore-function.md)).

В случае сбоя этой функции внешнее резервное копирование обычно завершается. Сбой означает, что резервная копия является недопустимой из-за ошибки использования клиента или приложения. Важно проверить код возврата для этого API, чтобы убедиться, что последовательность резервного копирования прошла успешно.

#### <a name="remarks"></a>Комментарии

Если для модуля настроено ведение журнала событий, в журнал заносится событие, указывающее на разрешение внешней резервной копии.

Если последовательность резервного копирования не завершена по порядку и при успешном вызове **жетендекстерналбаккуп**, последующие добавочные резервные копии могут содержать больше данных, чем ожидалось приложением.

Дополнительные сведения о последовательности API внешней резервной копии см. в разделе [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md).

До Windows Vista, если усечение журнала не выполнялось, подсистема считалась резервной копией копии. Однако резервное копирование может быть обычной резервной копией, для которой не выполнялось усечение (например, при наличии отсоединенных баз данных). Параметр JET_bitBackupTruncateDone можно использовать для информирования ядра об этом и предоставления соответствующих изменений заголовка базы данных.

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

[Параметры обработки ошибок](./error-handling-parameters.md)  
[Ошибки расширяемого подсистемы хранилища](./extensible-storage-engine-errors.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)  
[жетклосефиле](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[жетекстерналресторе](./jetexternalrestore-function.md)  
[жетжетаттачинфо](./jetgetattachinfo-function.md)  
[жетжетлогинфо](./jetgetloginfo-function.md)  
[жетопенфиле](./jetopenfile-function.md)  
[жетреадфиле](./jetreadfile-function.md)  
[жетстопбаккуп](./jetstopbackup-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[жеттрункателог](./jettruncatelog-function.md)
