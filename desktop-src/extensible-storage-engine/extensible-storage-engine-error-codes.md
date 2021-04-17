---
description: 'Дополнительные сведения: коды ошибок расширенного подсистемы хранилища'
title: Коды ошибок расширенного подсистемы хранилища
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712739"
---
# <a name="extensible-storage-engine-error-codes"></a>Коды ошибок расширенного подсистемы хранилища


_**Применимо к:** Windows | Windows Server_

## <a name="extensible-storage-engine-error-codes"></a>Коды ошибок расширенного подсистемы хранилища

Следующие коды ошибок (flags) используются функциями в API-интерфейсе расширяемого механизма хранилища.

Значение [JET_ERR](./jet-err.md) , равное нулю, должно интерпретироваться как Success.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Успешно</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>Функция выполнена успешно.</p></td>
</tr>
</tbody>
</table>


Значение [JET_ERR](./jet-err.md) , большее нуля, должно интерпретироваться как предупреждение.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Предупреждения</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>Хранилище версий все еще активно. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>Поиск в неуникальном индексе подает уникальный ключ. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>Столбец базы данных имеет разделенное длинное значение. Эта ошибка возвращается диспетчером записей.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>Существующий файл журнала имеет неправильную подпись.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>Существующий файл журнала не является смежным.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>Эта ошибка относится только к внутреннему использованию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>TargetInstance, указанный для восстановления, работает.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>Повреждение базы данных восстановлено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>Столбец имеет значение <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>Буфер слишком мал для данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>База данных уже присоединена.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>Для выполнения сортировки не хватает памяти.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>Точное совпадение не найдено во время поиска.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Точное совпадение не найдено во время поиска. Эта ошибка возвращается диспетчером записей.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Точное совпадение не найдено во время поиска. Эта ошибка возвращается диспетчером записей.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1055</p></td>
<td><p>Расширенные сведения об ошибках отсутствуют.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>Неактивное действие не выполнено.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067.</p></td>
<td><p>Отсутствует блокировка записи на уровне транзакций 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>Для столбца задается значение <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>Была открыта пустая таблица.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>Для очистки системы в таблице открыт курсор.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>Неактуальный индекс должен быть удален.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>Максимальная длина слишком велика и была усечена.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>Значение большого двоичного объекта было перемещено из записи в отдельное хранилище больших двоичных объектов.</p>
<p><strong>Примечание</strong> . Эта ошибка относится только к внутреннему использованию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>Значения столбца не были возвращены, так как соответствующий идентификатор столбца или элемент <em>итагсекуенце</em> из структуры <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> , запрошенной для перечисления, имел значение null.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>Значения столбца не были возвращены, так как их не удалось перестроить из существующих данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>Существующие значения столбца не были запрошены для перечисления.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>Значение столбца было усечено по запрошенному пределу размера во время перечисления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>Значения столбца существуют, но не возвращены запросом.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>Значение столбца было возвращено в JET_COLUMNENUM в результате задания JET_bitEnumerateCompressOutput.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>Значение столбца устанавливается в значение по умолчанию для столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>Данные были изменены.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>Используется новый ключ.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>Файл базы данных доступен только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>Неактивный реестр заполнен.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>В указанной базе данных уже запущена оперативная дефрагментация.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>В указанной базе данных не запущена оперативная дефрагментация.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2100</p></td>
<td><p>Регистрация несуществующей функции обратного вызова отменена.</p></td>
</tr>
</tbody>
</table>


Значение [JET_ERR](./jet-err.md) , меньшее нуля, должно интерпретироваться как ошибка.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ошибки</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>Функция еще не реализована.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
–100</p></td>
<td><p>Не удалось выполнить симулятор сбоя ресурса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
–101</p></td>
<td><p>Симулятор сбоя ресурса не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
–102</p></td>
<td><p>Не удалось закрыть файл.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>Не удалось запустить поток.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>Система занята из-за слишком большого количества IOs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>Не удалось выполнить запрошенную асинхронную задачу.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>Произошла неустранимая внутренняя ошибка.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
— 255</p></td>
<td><p>Неправильно заданы зависимости буфера, и произошла ошибка восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
— 322</p></td>
<td><p>Версия уже существовала, и произошла ошибка восстановления. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
— 323</p></td>
<td><p>Достигнута граница страницы. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
— 324</p></td>
<td><p>Достигнута граница ключа. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
— 327</p></td>
<td><p>База данных повреждена. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
— 328</p></td>
<td><p>Закладка не имеет соответствующего адреса в базе данных. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
— 334</p></td>
<td><p>Сбой вызова операционной системы. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
— 338</p></td>
<td><p>Родительская база данных повреждена. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
— 340</p></td>
<td><p>Кэш Аваилекст не соответствует дереву B +. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
— 341</p></td>
<td><p>Дерево пространства Аллаваилекст повреждено. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
— 342</p></td>
<td><p>Произошла ошибка нехватки памяти при выделении узла кэша Аваилекст. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
— 343</p></td>
<td><p>Дерево пространства Овнекст повреждено. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
— 344</p></td>
<td><p>Дбтиме на текущей странице больше, чем глобальная база данных дбтиме. Эта ошибка возвращается диспетчером каталогов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
— 346</p></td>
<td><p>Попытка создать ключ для элемента индекса завершилась неудачей, так как ключ был усечен, а определение индекса не разрешает усечение ключа.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
— 408</p></td>
<td><p>Слишком большой ключ. Эта ошибка возвращается диспетчером записей.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>Не удается выполнить запротоколированную операцию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
— 501</p></td>
<td><p>Файл журнала поврежден.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
— 503</p></td>
<td><p>Не указан каталог резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
— 504</p></td>
<td><p>Каталог резервного копирования не пуст.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
— 505</p></td>
<td><p>Резервная копия уже активна.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
— 506</p></td>
<td><p>Выполняется восстановление.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
— 509</p></td>
<td><p>Отсутствует файл журнала для контрольной точки.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
— 510</p></td>
<td><p>Ошибка записи в файл журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
— 511</p></td>
<td><p>Попытка записи в журнал после сбоя восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
— 512</p></td>
<td><p>Попытка записи в журнал во время повтора восстановления завершилась сбоем.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
— 513</p></td>
<td><p>Имя файла журнала не соответствует номеру внутреннего поколения.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
— 514</p></td>
<td><p>Версия файла журнала несовместима с версией ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
— 515</p></td>
<td><p>Метка времени в следующем журнале не соответствует ожидаемой метке времени.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
— 516</p></td>
<td><p>Журнал неактивен.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
— 517</p></td>
<td><p>Буфер журнала слишком мал для восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
— 519</p></td>
<td><p>Превышен максимальный номер файла журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
— 520</p></td>
<td><p>Резервное копирование не выполняется.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
— 521</p></td>
<td><p>Вызов резервного копирования не является последовательным.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
— 523</p></td>
<td><p>В настоящее время невозможно выполнить резервное копирование.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
— 524</p></td>
<td><p>Не удалось удалить файл резервной копии.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
— 525</p></td>
<td><p>Не удалось создать временный каталог резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
— 526</p></td>
<td><p>Циклическое ведение журнала включено; невозможно выполнить добавочное резервное копирование.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
— 527</p></td>
<td><p>Данные были восстановлены с ошибками.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
— 528</p></td>
<td><p>Текущий файл журнала отсутствует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
— 529</p></td>
<td><p>Диск журнала заполнен.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
— 530</p></td>
<td><p>Неверная подпись для файла журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
— 531</p></td>
<td><p>Неверная подпись для файла базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
— 532</p></td>
<td><p>Неверное описание файла контрольных точек.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
— 533</p></td>
<td><p>Файл контрольных точек не найден или поврежден.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
— 534</p></td>
<td><p>Страница файла исправления базы данных не найдена во время восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
— 535</p></td>
<td><p>Недопустимая страница файла исправления базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
— 536</p></td>
<td><p>Непредвиденное завершение операции повтора из-за внезапного сбоя при чтении журналов из файла журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
— 537</p></td>
<td><p>Этот флаг зарезервирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
— 538</p></td>
<td><p>При сложном восстановлении обнаружено, что в резервном наборе данных отсутствует файл исправления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
— 539</p></td>
<td><p>База данных не принадлежит текущему набору файлов журнала.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
— 540</p></td>
<td><p>Этот флаг зарезервирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
— 541</p></td>
<td><p>Фактический размер файла журнала не совпадает с <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
— 542</p></td>
<td><p>Не удалось найти файл контрольных точек.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
— 543</p></td>
<td><p>Отсутствуют необходимые файлы журнала для восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
— 544</p></td>
<td><p>Мягкое восстановление будет использоваться в базе данных резервного копирования, когда вместо этого следует использовать восстановление.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
— 545</p></td>
<td><p>Базы данных восстановлены, но размер файла журнала, используемый во время восстановления, не соответствует <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
— 546</p></td>
<td><p>Размер сектора файла журнала не совпадает с размером сектора текущего тома.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
— 547</p></td>
<td><p>Базы данных восстановлены, но размер сектора файла журнала (используемый во время восстановления) не совпадает с размером сектора текущего тома.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
— 548</p></td>
<td><p>Базы данных восстановлены, но использовались все возможные поколения журналов в текущей последовательности. Перед продолжением необходимо удалить все файлы журналов и файл контрольных точек, а также создать резервные копии баз данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
— 549</p></td>
<td><p>Недопустимая попытка воспроизвести операцию потокового файла, в которой данные не были занесены в журнал. Возможно, это вызвано попыткой Накату с включением циклического ведения журнала.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
— 550</p></td>
<td><p>Работа базы данных не была завершена аккуратно. Сначала необходимо выполнить восстановление, чтобы правильно завершить операции с базой данных для предыдущего завершения работы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>Эта ошибка устарела и была заменена JET_errDatabaseDirtyShutdown.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
— 551</p></td>
<td><p>Последнее согласованное время для базы данных не сопоставлено.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
— 552</p></td>
<td><p>Файл исправления базы данных не создается из этой резервной копии.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
— 553</p></td>
<td><p>Начальный номер журнала слишком мал для восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
— 554</p></td>
<td><p>Начальный номер журнала слишком велик для восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
— 555</p></td>
<td><p>Файл журнала восстановления имеет неправильную подпись.</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
— 556</p></td>
<td><p>Файл журнала восстановления не является смежным.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
— 557</p></td>
<td><p>Отсутствуют некоторые файлы журнала восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
— 560</p></td>
<td><p>Перед попыткой выполнить добавочное резервное копирование база данных пропустила предыдущую полную резервную копию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
— 561</p></td>
<td><p>Размер базы данных резервного копирования не кратен размеру страницы базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
— 562</p></td>
<td><p>Текущая попытка обновить базу данных остановлена, так как база данных уже является текущей.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
— 563</p></td>
<td><p>База данных была частично преобразована в текущий формат. База данных должна быть восстановлена из резервной копии.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
— 565</p></td>
<td><p>Некоторые текущие файлы журнала отсутствуют для непрерывного восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
— 566</p></td>
<td><p>Дбтиме на странице меньше, чем Дбтимебефоре в записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
— 567</p></td>
<td><p>Дбтиме на странице предварительно находится в Дбтимебефоре, который находится в записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
— 569</p></td>
<td><p>Некоторые файлы журнала или исправления базы данных отсутствовали во время резервного копирования.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
— 570</p></td>
<td><p>В резервной копии, заданной во время жесткого восстановления, обнаружена разорванная запись.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
— 571</p></td>
<td><p>Обнаружена разорванная запись во время жесткого восстановления (журнал не был частью резервного набора данных).</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
— 573</p></td>
<td><p>Во время жесткого восстановления обнаружено повреждение в резервном наборе данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
— 574</p></td>
<td><p>Во время жесткого восстановления обнаружено повреждение (журнал не был частью резервного набора данных).</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
— 575</p></td>
<td><p>Ведение журнала невозможно включить при попытке обновления базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
— 577</p></td>
<td><p>Либо TargetInstance, который был указан для восстановления, не найден, либо файлы журнала не совпадают.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
— 579</p></td>
<td><p>Ядро СУБД успешно воспроизводило все операции в журнале транзакций, чтобы выполнить восстановление после сбоя, но вызывающий объект, выбранный для отмены восстановления без отката незафиксированных обновлений.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
— 580</p></td>
<td><p>Восстанавливаемые базы данных не относятся к одной резервной копии теневого копирования.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
— 581</p></td>
<td><p>Существует мягкое восстановление базы данных из резервного набора данных теневого копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
— 601</p></td>
<td><p>Буфер преобразования Юникода слишком мал.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
— 602</p></td>
<td><p>Сбой нормализации Юникода.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
— 603</p></td>
<td><p>Операционная система не поддерживает нормализацию Юникода, и обратный вызов нормализации не был указан.</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
— 610</p></td>
<td><p>Существующий файл журнала имеет неправильную подпись.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
— 611</p></td>
<td><p>Существующий файл журнала не является смежным.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
— 612</p></td>
<td><p>В файле журнала во время резервного копирования обнаружена ошибка контрольной суммы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
— 613</p></td>
<td><p>Этот флаг зарезервирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
— 614</p></td>
<td><p>Существует слишком много невыполненных поколений между контрольной точкой и текущим поколением.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
— 615</p></td>
<td><p>Предпринята попытка принудительного восстановления базы данных, которая не является резервной базой данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
— 900</p></td>
<td><p>Недопустимый параметр грбит.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
–1000</p></td>
<td><p>Выполняется завершение.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
— 1001</p></td>
<td><p>Этот элемент API не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
— 1002</p></td>
<td><p>Используется недопустимое имя.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
— 1003</p></td>
<td><p>Используется недопустимый параметр API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
— 1008</p></td>
<td><p>Попытка присоединиться к файлу базы данных, доступному только для чтения, для операций чтения и записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
— 1010</p></td>
<td><p>Недопустимый идентификатор базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
— 1011</p></td>
<td><p>Системе не хватает памяти.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
— 1012</p></td>
<td><p>Достигнут максимальный размер базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
— 1013</p></td>
<td><p>Таблица находится за пределами курсоров.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
— 1014</p></td>
<td><p>В базе данных недостаточно буферов страниц.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
— 1015</p></td>
<td><p>Слишком много индексов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
— 1016</p></td>
<td><p>Слишком много столбцов в индексе.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
— 1017</p></td>
<td><p>Запись была удалена.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
— 1018</p></td>
<td><p>Ошибка контрольной суммы на странице базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
— 1019</p></td>
<td><p>Пустая страница базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
— 1020</p></td>
<td><p>Дескрипторы файлов отсутствуют.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
— 1022</p></td>
<td><p>Ошибка ввода-вывода на диск.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
— 1023</p></td>
<td><p>Недопустимый путь к файлу.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
— 1024</p></td>
<td><p>Недопустимый системный путь.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
— 1025</p></td>
<td><p>Недопустимый каталог журнала.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
— 1026</p></td>
<td><p>Запись больше, чем максимальный размер.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
— 1027</p></td>
<td><p>Слишком много открытых баз данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
— 1028</p></td>
<td><p>Это не файл базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
— 1029</p></td>
<td><p>Ядро СУБД не инициализировано.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
— 1030</p></td>
<td><p>Ядро СУБД уже инициализировано.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
— 1031</p></td>
<td><p>Инициализируется ядро СУБД.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
— 1032</p></td>
<td><p>Не удается получить доступ к файлу, так как файл заблокирован или используется.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
— 1038</p></td>
<td><p>Буфер слишком мал.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
— 1040</p></td>
<td><p>Определено слишком много столбцов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
— 1043</p></td>
<td><p>Контейнер не пуст.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
— 1044</p></td>
<td><p>Недопустимое имя файла.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
— 1045</p></td>
<td><p>Недопустимая закладка.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
— 1046</p></td>
<td><p>Используемый столбец находится в индексе.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
— 1047</p></td>
<td><p>Буфер данных не соответствует размеру столбца.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
— 1048</p></td>
<td><p>Не удается задать значение столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
— 1051</p></td>
<td><p>Индекс используется.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
— 1052</p></td>
<td><p>Ссылка недоступна.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
— 1053</p></td>
<td><p>Ключи NULL не допускаются в индексе.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
— 1054</p></td>
<td><p>Операция должна выполняться в рамках транзакции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
— 1059</p></td>
<td><p>Слишком много активных пользователей базы данных</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
— 1061</p></td>
<td><p>Недопустимый или неизвестный код страны.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
— 1062</p></td>
<td><p>Недопустимый или Неизвестный идентификатор языка.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
— 1063</p></td>
<td><p>Недопустимая или неизвестная кодовая страница.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
— 1064</p></td>
<td><p>Для <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString завершилось ошибкой</a>используются недопустимые флаги.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
— 1065</p></td>
<td><p>Попытка создать запись в хранилище версий (RCE), которая была больше, чем у контейнера версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
— 1066</p></td>
<td><p>В хранилище версий недостаточно памяти, попытка очистки завершилась сбоем.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
— 1069</p></td>
<td><p>В хранилище версий недостаточно памяти, и уже была предпринята попытка очистки.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
— 1071</p></td>
<td><p>Столбцы депонирования и SLV не могут быть проиндексированы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
— 1072</p></td>
<td><p>Запись не была удалена.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
— 1073</p></td>
<td><p>Запрошено слишком много записей мемпул.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
— 1074</p></td>
<td><p>База данных находится за пределами объектов ObjectID дерева B +, поэтому для освобождения или неиспользуемых идентификаторов ObjectId необходимо выполнить автономную дефрагментацию.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
— 1075</p></td>
<td><p>Счетчик с ИДЕНТИФИКАТОРом длинных значений достиг максимального значения. Для освобождения бесплатной или неиспользуемой Лонгвалуеидс необходимо выполнить автономную дефрагментацию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
— 1076</p></td>
<td><p>Счетчик автоматического приращения достиг максимального значения. Автономная дефрагментация не сможет освободить свободные или неиспользуемые значения автоинкремента.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
— 1077</p></td>
<td><p>Счетчик Дбтиме достиг максимального значения. Для освобождения бесплатных или неиспользуемых значений Дбтиме необходимо выполнить автономную дефрагментацию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
— 1078</p></td>
<td><p>Достигнуто максимальное значение счетчика последовательных индексов. Для освобождения бесплатных или неиспользуемых значений Секуентиалиндекс необходимо выполнить автономную дефрагментацию.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
— 1080</p></td>
<td><p>В этом вызове с несколькими экземплярами включен режим с одним экземпляром.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
— 1081</p></td>
<td><p>В этом вызове одного экземпляра включен режим с несколькими экземплярами.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
— 1082</p></td>
<td><p>Глобальные системные параметры уже заданы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
— 1083</p></td>
<td><p>Системный путь уже используется другим экземпляром базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
— 1084</p></td>
<td><p>Путь к файлу журнала уже используется другим экземпляром базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
— 1085</p></td>
<td><p>Путь к временной базе данных уже используется другим экземпляром базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
— 1086</p></td>
<td><p>Имя экземпляра уже используется.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
— 1090</p></td>
<td><p>Этот экземпляр нельзя использовать, так как в нем возникла неустранимая ошибка.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
— 1091</p></td>
<td><p>Эту базу данных невозможно использовать, так как произошла неустранимая ошибка.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
— 1092</p></td>
<td><p>Этот экземпляр не может быть использован, так как при выполнении операции (например, откат транзакции), которая не допускает ошибок, произошла ошибка переполнения журнала диска.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
— 1101</p></td>
<td><p>В базе данных недостаточно сеансов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
— 1102</p></td>
<td><p>Сбой блокировки записи из-за существования ожидающей блокировки записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
— 1103</p></td>
<td><p>Слишком глубокая вложенность транзакций.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
— 1104</p></td>
<td><p>Недопустимый обработчик сеанса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
— 1105</p></td>
<td><p>Попытка обновления для незафиксированного первичного индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
— 1108</p></td>
<td><p>Операция не разрешена в рамках транзакции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
— 1109</p></td>
<td><p>Должна быть произведена откат текущей транзакции. Она не может быть зафиксирована, и не может быть запущена новая.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
— 1110</p></td>
<td><p>Транзакция, доступная только для чтения, попыталась изменить базу данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
— 1111</p></td>
<td><p>Предпринята попытка заменить одну и ту же запись двумя разными курсорами в одном сеансе.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
— 1112</p></td>
<td><p>Запись будет слишком большой, если она представлена в формате базы данных из предыдущей версии Jet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
— 1113</p></td>
<td><p>Не удалось создать временную таблицу из-за параметров, конфликтующих с JET_bitTTForwardOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
— 1114</p></td>
<td><p>Невозможно использовать этот обработчик сеанса с идентификатором таблицы, так как он не использовался для его создания.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
— 1115</p></td>
<td><p>Недопустимый указатель экземпляра или ссылка на экземпляр, который был закрыт.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
— 1119</p></td>
<td><p>На странице базы данных, считанной с диска, была записана Предыдущая запись, не представленная на странице. Доступно в Windows 8 и более поздних версиях для Client, Windows Server 2012 и более поздних версий для сервера.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
— 1201</p></td>
<td><p>База данных уже существует.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
— 1202</p></td>
<td><p>Используемая база данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
— 1203</p></td>
<td><p>Такая база данных отсутствует.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
— 1204</p></td>
<td><p>Недопустимое имя базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
— 1205</p></td>
<td><p>Недопустимое число страниц.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
— 1206</p></td>
<td><p>Отсутствует файл, отличный от базы данных, или повреждена база данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
— 1207</p></td>
<td><p>База данных заблокирована в монопольном режиме.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
— 1208</p></td>
<td><p>Не удается отключить управление версиями для этой базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
— 1209</p></td>
<td><p>Ядро СУБД несовместимо с базой данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
— 1210</p></td>
<td><p>База данных имеет более старый формат (200). Эта ошибка возвращается функцией <a href="gg294068(v=exchg.10).md">жетинит</a> , если задан параметр <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Только клиент Windows NT.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
— 1211</p></td>
<td><p>База данных имеет более старый формат (400). Эта ошибка возвращается функцией <a href="gg294068(v=exchg.10).md">жетинит</a> , если задан параметр <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Только клиент Windows NT.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
— 1212</p></td>
<td><p>База данных имеет более старый формат (500). Эта ошибка возвращается функцией <a href="gg294068(v=exchg.10).md">жетинит</a> , если задан параметр <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Только клиент Windows NT.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
— 1213</p></td>
<td><p>Размер страницы базы данных не соответствует подсистеме.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
— 1214</p></td>
<td><p>Больше нельзя запускать экземпляры базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
— 1215</p></td>
<td><p>База данных используется другим экземпляром базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
— 1216</p></td>
<td><p>Необработанное вложение базы данных обнаружено в начале или в конце восстановления, но база данных отсутствует или не соответствует сведениям о вложении.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
— 1217</p></td>
<td><p>Указан недопустимый путь к файлу базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
— 1218</p></td>
<td><p>Базе данных назначается идентификатор, который уже используется.</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
— 1219</p></td>
<td><p>Принудительная отсоединение разрешена только после того, как нормальная отсоединение была остановлена из-за ошибки.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
— 1220</p></td>
<td><p>В каталоге обнаружено повреждение.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
— 1221</p></td>
<td><p>База данных присоединена только частично, а операция присоединения не может быть завершена.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
— 1222</p></td>
<td><p>База данных с такой же подписью уже используется.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
— 1224</p></td>
<td><p>База данных повреждена, но восстановление не разрешено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
— 1225</p></td>
<td><p>Ядро СУБД попыталось воспроизвести операцию создания базы данных из журнала транзакций, но не удалось выполнить из-за несовместимой версии этой операции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
— 1302</p></td>
<td><p>Таблица монопольно заблокирована.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
— 1303</p></td>
<td><p>Таблица уже существует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
— 1304</p></td>
<td><p>Таблица используется и не может быть заблокирована.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
— 1305</p></td>
<td><p>Такой таблицы или объекта нет.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
— 1307</p></td>
<td><p>Недопустимая плотность файла или индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
— 1308</p></td>
<td><p>Таблица не пуста.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
— 1310</p></td>
<td><p>Недопустимый идентификатор таблицы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
— 1311</p></td>
<td><p>Невозможно открыть больше таблиц даже после выполнения внутренней задачи очистки.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
— 1312</p></td>
<td><p>Операция не поддерживается для таблицы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
— 1313</p></td>
<td><p>Не удается открыть больше таблиц, так как не удалось завершить попытку очистки.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
— 1314</p></td>
<td><p>Имя таблицы или объекта используется.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
— 1316</p></td>
<td><p>Объект недопустим для операции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
— 1317</p></td>
<td><p>Для удаления временной таблицы необходимо использовать <a href="gg294087(v=exchg.10).md">жетклосетабле</a> вместо <a href="gg294128(v=exchg.10).md">жетделететабле</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
— 1318</p></td>
<td><p>Недопустимая попытка удалить системную таблицу.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
— 1319</p></td>
<td><p>Недопустимая попытка удалить таблицу шаблонов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
— 1322</p></td>
<td><p>Должна быть монопольная блокировка таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
— 1323</p></td>
<td><p>В этой таблице запрещены операции DDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
— 1324</p></td>
<td><p>В производной таблице операции DDL запрещены в наследуемой части DDL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
— 1325</p></td>
<td><p>Вложенные иерархические DDL в настоящее время не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
— 1326</p></td>
<td><p>Предпринята попытка наследования DDL из таблицы, которая не помечена как таблица шаблона.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
— 1328</p></td>
<td><p>Системные параметры заданы неправильно.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
— 1329</p></td>
<td><p>Клиент запросил остановку службы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
— 1330</p></td>
<td><p>Таблица шаблона была создана с установленным флагом Нофикседварколумнсиндериведтаблес.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
— 1401</p></td>
<td><p>Не удалось выполнить сборку индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
— 1402</p></td>
<td><p>Первичный индекс уже определен.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
— 1403</p></td>
<td><p>Индекс уже определен.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
— 1404</p></td>
<td><p>Такого индекса нет.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
— 1405</p></td>
<td><p>Невозможно удалить кластеризованный индекс.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
— 1406</p></td>
<td><p>Недопустимое определение индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
— 1409</p></td>
<td><p>Недопустимое создание описания индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
— 1410</p></td>
<td><p>База данных выходит за пределы блоков описания индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
— 1411</p></td>
<td><p>Для многозначного индекса были созданы неуникальные ключи индексов между записями.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
— 1412</p></td>
<td><p>Вторичный индекс, который правильно отражает первичный индекс, не удалось построить.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
— 1413</p></td>
<td><p>Первичный индекс поврежден, и база данных должна быть дефрагментирована.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
— 1414</p></td>
<td><p>Вторичный индекс поврежден, и база данных должна быть дефрагментирована.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
— 1416</p></td>
<td><p>Недопустимый идентификатор индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
— 1430</p></td>
<td><p>Индекс кортежа можно задать только для вторичного индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
— 1431</p></td>
<td><p>Определение индекса для индекса кортежа содержит дополнительные ключевые столбцы, которые может поддерживать ядро СУБД.</p>
<p><strong>Примечание  </strong> . JET_errIndexTuplesOneColumnOnlyная ошибка устарела и заменена JET_errIndexTuplesTooManyColumns.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
— 1432</p></td>
<td><p>Индекс кортежа должен быть неуникальным индексом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
— 1433</p></td>
<td><p>Определение индекса кортежа может содержать только ключевые столбцы с типами столбцов text или binary.</p>
<p><strong>Примечание  </strong> . JET_errIndexTuplesTextColumnsOnlyная ошибка устарела и заменена JET_errIndexTuplesTextBinaryColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
— 1434</p></td>
<td><p>Индекс кортежа не допускает настройки Кбварсегмак.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
— 1435</p></td>
<td><p>Минимальная или максимальная длина кортежа или максимальное число символов, указанных для индекса, недопустимы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
— 1436</p></td>
<td><p><a href="gg269198(v=exchg.10).md">Жетретриевеколумн</a> не может быть вызван с установленным флагом JET_bitRetrieveFromIndex при извлечении столбца в индексе кортежа.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
— 1437</p></td>
<td><p>Указанный ключ не соответствует минимальной длине кортежа.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
— 1501</p></td>
<td><p>Значение столбца является длинным.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
— 1502</p></td>
<td><p>Такой фрагмент не существует в длинном значении.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
— 1503</p></td>
<td><p>Поле не будет помещаться в записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
— 1504</p></td>
<td><p>Недопустимое значение null.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>Недопустимое значение null. Эта ошибка возвращается диспетчером записей.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>Столбец индексируется и не может быть удален.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>Длина поля превышает максимально допустимую длину.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>Такого столбца нет.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>Это поле уже определено.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>Предпринята попытка создать столбец с несколькими значениями, но столбец не был помечен.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>Второй столбец с автоматическим приращением или версией.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>Недопустимый тип данных столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNULL-1514</p></td>
<td><p>Нет помеченных столбцов, относящихся к NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>База данных недопустима, так как она не содержит текущего индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>Ключ полностью создан.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>Неправильный идентификатор столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>Некорректный Итагсекуенце для столбца с тегами.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>Невозможно удалить столбец, так как он является частью связи.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>Автоматическое увеличение и версия не могут быть помечены.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>Значение по умолчанию превышает максимальный размер.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>В уникальном столбце с несколькими значениями обнаружено повторяющееся значение.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>Обнаружено повреждение в дереве длинных значений.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>Обнаружено повторяющееся значение в уникальном столбце с несколькими значениями после нормализации данных, и нормализация усекает данные перед сравнением.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>Недопустимый столбец в производной таблице.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>Предпринята попытка преобразовать столбец в заполнитель первичного индекса, но этот столбец не соответствует необходимым критериям.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>Ключ не найден.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>Нет рабочего буфера.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>Отсутствует текущая запись.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>Первичный ключ может не измениться.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>Недопустимый дублирующийся ключ.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>Предпринята попытка обновить запись, пока уже выполняется обновление записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>Вызов не был сделан в <a href="gg269329(v=exchg.10).md">жетмакекэй</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>Вызов не был сделан в <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>Данные были изменены, операция прервана.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>Эта установка Windows не поддерживает выбранный язык.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>Слишком много процессов сортировки.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>Во время сортировки произошла Недопустимая операция.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>Не удалось открыть временный файл.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>Открыто слишком много баз данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>На диске не осталось места.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>Отказано в разрешении.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>Файл не найден.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>Недопустимый тип файла.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>Невозможно запустить восстановление после инициализации.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>Не удалось интерпретировать журналы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>Недопустимая операция.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>Отказано в доступе".</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>Бесконечное разбиение.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>Несколько потоков используют один сеанс.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>Не удалось найти точку входа в требуемой библиотеке DLL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionContextAlreadySet-1912</p></td>
<td><p>Для указанного сеанса уже задан контекст сеанса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextNotSetByThisThread-1913</p></td>
<td><p>Предпринята попытка сбросить контекст сеанса, но текущий поток не был исходным, который задает контекст сеанса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>Предпринята попытка завершить сеанс, который сейчас используется.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>Произошла внутренняя ошибка при преобразовании формата динамической записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p>Допускается только одна открытая пользовательская база данных на сеанс (как указано установкой флага <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> во время создания базы данных).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>Произошла ошибка во время отката.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>Не удалось вызвать функцию обратного вызова.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>Не удалось найти функцию обратного вызова.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>API теневого копирования операционной системы использован в недопустимой последовательности.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>Теневое копирование операционной системы завершилось с превышением времени ожидания.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>Теневое копирование операционной системы запрещено, так как выполняется резервное копирование или восстановление.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>Не удалось выполнить операцию, так как указан недопустимый маркер теневого копирования операционной системы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>Предпринята попытка использовать локальное хранилище без указания функции обратного вызова.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>Была предпринята попытка задать локальное хранилище для объекта, который уже был задан.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>Предпринята попытка получить локальное хранилище из объекта, в котором он не был задан.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>Не удалось выполнить операцию ввода-вывода, так как она была предпринята для нераспределенной области файла.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>Операция чтения была выдана в расположение после конца файла (операции записи разворачивают файл).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>Этот флаг указывает JET_ABORTRETRYFAILCALLBACK вызывающему объекту прервать указанный ввод-вывод.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>Этот флаг указывает JET_ABORTRETRYFAILCALLBACK вызывающему объекту повторить указанный ввод-вывод.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>Этот флаг указывает JET_ABORTRETRYFAILCALLBACK вызывающему объекту завершиться ошибкой указанного ввода-вывода.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>Доступ для чтения и записи не поддерживается для сжатых файлов.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Комментарии

В общем случае значение, большее нуля, должно интерпретироваться как предупреждение, нулевое значение должно интерпретироваться как успешно, а значение меньше нуля должно интерпретироваться как ошибка. Никакие другие шаблоны в этих значениях, например диапазоны значений, должны быть полагаться на приложения.

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

[Параметры обработки ошибок](./error-handling-parameters.md)  
[Ошибки расширяемого подсистемы хранилища](./extensible-storage-engine-errors.md)  
[Расширяемые файлы подсистемы хранилища](./extensible-storage-engine-files.md)
