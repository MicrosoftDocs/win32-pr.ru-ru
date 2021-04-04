---
description: Дополнительные сведения о параметрах ввода-вывода
title: Параметры ввода-вывода
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811639"
---
# <a name="io-parameters"></a>Параметры ввода-вывода


_**Применимо к:** Windows | Windows Server_

## <a name="io-parameters"></a>Параметры ввода-вывода

Этот раздел содержит параметры, используемые для ввода-вывода.

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP и более поздние версии:**  Этот параметр задает длительность времени (в миллисекундах), в течение которого ядро СУБД будет обращаться к файлу, заблокированному до сбоя JET_errFileAccessDenied. Эта временная задержка предназначена для работы с антивирусным программным обеспечением, которое может содержать некоторые файлы ядра СУБД, открытые после их закрытия.

**Примечание**  .  В результате выполнения описанной выше логики повторных попыток присоединения к базе данных или использования файла журнала, который уже используется ядром СУБД, произойдет задержка этого размера, прежде чем вызов API вернет несанкционированный сбой. Этот параметр можно использовать для отключения задержки в случае, если это распространенный сценарий.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>10000</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 – 4294967295</p></td>
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
<td><p>Да</p></td>
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
<td><p>Windows XP и более поздних версий.</p></td>
</tr>
</tbody>
</table>


*JET_paramCreatePathIfNotExist*  
100  

Если этот параметр имеет значение true, любая папка, отсутствующая в пути файловой системы, используемой ядром СУБД, будет создана автоматически. В противном случае операция, использующая отсутствующий путь файловой системы, завершится с JET_errInvalidPath.

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


*JET_paramEnableFileCache*  
126  

Если этот параметр имеет **значение true**, ядро СУБД будет использовать файловый кэш Windows в качестве кэша чтения для всех его различных файлов. Он также будет использовать его как кэш записи для временной базы данных или для баз данных, открываемых с отключенным восстановлением. Ядро СУБД должно отключить кэширование записи для обычных баз данных, файлов журналов транзакций и файлов контрольных точек для защиты транзакционной целостности баз данных.

Важно отметить, что использование кэша файлов Windows приведет к добавлению второго уровня кэширования для файлов базы данных. Кэш базы данных по-прежнему будет использовать собственную память для кэширования файлов базы данных. Цель этого режима — позволить приложению настроить ядро СУБД с помощью небольшого выделенного кэша и позволить Windows подносить запасную память для дальнейшего улучшения кэширования данных базы данных.

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
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Нет</p></td>
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
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows Vista и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramIOPriority*  
152  

Этот параметр определяет, как ESE обрабатывает операции ввода-вывода. Для нормальной работы можно задать значения 0 (JET_IOPriorityNormal) или 1 (JET_IOPriorityLow) для операции с низким приоритетом. Если для параметра Priority задано значение JET_IOPriorityLow, ESE использует новые функции приоритета ввода-вывода потока, доступные в Windows Vista, чтобы уменьшить приоритет ввода-вывода в потоке, чтобы последующие операции ввода-вывода выдавались с новым низким приоритетом.

**Windows Vista:**  JET_paramIOPriority введен в Windows Vista.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0 - 1</p></td>
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
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramOutstandingIOMax*  
30 

Этот параметр определяет, сколько операций ввода-вывода в файле базы данных может быть поставлено в очередь в операционной системе узла в один момент времени.

Большее значение этого параметра может значительно помочь в производительности большого приложения базы данных.

**Windows XP и Windows Server 2003:**  Этот параметр не учитывается в Windows XP и Windows Server 2003 и не влияет на работу ядра СУБД.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p><strong>Windows 2000: </strong>  64</p>
<p><strong>Windows Vista:</strong>   1024</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  8 – 2147483647</p>
<p><strong>Windows Vista:</strong>  0 – 65536</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Нет</p></td>
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
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceReadSize*  
164  

Максимальное число байтов, которые могут быть сгруппированы для совместной операции чтения.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0-1073741824</p></td>
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
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceWriteSize*  
165  

Максимальное число байтов, которые могут быть сгруппированы для совместной операции записи.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>393216</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0-1073741824</p></td>
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
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceReadGapSize*  
166  

Максимальное число байтов, которое может быть гаппед для операции совместного ввода-вывода.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0-1073741824</p></td>
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
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCoalesceWriteGapSize*  
167  

Максимальное число байтов, которое может быть гаппед для совместной операции чтения ввода-вывода.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>393216</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0-1073741824</p></td>
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
<td><p>Windows 7</p></td>
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
