---
description: Таблица Филесфпкаталог связывает указанные файлы с файлами каталога, используемыми системой защиты системных файлов.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Таблица Филесфпкаталог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663976"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="21122-103">Таблица Филесфпкаталог</span><span class="sxs-lookup"><span data-stu-id="21122-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="21122-104">Таблица Филесфпкаталог связывает указанные файлы с файлами каталога, используемыми системой защиты системных файлов.</span><span class="sxs-lookup"><span data-stu-id="21122-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="21122-105">Windows **Vista, Windows Server 2003 и Windows XP:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21122-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="21122-106">Таблица Филесфпкаталог содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="21122-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="21122-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="21122-107">Column</span></span>       | <span data-ttu-id="21122-108">Type</span><span class="sxs-lookup"><span data-stu-id="21122-108">Type</span></span>                         | <span data-ttu-id="21122-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="21122-109">Key</span></span> | <span data-ttu-id="21122-110">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="21122-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="21122-111">Файл\_</span><span class="sxs-lookup"><span data-stu-id="21122-111">File\_</span></span>       | [<span data-ttu-id="21122-112">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="21122-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="21122-113">Да</span><span class="sxs-lookup"><span data-stu-id="21122-113">Y</span></span>   | <span data-ttu-id="21122-114">Нет</span><span class="sxs-lookup"><span data-stu-id="21122-114">N</span></span>        |
| <span data-ttu-id="21122-115">сфпкаталог\_</span><span class="sxs-lookup"><span data-stu-id="21122-115">SFPCatalog\_</span></span> | [<span data-ttu-id="21122-116">Имя файла</span><span class="sxs-lookup"><span data-stu-id="21122-116">Filename</span></span>](filename.md)     | <span data-ttu-id="21122-117">Да</span><span class="sxs-lookup"><span data-stu-id="21122-117">Y</span></span>   | <span data-ttu-id="21122-118">Нет</span><span class="sxs-lookup"><span data-stu-id="21122-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="21122-119">Столбцы</span><span class="sxs-lookup"><span data-stu-id="21122-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="21122-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="21122-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="21122-121">Внешний ключ к [таблице файлов](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="21122-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="21122-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>сфпкаталог\_</span><span class="sxs-lookup"><span data-stu-id="21122-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="21122-123">Внешний ключ к [таблице сфпкаталог](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="21122-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21122-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21122-124">Remarks</span></span>

<span data-ttu-id="21122-125">[Действие инсталлсфпкаталогфиле](installsfpcatalogfile-action.md) запрашивает [таблицу компонентов](component-table.md), [таблицу файлов](file-table.md), таблицу филесфпкаталог и [таблицу сфпкаталог](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="21122-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="21122-126">Проверка</span><span class="sxs-lookup"><span data-stu-id="21122-126">Validation</span></span>

<dl>

[<span data-ttu-id="21122-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="21122-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="21122-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="21122-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="21122-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="21122-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="21122-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="21122-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="21122-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="21122-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



