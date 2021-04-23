---
description: Таблица ModuleSignature является обязательной таблицей.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Таблица ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545682"
---
# <a name="modulesignature-table"></a><span data-ttu-id="9cb88-103">Таблица ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="9cb88-103">ModuleSignature Table</span></span>

<span data-ttu-id="9cb88-104">Таблица ModuleSignature является обязательной таблицей.</span><span class="sxs-lookup"><span data-stu-id="9cb88-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="9cb88-105">Он содержит все сведения, необходимые для обнаружения модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="9cb88-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="9cb88-106">Средство слияния добавляет эту таблицу в MSI файл, если она еще не существует.</span><span class="sxs-lookup"><span data-stu-id="9cb88-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="9cb88-107">Таблица ModuleSignature в модуле слияния содержит только одну строку, содержащую ModuleID, Language и Version.</span><span class="sxs-lookup"><span data-stu-id="9cb88-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="9cb88-108">Однако таблица ModuleSignature в MSI-файле содержит строку, содержащую эту информацию для каждого файла. MSM, который был объединен в него.</span><span class="sxs-lookup"><span data-stu-id="9cb88-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="9cb88-109">Средства слияния и проверки проверьте таблицу ModuleSignature в MSI-файлах, чтобы определить наличие всех зависимых модулей слияния, необходимых текущему модулю слияния (см. [таблицу модуледепенденци](moduledependency-table.md)), а также сведения о том, был ли ранее объединен пакет установки с любыми конфликтующими модулями слияния (см. [таблицу модуликсклусион Table](moduleexclusion-table.md)).</span><span class="sxs-lookup"><span data-stu-id="9cb88-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="9cb88-110">Таблица ModuleSignature содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="9cb88-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="9cb88-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="9cb88-111">Column</span></span>   | <span data-ttu-id="9cb88-112">Type</span><span class="sxs-lookup"><span data-stu-id="9cb88-112">Type</span></span>                         | <span data-ttu-id="9cb88-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="9cb88-113">Key</span></span> | <span data-ttu-id="9cb88-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="9cb88-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="9cb88-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="9cb88-115">ModuleID</span></span> | [<span data-ttu-id="9cb88-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="9cb88-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="9cb88-117">Да</span><span class="sxs-lookup"><span data-stu-id="9cb88-117">Y</span></span>   | <span data-ttu-id="9cb88-118">Нет</span><span class="sxs-lookup"><span data-stu-id="9cb88-118">N</span></span>        |
| <span data-ttu-id="9cb88-119">Язык</span><span class="sxs-lookup"><span data-stu-id="9cb88-119">Language</span></span> | [<span data-ttu-id="9cb88-120">Integer</span><span class="sxs-lookup"><span data-stu-id="9cb88-120">Integer</span></span>](integer.md)       | <span data-ttu-id="9cb88-121">Да</span><span class="sxs-lookup"><span data-stu-id="9cb88-121">Y</span></span>   | <span data-ttu-id="9cb88-122">Нет</span><span class="sxs-lookup"><span data-stu-id="9cb88-122">N</span></span>        |
| <span data-ttu-id="9cb88-123">Версия</span><span class="sxs-lookup"><span data-stu-id="9cb88-123">Version</span></span>  | [<span data-ttu-id="9cb88-124">Version</span><span class="sxs-lookup"><span data-stu-id="9cb88-124">Version</span></span>](version.md)       |     | <span data-ttu-id="9cb88-125">Нет</span><span class="sxs-lookup"><span data-stu-id="9cb88-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9cb88-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="9cb88-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9cb88-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="9cb88-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="9cb88-128">Идентификатор, который уникальным образом идентифицирует модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="9cb88-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="9cb88-129">Два модуля слияния не могут иметь одинаковый ModuleID, если только модуль слияния не полностью обратно совместим с его предшественником.</span><span class="sxs-lookup"><span data-stu-id="9cb88-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="9cb88-130">Идентификатор GUID для этого поля можно создать с помощью служебной программы, такой как GUIDGEN.</span><span class="sxs-lookup"><span data-stu-id="9cb88-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="9cb88-131">Столбец ModuleID является первичным ключом для таблицы, поэтому он должен соответствовать соглашению об именовании для [именования первичных ключей в базах данных модуля слияния](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="9cb88-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="9cb88-132">Например, если понятное имя модуля слияния — MyLibrary, а GUID — {880DE2F0-CDD8-11D1-A849-006097ABDE17}, запись в столбце ModuleID становится MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="9cb88-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="9cb88-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Языке</span><span class="sxs-lookup"><span data-stu-id="9cb88-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="9cb88-134">Идентификатор языка задает язык по умолчанию для модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="9cb88-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="9cb88-135">Идентификатор языка имеет десятичный формат, например, Английский (США) — 1033.</span><span class="sxs-lookup"><span data-stu-id="9cb88-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="9cb88-136">Язык, используемый модулем слияния, можно изменить, применив преобразование к модулю слияния перед слиянием.</span><span class="sxs-lookup"><span data-stu-id="9cb88-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="9cb88-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Версия</span><span class="sxs-lookup"><span data-stu-id="9cb88-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="9cb88-138">Поле Version содержит строку, описывающую основную и дополнительную версии модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="9cb88-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="9cb88-139">Проверка</span><span class="sxs-lookup"><span data-stu-id="9cb88-139">Validation</span></span>

<dl>

[<span data-ttu-id="9cb88-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="9cb88-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9cb88-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="9cb88-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9cb88-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="9cb88-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="9cb88-143">См. также</span><span class="sxs-lookup"><span data-stu-id="9cb88-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb88-144">Модули слияния с несколькими языками</span><span class="sxs-lookup"><span data-stu-id="9cb88-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



