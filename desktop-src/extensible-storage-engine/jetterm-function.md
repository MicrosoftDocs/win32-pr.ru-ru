---
description: Дополнительные сведения о функции Жеттерм
title: Функция JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692200"
---
# <a name="jetterm-function"></a>Функция JetTerm


_**Применимо к:** Windows | Windows Server_

## <a name="jetterm-function"></a>Функция JetTerm

Функция **жеттерм** инициирует завершение работы экземпляра, инициализированного [жетинит](./jetinit-function.md).

**Жеттерм** также можно использовать для уничтожения неинициализированного экземпляра, созданного с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Указывает экземпляр, используемый для этого вызова.

**Windows 2000:**  Этот параметр пропускается и всегда должен иметь **значение NULL**.

**Windows XP и более поздние версии:**  Этот параметр перегружен. Если ядро работает в устаревшем режиме (режим совместимости Windows 2000), где поддерживается только один экземпляр, этот параметр может иметь **значение NULL** или содержать фактический экземпляр, возвращаемый функцией [жетинит](./jetinit-function.md). Если ядро работает в режиме с несколькими экземплярами, этот параметр должен быть указателем на экземпляр, созданный с помощью [жеткреатеинстанце](./jetcreateinstance-function.md).

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
<td><p>Один из указанных параметров содержал непредвиденное значение, или сочетание нескольких параметров привело к непредвиденному результату. Эта ошибка будет возвращена функцией <strong>жеттерм</strong> , когда модуль находится в режиме с несколькими экземплярами и когда <em>пинстанце</em> ссылается на недопустимый экземпляр.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Операция не может быть завершена, так как работа экземпляра завершается.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>Операция не может быть завершена, так как в экземпляре выполняется операция резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>Не удается завершить работу экземпляра, так как в настоящий момент имеются сеансы с активными транзакциями для указанного экземпляра. Эта ошибка возникает только в том случае, если используется JET_bitTermComplete.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается, работа указанного экземпляра будет завершена. Кроме того, этот экземпляр будет закрыт и сделан недоступным для любого API, который принимает экземпляр. Все остальные объекты, связанные с экземпляром, например сеансы, также будут закрыты. Состояние файла контрольных точек, файлов журнала транзакций и файлов базы данных, присоединенных к экземпляру, будет изменено в процессе завершения работы.

Если эта функция завершается ошибкой в результате ошибки использования, экземпляр остается в инициализированном состоянии и ничего не меняется. В противном случае экземпляр по-прежнему завершает работу, как в случае успешного выполнения. Разница заключается в том, что экземпляру потребуется выполнить восстановление после сбоя при следующей инициализации. Ядро попытается очистить как можно больше данных, чтобы максимально увеличить требуемый объем восстановления. По сути, такой сбой **жеттерм** не отличается от сбоя процесса.

#### <a name="remarks"></a>Комментарии

Если ведущий процесс экземпляра завершается по какой-либо причине, прежде чем **жеттерм** успешно вызывается для этого экземпляра, считается, что экземпляр находится в состоянии сбоя. Восстановление после сбоя произойдет при следующей попытке инициализации этого экземпляра.

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
[JetTerm2](./jetterm2-function.md)
