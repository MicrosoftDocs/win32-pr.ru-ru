---
description: Таблица Мсипатчолдассемблифиле связывает файл в таблице file с именем сборки в таблице Мсипатчолдассемблинаме. Несколько старых имен сборок могут быть связаны с одним файлом.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Таблица Мсипатчолдассемблифиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664585"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="182fa-104">Таблица Мсипатчолдассемблифиле</span><span class="sxs-lookup"><span data-stu-id="182fa-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="182fa-105">Таблица Мсипатчолдассемблифиле связывает файл в [таблице File](file-table.md) с именем сборки в [таблице мсипатчолдассемблинаме](msipatcholdassemblyname-table.md).</span><span class="sxs-lookup"><span data-stu-id="182fa-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="182fa-106">Несколько старых имен сборок могут быть связаны с одним файлом.</span><span class="sxs-lookup"><span data-stu-id="182fa-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="182fa-107">Таблица Мсипатчолдассемблифиле содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="182fa-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="182fa-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="182fa-108">Column</span></span>     | <span data-ttu-id="182fa-109">Type</span><span class="sxs-lookup"><span data-stu-id="182fa-109">Type</span></span>                         | <span data-ttu-id="182fa-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="182fa-110">Key</span></span> | <span data-ttu-id="182fa-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="182fa-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="182fa-112">Файл\_</span><span class="sxs-lookup"><span data-stu-id="182fa-112">File\_</span></span>     | [<span data-ttu-id="182fa-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="182fa-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="182fa-114">Да</span><span class="sxs-lookup"><span data-stu-id="182fa-114">Y</span></span>   | <span data-ttu-id="182fa-115">Нет</span><span class="sxs-lookup"><span data-stu-id="182fa-115">N</span></span>        |
| <span data-ttu-id="182fa-116">Сборка\_</span><span class="sxs-lookup"><span data-stu-id="182fa-116">Assembly\_</span></span> | [<span data-ttu-id="182fa-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="182fa-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="182fa-118">Да</span><span class="sxs-lookup"><span data-stu-id="182fa-118">Y</span></span>   | <span data-ttu-id="182fa-119">Нет</span><span class="sxs-lookup"><span data-stu-id="182fa-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="182fa-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="182fa-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="182fa-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="182fa-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="182fa-122">Внешний ключ к [таблице файлов](file-table.md) , указывающий сборку для исправления.</span><span class="sxs-lookup"><span data-stu-id="182fa-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="182fa-123">Этот столбец является частью первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="182fa-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="182fa-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Сборок\_</span><span class="sxs-lookup"><span data-stu-id="182fa-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="182fa-125">Внешний ключ к [таблице мсипатчолдассемблинаме](msipatcholdassemblyname-table.md) , который определяет одно из старых имен сборок для сборки.</span><span class="sxs-lookup"><span data-stu-id="182fa-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="182fa-126">Этот столбец является частью первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="182fa-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="182fa-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="182fa-127">Remarks</span></span>

<span data-ttu-id="182fa-128">Установщик Windows использует таблицу Мсипатчолдассемблифиле и [таблицу мсипатчолдассемблинаме](msipatcholdassemblyname-table.md) при установке исправлений сборок, установленных в глобальном кэше сборок (GAC).</span><span class="sxs-lookup"><span data-stu-id="182fa-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="182fa-129">При освобождении более новой версии сборки будет изменено строгое имя сборки.</span><span class="sxs-lookup"><span data-stu-id="182fa-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="182fa-130">Эти две таблицы вместе указывают старое имя сборки для обновленной сборки.</span><span class="sxs-lookup"><span data-stu-id="182fa-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="182fa-131">Это позволяет установщику использовать старое имя сборки для поиска исходного файла в глобальном кэше сборок и применения двоичного исправления.</span><span class="sxs-lookup"><span data-stu-id="182fa-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="182fa-132">Без этих сведений установщику может потребоваться доступ к исходному источнику установки для исправления сборки, установленной в глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="182fa-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="182fa-133">Таблица Мсипатчолдассемблифиле и [Таблица мсипатчолдассемблинаме](msipatcholdassemblyname-table.md) не создаются автоматически [патчвиз](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="182fa-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="182fa-134">Пакет обновления, указанный в [таблице упградедимажес](upgradedimages-table-patchwiz-dll-.md) , должен содержать эти таблицы, чтобы исправление имело эти данные.</span><span class="sxs-lookup"><span data-stu-id="182fa-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="182fa-135">Проверка</span><span class="sxs-lookup"><span data-stu-id="182fa-135">Validation</span></span>

<dl>

[<span data-ttu-id="182fa-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="182fa-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="182fa-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="182fa-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="182fa-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="182fa-138">ICE32</span></span>](ice32.md)  
</dl>

 

 



