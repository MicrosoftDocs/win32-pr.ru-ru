---
description: ICEM09 проверяет, безопасно ли модуль слияния обрабатывает предопределенные каталоги.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265421"
---
# <a name="icem09"></a><span data-ttu-id="63625-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="63625-103">ICEM09</span></span>

<span data-ttu-id="63625-104">ICEM09 проверяет, безопасно ли модуль слияния обрабатывает предопределенные каталоги.</span><span class="sxs-lookup"><span data-stu-id="63625-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="63625-105">Это достигается путем проверки того, что ни один компонент в модуле не устанавливает каталог в предопределенный системный каталог, например "ProgramFilesFolder" или "Programmenufolder".</span><span class="sxs-lookup"><span data-stu-id="63625-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="63625-106">Вместо этого модули должны использовать каталоги с уникальными именами (созданные с помощью соглашения об именовании модулей слияния) и использовать настраиваемые действия для соответствующего целевого каталога.</span><span class="sxs-lookup"><span data-stu-id="63625-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="63625-107">Этот подход предотвращает конфликт модулей с существующей структурой каталогов в конечной базе данных.</span><span class="sxs-lookup"><span data-stu-id="63625-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="63625-108">ICEM09 проверяет, что настраиваемые действия, необходимые для работы этого метода, не существуют (чтобы средство слияния создавало их) или существовало в правильной форме (чтобы они работали должным образом).</span><span class="sxs-lookup"><span data-stu-id="63625-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="63625-109">Ошибка при исправлении предупреждения или ошибки, о которой сообщило ICEM09, может привести к проблемам с клиентами модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="63625-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="63625-110">Строки таблицы каталогов с первичными ключами, например ProgramFilesFolder, часто существуют в базе данных. Таким образом, если компоненты модуля устанавливаются непосредственно в предопределенные каталоги, такие как ProgramFilesFolder, записи каталога в модуле могут конфликтовать с уже существующими строками.</span><span class="sxs-lookup"><span data-stu-id="63625-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="63625-111">Это условие потребует от пользователя модуля разделить исходные файлы из модуля для сопоставления с существующим исходным каталогом.</span><span class="sxs-lookup"><span data-stu-id="63625-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="63625-112">Результат</span><span class="sxs-lookup"><span data-stu-id="63625-112">Result</span></span>

<span data-ttu-id="63625-113">ICEM09 сообщает об ошибке или предупреждении, когда компонент модуля устанавливает каталог в предварительно определенный системный каталог, что приводит к конфликту имен с существующей структурой каталогов.</span><span class="sxs-lookup"><span data-stu-id="63625-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="63625-114">Пример</span><span class="sxs-lookup"><span data-stu-id="63625-114">Example</span></span>

<span data-ttu-id="63625-115">ICEM09 отправляет следующие предупреждения для модуля, содержащего отображаемые записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="63625-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="63625-116">Переименуйте каталог модуля слияния, чтобы он не совпадал со свойством установщик Windows и, следовательно, уникален.</span><span class="sxs-lookup"><span data-stu-id="63625-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="63625-117">Затем задайте свойству с тем же именем значение каталога установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="63625-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="63625-118">При разрешении каталога Каталог имеет свойство с тем же именем, поэтому расположение установки каталога является значением свойства.</span><span class="sxs-lookup"><span data-stu-id="63625-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="63625-119">Файлы перемещаются из отдельного исходного расположения в то же целевое расположение.</span><span class="sxs-lookup"><span data-stu-id="63625-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="63625-120">Этот процесс должен полностью удалить конфликты слияния.</span><span class="sxs-lookup"><span data-stu-id="63625-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="63625-121">Если действие не имеет порядкового номера 1, оно может не выполнить слияние в целевую базу данных, достаточно ранней в последовательности, чтобы эффективно работать.</span><span class="sxs-lookup"><span data-stu-id="63625-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="63625-122">Чтобы устранить это предупреждение, установите порядковый номер равным 1.</span><span class="sxs-lookup"><span data-stu-id="63625-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="63625-123">Обратите внимание, что большинство текущих средств слияния (но не некоторых старых версий) будут создавать эти настраиваемые действия во время слияния, поэтому не всегда нужно явно создавать действия в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="63625-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="63625-124">Поскольку столбец CustomAction является первичным ключом таблицы CustomAction, некоторые средства слияния могут создавать дублирующиеся действия, так как имя предварительно созданного действия отличается.</span><span class="sxs-lookup"><span data-stu-id="63625-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="63625-125">Чтобы устранить это предупреждение, присвойте действию имя, совпадающее с именем целевого каталога.</span><span class="sxs-lookup"><span data-stu-id="63625-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="63625-126">Обратите внимание, что большинство текущих средств слияния (но не некоторых старых версий) создают эти пользовательские действия во время слияния, поэтому не всегда нужно явно создавать действия в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="63625-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="63625-127">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="63625-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="63625-128">Каталог</span><span class="sxs-lookup"><span data-stu-id="63625-128">Directory</span></span>          | <span data-ttu-id="63625-129">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="63625-129">Directory\_Parent</span></span> | <span data-ttu-id="63625-130">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="63625-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="63625-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="63625-131">ProgramFilesFolder</span></span> | <span data-ttu-id="63625-132">Directory1</span><span class="sxs-lookup"><span data-stu-id="63625-132">Directory1</span></span>        | <span data-ttu-id="63625-133">Объект</span><span class="sxs-lookup"><span data-stu-id="63625-133">A</span></span>          |
| <span data-ttu-id="63625-134">Programmenufolder</span><span class="sxs-lookup"><span data-stu-id="63625-134">StartMenuFolder</span></span>    | <span data-ttu-id="63625-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="63625-135">Directory2</span></span>        | <span data-ttu-id="63625-136">б:к</span><span class="sxs-lookup"><span data-stu-id="63625-136">B:C</span></span>        |
| <span data-ttu-id="63625-137">аппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="63625-137">AppDataFolder</span></span>      | <span data-ttu-id="63625-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="63625-138">Directory3</span></span>        | <span data-ttu-id="63625-139">D</span><span class="sxs-lookup"><span data-stu-id="63625-139">D</span></span>          |
| <span data-ttu-id="63625-140">мипиктуресфолдер</span><span class="sxs-lookup"><span data-stu-id="63625-140">MyPicturesFolder</span></span>   | <span data-ttu-id="63625-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="63625-141">Directory4</span></span>        | <span data-ttu-id="63625-142">E</span><span class="sxs-lookup"><span data-stu-id="63625-142">E</span></span>          |



 

[<span data-ttu-id="63625-143">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="63625-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="63625-144">Компонент</span><span class="sxs-lookup"><span data-stu-id="63625-144">Component</span></span>               | <span data-ttu-id="63625-145">Каталог</span><span class="sxs-lookup"><span data-stu-id="63625-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="63625-146">Component1.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-146">Component1.<GUID></span></span> | <span data-ttu-id="63625-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="63625-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="63625-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-148">Component2.<GUID></span></span> | <span data-ttu-id="63625-149">Programmenufolder</span><span class="sxs-lookup"><span data-stu-id="63625-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="63625-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-150">Component3.<GUID></span></span> | <span data-ttu-id="63625-151">аппдатафолдер</span><span class="sxs-lookup"><span data-stu-id="63625-151">AppDataFolder</span></span>      |
| <span data-ttu-id="63625-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-152">Component4.<GUID></span></span> | <span data-ttu-id="63625-153">мипиктуресфолдер</span><span class="sxs-lookup"><span data-stu-id="63625-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="63625-154">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="63625-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="63625-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="63625-155">CustomAction</span></span>                 | <span data-ttu-id="63625-156">Тип</span><span class="sxs-lookup"><span data-stu-id="63625-156">Type</span></span> | <span data-ttu-id="63625-157">Источник</span><span class="sxs-lookup"><span data-stu-id="63625-157">Source</span></span>                       | <span data-ttu-id="63625-158">Назначение</span><span class="sxs-lookup"><span data-stu-id="63625-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="63625-159">Programmenufolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="63625-160">51</span><span class="sxs-lookup"><span data-stu-id="63625-160">51</span></span>   | <span data-ttu-id="63625-161">Programmenufolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="63625-162">\[Programmenufolder\]</span><span class="sxs-lookup"><span data-stu-id="63625-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="63625-163">мяппдатафолдерактион</span><span class="sxs-lookup"><span data-stu-id="63625-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="63625-164">51</span><span class="sxs-lookup"><span data-stu-id="63625-164">51</span></span>   | <span data-ttu-id="63625-165">Аппдатафолдер.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="63625-166">\[аппдатафолдер\]</span><span class="sxs-lookup"><span data-stu-id="63625-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="63625-167">Таблица Модулеинсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="63625-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="63625-168">Действие</span><span class="sxs-lookup"><span data-stu-id="63625-168">Action</span></span>                       | <span data-ttu-id="63625-169">Последовательность</span><span class="sxs-lookup"><span data-stu-id="63625-169">Sequence</span></span> | <span data-ttu-id="63625-170">басеактион</span><span class="sxs-lookup"><span data-stu-id="63625-170">BaseAction</span></span> | <span data-ttu-id="63625-171">После</span><span class="sxs-lookup"><span data-stu-id="63625-171">After</span></span> | <span data-ttu-id="63625-172">Условие</span><span class="sxs-lookup"><span data-stu-id="63625-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="63625-173">Programmenufolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="63625-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="63625-174">100</span><span class="sxs-lookup"><span data-stu-id="63625-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="63625-175">См. также</span><span class="sxs-lookup"><span data-stu-id="63625-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63625-176">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="63625-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



