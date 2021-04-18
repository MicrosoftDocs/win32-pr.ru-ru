---
description: Дополнительные сведения о функции JetGetLogInfoInstance2
title: Функция JetGetLogInfoInstance2
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693148"
---
# <a name="jetgetloginfoinstance2-function"></a>Функция JetGetLogInfoInstance2


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetloginfoinstance2-function"></a>Функция JetGetLogInfoInstance2

Функция **JetGetLogInfoInstance2** используется во время резервного копирования, инициированного [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) , для запроса экземпляра имен файлов исправления базы данных и файлов журнала транзакций, которые должны стать частью набора файлов резервной копии. Эти файлы впоследствии можно открыть с помощью [жетопенфиле](./jetopenfile-function.md) и прочитать с помощью [жетреадфиле](./jetreadfile-function.md).

**Windows XP: JetGetLogInfoInstance2** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр, используемый для этого вызова.

Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр. В этом случае подразумевается использование этого одного глобального экземпляра.

Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр. В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.

*сзз*

Выходной буфер, который получит список строк, заканчивающихся нулем, описывающих набор файлов исправления базы данных и файлов журнала транзакций, которые должны быть частью набора файлов резервной копии.

Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром. Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.

*кбмакс*

Максимальный размер выходного буфера в байтах.

*пкбактуал*

Получает фактический объем строковых данных, полученных в выходном буфере.

*плогинфо*

Получает структурированные сведения о файлах журнала транзакций, которые должны быть частью набора файлов резервной копии.

Если этот параметр отсутствует, предполагается, что его значение равно NULL.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности. <a href="gg294055(v=exchg.10).md">Жетжетлогинфо</a> возвращает эту ошибку, если в экземпляре имеются необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <a href="gg294055(v=exchg.10).md">жетжетлогинфо</a> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Не удалось выполнить операцию, так как не выполняется внешняя архивация.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Операция завершилась с ошибкой, так как была предпринята попытка использовать модуль в устаревшем режиме (режим совместимости Windows 2000), где только один экземпляр поддерживается, если в действительности несколько экземпляров уже существуют.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении запрошенные сведения о наборе файлов исправления базы данных и журналов транзакций, которые должны быть частью набора файлов резервной копии, помещаются в выходные буферы там, где они предоставлены. Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается. Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за пределами этой точки.

В случае сбоя состояние выходных буферов не определено. Сбой приведет к отмене всего процесса резервного копирования для экземпляра.

#### <a name="remarks"></a>Комментарии

Важно отметить, что этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии. Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
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
<td><p>Реализуется как <strong>JetGetLogInfoInstance2W</strong> (Юникод) и <strong>JetGetLogInfoInstance2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)  
[жетопенфиле](./jetopenfile-function.md)  
[жетреадфиле](./jetreadfile-function.md)  
[жетстопбаккуп](./jetstopbackup-function.md)
