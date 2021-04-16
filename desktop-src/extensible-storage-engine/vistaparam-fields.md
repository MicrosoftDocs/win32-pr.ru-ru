---
description: 'Дополнительные сведения о: Вистапарам Fields'
title: Поля Вистапарам (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6e20c4b784b9a4421c447f24d5736d7c6ef67f41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565699"
---
# <a name="vistaparam-fields"></a><span data-ttu-id="b2d63-103">Поля Вистапарам</span><span class="sxs-lookup"><span data-stu-id="b2d63-103">VistaParam fields</span></span>

<span data-ttu-id="b2d63-104">Включить защищенные члены</span><span class="sxs-lookup"><span data-stu-id="b2d63-104">Include protected members</span></span>  
<span data-ttu-id="b2d63-105">Включить унаследованные члены</span><span class="sxs-lookup"><span data-stu-id="b2d63-105">Include inherited members</span></span>  

<span data-ttu-id="b2d63-106">Тип [вистапарам](./vistaparam-class.md) предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="b2d63-106">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="b2d63-107">Поля</span><span class="sxs-lookup"><span data-stu-id="b2d63-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b2d63-108">name</span><span class="sxs-lookup"><span data-stu-id="b2d63-108">Name</span></span></th>
<th><span data-ttu-id="b2d63-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b2d63-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-112"><a href="dn335379(v=exchg.10).md">качедклоседтаблес</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="b2d63-113">Этот параметр определяет количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением.</span><span class="sxs-lookup"><span data-stu-id="b2d63-113">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="b2d63-114">Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц.</span><span class="sxs-lookup"><span data-stu-id="b2d63-114">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="b2d63-115">Это полезно для приложений, имеющих схему с очень большим количеством таблиц.</span><span class="sxs-lookup"><span data-stu-id="b2d63-115">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-118"><a href="dn335289(v=exchg.10).md">Конфигурация</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-118"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="b2d63-119">Этот параметр предоставляет несколько наборов значений по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="b2d63-119">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="b2d63-120">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b2d63-120">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="b2d63-121">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2d63-121">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="b2d63-122">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="b2d63-122">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="b2d63-123">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2d63-123">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-126"><a href="dn335380(v=exchg.10).md">енаблеадванцед</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="b2d63-127">Этот параметр используется для управления тем, когда ядро СУБД принимает или отклоняет изменения в подмножестве системных параметров.</span><span class="sxs-lookup"><span data-stu-id="b2d63-127">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="b2d63-128">Этот параметр используется вместе с <a href="dn335289(v=exchg.10).md">конфигурацией</a> , чтобы предотвратить установку некоторых параметров системы из значений по умолчанию выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b2d63-128">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-131"><a href="dn335291(v=exchg.10).md">енаблефилекаче</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="b2d63-132">Разрешить использование кэша файлов операционной системы для всех управляемых файлов.</span><span class="sxs-lookup"><span data-stu-id="b2d63-132">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-135"><a href="dn335381(v=exchg.10).md">енаблевиевкаче</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="b2d63-136">Позволяет использовать файловый ввод-вывод, сопоставленный с памятью, для файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="b2d63-136">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-139"><a href="dn335292(v=exchg.10).md">кэймост</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-139"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="b2d63-140">Этот параметр только для чтения указывает максимальную допустимую длину ключа индекса, которую можно выбрать для текущего размера страницы базы данных (согласно настройкам <a href="hh596135(v=exchg.10).md">датабасепажесизе</a>).</span><span class="sxs-lookup"><span data-stu-id="b2d63-140">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-143"><a href="dn335384(v=exchg.10).md">легацифиленамес</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="b2d63-144">Этот параметр обеспечивает обратную совместимость с соглашениями об именовании файлов более ранних версий ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="b2d63-144">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="b2d63-148">Задайте имя, связанное с классом таблицы 10.</span><span class="sxs-lookup"><span data-stu-id="b2d63-148">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="b2d63-152">Задайте имя, связанное с классом таблицы 11.</span><span class="sxs-lookup"><span data-stu-id="b2d63-152">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="b2d63-156">Задайте имя, связанное с классом Table 12.</span><span class="sxs-lookup"><span data-stu-id="b2d63-156">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="b2d63-160">Задайте имя, связанное с классом таблицы 13.</span><span class="sxs-lookup"><span data-stu-id="b2d63-160">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="b2d63-164">Задайте имя, связанное с классом таблицы 14.</span><span class="sxs-lookup"><span data-stu-id="b2d63-164">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="b2d63-168">Задайте имя, связанное с классом таблицы 15.</span><span class="sxs-lookup"><span data-stu-id="b2d63-168">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="b2d63-172">Задайте имя, связанное с классом таблицы 1.</span><span class="sxs-lookup"><span data-stu-id="b2d63-172">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="b2d63-176">Задайте имя, связанное с классом таблицы 2.</span><span class="sxs-lookup"><span data-stu-id="b2d63-176">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="b2d63-180">Задайте имя, связанное с классом таблицы 3.</span><span class="sxs-lookup"><span data-stu-id="b2d63-180">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="b2d63-184">Задайте имя, связанное с классом 4 таблицы.</span><span class="sxs-lookup"><span data-stu-id="b2d63-184">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="b2d63-188">Задайте имя, связанное с классом таблицы 5.</span><span class="sxs-lookup"><span data-stu-id="b2d63-188">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="b2d63-192">Задайте имя, связанное с классом таблицы 6.</span><span class="sxs-lookup"><span data-stu-id="b2d63-192">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="b2d63-196">Задайте имя, связанное с классом таблицы 7.</span><span class="sxs-lookup"><span data-stu-id="b2d63-196">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="b2d63-200">Задайте имя, связанное с классом таблицы 8.</span><span class="sxs-lookup"><span data-stu-id="b2d63-200">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Открытое поле" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Статический член" alt="Static member" /></td>
<td><span data-ttu-id="b2d63-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="b2d63-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="b2d63-204">Задайте имя, связанное с классом таблицы 9.</span><span class="sxs-lookup"><span data-stu-id="b2d63-204">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b2d63-205">Начало</span><span class="sxs-lookup"><span data-stu-id="b2d63-205">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b2d63-206">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2d63-206">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2d63-207">Справочник</span><span class="sxs-lookup"><span data-stu-id="b2d63-207">Reference</span></span>

[<span data-ttu-id="b2d63-208">Класс Вистапарам</span><span class="sxs-lookup"><span data-stu-id="b2d63-208">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="b2d63-209">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="b2d63-209">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
