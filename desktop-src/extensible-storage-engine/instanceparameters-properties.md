---
description: 'Дополнительные сведения о: Инстанцепараметерс свойства'
title: Свойства Инстанцепараметерс
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0ac2b8aa959b8fa07f06e2de86dcfc173bab15ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569289"
---
# <a name="instanceparameters-properties"></a><span data-ttu-id="b1da3-103">Свойства Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="b1da3-103">InstanceParameters properties</span></span>

<span data-ttu-id="b1da3-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="b1da3-104">Include protected members</span></span>  
<span data-ttu-id="b1da3-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="b1da3-105">Include inherited members</span></span>  

<span data-ttu-id="b1da3-106">Тип [инстанцепараметерс](./instanceparameters-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="b1da3-106">The [InstanceParameters](./instanceparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="b1da3-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1da3-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b1da3-108">Имя</span><span class="sxs-lookup"><span data-stu-id="b1da3-108">Name</span></span></th>
<th><span data-ttu-id="b1da3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b1da3-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-111"><a href="dn350971(v=exchg.10).md">алтернатедатабасерековеридиректори</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-111"><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></span></span></td>
<td><span data-ttu-id="b1da3-112">Возвращает или задает относительный или абсолютный путь к файловой системе папки, в которой восстановление после сбоя или операция восстановления могут найти базы данных, на которые имеются ссылки в журнале транзакций в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="b1da3-112">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-114"><a href="dn350972(v=exchg.10).md">Базов</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-114"><a href="dn350972(v=exchg.10).md">BaseName</a></span></span></td>
<td><span data-ttu-id="b1da3-115">Возвращает или задает префикс из трех букв, используемый для многих файлов, используемых ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="b1da3-115">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="b1da3-116">Например, файл контрольных точек называется EDB. CHK по умолчанию, так как EDB является базовым именем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1da3-116">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-118"><a href="dn350951(v=exchg.10).md">качедклоседтаблес</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-118"><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="b1da3-119">Возвращает или задает значение, определяющее количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением.</span><span class="sxs-lookup"><span data-stu-id="b1da3-119">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="b1da3-120">Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц.</span><span class="sxs-lookup"><span data-stu-id="b1da3-120">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="b1da3-121">Это полезно для приложений, имеющих схему с очень большим количеством таблиц.</span><span class="sxs-lookup"><span data-stu-id="b1da3-121">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="b1da3-122">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="b1da3-122">Supported on Windows Vista and up.</span></span> <span data-ttu-id="b1da3-123">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1da3-123">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-125"><a href="dn350974(v=exchg.10).md">качеприорити</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-125"><a href="dn350974(v=exchg.10).md">CachePriority</a></span></span></td>
<td><span data-ttu-id="b1da3-126">Возвращает или задает свойство для каждого экземпляра для относительных приоритетов кэша (по умолчанию = 100).</span><span class="sxs-lookup"><span data-stu-id="b1da3-126">Gets or sets the per-instance property for relative cache priorities (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-128"><a href="dn350953(v=exchg.10).md">чеккпоинтдепсмакс</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-128"><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></span></span></td>
<td><span data-ttu-id="b1da3-129">Возвращает или задает пороговое значение в байтах для того, сколько файлов журнала транзакций потребуется воспроизвести после сбоя.</span><span class="sxs-lookup"><span data-stu-id="b1da3-129">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="b1da3-130">Если циклическое ведение журнала включено с помощью Циркуларлог, этот параметр также управляет приблизительным объемом файлов журнала транзакций, которые будут храниться на диске.</span><span class="sxs-lookup"><span data-stu-id="b1da3-130">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-132"><a href="dn350977(v=exchg.10).md">Циркуларлог</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-132"><a href="dn350977(v=exchg.10).md">CircularLog</a></span></span></td>
<td><span data-ttu-id="b1da3-133">Возвращает или задает значение, указывающее, включено ли циклическое ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="b1da3-133">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="b1da3-134">Если циклическое ведение журнала отключено, все созданные файлы журнала транзакций сохраняются на диске до тех пор, пока они больше не нужны, так как была выполнена полная резервная копия базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1da3-134">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="b1da3-135">Если циклическое ведение журнала включено, на диске сохраняются только файлы журнала транзакций, которые являются моложе текущей контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="b1da3-135">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="b1da3-136">Преимущество этого режима заключается в том, что для снятия старых файлов журнала транзакций резервные копии не требуются.</span><span class="sxs-lookup"><span data-stu-id="b1da3-136">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-138"><a href="dn350955(v=exchg.10).md">клеанупмисматчедлогфилес</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-138"><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></span></span></td>
<td><span data-ttu-id="b1da3-139">Возвращает или задает значение, указывающее, завершается ли Жетинит сбоем, когда ядро СУБД настроено для начала использования файлов журнала транзакций на диске, размер которых отличается от настроенного.</span><span class="sxs-lookup"><span data-stu-id="b1da3-139">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="b1da3-140">Обычно <a href="dn292210(v=exchg.10).md">жетинит (JET_INSTANCE)</a> успешно восстановит базы данных, но завершится с ошибкой <a href="hh564840(v=exchg.10).md">логфилесиземисматчдатабасесконсистент</a> , чтобы указать, что размер файла журнала настроен неправильно.</span><span class="sxs-lookup"><span data-stu-id="b1da3-140">Normally, <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> will successfully recover the databases but will fail with <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="b1da3-141">Однако если этот параметр имеет значение true, то ядро СУБД автоматически удалит все старые файлы журналов, а затем запустит новый набор файлов журнала транзакций, используя настроенный размер файла журнала.</span><span class="sxs-lookup"><span data-stu-id="b1da3-141">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="b1da3-142">Этот параметр полезен, когда приложению требуется прозрачно изменить размер файла журнала транзакций, но все равно работать прозрачно в сценариях обновления и восстановления.</span><span class="sxs-lookup"><span data-stu-id="b1da3-142">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-144"><a href="dn350978(v=exchg.10).md">креатепасифнотексист</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-144"><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></span></span></td>
<td><span data-ttu-id="b1da3-145">Возвращает или задает значение, указывающее, будет ли ESENT автоматически создавать папки, отсутствующие в путях файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b1da3-145">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-147"><a href="dn350957(v=exchg.10).md">дбекстенсионсизе</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-147"><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></span></span></td>
<td><span data-ttu-id="b1da3-148">Возвращает или задает количество страниц, которые добавляются в файл базы данных каждый раз, когда им нужно увеличиваться в соответствии с большим объемом данных.</span><span class="sxs-lookup"><span data-stu-id="b1da3-148">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-150"><a href="dn350980(v=exchg.10).md">дбсканинтервалмакссек</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-150"><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></span></span></td>
<td><span data-ttu-id="b1da3-151">Возвращает или задает максимальный интервал времени, в течение которого сканирование базы данных будет готово.</span><span class="sxs-lookup"><span data-stu-id="b1da3-151">Gets or sets the maximum interval to allow the database scan to finish, in seconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-153"><a href="dn350959(v=exchg.10).md">дбсканинтервалминсек</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-153"><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></span></span></td>
<td><span data-ttu-id="b1da3-154">Возвращает или задает минимальный интервал повторения просмотра базы данных в секундах.</span><span class="sxs-lookup"><span data-stu-id="b1da3-154">Gets or sets the minimum interval to repeat the database scan, in seconds.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-156"><a href="dn350982(v=exchg.10).md">дбскансроттле</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-156"><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></span></span></td>
<td><span data-ttu-id="b1da3-157">Возвращает или задает регулирование сканирования базы данных в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="b1da3-157">Gets or sets the throttling of the database scan, in milliseconds.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-159"><a href="dn350961(v=exchg.10).md">енабледбсканинрековери</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-159"><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></span></span></td>
<td><span data-ttu-id="b1da3-160">Возвращает или задает значение, указывающее, должно ли выполняться обслуживание базы данных во время восстановления.</span><span class="sxs-lookup"><span data-stu-id="b1da3-160">Gets or sets a value indicating whether Database Maintenance should run during recovery.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-162"><a href="dn350984(v=exchg.10).md">енабледбскансериализатион</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-162"><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></span></span></td>
<td><span data-ttu-id="b1da3-163">Возвращает или задает значение, указывающее, включена ли сериализация обслуживания базы данных для баз данных, совместно использующих один и тот же диск.</span><span class="sxs-lookup"><span data-stu-id="b1da3-163">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-165"><a href="dn350986(v=exchg.10).md">енаблеиндексчеккинг</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-165"><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></span></span></td>
<td><span data-ttu-id="b1da3-166">Возвращает или задает значение, указывающее, будет ли <a href="dn292096(v=exchg.10).md">жетаттачдатабасе (JET_SESID, String, аттачдатабасегрбит)</a> проверять индексы, построенные с помощью более старой версии библиотеки NLS в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="b1da3-166">Gets or sets a value indicating whether <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will check for indexes that were build using an older version of the NLS library in the operating system.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-168"><a href="dn350963(v=exchg.10).md">енаблеонлинедефраг</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-168"><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></span></span></td>
<td><span data-ttu-id="b1da3-169">Возвращает или задает значение, указывающее, включена ли оперативная дефрагментация.</span><span class="sxs-lookup"><span data-stu-id="b1da3-169">Gets or sets a value indicating whether online defragmentation is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-171"><a href="dn350988(v=exchg.10).md">EventSource</a></span></span></td>
<td><span data-ttu-id="b1da3-172">Возвращает или задает специфичную для приложения строку, которая будет добавлена в любые сообщения журнала событий, созданные ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="b1da3-172">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="b1da3-173">Это позволяет легко сопоставить сообщения журнала событий с исходным приложением.</span><span class="sxs-lookup"><span data-stu-id="b1da3-173">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="b1da3-174">По умолчанию будет использоваться имя исполняемого файла ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="b1da3-174">By default the host application executable name will be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-176"><a href="dn350966(v=exchg.10).md">евентсаурцекэй</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-176"><a href="dn350966(v=exchg.10).md">EventSourceKey</a></span></span></td>
<td><span data-ttu-id="b1da3-177">Возвращает или задает имя журнала событий, используемого ядром СУБД для сообщений журнала событий.</span><span class="sxs-lookup"><span data-stu-id="b1da3-177">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="b1da3-178">По умолчанию все сообщения журнала событий перемещаются в журнал событий приложений.</span><span class="sxs-lookup"><span data-stu-id="b1da3-178">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="b1da3-179">Если будет настроено имя раздела реестра для другого журнала событий, вместо этого будут отправлены сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="b1da3-179">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-181"><a href="dn350968(v=exchg.10).md">логбуфферс</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-181"><a href="dn350968(v=exchg.10).md">LogBuffers</a></span></span></td>
<td><span data-ttu-id="b1da3-182">Возвращает или задает объем памяти, используемый для кэширования записей журнала до их записи в файл журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="b1da3-182">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="b1da3-183">Единицей для этого параметра является размер сектора тома, содержащего файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="b1da3-183">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="b1da3-184">Размер сектора почти всегда 512 байт, поэтому можно считать, что размер для единицы является надежным.</span><span class="sxs-lookup"><span data-stu-id="b1da3-184">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="b1da3-185">Этот параметр влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="b1da3-185">This parameter has an impact on performance.</span></span> <span data-ttu-id="b1da3-186">Когда ядро СУБД находится в режиме высокой нагрузки на обновление, этот буфер может быстро стать полностью загруженным.</span><span class="sxs-lookup"><span data-stu-id="b1da3-186">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="b1da3-187">Больший размер кэша для файла журнала транзакций очень важен для хорошего уровня производительности при такой высокой нагрузке.</span><span class="sxs-lookup"><span data-stu-id="b1da3-187">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="b1da3-188">Значение по умолчанию для этого случая известно слишком мало.</span><span class="sxs-lookup"><span data-stu-id="b1da3-188">The default is known to be too small for this case.</span></span> <span data-ttu-id="b1da3-189">Не устанавливайте для этого параметра количество буферов большего размера (в байтах), чем размер файла журнала транзакций, превышающий половину.</span><span class="sxs-lookup"><span data-stu-id="b1da3-189">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-191"><a href="dn350991(v=exchg.10).md">логфиледиректори</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-191"><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></span></span></td>
<td><span data-ttu-id="b1da3-192">Возвращает или задает относительный или абсолютный путь файловой системы к папке, которая будет содержать журналы транзакций для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-192">Gets or sets the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-194"><a href="dn350969(v=exchg.10).md">LogFileSize</a></span></span></td>
<td><span data-ttu-id="b1da3-195">Возвращает или задает размер файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="b1da3-195">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="b1da3-196">Этот параметр должен быть задан в единицах, равных 1024 байт (например, параметр 2048 будет предоставлять файлы журнала в 2 МБ).</span><span class="sxs-lookup"><span data-stu-id="b1da3-196">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-198"><a href="dn350993(v=exchg.10).md">макскурсорс</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-198"><a href="dn350993(v=exchg.10).md">MaxCursors</a></span></span></td>
<td><span data-ttu-id="b1da3-199">Возвращает или задает количество ресурсов курсора, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-199">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="b1da3-200">Ресурс курсора непосредственно соответствует JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="b1da3-200">A cursor resource directly corresponds to a JET_TABLEID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-202"><a href="dn350970(v=exchg.10).md">максопентаблес</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-202"><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></span></span></td>
<td><span data-ttu-id="b1da3-203">Возвращает или задает число ресурсов дерева B +, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-203">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-205"><a href="dn350994(v=exchg.10).md">MaxSessions</a></span></span></td>
<td><span data-ttu-id="b1da3-206">Возвращает или задает количество ресурсов сеансов, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-206">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="b1da3-207">Ресурс сеанса непосредственно соответствует JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="b1da3-207">A session resource directly corresponds to a JET_SESID.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-209"><a href="dn350997(v=exchg.10).md">макстемпораритаблес</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-209"><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></span></span></td>
<td><span data-ttu-id="b1da3-210">Возвращает или задает количество временных ресурсов таблицы для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b1da3-210">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="b1da3-211">Этот параметр влияет на количество временных таблиц, которые можно использовать одновременно.</span><span class="sxs-lookup"><span data-stu-id="b1da3-211">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="b1da3-212">Если этот системный параметр имеет значение 0, то временная база данных не будет создана и любое действие, требующее использования временной базы данных, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b1da3-212">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="b1da3-213">Этот параметр может быть полезен, чтобы избежать операций ввода-вывода, необходимых для создания временной базы данных, если известно, что она не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="b1da3-213">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-215"><a href="dn350973(v=exchg.10).md">макстрансактионсизе</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-215"><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></span></span></td>
<td><span data-ttu-id="b1da3-216">Возвращает или задает процентное значение хранилища версий, которое может использоваться самой старой транзакцией перед <a href="hh564840(v=exchg.10).md">версионстореаутофмемори</a> (по умолчанию = 100).</span><span class="sxs-lookup"><span data-stu-id="b1da3-216">Gets or sets the percentage of version store that can be used by oldest transaction before <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (default = 100).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-218"><a href="dn350975(v=exchg.10).md">MaxVerPages</a></span></span></td>
<td><span data-ttu-id="b1da3-219">Возвращает или задает максимальное число страниц хранилища версий, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-219">Gets or sets the maximum number of version store pages reserved for this instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-221"><a href="dn351001(v=exchg.10).md">ноинформатионевент</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-221"><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></span></span></td>
<td><span data-ttu-id="b1da3-222">Возвращает или задает значение, указывающее, будут ли подавлены информационные сообщения журнала событий, обычно создаваемые ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="b1da3-222">Gets or sets a value indicating whether informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-224"><a href="dn350976(v=exchg.10).md">онедатабасеперсессион</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-224"><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></span></span></td>
<td><span data-ttu-id="b1da3-225">Возвращает или задает значение, указывающее, разрешается ли открывать только одну базу данных с помощью Жетопендатабасе в заданном сеансе одновременно.</span><span class="sxs-lookup"><span data-stu-id="b1da3-225">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="b1da3-226">Временная база данных исключается из этого ограничения.</span><span class="sxs-lookup"><span data-stu-id="b1da3-226">The temporary database is excluded from this restriction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-228"><a href="dn351002(v=exchg.10).md">пажетемпдбмин</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-228"><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></span></span></td>
<td><span data-ttu-id="b1da3-229">Возвращает или задает начальный размер временной базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1da3-229">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="b1da3-230">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1da3-230">The size is in database pages.</span></span> <span data-ttu-id="b1da3-231">Нулевой размер означает, что следует использовать стандартный размер обычной базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1da3-231">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="b1da3-232">Часто нежелательно, чтобы небольшие приложения настроили временную базу данных как можно меньше.</span><span class="sxs-lookup"><span data-stu-id="b1da3-232">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="b1da3-233">Если задать для этого параметра значение <a href="dn351211(v=exchg.10).md">пажетемпдбсмаллест</a> , будет достигнута наименьшая временная база данных.</span><span class="sxs-lookup"><span data-stu-id="b1da3-233">Setting this parameter to <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> will achieve the smallest temporary database possible.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-235"><a href="dn350979(v=exchg.10).md">преферредверпажес</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-235"><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></span></span></td>
<td><span data-ttu-id="b1da3-236">Возвращает или задает предпочтительное количество страниц хранилища версий, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-236">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="b1da3-237">Если размер хранилища версий превышает это пороговое значение, то любая информация, которая используется только для необязательных фоновых задач, таких как освобождение места на удаленном диске в базе данных, задается для сохранения сведений о транзакциях.</span><span class="sxs-lookup"><span data-stu-id="b1da3-237">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-239"><a href="dn351004(v=exchg.10).md">пререадиомакс</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-239"><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></span></span></td>
<td><span data-ttu-id="b1da3-240">Возвращает или задает максимальное количество операций ввода-вывода, отправленных для данной цели.</span><span class="sxs-lookup"><span data-stu-id="b1da3-240">Gets or sets the maximum number of I/O operations dispatched for a given purpose.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-242"><a href="dn350981(v=exchg.10).md">Восстановление</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-242"><a href="dn350981(v=exchg.10).md">Recovery</a></span></span></td>
<td><span data-ttu-id="b1da3-243">Возвращает или задает значение, указывающее, включено ли восстановление после сбоя.</span><span class="sxs-lookup"><span data-stu-id="b1da3-243">Gets or sets a value indicating whether crash recovery is on.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-245"><a href="dn351007(v=exchg.10).md">системдиректори</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-245"><a href="dn351007(v=exchg.10).md">SystemDirectory</a></span></span></td>
<td><span data-ttu-id="b1da3-246">Возвращает или задает относительный или абсолютный путь файловой системы к папке, которая будет содержать файл контрольных точек для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-246">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-248"><a href="dn350983(v=exchg.10).md">TempDirectory</a></span></span></td>
<td><span data-ttu-id="b1da3-249">Возвращает или задает относительный или абсолютный путь файловой системы к папке, которая будет содержать временную базу данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1da3-249">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-251"><a href="dn351008(v=exchg.10).md">версионсторетасккуеуемакс</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-251"><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></span></span></td>
<td><span data-ttu-id="b1da3-252">Возвращает или задает количество рабочих элементов фоновой очистки, которые могут быть поставлены в очередь пула потоков компонента Database Engine в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="b1da3-252">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /></td>
<td><span data-ttu-id="b1da3-254"><a href="dn350985(v=exchg.10).md">вайпоинтлатенци</a></span><span class="sxs-lookup"><span data-stu-id="b1da3-254"><a href="dn350985(v=exchg.10).md">WaypointLatency</a></span></span></td>
<td><span data-ttu-id="b1da3-255">Возвращает или задает число журналов, в которых ESENT будет откладывать сбросы базы данных для.</span><span class="sxs-lookup"><span data-stu-id="b1da3-255">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="b1da3-256">Это можно использовать для повышения возможности восстановления базы данных, если ошибки приводят к потере файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="b1da3-256">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="b1da3-257">Поддерживается в Windows 7 и выше.</span><span class="sxs-lookup"><span data-stu-id="b1da3-257">Supported on Windows 7 and up.</span></span> <span data-ttu-id="b1da3-258">Игнорируется в Windows XP, Windows Server 2003, Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b1da3-258">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1da3-259">Начало</span><span class="sxs-lookup"><span data-stu-id="b1da3-259">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b1da3-260">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1da3-260">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1da3-261">Справочник</span><span class="sxs-lookup"><span data-stu-id="b1da3-261">Reference</span></span>

[<span data-ttu-id="b1da3-262">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="b1da3-262">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="b1da3-263">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b1da3-263">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
