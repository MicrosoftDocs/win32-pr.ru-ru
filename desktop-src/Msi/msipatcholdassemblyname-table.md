---
description: В таблице Мсипатчолдассемблинаме указывается старое имя сборки.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Таблица Мсипатчолдассемблинаме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347345"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="f4381-103">Таблица Мсипатчолдассемблинаме</span><span class="sxs-lookup"><span data-stu-id="f4381-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="f4381-104">В таблице Мсипатчолдассемблинаме указывается старое имя сборки.</span><span class="sxs-lookup"><span data-stu-id="f4381-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="f4381-105">Таблица Мсипатчолдассемблинаме содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="f4381-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="f4381-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="f4381-106">Column</span></span>   | <span data-ttu-id="f4381-107">Type</span><span class="sxs-lookup"><span data-stu-id="f4381-107">Type</span></span>                         | <span data-ttu-id="f4381-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="f4381-108">Key</span></span> | <span data-ttu-id="f4381-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="f4381-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="f4381-110">Сборка</span><span class="sxs-lookup"><span data-stu-id="f4381-110">Assembly</span></span> | [<span data-ttu-id="f4381-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="f4381-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f4381-112">Да</span><span class="sxs-lookup"><span data-stu-id="f4381-112">Y</span></span>   | <span data-ttu-id="f4381-113">Нет</span><span class="sxs-lookup"><span data-stu-id="f4381-113">N</span></span>        |
| <span data-ttu-id="f4381-114">Имя</span><span class="sxs-lookup"><span data-stu-id="f4381-114">Name</span></span>     | [<span data-ttu-id="f4381-115">Text</span><span class="sxs-lookup"><span data-stu-id="f4381-115">Text</span></span>](text.md)             | <span data-ttu-id="f4381-116">Да</span><span class="sxs-lookup"><span data-stu-id="f4381-116">Y</span></span>   | <span data-ttu-id="f4381-117">Нет</span><span class="sxs-lookup"><span data-stu-id="f4381-117">N</span></span>        |
| <span data-ttu-id="f4381-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f4381-118">Value</span></span>    | [<span data-ttu-id="f4381-119">Text</span><span class="sxs-lookup"><span data-stu-id="f4381-119">Text</span></span>](text.md)             | <span data-ttu-id="f4381-120">Нет</span><span class="sxs-lookup"><span data-stu-id="f4381-120">N</span></span>   | <span data-ttu-id="f4381-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f4381-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f4381-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="f4381-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f4381-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Сборок</span><span class="sxs-lookup"><span data-stu-id="f4381-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="f4381-124">Уникальный идентификатор для старого имени сборки.</span><span class="sxs-lookup"><span data-stu-id="f4381-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="f4381-125">Этот ключ используется в качестве сопоставления между этой и [таблицей мсипатчолдассемблифиле](msipatcholdassemblyfile-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4381-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4381-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="f4381-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="f4381-127">Имя атрибута, связанного со значением, указанным в столбце значение.</span><span class="sxs-lookup"><span data-stu-id="f4381-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="f4381-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="f4381-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="f4381-129">Значение, связанное с именем, указанным в столбце имя.</span><span class="sxs-lookup"><span data-stu-id="f4381-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4381-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4381-130">Remarks</span></span>

<span data-ttu-id="f4381-131">Установщик Windows использует [таблицу мсипатчолдассемблифиле](msipatcholdassemblyfile-table.md) и таблицу мсипатчолдассемблинаме при установке исправлений сборок, установленных в глобальном кэше сборок (GAC).</span><span class="sxs-lookup"><span data-stu-id="f4381-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="f4381-132">При освобождении более новой версии сборки будет изменено строгое имя сборки.</span><span class="sxs-lookup"><span data-stu-id="f4381-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="f4381-133">Эти две таблицы вместе указывают старое имя сборки для обновленной сборки.</span><span class="sxs-lookup"><span data-stu-id="f4381-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="f4381-134">Это позволяет установщику использовать старое имя сборки для поиска исходного файла в глобальном кэше сборок и применения двоичного исправления.</span><span class="sxs-lookup"><span data-stu-id="f4381-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="f4381-135">Без этих сведений установщику может потребоваться доступ к исходному источнику установки для исправления сборки, установленной в глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="f4381-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="f4381-136">[Таблица мсипатчолдассемблифиле](msipatcholdassemblyfile-table.md) и таблица мсипатчолдассемблинаме не создаются автоматически [патчвиз](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="f4381-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="f4381-137">Пакет обновления, указанный в [таблице упградедимажес](upgradedimages-table-patchwiz-dll-.md) , должен содержать эти таблицы, чтобы исправление имело эти данные.</span><span class="sxs-lookup"><span data-stu-id="f4381-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="f4381-138">Проверка</span><span class="sxs-lookup"><span data-stu-id="f4381-138">Validation</span></span>

<dl>

[<span data-ttu-id="f4381-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="f4381-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f4381-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="f4381-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f4381-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="f4381-141">ICE32</span></span>](ice32.md)  
</dl>

 

 



