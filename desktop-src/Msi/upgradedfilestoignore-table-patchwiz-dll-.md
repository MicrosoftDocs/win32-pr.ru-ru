---
description: Таблица Упградедфилестоигноре предотвращает обновление конкретных файлов, которые фактически изменились в обновленном образе относительно целевых образов.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Таблица Упградедфилестоигноре (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651136"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="1ddd6-103">Таблица Упградедфилестоигноре (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="1ddd6-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="1ddd6-104">Таблица Упградедфилестоигноре предотвращает обновление конкретных файлов, которые фактически изменились в обновленном образе относительно целевых образов.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="1ddd6-105">В некоторых случаях это может оказаться полезным.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="1ddd6-106">Например, пакет исправлений, предназначенный только для установки без административных установок, не должен включать файлы исправлений, которые являются частью административных образов.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="1ddd6-107">Исключение таких файлов, которые используются только в административных образах, может уменьшить размер пакета исправлений; Однако администраторам следует знать, как обновлять эти файлы отдельно.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="1ddd6-108">Эта таблица является необязательной в базе данных создания исправлений (файл PCP) и используется функцией [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="1ddd6-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="1ddd6-109">Таблица Упградедфилестоигноре содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="1ddd6-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="1ddd6-110">Column</span></span>   | <span data-ttu-id="1ddd6-111">Type</span><span class="sxs-lookup"><span data-stu-id="1ddd6-111">Type</span></span> | <span data-ttu-id="1ddd6-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="1ddd6-112">Key</span></span> | <span data-ttu-id="1ddd6-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="1ddd6-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="1ddd6-114">Обновлено</span><span class="sxs-lookup"><span data-stu-id="1ddd6-114">Upgraded</span></span> | <span data-ttu-id="1ddd6-115">text</span><span class="sxs-lookup"><span data-stu-id="1ddd6-115">text</span></span> | <span data-ttu-id="1ddd6-116">Да</span><span class="sxs-lookup"><span data-stu-id="1ddd6-116">Y</span></span>   | <span data-ttu-id="1ddd6-117">Нет</span><span class="sxs-lookup"><span data-stu-id="1ddd6-117">N</span></span>        |
| <span data-ttu-id="1ddd6-118">фтк</span><span class="sxs-lookup"><span data-stu-id="1ddd6-118">FTK</span></span>      | <span data-ttu-id="1ddd6-119">text</span><span class="sxs-lookup"><span data-stu-id="1ddd6-119">text</span></span> | <span data-ttu-id="1ddd6-120">Да</span><span class="sxs-lookup"><span data-stu-id="1ddd6-120">Y</span></span>   | <span data-ttu-id="1ddd6-121">Нет</span><span class="sxs-lookup"><span data-stu-id="1ddd6-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1ddd6-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="1ddd6-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1ddd6-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Обновит</span><span class="sxs-lookup"><span data-stu-id="1ddd6-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="1ddd6-124">Внешний ключ к обновленному столбцу [таблицы упградедимажес (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="1ddd6-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="1ddd6-125">Средство создания исправлений исключает обновление файла, указанного в столбце ФТК таблицы Упградедфилестоигноре, при обновлении целевого объекта до изображения, указанного в обновленном поле.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="1ddd6-126">Введите значение " \* " в обновленном поле, чтобы исключить обновление файла для всех обновленных образов.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="1ddd6-127"><span id="FTK"></span><span id="ftk"></span>фтк</span><span class="sxs-lookup"><span data-stu-id="1ddd6-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="1ddd6-128">Внешний ключ в [таблице файлов](file-table.md) обновленного образа.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="1ddd6-129">Значение в формате " <prefix> \* " соответствует всем ключам таблицы файлов в таблице File, которые начинаются с этого префикса.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="1ddd6-130">Текст не может следовать за звездочкой.</span><span class="sxs-lookup"><span data-stu-id="1ddd6-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 



