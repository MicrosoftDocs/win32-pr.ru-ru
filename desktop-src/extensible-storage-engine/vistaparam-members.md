---
description: 'Дополнительные сведения о: Вистапарам Members'
title: Элементы Вистапарам (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaParam members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_members(v=EXCHG.10)
ms:contentKeyID: 55104333
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c56c8ad3a64eb08654ee893e86683e95e32af443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896697"
---
# <a name="vistaparam-members"></a><span data-ttu-id="ef8c4-103">Элементы Вистапарам</span><span class="sxs-lookup"><span data-stu-id="ef8c4-103">VistaParam members</span></span>

<span data-ttu-id="ef8c4-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="ef8c4-104">Include protected members</span></span>  
<span data-ttu-id="ef8c4-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="ef8c4-105">Include inherited members</span></span>  

<span data-ttu-id="ef8c4-106">Системные параметры, добавленные в версию ESENT для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-106">System parameters that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="ef8c4-107">Тип [вистапарам](./vistaparam-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-107">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="ef8c4-108">Поля</span><span class="sxs-lookup"><span data-stu-id="ef8c4-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ef8c4-109">name</span><span class="sxs-lookup"><span data-stu-id="ef8c4-109">Name</span></span></th>
<th><span data-ttu-id="ef8c4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ef8c4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-113"><a href="dn335379(v=exchg.10).md">качедклоседтаблес</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="ef8c4-114">Этот параметр определяет количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-114">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="ef8c4-115">Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-115">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="ef8c4-116">Это полезно для приложений, имеющих схему с очень большим количеством таблиц.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-116">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-119"><a href="dn335289(v=exchg.10).md">Конфигурация</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="ef8c4-120">Этот параметр предоставляет несколько наборов значений по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-120">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="ef8c4-121">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-121">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="ef8c4-122">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-122">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="ef8c4-123">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-123">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="ef8c4-124">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-124">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-127"><a href="dn335380(v=exchg.10).md">енаблеадванцед</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="ef8c4-128">Этот параметр используется для управления тем, когда ядро СУБД принимает или отклоняет изменения в подмножестве системных параметров.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-128">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="ef8c4-129">Этот параметр используется вместе с <a href="dn335289(v=exchg.10).md">конфигурацией</a> , чтобы предотвратить установку некоторых параметров системы из значений по умолчанию выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-129">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-132"><a href="dn335291(v=exchg.10).md">енаблефилекаче</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="ef8c4-133">Разрешить использование кэша файлов операционной системы для всех управляемых файлов.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-133">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-136"><a href="dn335381(v=exchg.10).md">енаблевиевкаче</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="ef8c4-137">Позволяет использовать файловый ввод-вывод, сопоставленный с памятью, для файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-137">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-140"><a href="dn335292(v=exchg.10).md">кэймост</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-140"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="ef8c4-141">Этот параметр только для чтения указывает максимальную допустимую длину ключа индекса, которую можно выбрать для текущего размера страницы базы данных (согласно настройкам <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>).</span><span class="sxs-lookup"><span data-stu-id="ef8c4-141">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-144"><a href="dn335384(v=exchg.10).md">легацифиленамес</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="ef8c4-145">Этот параметр обеспечивает обратную совместимость с соглашениями об именовании файлов более ранних версий ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-145">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-149">Задайте имя, связанное с классом таблицы 10.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-149">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-153">Задайте имя, связанное с классом таблицы 11.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-153">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-157">Задайте имя, связанное с классом Table 12.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-157">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-161">Задайте имя, связанное с классом таблицы 13.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-161">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-165">Задайте имя, связанное с классом таблицы 14.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-165">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-169">Задайте имя, связанное с классом таблицы 15.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-169">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-173">Задайте имя, связанное с классом таблицы 1.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-173">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-177">Задайте имя, связанное с классом таблицы 2.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-177">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-181">Задайте имя, связанное с классом таблицы 3.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-181">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-185">Задайте имя, связанное с классом 4 таблицы.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-185">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-189">Задайте имя, связанное с классом таблицы 5.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-189">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-193">Задайте имя, связанное с классом таблицы 6.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-193">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-197">Задайте имя, связанное с классом таблицы 7.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-197">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-201">Задайте имя, связанное с классом таблицы 8.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-201">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="ef8c4-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="ef8c4-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="ef8c4-205">Задайте имя, связанное с классом таблицы 9.</span><span class="sxs-lookup"><span data-stu-id="ef8c4-205">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef8c4-206">Начало</span><span class="sxs-lookup"><span data-stu-id="ef8c4-206">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ef8c4-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef8c4-207">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef8c4-208">Справочник</span><span class="sxs-lookup"><span data-stu-id="ef8c4-208">Reference</span></span>

[<span data-ttu-id="ef8c4-209">Класс Вистапарам</span><span class="sxs-lookup"><span data-stu-id="ef8c4-209">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="ef8c4-210">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="ef8c4-210">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
