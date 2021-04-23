---
description: В стандартном модуле слияния требуются следующие таблицы.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Таблицы базы данных модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674157"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="9e51c-103">Таблицы базы данных модуля слияния</span><span class="sxs-lookup"><span data-stu-id="9e51c-103">Merge Module Database Tables</span></span>

<span data-ttu-id="9e51c-104">В стандартном модуле слияния требуются следующие таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e51c-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="9e51c-105">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="9e51c-105">Table name</span></span>                                       | <span data-ttu-id="9e51c-106">Комментировать</span><span class="sxs-lookup"><span data-stu-id="9e51c-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e51c-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="9e51c-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="9e51c-108">НЕОБХОДИМОСТИ</span><span class="sxs-lookup"><span data-stu-id="9e51c-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="9e51c-109">Каталог</span><span class="sxs-lookup"><span data-stu-id="9e51c-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="9e51c-110">НЕОБХОДИМОСТИ</span><span class="sxs-lookup"><span data-stu-id="9e51c-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="9e51c-111">феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="9e51c-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="9e51c-112">НЕОБХОДИМОСТИ</span><span class="sxs-lookup"><span data-stu-id="9e51c-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="9e51c-113">Файл</span><span class="sxs-lookup"><span data-stu-id="9e51c-113">File</span></span>](file-table.md)                           | <span data-ttu-id="9e51c-114">НЕОБХОДИМОСТИ</span><span class="sxs-lookup"><span data-stu-id="9e51c-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="9e51c-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="9e51c-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="9e51c-116">НЕОБХОДИМОСТИ Слияние с базой данных установщика.</span><span class="sxs-lookup"><span data-stu-id="9e51c-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="9e51c-117">Содержит сведения, идентифицирующие модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="9e51c-118">модулекомпонентс</span><span class="sxs-lookup"><span data-stu-id="9e51c-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="9e51c-119">НЕОБХОДИМОСТИ Слияние с базой данных установщика.</span><span class="sxs-lookup"><span data-stu-id="9e51c-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="9e51c-120">Список всех компонентов в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="9e51c-121">Следующие таблицы происходят только в модулях слияния или в других базах данных установщика, которые уже объединены с модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="9e51c-122">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="9e51c-122">Table name</span></span>                                     | <span data-ttu-id="9e51c-123">Комментировать</span><span class="sxs-lookup"><span data-stu-id="9e51c-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e51c-124">модуледепенденци</span><span class="sxs-lookup"><span data-stu-id="9e51c-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="9e51c-125">Слияние с базой данных установщика.</span><span class="sxs-lookup"><span data-stu-id="9e51c-125">Merged into the installer database.</span></span> <span data-ttu-id="9e51c-126">Список других модулей слияния, необходимых для этого модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="9e51c-127">модуликсклусион</span><span class="sxs-lookup"><span data-stu-id="9e51c-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="9e51c-128">Слияние с базой данных установщика.</span><span class="sxs-lookup"><span data-stu-id="9e51c-128">Merged into the installer database.</span></span> <span data-ttu-id="9e51c-129">Список других модулей слияния, несовместимых с этим модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="9e51c-130">Следующие таблицы Модулесекуенце встречаются только в модулях слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="9e51c-131">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="9e51c-131">Table name</span></span>                                                             | <span data-ttu-id="9e51c-132">Комментировать</span><span class="sxs-lookup"><span data-stu-id="9e51c-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e51c-133">модулеадминуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="9e51c-134">Выполняет слияние действий в [таблицу админуисекуенце](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="9e51c-135">модулеадминексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="9e51c-136">Выполняет слияние действий в [таблицу админексекутесекуенце](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="9e51c-137">модулеадвтуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="9e51c-138">Не используйте эту таблицу.</span><span class="sxs-lookup"><span data-stu-id="9e51c-138">Do not use this table.</span></span> <span data-ttu-id="9e51c-139">Дополнительные сведения см. в разделе [адвтуисекуенце Table](advtuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="9e51c-140">модулеадвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="9e51c-141">Выполняет слияние действий в [таблицу адвтексекутесекуенце](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="9e51c-142">модулеигноретабле</span><span class="sxs-lookup"><span data-stu-id="9e51c-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="9e51c-143">Содержит список таблиц в модуле, которые не объединены в MSI файл.</span><span class="sxs-lookup"><span data-stu-id="9e51c-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="9e51c-144">модулеинсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="9e51c-145">Выполняет слияние действий в [таблицу инсталлуисекуенце](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="9e51c-146">модулеинсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="9e51c-147">Выполняет слияние действий в [таблицу инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="9e51c-148">В каждом настраиваемом модуле слияния необходимы следующие таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e51c-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="9e51c-149">Для создания настраиваемого модуля слияния требуется Mergemod.dll 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9e51c-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="9e51c-150">Дополнительные сведения см. в разделе [настраиваемые модули слияния](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="9e51c-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="9e51c-151">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="9e51c-151">Table name</span></span>                                                 | <span data-ttu-id="9e51c-152">Комментировать</span><span class="sxs-lookup"><span data-stu-id="9e51c-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e51c-153">Таблица Модулесубститутион</span><span class="sxs-lookup"><span data-stu-id="9e51c-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="9e51c-154">НЕОБХОДИМОСТИ Эта таблица не объединяется с целевой базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="9e51c-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="9e51c-155">Задает настраиваемые поля в целевой базе данных и предоставляет шаблон для конфигурации каждого поля.</span><span class="sxs-lookup"><span data-stu-id="9e51c-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="9e51c-156">Таблица Модулеконфигуратион</span><span class="sxs-lookup"><span data-stu-id="9e51c-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="9e51c-157">НЕОБХОДИМОСТИ Эта таблица не объединяется с целевой базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="9e51c-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="9e51c-158">Определяет настраиваемые атрибуты модуля.</span><span class="sxs-lookup"><span data-stu-id="9e51c-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="9e51c-159">Следующие таблицы установщика не могут встречаться в стандартном модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="9e51c-160">ббконтрол</span><span class="sxs-lookup"><span data-stu-id="9e51c-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="9e51c-161">Печат</span><span class="sxs-lookup"><span data-stu-id="9e51c-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="9e51c-162">ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="9e51c-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="9e51c-163">Ошибка</span><span class="sxs-lookup"><span data-stu-id="9e51c-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="9e51c-164">Компонент</span><span class="sxs-lookup"><span data-stu-id="9e51c-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="9e51c-165">Таблица Лаунчкондитион</span><span class="sxs-lookup"><span data-stu-id="9e51c-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="9e51c-166">Носитель</span><span class="sxs-lookup"><span data-stu-id="9e51c-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="9e51c-167">Обновление</span><span class="sxs-lookup"><span data-stu-id="9e51c-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="9e51c-168">Обновление</span><span class="sxs-lookup"><span data-stu-id="9e51c-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="9e51c-169">Следующие таблицы установщика являются необязательными в модулях слияния.</span><span class="sxs-lookup"><span data-stu-id="9e51c-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="9e51c-170">актионтекст</span><span class="sxs-lookup"><span data-stu-id="9e51c-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="9e51c-171">админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="9e51c-172">админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="9e51c-173">адвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="9e51c-174">адвтуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="9e51c-175">AppId</span><span class="sxs-lookup"><span data-stu-id="9e51c-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="9e51c-176">аппсеарч</span><span class="sxs-lookup"><span data-stu-id="9e51c-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="9e51c-177">BindImage</span><span class="sxs-lookup"><span data-stu-id="9e51c-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="9e51c-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="9e51c-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="9e51c-179">Класс</span><span class="sxs-lookup"><span data-stu-id="9e51c-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="9e51c-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="9e51c-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="9e51c-181">комплокатор</span><span class="sxs-lookup"><span data-stu-id="9e51c-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="9e51c-182">Управление</span><span class="sxs-lookup"><span data-stu-id="9e51c-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="9e51c-183">Таблица controlcondition</span><span class="sxs-lookup"><span data-stu-id="9e51c-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="9e51c-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="9e51c-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="9e51c-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="9e51c-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="9e51c-186">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="9e51c-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="9e51c-187">дрлокатор</span><span class="sxs-lookup"><span data-stu-id="9e51c-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="9e51c-188">дупликатефиле</span><span class="sxs-lookup"><span data-stu-id="9e51c-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="9e51c-189">Среда</span><span class="sxs-lookup"><span data-stu-id="9e51c-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="9e51c-190">Таблица eventmapping</span><span class="sxs-lookup"><span data-stu-id="9e51c-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="9e51c-191">Расширение</span><span class="sxs-lookup"><span data-stu-id="9e51c-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="9e51c-192">Шрифт</span><span class="sxs-lookup"><span data-stu-id="9e51c-192">Font</span></span>](font-table.md)
-   <span data-ttu-id="9e51c-193">[Значок](icon-table.md):</span><span class="sxs-lookup"><span data-stu-id="9e51c-193">[Icon](icon-table.md)</span></span>
-   [<span data-ttu-id="9e51c-194">инифиле</span><span class="sxs-lookup"><span data-stu-id="9e51c-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="9e51c-195">инилокатор</span><span class="sxs-lookup"><span data-stu-id="9e51c-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="9e51c-196">инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="9e51c-197">инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="9e51c-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="9e51c-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="9e51c-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="9e51c-199">ListView</span><span class="sxs-lookup"><span data-stu-id="9e51c-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="9e51c-200">MIME</span><span class="sxs-lookup"><span data-stu-id="9e51c-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="9e51c-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="9e51c-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="9e51c-202">одбкаттрибуте</span><span class="sxs-lookup"><span data-stu-id="9e51c-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="9e51c-203">одбкдатасаурце</span><span class="sxs-lookup"><span data-stu-id="9e51c-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="9e51c-204">одбкдривер</span><span class="sxs-lookup"><span data-stu-id="9e51c-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="9e51c-205">одбксаурцеаттрибуте</span><span class="sxs-lookup"><span data-stu-id="9e51c-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="9e51c-206">одбктранслатор</span><span class="sxs-lookup"><span data-stu-id="9e51c-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="9e51c-207">Таблица ProgID</span><span class="sxs-lookup"><span data-stu-id="9e51c-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="9e51c-208">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e51c-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="9e51c-209">публишкомпонент</span><span class="sxs-lookup"><span data-stu-id="9e51c-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="9e51c-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="9e51c-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="9e51c-211">Таблица реестра</span><span class="sxs-lookup"><span data-stu-id="9e51c-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="9e51c-212">реглокатор</span><span class="sxs-lookup"><span data-stu-id="9e51c-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="9e51c-213">ремовефиле</span><span class="sxs-lookup"><span data-stu-id="9e51c-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="9e51c-214">ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="9e51c-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="9e51c-215">ремоверегистри</span><span class="sxs-lookup"><span data-stu-id="9e51c-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="9e51c-216">ресервекост</span><span class="sxs-lookup"><span data-stu-id="9e51c-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="9e51c-217">селфрег</span><span class="sxs-lookup"><span data-stu-id="9e51c-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="9e51c-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="9e51c-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="9e51c-219">сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="9e51c-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="9e51c-220">Клавиша</span><span class="sxs-lookup"><span data-stu-id="9e51c-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="9e51c-221">Образец</span><span class="sxs-lookup"><span data-stu-id="9e51c-221">Signature</span></span>](signature-table.md)
-   [<span data-ttu-id="9e51c-222">Система создала шрифт</span><span class="sxs-lookup"><span data-stu-id="9e51c-222">TextStyle</span></span>](textstyle-table.md)
-   [<span data-ttu-id="9e51c-223">Экспорт Typelib</span><span class="sxs-lookup"><span data-stu-id="9e51c-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="9e51c-224">уитекст</span><span class="sxs-lookup"><span data-stu-id="9e51c-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="9e51c-225">Команда</span><span class="sxs-lookup"><span data-stu-id="9e51c-225">Verb</span></span>](verb-table.md)

 

 



