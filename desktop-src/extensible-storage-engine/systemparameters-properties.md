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
# <a name="systemparameters-properties"></a><span data-ttu-id="ce282-103">Свойства SystemParameters</span><span class="sxs-lookup"><span data-stu-id="ce282-103">SystemParameters properties</span></span>

<span data-ttu-id="ce282-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="ce282-104">Include protected members</span></span>  
<span data-ttu-id="ce282-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="ce282-105">Include inherited members</span></span>  

<span data-ttu-id="ce282-106">Тип [SystemParameters](./systemparameters-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="ce282-106">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="ce282-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce282-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ce282-108">Имя</span><span class="sxs-lookup"><span data-stu-id="ce282-108">Name</span></span></th>
<th><span data-ttu-id="ce282-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ce282-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-112"><a href="dn351215(v=exchg.10).md">букмаркмост</a></span><span class="sxs-lookup"><span data-stu-id="ce282-112"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="ce282-113">Возвращает максимальный размер закладки.</span><span class="sxs-lookup"><span data-stu-id="ce282-113">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="ce282-114"><a href="dn292149(v=exchg.10).md">Жетжетбукмарк (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="ce282-114"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="ce282-117"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="ce282-118">Возвращает или задает размер кэша базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="ce282-118">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="ce282-119">По умолчанию кэш базы данных автоматически настраивает свой размер, а установка этого свойства в ненулевое значение приводит к тому, что кэш подстраивается к целевому размеру.</span><span class="sxs-lookup"><span data-stu-id="ce282-119">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-122"><a href="dn351149(v=exchg.10).md">качесиземакс</a></span><span class="sxs-lookup"><span data-stu-id="ce282-122"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="ce282-123">Возвращает или задает максимальный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-123">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="ce282-124">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-124">The size is in database pages.</span></span> <span data-ttu-id="ce282-125">Если этот параметр оставлен со значением по умолчанию, максимальный размер кэша будет установлен в размер физической памяти при вызове Жетинит.</span><span class="sxs-lookup"><span data-stu-id="ce282-125">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-128"><a href="dn351216(v=exchg.10).md">качесиземин</a></span><span class="sxs-lookup"><span data-stu-id="ce282-128"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="ce282-129">Возвращает или задает минимальный размер кэша страниц базы данных в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-129">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-132"><a href="dn351151(v=exchg.10).md">колумнскэймост</a></span><span class="sxs-lookup"><span data-stu-id="ce282-132"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="ce282-133">Возвращает максимальное число компонентов в ключе сортировки или индекса.</span><span class="sxs-lookup"><span data-stu-id="ce282-133">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-136"><a href="dn351218(v=exchg.10).md">Конфигурация</a></span><span class="sxs-lookup"><span data-stu-id="ce282-136"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="ce282-137">Возвращает или задает значение, указывающее значения по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="ce282-137">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="ce282-138">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ce282-138">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="ce282-139">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce282-139">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="ce282-140">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="ce282-140">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="ce282-141">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce282-141">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="ce282-142">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="ce282-142">Supported on Windows Vista and up.</span></span> <span data-ttu-id="ce282-143">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce282-143">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-146"><a href="dn351153(v=exchg.10).md">датабасепажесизе</a></span><span class="sxs-lookup"><span data-stu-id="ce282-146"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="ce282-147">Возвращает или задает размер страниц базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="ce282-147">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-150"><a href="dn351221(v=exchg.10).md">енаблеадванцед</a></span><span class="sxs-lookup"><span data-stu-id="ce282-150"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="ce282-151">Возвращает или задает значение, указывающее, принимает ли ядро СУБД изменения, внесенные в подмножество системных параметров, или отклоняет их.</span><span class="sxs-lookup"><span data-stu-id="ce282-151">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="ce282-152">Этот параметр используется вместе с <a href="dn351218(v=exchg.10).md">конфигурацией</a> , чтобы предотвратить установку некоторых параметров системы из значений по умолчанию выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ce282-152">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="ce282-153">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="ce282-153">Supported on Windows Vista and up.</span></span> <span data-ttu-id="ce282-154">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce282-154">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-157"><a href="dn351152(v=exchg.10).md">енаблефилекаче</a></span><span class="sxs-lookup"><span data-stu-id="ce282-157"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="ce282-158">Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать кэш файлов ОС для всех управляемых файлов.</span><span class="sxs-lookup"><span data-stu-id="ce282-158">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-161"><a href="dn351220(v=exchg.10).md">енаблевиевкаче</a></span><span class="sxs-lookup"><span data-stu-id="ce282-161"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="ce282-162">Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать файловый ввод-вывод, размещенный в памяти, для файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-162">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-165"><a href="dn351223(v=exchg.10).md">евентлоггинглевел</a></span><span class="sxs-lookup"><span data-stu-id="ce282-165"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="ce282-166">Возвращает или задает уровень детализации сообщений журнала событий, которые передаются в журнал событий ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="ce282-166">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="ce282-167">Более высокие значения приводят к более подробным сообщениям журнала событий.</span><span class="sxs-lookup"><span data-stu-id="ce282-167">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-170"><a href="dn351154(v=exchg.10).md">ексцептионактион</a></span><span class="sxs-lookup"><span data-stu-id="ce282-170"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="ce282-171">Возвращает или задает кодировку значений, выполняемых с исключениями, созданными в JET.</span><span class="sxs-lookup"><span data-stu-id="ce282-171">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-174"><a href="dn351227(v=exchg.10).md">хунгиоактионс</a></span><span class="sxs-lookup"><span data-stu-id="ce282-174"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="ce282-175">Возвращает или задает набор действий, выполняемых в IOs, которые отображаются как зависые.</span><span class="sxs-lookup"><span data-stu-id="ce282-175">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-178"><a href="dn351155(v=exchg.10).md">хунгиосрешолд</a></span><span class="sxs-lookup"><span data-stu-id="ce282-178"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="ce282-179">Возвращает или задает пороговое значение для того, что считается незавершенным вводом-выводом.</span><span class="sxs-lookup"><span data-stu-id="ce282-179">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-182"><a href="dn351156(v=exchg.10).md">кэймост</a></span><span class="sxs-lookup"><span data-stu-id="ce282-182"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="ce282-183">Возвращает максимальный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="ce282-183">Gets the maximum key size.</span></span> <span data-ttu-id="ce282-184">Это зависит от версии ESENT и размера страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-184">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-187"><a href="dn351229(v=exchg.10).md">легацифиленамес</a></span><span class="sxs-lookup"><span data-stu-id="ce282-187"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="ce282-188">Возвращает или задает обратную совместимость с соглашениями об именовании файлов более ранних выпусков ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="ce282-188">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-191"><a href="dn351157(v=exchg.10).md">лвчунксиземост</a></span><span class="sxs-lookup"><span data-stu-id="ce282-191"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="ce282-192">Возвращает размер фрагментов lv.</span><span class="sxs-lookup"><span data-stu-id="ce282-192">Gets the lv chunks size.</span></span> <span data-ttu-id="ce282-193">Это зависит от размера страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-193">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-196"><a href="dn351230(v=exchg.10).md">максинстанцес</a></span><span class="sxs-lookup"><span data-stu-id="ce282-196"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="ce282-197">Возвращает или задает максимальное количество экземпляров, которые могут быть созданы.</span><span class="sxs-lookup"><span data-stu-id="ce282-197">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-200"><a href="dn351160(v=exchg.10).md">миндатафоркспресс</a></span><span class="sxs-lookup"><span data-stu-id="ce282-200"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="ce282-201">Возвращает или задает наименьший объем данных, которые должны быть сжаты с помощью сжатия Xpress.</span><span class="sxs-lookup"><span data-stu-id="ce282-201">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-204"><a href="dn351159(v=exchg.10).md">аутстандингиомакс</a></span><span class="sxs-lookup"><span data-stu-id="ce282-204"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="ce282-205">Этот параметр определяет, сколько операций ввода-вывода в файле базы данных может быть помещено в очередь на диск в операционной системе узла.</span><span class="sxs-lookup"><span data-stu-id="ce282-205">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="ce282-206">Большее значение этого параметра может значительно помочь в производительности большого приложения базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-206">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-209"><a href="dn351158(v=exchg.10).md">процессфриендлинаме</a></span><span class="sxs-lookup"><span data-stu-id="ce282-209"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="ce282-210">Возвращает или задает понятное имя для данного экземпляра процесса.</span><span class="sxs-lookup"><span data-stu-id="ce282-210">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-213"><a href="dn351161(v=exchg.10).md">стартфлушсрешолд</a></span><span class="sxs-lookup"><span data-stu-id="ce282-213"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="ce282-214">Возвращает или задает пороговое значение, при котором кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="ce282-214">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="ce282-215">Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов.</span><span class="sxs-lookup"><span data-stu-id="ce282-215">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="ce282-216">Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="ce282-216">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="ce282-217">Это пороговое значение также должно быть меньше порога окончания, установленного JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="ce282-217">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="ce282-218">Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их.</span><span class="sxs-lookup"><span data-stu-id="ce282-218">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="ce282-219">При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование.</span><span class="sxs-lookup"><span data-stu-id="ce282-219">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="ce282-220">Тем не менее, при высоком пороговом значении приостанавливается более высокий порог, что уменьшает эффективный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-220">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ce282-223"><a href="dn351231(v=exchg.10).md">стопфлушсрешолд</a></span><span class="sxs-lookup"><span data-stu-id="ce282-223"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="ce282-224">Возвращает или задает пороговое значение, при котором кэш страниц базы данных завершает исключение страниц из кэша, освобождая пространство для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="ce282-224">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="ce282-225">Когда количество буферов страниц в кэше превышает это пороговое значение, фоновый процесс, который был запущен для пополнения пула доступных буферов, останавливается.</span><span class="sxs-lookup"><span data-stu-id="ce282-225">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="ce282-226">Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="ce282-226">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="ce282-227">Это пороговое значение также должно быть больше, чем пороговое значение начала, заданное JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="ce282-227">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="ce282-228">Расстояние между пороговым значением начала и порогом окончания влияет на эффективность, с которой страницы базы данных сбрасываются фоновым процессом.</span><span class="sxs-lookup"><span data-stu-id="ce282-228">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="ce282-229">Чем больше промежуток, тем больше вероятность, что записи на соседние страницы могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="ce282-229">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="ce282-230">Однако при высоком пороговом значении будет уменьшен эффективный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce282-230">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce282-231">Начало</span><span class="sxs-lookup"><span data-stu-id="ce282-231">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ce282-232">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce282-232">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce282-233">Справочник</span><span class="sxs-lookup"><span data-stu-id="ce282-233">Reference</span></span>

[<span data-ttu-id="ce282-234">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="ce282-234">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="ce282-235">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ce282-235">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
