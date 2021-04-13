---
description: Дополнительные сведения о функции Жетосснапшотфризе
title: Функция JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265714"
---
# <a name="jetossnapshotfreeze-function"></a>Функция JetOSSnapshotFreeze


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>Функция JetOSSnapshotFreeze

Функция **жетосснапшотфризе** запускает моментальный снимок. Во время выполнения моментального снимка подсистема не может выполнить действия записи на диск.

**Windows XP:**  **Жетосснапшотфризе** появился в Windows XP.

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*пЦинстанцеинфо*

Число экземпляров, выполняемых в данный момент в ядре, которые являются частью сеанса моментальных снимков.

*паинстанцеинфо*

Массив структур, по одному для каждого работающего экземпляра, который является частью сеанса моментального снимка, описывающий экземпляр и базы данных, которые являются его частью.

*грбит*

Параметры для этого вызова. Этот параметр зарезервирован для будущего использования, и поддерживается только допустимое значение 0.

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
<td><p>Указатели, предоставленные для выходных параметров, имеют значение NULL, сеанс моментального снимка недопустим, или параметр <em>грбит</em> является недопустимым.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Сеанс моментального снимка находится в неправильном состоянии, чтобы начать замораживание (например, если предыдущая фиксация не удалась в этом сеансе).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>Обработчик не находится в состоянии, в котором можно выполнить моментальный снимок. Уже выполняется одно или несколько резервных копий потоковой передачи, либо один или несколько экземпляров проходят через этапы восстановления или завершаются.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Недопустимый идентификатор сеанса моментального снимка.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Ошибка при выполнении функции из-за нехватки памяти.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>Не удалось выполнить функцию, так как не удалось запустить новый поток, выполняющий замораживание.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершится с ошибкой, то для файлов базы данных или файлов журнала, которые являются частью замороженных экземпляров, не будет выдана запись IOs. Кроме того, сведения об экземпляре будут заполнены должным образом и должны быть освобождены позже путем вызова [жетфрибуффер](./jetfreebuffer-function.md) с указателем на возвращаемый массив сведений об экземпляре.

Если эта функция завершается с ошибкой, ядро продолжает работать нормально с IOs, как обычно. Нет необходимости вызывать [жетосснапшотсав](./jetossnapshotthaw-function.md) в случае сбоя Freeze. Кроме того, сведения об экземпляре не будут заполнены, поэтому освободить этот ресурс не нужно.

#### <a name="remarks"></a>Комментарии

В течение периода закрепления не будет никаких операций записи IOs, выданных подключенным базам данных или журналам транзакций, несмотря на то, что для временных баз данных или потоковых файлов может быть выдана операция ввода/вывода.

Состояние, в котором базы данных и файлы журналов будут находиться во время замораживания (состояние, в котором файлы будут находиться в образе моментального снимка тома), будет иметь возможность нормального восстановления, если эти файлы будут восстановлены позже.

Так как в течение периода замораживания нет операций записи, обычно вызовы API в механизме могут быть остановлены для этого интервала. Клиентское приложение должно иметь возможность обрабатывать вызовы API, которые могут занимать больше времени, если происходит зависание.

Из-за возможных эффектов, описанных выше, существует внутреннее время ожидания, по истечении которого сеанс моментальных снимков останавливает фазу замораживания даже в том случае, если не были вызваны API, выполняющие разморозку или прерывание. Значение времени ожидания можно изменить с помощью параметра системы [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) . Обратите внимание, что стандартный интервал замораживания находится в диапазоне 10 секунд, а время ожидания по умолчанию — около 60 секунд.

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
<td><p>Реализуется как <strong>жетосснапшотфризев</strong> (Юникод) и <strong>жетосснапшотфризеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[жетосснапшотаборт](./jetossnapshotabort-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
