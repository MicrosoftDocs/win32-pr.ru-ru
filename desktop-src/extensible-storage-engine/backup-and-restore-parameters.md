---
description: 'Дополнительные сведения: параметры резервного копирования и восстановления'
title: Параметры резервного копирования и восстановления
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546847"
---
# <a name="backup-and-restore-parameters"></a>Параметры резервного копирования и восстановления


_**Применимо к:** Windows | Windows Server_

## <a name="backup-and-restore-parameters"></a>Параметры резервного копирования и восстановления

Этот раздел содержит параметры, используемые для резервного копирования и восстановления.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Полный путь к каждой базе данных сохраняется в журналах транзакций во время выполнения. Обычно эти базы данных должны оставаться в исходном расположении для правильной работы воспроизведения транзакций. Этот параметр можно использовать для принудительного восстановления после сбоя или операции восстановления, чтобы найти базы данных, упоминаемые в журнале транзакций в указанной папке.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Путь к папке (строка)</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 – 246 символов</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramCleanupMismatchedLogFiles*  
77  

Этот параметр управляет результатом [жетинит](./jetinit-function.md) , когда ядро СУБД настроено для начала использования файлов журнала транзакций на диске, размер которых отличается от настроенного. Обычно [жетинит](./jetinit-function.md) успешно восстановит базы данных, но завершится сбоем с JET_errLogFileSizeMismatchDatabasesConsistent, чтобы указать, что размер файла журнала настроен неправильно. Однако если этот параметр имеет значение true, то ядро СУБД автоматически удалит все старые файлы журналов, запустит новый набор файлов журнала транзакций, используя настроенный размер файла журнала, и возвратит JET_errSuccess.

Этот параметр полезен, когда приложению требуется прозрачно изменить размер файла журнала транзакций, но все равно работать прозрачно в сценариях обновления и восстановления.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Неверно</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Логическое</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>False, true</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOutOfRangeLogs*  
52  

Если этот параметр имеет значение true, то все файлы журнала транзакций, находящиеся на диске, не являющиеся частью текущей последовательности файлов журнала, будут удалены с помощью [жетинит](./jetinit-function.md). Это может использоваться для автоматической очистки лишних файлов журнала после операции восстановления.

**Windows XP:**  Впервые появился в Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Неверно</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Логическое</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>False, true</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramOSSnapshotTimeout*  
82  

Этот параметр позволяет настроить период времени между вызовом [жетосснапшотфризе](./jetossnapshotfreeze-function.md) и [жетосснапшотсав](./jetossnapshotthaw-function.md) до наступления времени ожидания. Дополнительные сведения см. в разделе [жетосснапшотфризе](./jetossnapshotfreeze-function.md) и [жетосснапшотсав](./jetossnapshotthaw-function.md) . Время ожидания задается в миллисекундах.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>20000 (Windows XP и Windows Server 2003);</p>
<p>70000 (пакет обновления 1 (SP1) для Windows Server 2003)</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramZeroDatabaseDuringBackup*  
71  

Если этот параметр имеет значение true, то каждая страница в базе данных, для которой выполняется потоковая архивация, будет очищена от удаленных данных. Важно отметить, что страницы базы данных, для которых выполняется очистка, находятся на диске. Перед процессом очистки создается резервная копия полного набора данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Неверно</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Логическое</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>False, true</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздние версии</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Требования

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
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
