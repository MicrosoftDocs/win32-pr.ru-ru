---
description: Дополнительные сведения о функции Жетжеттрункателогинфоинстанце
title: Функция Жетжеттрункателогинфоинстанце
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703092"
---
# <a name="jetgettruncateloginfoinstance-function"></a>Функция Жетжеттрункателогинфоинстанце


_**Применимо к:** Windows | Windows Server_

## <a name="jetgettruncateloginfoinstance-function"></a>Функция Жетжеттрункателогинфоинстанце

Функция **жетжеттрункателогинфоинстанце** используется во время резервного копирования, которое инициируется [жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md) для запроса экземпляров имен файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования.

**Windows XP:**  **Жетжеттрункателогинфоинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр, используемый для этого вызова.

*сзз*

Выходной буфер, который получает список строк, заканчивающихся нулем, описывающих набор файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования.

Список строк, возвращаемых в этом буфере, имеет тот же формат, что и многострочная, используемая реестром. Каждая строка, завершающаяся нулем, возвращается в последовательности, за которой следует завершающий завершающий символ null.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержал непредвиденное значение или сочетание нескольких значений параметров привело к непредвиденному результату.</p>
<p><strong>Windows XP и более поздние версии:</strong>  Это может произойти для <strong>жетжеттрункателогинфоинстанце</strong> , если указанный экземпляр является недопустимым.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение было введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Не удалось выполнить операцию, так как текущая Внешняя резервная копия была прервана вызовом <a href="gg294067(v=exchg.10).md">жетстопбаккуп</a>.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение было введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Не удалось выполнить операцию резервного копирования, так как она была вызвана вне последовательности.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>Не удалось выполнить операцию, так как не выполняется внешняя архивация.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>жетжеттрункателогинфоинстанце</strong></p></td>
<td><p>Существуют необработанные дескрипторы файлов, созданные с помощью <a href="gg269249(v=exchg.10).md">жетопенфиле</a> для экземпляра.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается успешно, запрашиваемые сведения о наборе файлов журнала транзакций, которые можно безопасно удалить после успешного завершения резервного копирования, помещаются в выходные буферы, где они указаны. Конечный автомат резервного копирования будет дополнительно таким, что резервная копия файлов базы данных больше не разрешается. Только файлы исправления базы данных и файлы журнала транзакций могут быть открыты для резервного копирования за этот момент.

Если эта функция завершается ошибкой, состояние буферов вывода не определено. Сбой приведет к отмене всего процесса резервного копирования для экземпляра.

#### <a name="remarks"></a>Комментарии

Этот API не возвращает ошибку или предупреждение, если выходной буфер слишком мал, чтобы принять полный список файлов, которые должны быть частью набора файлов резервной копии. Приложение всегда должно предоставлять буфер для получения фактического размера этого списка и использовать эти сведения для определения усечения списка.

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
<td><p>Реализуется как <strong>жетжеттрункателогинфоинстанцев</strong> (Юникод) и <strong>жетжеттрункателогинфоинстанцеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетбегинекстерналбаккуп](./jetbeginexternalbackup-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетендсессион](./jetendsession-function.md)  
[жетопенфиле](./jetopenfile-function.md)  
[жетресетсессионконтекст](./jetresetsessioncontext-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетстопбаккуп](./jetstopbackup-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[жеттерм](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
