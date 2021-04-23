---
description: Таблица Упградедфиле \_ оптионалдата содержит сведения о конкретных файлах в обновленном образе. Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией Уикреатепатчпаккажеекс.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Таблица UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272466"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="e8c85-104">\_Таблица Оптионалдата упградедфилес (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="e8c85-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="e8c85-105">Таблица Упградедфиле \_ оптионалдата содержит сведения о конкретных файлах в обновленном образе.</span><span class="sxs-lookup"><span data-stu-id="e8c85-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="e8c85-106">Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c85-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="e8c85-107">Таблица Упградедфиле \_ оптионалдата содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e8c85-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="e8c85-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="e8c85-108">Column</span></span>                  | <span data-ttu-id="e8c85-109">Type</span><span class="sxs-lookup"><span data-stu-id="e8c85-109">Type</span></span>    | <span data-ttu-id="e8c85-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="e8c85-110">Key</span></span> | <span data-ttu-id="e8c85-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="e8c85-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="e8c85-112">Обновлено</span><span class="sxs-lookup"><span data-stu-id="e8c85-112">Upgraded</span></span>                | <span data-ttu-id="e8c85-113">text</span><span class="sxs-lookup"><span data-stu-id="e8c85-113">text</span></span>    | <span data-ttu-id="e8c85-114">Да</span><span class="sxs-lookup"><span data-stu-id="e8c85-114">Y</span></span>   | <span data-ttu-id="e8c85-115">Нет</span><span class="sxs-lookup"><span data-stu-id="e8c85-115">N</span></span>        |
| <span data-ttu-id="e8c85-116">фтк</span><span class="sxs-lookup"><span data-stu-id="e8c85-116">FTK</span></span>                     | <span data-ttu-id="e8c85-117">text</span><span class="sxs-lookup"><span data-stu-id="e8c85-117">text</span></span>    | <span data-ttu-id="e8c85-118">Да</span><span class="sxs-lookup"><span data-stu-id="e8c85-118">Y</span></span>   | <span data-ttu-id="e8c85-119">Нет</span><span class="sxs-lookup"><span data-stu-id="e8c85-119">N</span></span>        |
| <span data-ttu-id="e8c85-120">симболпасс</span><span class="sxs-lookup"><span data-stu-id="e8c85-120">SymbolPaths</span></span>             | <span data-ttu-id="e8c85-121">text</span><span class="sxs-lookup"><span data-stu-id="e8c85-121">text</span></span>    |     | <span data-ttu-id="e8c85-122">Да</span><span class="sxs-lookup"><span data-stu-id="e8c85-122">Y</span></span>        |
| <span data-ttu-id="e8c85-123">алловигнореонпатчеррор</span><span class="sxs-lookup"><span data-stu-id="e8c85-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="e8c85-124">Целое число</span><span class="sxs-lookup"><span data-stu-id="e8c85-124">integer</span></span> |     | <span data-ttu-id="e8c85-125">Да</span><span class="sxs-lookup"><span data-stu-id="e8c85-125">Y</span></span>        |
| <span data-ttu-id="e8c85-126">инклудевхолефиле</span><span class="sxs-lookup"><span data-stu-id="e8c85-126">IncludeWholeFile</span></span>        | <span data-ttu-id="e8c85-127">Целое число</span><span class="sxs-lookup"><span data-stu-id="e8c85-127">integer</span></span> |     | <span data-ttu-id="e8c85-128">Да</span><span class="sxs-lookup"><span data-stu-id="e8c85-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e8c85-129">Столбцы</span><span class="sxs-lookup"><span data-stu-id="e8c85-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e8c85-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Обновит</span><span class="sxs-lookup"><span data-stu-id="e8c85-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="e8c85-131">Внешний ключ к обновленному столбцу [таблицы упградедимажес (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="e8c85-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8c85-132"><span id="FTK"></span><span id="ftk"></span>фтк</span><span class="sxs-lookup"><span data-stu-id="e8c85-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="e8c85-133">Ключ таблицы файлов.</span><span class="sxs-lookup"><span data-stu-id="e8c85-133">File table key.</span></span> <span data-ttu-id="e8c85-134">Внешний ключ в [таблицу File](file-table.md) файла MSI обновленного образа.</span><span class="sxs-lookup"><span data-stu-id="e8c85-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="e8c85-135">Если два или более обновленных образа в семействе имеют одно и то же значение ФТК, оно должно ссылаться на один и тот же файл.</span><span class="sxs-lookup"><span data-stu-id="e8c85-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="e8c85-136">Файлы, совместно используемые несколькими образами обновления, должны иметь одинаковые ФТК для минимального размера CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="e8c85-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="e8c85-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>симболпасс</span><span class="sxs-lookup"><span data-stu-id="e8c85-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="e8c85-138">Значение в этом поле добавляется в список папок, разделенных точкой с запятой, в столбце Симболпасс [таблицы упградедимажес (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) при создании исправления и может использоваться для добавления файлов символов для определенного файла.</span><span class="sxs-lookup"><span data-stu-id="e8c85-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="e8c85-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>алловигнореонпатчеррор</span><span class="sxs-lookup"><span data-stu-id="e8c85-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="e8c85-140">Задайте значение 1, чтобы указать, что исправление не является критически важным.</span><span class="sxs-lookup"><span data-stu-id="e8c85-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="e8c85-141">Задайте значение 0, чтобы указать, что это исправление является жизненно важным.</span><span class="sxs-lookup"><span data-stu-id="e8c85-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="e8c85-142">Если установщик Windows сталкивается с проблемой при применении этого обновления к файлу, указанному в столбце ФТК, значение в этом поле определяет, содержит ли окно сообщения об ошибке кнопку **пропустить** , чтобы разрешить пользователю продолжить процесс установки исправлений.</span><span class="sxs-lookup"><span data-stu-id="e8c85-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="e8c85-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>инклудевхолефиле</span><span class="sxs-lookup"><span data-stu-id="e8c85-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="e8c85-144">Задайте ненулевое значение, если необходимо установить весь файл, указанный в столбце ФТК, а не создавать двоичное исправление.</span><span class="sxs-lookup"><span data-stu-id="e8c85-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 



