---
description: Следующая процедура описывает общие шаги по созданию модулей слияния.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Создание модулей слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264190"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="a680d-103">Создание модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-103">Authoring Merge Modules</span></span>

<span data-ttu-id="a680d-104">Следующая процедура описывает общие шаги по созданию модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="a680d-105">**Создание нового модуля слияния**</span><span class="sxs-lookup"><span data-stu-id="a680d-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="a680d-106">Получите программное средство, которое можно использовать для изменения базы данных модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="a680d-107">Получите пустую базу данных модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="a680d-108">Создание [идентификатора GUID](guid.md) для модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="a680d-109">Этот идентификатор GUID необходимо использовать при создании первичных ключей таблиц базы данных в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="a680d-110">Добавьте запись в [таблицу Component](component-table.md) для каждого компонента, доставленного слиянием.</span><span class="sxs-lookup"><span data-stu-id="a680d-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="a680d-111">Таблица Component необходима в каждом модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="a680d-112">Обратите внимание, что модули слияния работают с компонентами, а не с функциями.</span><span class="sxs-lookup"><span data-stu-id="a680d-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="a680d-113">Однако в некоторых случаях для записи в таблицу базы данных может потребоваться ссылка на функцию.</span><span class="sxs-lookup"><span data-stu-id="a680d-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="a680d-114">Дополнительные сведения см. [в разделе ссылки на функции в модулях слияния](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="a680d-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="a680d-115">Добавьте [таблицу каталогов](directory-table.md) в модуль слияния, указывающий расположение каталогов, которые модуль слияния добавляет в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="a680d-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="a680d-116">Таблица каталогов необходима в каждом модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="a680d-117">Импортируйте пустую [таблицу феатурекомпонентс](featurecomponents-table.md) в базу данных модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="a680d-118">Эта пустая таблица предоставляет рекомендации для средства слияния в случаях, когда MSI-файл не содержит собственную таблицу Феатурекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="a680d-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="a680d-119">Собирайте все файлы, доставляемые этим модулем слияния, и создайте CAB-файл [MergeModule.CABinet](mergemodule-cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="a680d-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="a680d-120">Добавьте CAB-файл в модуль слияния в виде потока внутри файла MSM.</span><span class="sxs-lookup"><span data-stu-id="a680d-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="a680d-121">Добавьте запись в таблицу файлов для каждого файла, хранящегося в MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="a680d-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="a680d-122">Добавьте сведения, необходимые для обнаружения модуля слияния в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a680d-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="a680d-123">Для каждого модуля слияния требуется таблица ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="a680d-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="a680d-124">Перечислите компоненты в модуле слияния в [таблице модулекомпонентс](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="a680d-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="a680d-125">Для каждого модуля слияния требуется таблица Модулекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="a680d-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="a680d-126">Добавьте таблицы последовательностей модуля слияния в файл MSM, только если модулю слияния необходимо изменить [*таблицы последовательности*](s-gly.md) целевой базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="a680d-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="a680d-127">Добавьте \_ таблицу проверки в модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="a680d-128">Для передачи проверки модулю слияния требуется \_ Таблица проверки.</span><span class="sxs-lookup"><span data-stu-id="a680d-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="a680d-129">Для модулей слияния требуется пользовательский интерфейс в редких случаях.</span><span class="sxs-lookup"><span data-stu-id="a680d-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="a680d-130">Не рекомендуется включать пользовательский интерфейс с модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="a680d-131">В случаях, когда требуется пользовательский интерфейс, таблицы пользовательского интерфейса можно объединить в MSI-файл так же, как и другие таблицы.</span><span class="sxs-lookup"><span data-stu-id="a680d-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="a680d-132">Добавьте сведения о реестре в соответствующие таблицы реестра в базе данных модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="a680d-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="a680d-133">Добавьте данные реестра для библиотек типов, классов, расширений и команд в таблицы [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [расширение](extension-table.md), [глагол](verb-table.md)или [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a680d-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="a680d-134">Все остальные данные реестра можно найти в [таблице реестра](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="a680d-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="a680d-135">Использовать таблицу Селфрег не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a680d-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="a680d-136">Добавьте сводные данные в [поток сводных данных модуля слияния](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a680d-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="a680d-137">Запустите проверку для всех модулей слияния, прежде чем пытаться установить.</span><span class="sxs-lookup"><span data-stu-id="a680d-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a680d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a680d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a680d-139">Получение пустых баз данных модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="a680d-140">Получение средств для создания модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="a680d-141">Именование первичных ключей в базах данных модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="a680d-142">Создание таблиц компонентов модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-143">Создание таблиц каталога для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-144">Создание таблиц Феатурекомпонентс для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-145">Создание CAB-файлов MergeModule.CABinet</span><span class="sxs-lookup"><span data-stu-id="a680d-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="a680d-146">Создание таблиц файлов модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-147">Создание таблиц ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="a680d-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-148">Создание Модулекомпонентс таблиц</span><span class="sxs-lookup"><span data-stu-id="a680d-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-149">Создание таблиц последовательности для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-150">Проверка модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="a680d-151">Создание пользовательских интерфейсов в модулях слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="a680d-152">Создание таблиц реестра для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="a680d-153">Создание сводных информационных потоков для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="a680d-154">Справочные сведения о потоке сводных данных модуля слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="a680d-155">Проверка модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="a680d-156">Использование 64-разрядных модулей слияния</span><span class="sxs-lookup"><span data-stu-id="a680d-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



