---
description: 'Дополнительные сведения: параметры кэша базы данных'
title: Параметры кэша базы данных
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711319"
---
# <a name="database-cache-parameters"></a>Параметры кэша базы данных


_**Применимо к:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Параметры кэша базы данных

Этот раздел содержит параметры, используемые для кэша базы данных.

*JET_paramBatchIOBufferMax*  
22  

Этот параметр определяет размер вспомогательной части кэша страниц базы данных, которая используется для имитации операций ввода-вывода при недоступности. Размер находится в страницах базы данных.

**Windows XP и более поздние версии:**  Этот параметр устарел и не влияет на работу ядра СУБД.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>0, 2 – 2147483647</p></td>
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


*JET_paramCacheSize*  
41  

Этот параметр можно использовать для управления размером кэша страниц базы данных во время выполнения. Обычно кэш автоматически настраивает свой размер в виде функции уровней активности базы данных и компьютера. Если приложение устанавливает для этого параметра значение 0, то кэш будет настраивать свой собственный размер таким образом. Однако если приложение задает для этого параметра ненулевое значение, то кэш будет настроен таким же целевым размером (на страницах базы данных). Кэш будет храниться в этом пороговом значении до получения нового размера или до тех пор, пока не будет выбран его собственный размер.

**Примечание**  .  Размер кэша по-прежнему подчиняется ограничениям, наложенным **JET_paramCacheSizeMin** и **JET_paramCacheSizeMax**.

При чтении этого параметра возвращается фактический размер кэша на страницах базы данных. Этот размер может использоваться приложением в качестве входных данных для выполнения ручной настройки размера кэша.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Специальные функции</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
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


*JET_paramCacheSizeMin*  
60  

Этот параметр задает минимальный размер кэша страниц базы данных. Размер находится в страницах базы данных.

По умолчанию кэш базы данных автоматически подстраивает свой размер между ограничениями, заданными **JET_paramCacheSizeMin** и **JET_paramCacheSizeMax**.

**Windows 2000:**  В Windows 2000 этому параметру должно быть присвоено значение примерно равное четырем количеству потоков, которые будут находиться внутри API ESE одновременно. Это необходимо, чтобы избежать взаимоблокировок, вызванных недостаточным количеством буферов кэша страниц базы данных для выполнения сложных операций, таких как разбиение дерева B +.

**Windows XP и более поздние версии:**  Диспетчер кэша автоматически установит свой минимальный размер кэша, чтобы избежать взаимоблокировок.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p><strong>Windows 2000:</strong>  64</p>
<p><strong>Windows XP:</strong>  1</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  Нет</p>
<p><strong>Windows XP:</strong>  Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  Нет</p>
<p><strong>Windows XP:</strong>  Да</p></td>
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


*JET_paramCacheSizeMax*  
23  

Этот параметр задает максимальный размер кэша страниц базы данных. Размер находится в страницах базы данных.

По умолчанию кэш базы данных автоматически подстраивает свой размер между ограничениями, заданными **JET_paramCacheSizeMin** и **JET_paramCacheSizeMax**.

**Примечание**   .   Если этот параметр оставлен со значением по умолчанию, максимальный размер кэша будет установлен в размер физической памяти при вызове [жетинит](./jetinit-function.md) .

**Windows Vista:**  Начиная с Windows Vista, значение этого параметра по умолчанию изменилось, чтобы объяснить это поведение.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  512</p>
<p><strong>Windows Vista:</strong>  2000000000</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Глобальный</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p><strong>Windows 2000:</strong>  Нет</p>
<p><strong>Windows XP:</strong>  Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p><strong>Windows XP и windows 2000:</strong>  Нет</p>
<p><strong>Windows Vista и Windows Server 2003:</strong>  Да</p></td>
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


*JET_paramCheckpointDepthMax*  
24 

Этот параметр определяет, как агрессивные страницы базы данных очищаются из кэша страниц базы данных, чтобы максимально сокращать время, необходимое для восстановления после сбоя. Параметр — это пороговое значение в байтах, необходимое для того, сколько файлов журнала транзакций потребуется воспроизвести после сбоя.

Если циклическое ведение журнала включено с помощью [JET_paramCircularLog](./transaction-log-parameters.md) то этот параметр также будет управлять приблизительным объемом файлов журнала транзакций, которые будут храниться на диске.

Важно, чтобы этот параметр не был задан слишком низким. Поскольку значение этого параметра приближается к нулю, кэш становится более и более агрессивным при сбросе страниц базы данных на диск. Это не только увеличивает число операций записи в файлы базы данных, но и косвенно приводит к увеличению числа операций чтения этих файлов. В некоторых случаях это может привести к очень значительным проблемам с производительностью. К сожалению, установка наименьшего оптимального значения для этого параметра может быть выполнена только с помощью эксперимента с целевым приложением.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>20971520</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Все значения</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Windows <strong>2000, Windows XP и Windows Server 2003:</strong> Этот параметр является глобальным.</p>
<p><strong>Windows Vista:</strong>  Этот параметр задан для каждого экземпляра.</p></td>
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
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointIOMax*  
135  

Этот параметр управляет максимальным числом одновременных операций записи, которые ядро СУБД будет использовать для сброса измененных страниц базы данных с целью перемещения контрольной точки. Значение этого параметра можно использовать для балансировки скорости, с которой может быть расширена контрольная точка, а также отрицательного воздействия на то, что этот процесс будет иметь время отклика для других операций ввода-вывода на дисках, где находится база данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>96</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>8 — 1024</p></td>
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
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows Vista и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableViewCache*  
127  

Если этот параметр имеет **значение true**, ядро СУБД будет использовать данные базы данных непосредственно из кэша файлов Windows, а не копировать кэшированные данные в собственную частную память. Все измененные данные базы данных по-прежнему будут кэшироваться в частной памяти.

Цель этого режима — еще больше уменьшить объем памяти, используемой ядром СУБД для кэширования данных базы данных.

Кэш представлений может использоваться только в том случае, если использование кэша файлов Windows включено путем установки JET_paramEnableFileCache в **значение true**.

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


*JET_paramLRUKCorrInterval*  
25  

Этот параметр задает интервал времени в микросекундах, в течение которого два доступа к странице базы данных считаются коррелированными. Этот интервал корреляции управляет чувствительностью алгоритма замены страниц кэша (LRU-K) к последовательному доступу к странице. Это, в свою очередь, повлияет на то, какие страницы он выбирает для сохранения кэширования.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>128 000</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003: </strong>    0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Все значения</p></td>
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
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKHistoryMax*  
26  

Этот параметр задает максимальное количество некэшированных страниц базы данных, для которых будет храниться время доступа к странице базы данных. Эти записи журнала позволяют алгоритму замены страниц кэша (LRU-K) более точно обнаруживать популярные страницы, которые были неправильно исключены из кэша страниц базы данных.

**Windows XP и Windows Server 2003:**  Этот параметр не учитывается в Windows XP и Windows Server 2003 и не влияет на работу ядра СУБД.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p><strong>Windows 2000:</strong>  1024</p>
<p><strong>Windows Vista:</strong>  100000</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  0 – 4194303</p>
<p><strong>Windows Vista:</strong>  Все значения</p></td>
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


*JET_paramLRUKPolicy*  
27  

Этот параметр задает количество обращений к странице базы данных, которые учитываются при определении полезности страницы. Этот параметр по сути является K в LRU-K, алгоритмом замены страниц кэша страниц базы данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>1–2</p></td>
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
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTimeout*  
28

Этот параметр указывает период времени (в секундах), по истечении которого считается, что страница в кэше страниц базы данных потеряла доступ к странице для учета полезности страницы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  1 – 2147483647</p>
<p><strong>Windows Vista:</strong>   1 – 4294967295</p></td>
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
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Все</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTrxCorrInterval*  
29  

Этот параметр устарел и не влияет на работу ядра СУБД.

*JET_paramStartFlushThreshold*  
31  

Этот параметр определяет, когда кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются. Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов. Это пороговое значение всегда относительно максимального размера кэша, установленного **JET_paramCacheSizeMax**. Это пороговое значение также должно быть меньше порога окончания, установленного **JET_paramStopFlushThreshold**.

Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их. При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование. Однако при высоком пороговом значении для параметра «Порог» появляется более высокий порог, что уменьшает эффективный размер кэша страниц базы данных для измененных страниц (Windows 2000) или для всех страниц (Windows XP и более поздних версий).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  5 (1%)</p>
<p><strong>Windows Vista:</strong>  20000000 (1%)</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Все значения</p></td>
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


*JET_paramStopFlushThreshold*  
32  

Этот параметр управляет тем, когда кэш страниц базы данных завершает исключение страниц из кэша, освобождая пространство для страниц, которые не кэшируются. Когда количество буферов страниц в кэше превышает это пороговое значение, фоновый процесс, который был запущен для пополнения пула доступных буферов, останавливается. Это пороговое значение всегда относительно максимального размера кэша, установленного **JET_paramCacheSizeMax**. Это пороговое значение также должно быть больше, чем пороговое значение начала, заданное **JET_paramStartFlushThreshold**.

Расстояние между пороговым значением начала и порогом окончания влияет на эффективность, с которой страницы базы данных сбрасываются фоновым процессом. Чем больше промежуток, тем больше вероятность, что записи на соседние страницы могут быть объединены. Однако при высоком пороговом значении будет уменьшен эффективный размер кэша страниц базы данных для измененных страниц (Windows 2000) или для всех страниц (Windows XP и более поздних версий).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p><strong>Windows 2000, Windows XP и Windows Server 2003:</strong>  10 (2%)</p>
<p><strong>Windows Vista:</strong>  40000000 (2%)</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Целочисленный тип</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Все значения</p></td>
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
