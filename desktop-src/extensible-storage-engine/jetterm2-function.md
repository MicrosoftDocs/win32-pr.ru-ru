---
description: Дополнительные сведения о функции JetTerm2
title: Функция JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154563"
---
# <a name="jetterm2-function"></a>Функция JetTerm2


_**Применимо к:** Windows | Windows Server_

## <a name="jetterm2-function"></a>Функция JetTerm2

Функция **JetTerm2** инициирует завершение работы экземпляра, инициализированного [жетинит](./jetinit-function.md).

**JetTerm2** также может уничтожить неинициализированный экземпляр, созданный [жеткреатеинстанце](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр, используемый для этого вызова.

**Windows 2000:**  Этот параметр пропускается и всегда должен иметь **значение NULL**.

**Windows XP и более поздние версии:**  Этот параметр перегружен. Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь **значение NULL** или содержать фактический экземпляр, возвращаемый функцией [жетинит](./jetinit-function.md). Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть указателем на экземпляр, созданный с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).

*грбит*

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.

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
<td><p>JET_bitTermComplete</p></td>
<td><p>Запрашивает корректное завершение работы экземпляра. Все необязательные операции по очистке, обычно выполняемые в фоновом режиме во время выполнения, выполняются немедленно.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermAbrupt</p></td>
<td><p>Запрашивает как можно быстрее завершить работу экземпляра. Все необязательные операции, которые обычно выполняются в фоновом режиме во время выполнения, прекращаются.</p>
<p><strong>Примечание</strong>  .  Этот параметр может вызвать временную или постоянную потери пространства в базе данных. Это потерянное пространство всегда может быть восстановлено с помощью автономной дефрагментации базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTermStopBackup</p></td>
<td><p>Запрашивает завершение работы экземпляра, даже если в данный момент выполняется резервное копирование. Как правило, отложенная Архивация приведет к сбою <a href="gg269298(v=exchg.10).md">жеттерм</a> с JET_errBackupInProgress. Если этот параметр отсутствует, предполагается, что его значение JET_bitTermAbrupt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermDirty</p></td>
<td><p>Запрашивает завершение работы экземпляра со всеми присоединенными базами данных, оставленными в состоянии «грязных».</p>
<p>Windows 7: JET_bitTermDirty введен в Windows 7.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Операция не может быть завершена, так как в экземпляре выполняется операция резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержал непредвиденное значение, или сочетание нескольких параметров привело к непредвиденному результату. Эта ошибка будет возвращена функцией <a href="gg269298(v=exchg.10).md">жеттерм</a> , когда модуль находится в режиме с несколькими экземплярами и когда <em>пинстанце</em> ссылается на недопустимый экземпляр.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Операция не может быть завершена, так как работа экземпляра завершается.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>Не удается завершить работу экземпляра, так как в настоящий момент имеются сеансы с активными транзакциями для указанного экземпляра. Эта ошибка возникает только в том случае, если используется JET_bitTermComplete.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается, работа указанного экземпляра будет завершена. Кроме того, этот экземпляр будет закрыт и сделан недоступным для любого API, который принимает экземпляр. Все остальные объекты, связанные с экземпляром, например сеансы, также будут закрыты. Состояние файла контрольных точек, файлов журнала транзакций и файлов базы данных, присоединенных к экземпляру, будет изменено в процессе завершения работы.

Если эта функция завершается сбоем в результате ошибки использования, экземпляр остается в инициализированном состоянии и ничего не меняется. В противном случае экземпляр по-прежнему завершает работу, как указано в случае успешного выполнения. Разница заключается в том, что экземпляру потребуется выполнить восстановление после сбоя при следующей инициализации. Ядро попытается очистить как можно больше данных, чтобы максимально увеличить требуемый объем восстановления. По сути, такой сбой [жеттерм](./jetterm-function.md) не отличается от сбоя процесса.

#### <a name="remarks"></a>Комментарии

См. [жеттерм](./jetterm-function.md).

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

[Расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[жетинит](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[жеттерм](./jetterm-function.md)
