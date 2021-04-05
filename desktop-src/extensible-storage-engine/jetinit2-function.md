---
description: Дополнительные сведения о функции JetInit2
title: Функция JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000548"
---
# <a name="jetinit2-function"></a>Функция JetInit2


_**Применимо к:** Windows | Windows Server_

## <a name="jetinit2-function"></a>Функция JetInit2

Функция **JetInit2** помещает ядро СУБД в состояние, где оно может поддерживать использование файлов базы данных приложением. Подсистема уже должна быть правильно настроена для инициализации с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md). Восстановление после сбоя базы данных выполняется автоматически в рамках процесса инициализации.

**Windows XP:**  **JetInit2** появился в Windows XP.

Эта функция является устаревшей. Вместо этого используйте [JetInit3](./jetinit3-function.md) .

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Параметры

*пинстанце*

Экземпляр, используемый для этого вызова.

Для Windows 2000 этот параметр игнорируется и всегда должен иметь значение NULL.

Для Windows XP и более поздних версий использование этого параметра зависит от режима работы ядра. Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь значение NULL или быть установлен в допустимый выходной буфер, содержащий NULL или JET_instanceNil, который возвращает глобальный экземпляр, созданный в качестве побочного результата инициализации. Этот экземпляр можно передать в любой другой API, который принимает экземпляр. Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть установлен в допустимый входной буфер, содержащий экземпляр, возвращенный [жеткреатеинстанце](./jetcreateinstance-function.md) , который инициализируется.

*грбит*

Группа битов, задающая ноль или более следующих параметров.

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
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Зарезервировано для последующего использования.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Зарезервировано для последующего использования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Этот параметр позволяет пользователю выполнять восстановление на наборе файлов журнала без всех существующих баз данных, подключенных к одной точке набора журналов.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Выполните восстановление, но остановите на этапе отката. Это позволяет копировать и применять дополнительные журналы транзакций.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>При успешном обратимом восстановлении усечение файлов журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Отсутствует запись схемы базы данных по умолчанию в то же расположение.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Игнорировать журналы, потерянные с конца потока журнала.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> введен в Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).


#### <a name="remarks"></a>Комментарии

Экземпляр должен быть инициализирован с помощью вызова **JetInit2** , прежде чем он сможет использоваться любым другим, кроме [жетсетсистемпараметер](./jetsetsystemparameter-function.md).

Экземпляр уничтожается вызовом функции [жеттерм](./jetterm-function.md) , даже если этот экземпляр никогда не был инициализирован с помощью [жетинит](./jetinit-function.md). Экземпляр — это единица восстановления для ядра СУБД. Он управляет жизненным циклом всех файлов, используемых для защиты целостности данных в наборе файлов базы данных. Эти файлы включают файл контрольных точек и файлы журнала транзакций.

Если восстановление выполняется на наборе журналов, для которых не все базы данных (возвращающие ошибку JET_errAttachedDatabaseMismatch при нормальных обстоятельствах), и клиент хочет, чтобы продолжение восстановления, несмотря на отсутствие баз данных, JET_ Битреплайигноремиссингдб используется для продолжения восстановления доступных баз данных.

Дополнительные сведения см. в разделе "Примечания" в [жетинит](./jetinit-function.md) .

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
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[Расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Параметры ресурсов](./resource-parameters.md)
