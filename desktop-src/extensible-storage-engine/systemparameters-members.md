---
description: 'Дополнительные сведения о: SystemParameters Members'
title: Элементы SystemParameters
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e317ef4e63a33951dc55e030718d226ae3eaeec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565273"
---
# <a name="systemparameters-members"></a><span data-ttu-id="edbda-103">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="edbda-103">SystemParameters members</span></span>

<span data-ttu-id="edbda-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="edbda-104">Include protected members</span></span>  
<span data-ttu-id="edbda-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="edbda-105">Include inherited members</span></span>  

<span data-ttu-id="edbda-106">Константы для API ESENT.</span><span class="sxs-lookup"><span data-stu-id="edbda-106">Constants for the ESENT API.</span></span> <span data-ttu-id="edbda-107">Их не нужно искать с помощью системных параметров.</span><span class="sxs-lookup"><span data-stu-id="edbda-107">These don't have to be looked up via system parameters.</span></span> <span data-ttu-id="edbda-108">Этот класс предоставляет статические свойства для установки и получения глобальных системных параметров ESENT.</span><span class="sxs-lookup"><span data-stu-id="edbda-108">This class provides static properties to set and get global ESENT system parameters.</span></span> <span data-ttu-id="edbda-109">Этот класс предоставляет статические свойства для установки и получения глобальных системных параметров ESENT.</span><span class="sxs-lookup"><span data-stu-id="edbda-109">This class provides static properties to set and get global ESENT system parameters.</span></span>

<span data-ttu-id="edbda-110">Тип [SystemParameters](./systemparameters-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="edbda-110">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="edbda-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="edbda-111">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="edbda-112">Имя</span><span class="sxs-lookup"><span data-stu-id="edbda-112">Name</span></span></th>
<th><span data-ttu-id="edbda-113">Описание</span><span class="sxs-lookup"><span data-stu-id="edbda-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-116"><a href="dn351215(v=exchg.10).md">букмаркмост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-116"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="edbda-117">Возвращает максимальный размер закладки.</span><span class="sxs-lookup"><span data-stu-id="edbda-117">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="edbda-118"><a href="dn292149(v=exchg.10).md">Жетжетбукмарк (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="edbda-118"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="edbda-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="edbda-122">Возвращает или задает размер кэша базы данных на страницах.</span><span class="sxs-lookup"><span data-stu-id="edbda-122">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="edbda-123">По умолчанию кэш базы данных автоматически настраивает свой размер, а установка этого свойства в ненулевое значение приводит к тому, что кэш подстраивается к целевому размеру.</span><span class="sxs-lookup"><span data-stu-id="edbda-123">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-126"><a href="dn351149(v=exchg.10).md">качесиземакс</a></span><span class="sxs-lookup"><span data-stu-id="edbda-126"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="edbda-127">Возвращает или задает максимальный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-127">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="edbda-128">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-128">The size is in database pages.</span></span> <span data-ttu-id="edbda-129">Если этот параметр оставлен со значением по умолчанию, максимальный размер кэша будет установлен в размер физической памяти при вызове Жетинит.</span><span class="sxs-lookup"><span data-stu-id="edbda-129">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-132"><a href="dn351216(v=exchg.10).md">качесиземин</a></span><span class="sxs-lookup"><span data-stu-id="edbda-132"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="edbda-133">Возвращает или задает минимальный размер кэша страниц базы данных в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-133">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-136"><a href="dn351151(v=exchg.10).md">колумнскэймост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-136"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="edbda-137">Возвращает максимальное число компонентов в ключе сортировки или индекса.</span><span class="sxs-lookup"><span data-stu-id="edbda-137">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-140"><a href="dn351218(v=exchg.10).md">Конфигурация</a></span><span class="sxs-lookup"><span data-stu-id="edbda-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="edbda-141">Возвращает или задает значение, указывающее значения по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="edbda-141">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="edbda-142">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="edbda-142">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="edbda-143">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="edbda-143">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="edbda-144">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="edbda-144">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="edbda-145">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="edbda-145">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="edbda-146">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="edbda-146">Supported on Windows Vista and up.</span></span> <span data-ttu-id="edbda-147">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="edbda-147">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-150"><a href="dn351153(v=exchg.10).md">датабасепажесизе</a></span><span class="sxs-lookup"><span data-stu-id="edbda-150"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="edbda-151">Возвращает или задает размер страниц базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="edbda-151">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-154"><a href="dn351221(v=exchg.10).md">енаблеадванцед</a></span><span class="sxs-lookup"><span data-stu-id="edbda-154"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="edbda-155">Возвращает или задает значение, указывающее, принимает ли ядро СУБД изменения, внесенные в подмножество системных параметров, или отклоняет их.</span><span class="sxs-lookup"><span data-stu-id="edbda-155">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="edbda-156">Этот параметр используется вместе с <a href="dn351218(v=exchg.10).md">конфигурацией</a> , чтобы предотвратить установку некоторых параметров системы из значений по умолчанию выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="edbda-156">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="edbda-157">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="edbda-157">Supported on Windows Vista and up.</span></span> <span data-ttu-id="edbda-158">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="edbda-158">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-161"><a href="dn351152(v=exchg.10).md">енаблефилекаче</a></span><span class="sxs-lookup"><span data-stu-id="edbda-161"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="edbda-162">Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать кэш файлов ОС для всех управляемых файлов.</span><span class="sxs-lookup"><span data-stu-id="edbda-162">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-165"><a href="dn351220(v=exchg.10).md">енаблевиевкаче</a></span><span class="sxs-lookup"><span data-stu-id="edbda-165"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="edbda-166">Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать файловый ввод-вывод, размещенный в памяти, для файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-166">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-169"><a href="dn351223(v=exchg.10).md">евентлоггинглевел</a></span><span class="sxs-lookup"><span data-stu-id="edbda-169"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="edbda-170">Возвращает или задает уровень детализации сообщений журнала событий, которые передаются в журнал событий ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="edbda-170">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="edbda-171">Более высокие значения приводят к более подробным сообщениям журнала событий.</span><span class="sxs-lookup"><span data-stu-id="edbda-171">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-174"><a href="dn351154(v=exchg.10).md">ексцептионактион</a></span><span class="sxs-lookup"><span data-stu-id="edbda-174"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="edbda-175">Возвращает или задает кодировку значений, выполняемых с исключениями, созданными в JET.</span><span class="sxs-lookup"><span data-stu-id="edbda-175">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-178"><a href="dn351227(v=exchg.10).md">хунгиоактионс</a></span><span class="sxs-lookup"><span data-stu-id="edbda-178"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="edbda-179">Возвращает или задает набор действий, выполняемых в IOs, которые отображаются как зависые.</span><span class="sxs-lookup"><span data-stu-id="edbda-179">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-182"><a href="dn351155(v=exchg.10).md">хунгиосрешолд</a></span><span class="sxs-lookup"><span data-stu-id="edbda-182"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="edbda-183">Возвращает или задает пороговое значение для того, что считается незавершенным вводом-выводом.</span><span class="sxs-lookup"><span data-stu-id="edbda-183">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-186"><a href="dn351156(v=exchg.10).md">кэймост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-186"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="edbda-187">Возвращает максимальный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="edbda-187">Gets the maximum key size.</span></span> <span data-ttu-id="edbda-188">Это зависит от версии ESENT и размера страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-188">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-191"><a href="dn351229(v=exchg.10).md">легацифиленамес</a></span><span class="sxs-lookup"><span data-stu-id="edbda-191"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="edbda-192">Возвращает или задает обратную совместимость с соглашениями об именовании файлов более ранних выпусков ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="edbda-192">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-195"><a href="dn351157(v=exchg.10).md">лвчунксиземост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-195"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="edbda-196">Возвращает размер фрагментов lv.</span><span class="sxs-lookup"><span data-stu-id="edbda-196">Gets the lv chunks size.</span></span> <span data-ttu-id="edbda-197">Это зависит от размера страницы базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-197">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-200"><a href="dn351230(v=exchg.10).md">максинстанцес</a></span><span class="sxs-lookup"><span data-stu-id="edbda-200"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="edbda-201">Возвращает или задает максимальное количество экземпляров, которые могут быть созданы.</span><span class="sxs-lookup"><span data-stu-id="edbda-201">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-204"><a href="dn351160(v=exchg.10).md">миндатафоркспресс</a></span><span class="sxs-lookup"><span data-stu-id="edbda-204"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="edbda-205">Возвращает или задает наименьший объем данных, которые должны быть сжаты с помощью сжатия Xpress.</span><span class="sxs-lookup"><span data-stu-id="edbda-205">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-208"><a href="dn351159(v=exchg.10).md">аутстандингиомакс</a></span><span class="sxs-lookup"><span data-stu-id="edbda-208"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="edbda-209">Этот параметр определяет, сколько операций ввода-вывода в файле базы данных может быть помещено в очередь на диск в операционной системе узла.</span><span class="sxs-lookup"><span data-stu-id="edbda-209">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="edbda-210">Большее значение этого параметра может значительно помочь в производительности большого приложения базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-210">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-213"><a href="dn351158(v=exchg.10).md">процессфриендлинаме</a></span><span class="sxs-lookup"><span data-stu-id="edbda-213"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="edbda-214">Возвращает или задает понятное имя для данного экземпляра процесса.</span><span class="sxs-lookup"><span data-stu-id="edbda-214">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-217"><a href="dn351161(v=exchg.10).md">стартфлушсрешолд</a></span><span class="sxs-lookup"><span data-stu-id="edbda-217"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="edbda-218">Возвращает или задает пороговое значение, при котором кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="edbda-218">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="edbda-219">Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов.</span><span class="sxs-lookup"><span data-stu-id="edbda-219">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="edbda-220">Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="edbda-220">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="edbda-221">Это пороговое значение также должно быть меньше порога окончания, установленного JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="edbda-221">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="edbda-222">Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их.</span><span class="sxs-lookup"><span data-stu-id="edbda-222">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="edbda-223">При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование.</span><span class="sxs-lookup"><span data-stu-id="edbda-223">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="edbda-224">Тем не менее, при высоком пороговом значении приостанавливается более высокий порог, что уменьшает эффективный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-224">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Открытое свойство" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-227"><a href="dn351231(v=exchg.10).md">стопфлушсрешолд</a></span><span class="sxs-lookup"><span data-stu-id="edbda-227"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="edbda-228">Возвращает или задает пороговое значение, при котором кэш страниц базы данных завершает исключение страниц из кэша, освобождая пространство для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="edbda-228">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="edbda-229">Когда количество буферов страниц в кэше превышает это пороговое значение, фоновый процесс, который был запущен для пополнения пула доступных буферов, останавливается.</span><span class="sxs-lookup"><span data-stu-id="edbda-229">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="edbda-230">Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="edbda-230">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="edbda-231">Это пороговое значение также должно быть больше, чем пороговое значение начала, заданное JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="edbda-231">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="edbda-232">Расстояние между пороговым значением начала и порогом окончания влияет на эффективность, с которой страницы базы данных сбрасываются фоновым процессом.</span><span class="sxs-lookup"><span data-stu-id="edbda-232">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="edbda-233">Чем больше промежуток, тем больше вероятность, что записи на соседние страницы могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="edbda-233">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="edbda-234">Однако при высоком пороговом значении будет уменьшен эффективный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-234">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edbda-235">Начало</span><span class="sxs-lookup"><span data-stu-id="edbda-235">Top</span></span>

## <a name="fields"></a><span data-ttu-id="edbda-236">Поля</span><span class="sxs-lookup"><span data-stu-id="edbda-236">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="edbda-237">name</span><span class="sxs-lookup"><span data-stu-id="edbda-237">Name</span></span></th>
<th><span data-ttu-id="edbda-238">Описание</span><span class="sxs-lookup"><span data-stu-id="edbda-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-241"><a href="dn351208(v=exchg.10).md">басенамеленгс</a></span><span class="sxs-lookup"><span data-stu-id="edbda-241"><a href="dn351208(v=exchg.10).md">BaseNameLength</a></span></span></td>
<td><span data-ttu-id="edbda-242">Длина префикса, используемого для имен файлов, используемых ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="edbda-242">The length of the prefix used to name files used by the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-245"><a href="dn351146(v=exchg.10).md">колумнмост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-245"><a href="dn351146(v=exchg.10).md">ColumnMost</a></span></span></td>
<td><span data-ttu-id="edbda-246">Максимальный размер для столбцов, которые не JET_coltyp. Лонгбинари или JET_coltyp. LongText.</span><span class="sxs-lookup"><span data-stu-id="edbda-246">Maximum size for columns which are not JET_coltyp.LongBinary or JET_coltyp.LongText.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-249"><a href="dn351210(v=exchg.10).md">колумнсфикседмост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-249"><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></span></span></td>
<td><span data-ttu-id="edbda-250">Максимально допустимое число фиксированных столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="edbda-250">Maximum number of fixed columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-253"><a href="dn351140(v=exchg.10).md">колумнсмост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-253"><a href="dn351140(v=exchg.10).md">ColumnsMost</a></span></span></td>
<td><span data-ttu-id="edbda-254">Максимально допустимое число столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="edbda-254">Maximum number of columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-257"><a href="dn351148(v=exchg.10).md">колумнстагжедмост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-257"><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></span></span></td>
<td><span data-ttu-id="edbda-258">Максимальное число столбцов с тегами, разрешенных в таблице.</span><span class="sxs-lookup"><span data-stu-id="edbda-258">Maximum number of tagged columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-261"><a href="dn351212(v=exchg.10).md">колумнсвармост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-261"><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></span></span></td>
<td><span data-ttu-id="edbda-262">Максимальное число столбцов переменной длины, разрешенное в таблице.</span><span class="sxs-lookup"><span data-stu-id="edbda-262">Maximum number of variable-length columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-265"><a href="dn351141(v=exchg.10).md">локаленамемаксленгс</a></span><span class="sxs-lookup"><span data-stu-id="edbda-265"><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></span></span></td>
<td><span data-ttu-id="edbda-266">Максимальная длина имени локали (LOCALE_NAME_MAX_LENGTH из Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="edbda-266">The maximum length of a locale name (LOCALE_NAME_MAX_LENGTH from winnt.h).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-269"><a href="dn351213(v=exchg.10).md">намемост</a></span><span class="sxs-lookup"><span data-stu-id="edbda-269"><a href="dn351213(v=exchg.10).md">NameMost</a></span></span></td>
<td><span data-ttu-id="edbda-270">Максимальный размер имени таблицы, столбца или индекса.</span><span class="sxs-lookup"><span data-stu-id="edbda-270">Maximum size of a table/column/index name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="edbda-273"><a href="dn351211(v=exchg.10).md">пажетемпдбсмаллест</a></span><span class="sxs-lookup"><span data-stu-id="edbda-273"><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></span></span></td>
<td><span data-ttu-id="edbda-274">Количество страниц, которые предоставляют наименьшую возможную временную базу данных.</span><span class="sxs-lookup"><span data-stu-id="edbda-274">The number of pages that gives the smallest possible temporary database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edbda-275">Начало</span><span class="sxs-lookup"><span data-stu-id="edbda-275">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="edbda-276">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edbda-276">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="edbda-277">Справочник</span><span class="sxs-lookup"><span data-stu-id="edbda-277">Reference</span></span>

[<span data-ttu-id="edbda-278">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="edbda-278">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="edbda-279">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="edbda-279">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
