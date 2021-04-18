---
description: 'Дополнительные сведения о: SystemParameters свойства'
title: Свойства SystemParameters
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 12e18b6c045758c8e9fd7ffb91f728c78dcf2e24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553068"
---
# <a name="systemparameters-properties"></a>Свойства SystemParameters

Включить защищенные члены  
Включить унаследованные члены  

Тип [SystemParameters](./systemparameters-class.md) предоставляет следующие члены.

## <a name="properties"></a>Свойства

<table>
<thead>
<tr class="header">
<th> </th>
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">букмаркмост</a></td>
<td>Возвращает максимальный размер закладки. <a href="dn292149(v=exchg.10).md">Жетжетбукмарк (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Возвращает или задает размер кэша базы данных на страницах. По умолчанию кэш базы данных автоматически настраивает свой размер, а установка этого свойства в ненулевое значение приводит к тому, что кэш подстраивается к целевому размеру.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">качесиземакс</a></td>
<td>Возвращает или задает максимальный размер кэша страниц базы данных. Размер находится в страницах базы данных. Если этот параметр оставлен со значением по умолчанию, максимальный размер кэша будет установлен в размер физической памяти при вызове Жетинит.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">качесиземин</a></td>
<td>Возвращает или задает минимальный размер кэша страниц базы данных в страницах базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">колумнскэймост</a></td>
<td>Возвращает максимальное число компонентов в ключе сортировки или индекса.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Конфигурация</a></td>
<td>Возвращает или задает значение, указывающее значения по умолчанию для всего набора системных параметров. Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации. Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию. Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти. Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию. Поддерживается в Windows Vista и выше. Игнорируется в Windows XP и Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">датабасепажесизе</a></td>
<td>Возвращает или задает размер страниц базы данных в байтах.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">енаблеадванцед</a></td>
<td>Возвращает или задает значение, указывающее, принимает ли ядро СУБД изменения, внесенные в подмножество системных параметров, или отклоняет их. Этот параметр используется вместе с <a href="dn351218(v=exchg.10).md">конфигурацией</a> , чтобы предотвратить установку некоторых параметров системы из значений по умолчанию выбранной конфигурации. Поддерживается в Windows Vista и выше. Игнорируется в Windows XP и Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">енаблефилекаче</a></td>
<td>Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать кэш файлов ОС для всех управляемых файлов.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">енаблевиевкаче</a></td>
<td>Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать файловый ввод-вывод, размещенный в памяти, для файлов базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">евентлоггинглевел</a></td>
<td>Возвращает или задает уровень детализации сообщений журнала событий, которые передаются в журнал событий ядром СУБД. Более высокие значения приводят к более подробным сообщениям журнала событий.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ексцептионактион</a></td>
<td>Возвращает или задает кодировку значений, выполняемых с исключениями, созданными в JET.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">хунгиоактионс</a></td>
<td>Возвращает или задает набор действий, выполняемых в IOs, которые отображаются как зависые.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">хунгиосрешолд</a></td>
<td>Возвращает или задает пороговое значение для того, что считается незавершенным вводом-выводом.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">кэймост</a></td>
<td>Возвращает максимальный размер ключа. Это зависит от версии ESENT и размера страницы базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">легацифиленамес</a></td>
<td>Возвращает или задает обратную совместимость с соглашениями об именовании файлов более ранних выпусков ядра СУБД.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">лвчунксиземост</a></td>
<td>Возвращает размер фрагментов lv. Это зависит от размера страницы базы данных.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">максинстанцес</a></td>
<td>Возвращает или задает максимальное количество экземпляров, которые могут быть созданы.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">миндатафоркспресс</a></td>
<td>Возвращает или задает наименьший объем данных, которые должны быть сжаты с помощью сжатия Xpress.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">аутстандингиомакс</a></td>
<td>Этот параметр определяет, сколько операций ввода-вывода в файле базы данных может быть помещено в очередь на диск в операционной системе узла. Большее значение этого параметра может значительно помочь в производительности большого приложения базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">процессфриендлинаме</a></td>
<td>Возвращает или задает понятное имя для данного экземпляра процесса.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">стартфлушсрешолд</a></td>
<td>Возвращает или задает пороговое значение, при котором кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются. Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов. Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax. Это пороговое значение также должно быть меньше порога окончания, установленного JET_paramStopFlushThreshold. Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их. При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование. Тем не менее, при высоком пороговом значении приостанавливается более высокий порог, что уменьшает эффективный размер кэша страниц базы данных.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">стопфлушсрешолд</a></td>
<td>Возвращает или задает пороговое значение, при котором кэш страниц базы данных завершает исключение страниц из кэша, освобождая пространство для страниц, которые не кэшируются. Когда количество буферов страниц в кэше превышает это пороговое значение, фоновый процесс, который был запущен для пополнения пула доступных буферов, останавливается. Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax. Это пороговое значение также должно быть больше, чем пороговое значение начала, заданное JET_paramStartFlushThreshold. Расстояние между пороговым значением начала и порогом окончания влияет на эффективность, с которой страницы базы данных сбрасываются фоновым процессом. Чем больше промежуток, тем больше вероятность, что записи на соседние страницы могут быть объединены. Однако при высоком пороговом значении будет уменьшен эффективный размер кэша страниц базы данных.</td>
</tr>
</tbody>
</table>


Начало

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[SystemParameters - класс](./systemparameters-class.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
