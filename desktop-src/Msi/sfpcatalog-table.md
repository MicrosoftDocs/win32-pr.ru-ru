---
description: Таблица Сфпкаталог содержит каталоги, используемые Windows Me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Таблица Сфпкаталог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263337"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="8d8f6-103">Таблица Сфпкаталог</span><span class="sxs-lookup"><span data-stu-id="8d8f6-103">SFPCatalog Table</span></span>

<span data-ttu-id="8d8f6-104">Таблица Сфпкаталог содержит каталоги, используемые Windows Me.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="8d8f6-105">Таблица Сфпкаталог содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="8d8f6-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="8d8f6-106">Column</span></span>     | <span data-ttu-id="8d8f6-107">Type</span><span class="sxs-lookup"><span data-stu-id="8d8f6-107">Type</span></span>                       | <span data-ttu-id="8d8f6-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="8d8f6-108">Key</span></span> | <span data-ttu-id="8d8f6-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="8d8f6-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="8d8f6-110">сфпкаталог</span><span class="sxs-lookup"><span data-stu-id="8d8f6-110">SFPCatalog</span></span> | [<span data-ttu-id="8d8f6-111">Имя файла</span><span class="sxs-lookup"><span data-stu-id="8d8f6-111">Filename</span></span>](filename.md)   | <span data-ttu-id="8d8f6-112">Да</span><span class="sxs-lookup"><span data-stu-id="8d8f6-112">Y</span></span>   | <span data-ttu-id="8d8f6-113">Нет</span><span class="sxs-lookup"><span data-stu-id="8d8f6-113">N</span></span>        |
| <span data-ttu-id="8d8f6-114">Каталог</span><span class="sxs-lookup"><span data-stu-id="8d8f6-114">Catalog</span></span>    | [<span data-ttu-id="8d8f6-115">Двоичный</span><span class="sxs-lookup"><span data-stu-id="8d8f6-115">Binary</span></span>](binary.md)       | <span data-ttu-id="8d8f6-116">Нет</span><span class="sxs-lookup"><span data-stu-id="8d8f6-116">N</span></span>   | <span data-ttu-id="8d8f6-117">Нет</span><span class="sxs-lookup"><span data-stu-id="8d8f6-117">N</span></span>        |
| <span data-ttu-id="8d8f6-118">Зависимость</span><span class="sxs-lookup"><span data-stu-id="8d8f6-118">Dependency</span></span> | [<span data-ttu-id="8d8f6-119">Формате</span><span class="sxs-lookup"><span data-stu-id="8d8f6-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="8d8f6-120">Нет</span><span class="sxs-lookup"><span data-stu-id="8d8f6-120">N</span></span>   | <span data-ttu-id="8d8f6-121">Да</span><span class="sxs-lookup"><span data-stu-id="8d8f6-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8d8f6-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="8d8f6-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8d8f6-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>сфпкаталог</span><span class="sxs-lookup"><span data-stu-id="8d8f6-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="8d8f6-124">Короткое имя файла для каталога.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-124">The short file name for the catalog.</span></span> <span data-ttu-id="8d8f6-125">Поскольку каталоги не имеют версии, каталог, указанный в этом столбце, может перезаписать каталог с тем же именем и уже установлен в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="8d8f6-126">См. раздел Управление версиями файлов. [ни один из файлов не имеет версии](neither-file-has-a-version.md).</span><span class="sxs-lookup"><span data-stu-id="8d8f6-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d8f6-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Каталога</span><span class="sxs-lookup"><span data-stu-id="8d8f6-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="8d8f6-128">Двоичные данные для каталога.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="8d8f6-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Зависимостей</span><span class="sxs-lookup"><span data-stu-id="8d8f6-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="8d8f6-130">Каталог, указанный в этом поле, является родительским по отношению к зависимому каталогу, указанному в поле Сфпкаталог.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="8d8f6-131">Введите короткое имя родительского каталога в поле зависимости.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="8d8f6-132">Это поле является ключом обратно в столбец Сфпкаталог.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="8d8f6-133">Соответствие зависимости учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="8d8f6-134">Если поле зависимости ссылается на другую запись в этой таблице Сфпкаталог, родительский каталог устанавливается перед зависимым каталогом.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="8d8f6-135">Если поле зависимости ссылается на родительский каталог, который отсутствует в поле Сфпкаталог этой таблицы, и если родительский каталог еще не установлен, установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d8f6-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d8f6-136">Remarks</span></span>

<span data-ttu-id="8d8f6-137">[Действие инсталлсфпкаталогфиле](installsfpcatalogfile-action.md) запрашивает [таблицу компонентов](component-table.md), [таблицу файлов](file-table.md), таблицу [филесфпкаталог](filesfpcatalog-table.md) и таблицу сфпкаталог.</span><span class="sxs-lookup"><span data-stu-id="8d8f6-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="8d8f6-138">Проверка</span><span class="sxs-lookup"><span data-stu-id="8d8f6-138">Validation</span></span>

<dl>

[<span data-ttu-id="8d8f6-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="8d8f6-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8d8f6-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="8d8f6-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8d8f6-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="8d8f6-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="8d8f6-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="8d8f6-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8d8f6-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="8d8f6-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8d8f6-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="8d8f6-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



