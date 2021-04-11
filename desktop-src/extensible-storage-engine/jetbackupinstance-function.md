---
description: Дополнительные сведения о функции Жетбаккупинстанце
title: Функция JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143540"
---
# <a name="jetbackupinstance-function"></a>Функция JetBackupInstance


_**Применимо к:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>Функция JetBackupInstance

Функция **жетбаккупинстанце** выполняет потоковую архивацию экземпляра, включая все подключенные базы данных, в каталог. При наличии нескольких методов резервного копирования, поддерживаемых ядром, это самая простая и наиболее Инкапсулированная функция.

**Windows XP: жетбаккупинстанце** появился в Windows XP.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр базы данных для резервного копирования.

*сзбаккуппас*

Каталог, в котором хранится резервная копия. Если путь резервного копирования имеет значение NULL для использования функции, по возможности будет усекать журналы.

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
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Создает полную резервную копию базы данных. Это позволяет сохранять существующую резервную копию в том же каталоге в случае сбоя новой резервной копии.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Создает добавочное резервное копирование, а не полное резервное копирование. Это означает, что резервное копирование выполняется только для файлов журнала, созданных с момента последнего полного или добавочного резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Зарезервировано для последующего использования.</p></td>
</tr>
</tbody>
</table>


*пфнстатус*

Указатель на функцию обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , которая предоставляет сведения о ходе выполнения операции резервного копирования.

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
<td><p>Для того же экземпляра уже выполняется резервное копирование. Одновременно не разрешено несколько резервных копий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>Экземпляр еще не готов для резервного копирования при инициализации.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg294108(v=exchg.10).md">жетстопсервицеинстанце</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Операция не может быть завершена, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Добавочное резервное копирование не разрешено, если включено циклическое ведение журнала.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Указаны недопустимые параметры.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>В API передан недопустимый параметр.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Конечный путь не существует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>Экземпляр работает без ведения журнала. Резервное копирование запрещено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Ошибка проверки контрольной суммы файла журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>Ведение журнала для экземпляра является временным или постоянно отключено из-за непредвиденной ошибки.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Ошибка проверки контрольной суммы на странице базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления для экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:  </strong> Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</p></td>
</tr>
</tbody>
</table>


После того как функция вернет значение Success, в каталоге Backup будут присутствовать все файлы, необходимые для восстановления до момента создания резервной копии. Если это полная резервная копия, то файлы будут файлами базы данных и журналами, необходимыми для перевода базы данных в целостное состояние. Если это добавочное резервное копирование, в каталоги будут добавлены только файлы журналов, но уже существующие файлы (базы данных и файлы журнала) вместе с новыми файлами журнала будут восстановлены и возвращены в состояние базы данных в момент создания резервной копии.

В качестве побочного результата резервного копирования файлы журнала, которые больше не нужны, будут обрезаны.

В то же время заголовки базы данных будут обновлены с учетом информации, которая была выполнена при последней архивации.

В случае сбоя в месте назначения каталога резервного копирования не будет файлов, поэтому восстановление будет невозможно. В то же время текущие файлы журнала не будут обрезаны.

#### <a name="remarks"></a>Комментарии

На различных шагах резервного копирования будут созданы записи журнала событий, включая имена файлов, усечение журнала и конечный результат резервного копирования.

Добавочное резервное копирование возможно только после создания полной резервной копии. Кроме того, добавочное резервное копирование возможно только в том случае, если циклическое ведение журнала отключено. Рекомендуется, чтобы каталог резервного копирования не содержал другие файлы, а затем один из них, участвующий в резервной копии или добавленный предыдущей успешной архивацией.

Каталог резервного копирования должен существовать, если для экземпляра не задан параметр *JET_paramCreatePathIfNotExist* . Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md).

Резервная копия выполнит проверку контрольной суммы на всех используемых страницах базы данных и начиная с Windows Server 2003, а также с файлами журналов. Это дает возможность оценить работоспособность базы данных даже для страниц, которые не считываются во время нормальной работы. Если такое повреждение будет обнаружено, произойдет сбой резервного копирования.

Во время резервного копирования текущий файл журнала будет завершен, и будет запущено новое поколение журнала. Это позволит копировать необходимые файлы журналов, так как последний из них больше не будет использоваться.

Настоятельно рекомендуется не использовать резервную копию для других целей, а затем резервное копирование и восстановление на уровне ядра. Это снизит изменение при получении ошибок во время операций резервного копирования и восстановления.

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
<td><p>Реализуется как <strong>жетбаккупинстанцев</strong> (Юникод) и <strong>жетбаккупинстанцеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[жетресторе](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[жетрестореинстанце](./jetrestoreinstance-function.md)  
[жетстопсервицеинстанце](./jetstopserviceinstance-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
