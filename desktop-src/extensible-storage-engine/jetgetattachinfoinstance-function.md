---
description: Дополнительные сведения о функции Жетжетаттачинфоинстанце
title: Функция Жетжетаттачинфоинстанце
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910244"
---
# <a name="jetgetattachinfoinstance-function"></a>Функция Жетжетаттачинфоинстанце


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetattachinfoinstance-function"></a>Функция Жетжетаттачинфоинстанце

Функция **жетжетаттачинфоинстанце** используется во время резервного копирования, инициированного [жетбегинекстерналбаккупинстанце](./jetbeginexternalbackupinstance-function.md) , чтобы запросить экземпляр для имен файлов базы данных, которые должны стать частью набора файлов резервной копии. Будут рассматриваться только те базы данных, которые в данный момент подключены к экземпляру с помощью [жетаттачдатабасе](./jetattachdatabase-function.md) . Эти файлы впоследствии можно открыть с помощью [жетопенфилеинстанце](./jetopenfileinstance-function.md) и прочитать с помощью [жетреадфилеинстанце](./jetreadfileinstance-function.md).

**Windows XP: жетжетаттачинфоинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр, используемый для этого вызова.

Для Windows 2000 вариант API, который принимает этот параметр, недоступен, так как поддерживается только один экземпляр. В этом случае подразумевается использование этого одного глобального экземпляра.

Для Windows XP и более поздних версий вариант API, который не принимает этот параметр, может вызываться только в том случае, если ядро находится в режиме совместимости с Windows 2000, где поддерживается только один экземпляр. В противном случае операция завершится ошибкой с JET_errRunningInMultiInstanceMode.

*сзз*

Выходной буфер, который получает список строк, заканчивающихся нулем, описывающих набор файлов базы данных, который должен быть частью набора файлов резервной копии. Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром. Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.

*кбмакс*

Максимальный размер выходного буфера в байтах.

*пкбактуал*

Указатель на выходной буфер, который получает фактический объем строковых данных.

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
<td><p>Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg269309(v=exchg.10).md">жетстопбаккупинстанце</a>. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg294108(v=exchg.10).md">жетстопсервицеинстанце</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности. <strong>Жетжетаттачинфоинстанце</strong> возвращает эту ошибку, если текущая резервная копия не является полной резервной копией.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жетжетаттачинфоинстанце</strong> , если указан недопустимый дескриптор экземпляра (Windows XP и более поздние версии).</p></td>
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


При успешном выполнении запрошенные сведения о наборе файлов базы данных, которые должны быть частью набора файлов резервной копии, будут помещены в выходные буферы там, где они предоставлены.

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
<td><p>Реализуется как <strong>жетжетаттачинфоинстанцев</strong> (Юникод) и <strong>жетжетаттачинфоинстанцеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[жетбегинекстерналбаккупинстанце](./jetbeginexternalbackupinstance-function.md)  
[жетопенфилеинстанце](./jetopenfileinstance-function.md)  
[жетреадфилеинстанце](./jetreadfileinstance-function.md)  
[жетстопбаккупинстанце](./jetstopbackupinstance-function.md)  
[жетстопсервицеинстанце](./jetstopserviceinstance-function.md)
