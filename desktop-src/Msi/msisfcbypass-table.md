---
description: Таблица Мсисфкбипасс содержит список файлов, которые должны обходить защиту файлов Windows при установке файлов в Microsoft Windows Me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Таблица Мсисфкбипасс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347335"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="78504-103">Таблица Мсисфкбипасс</span><span class="sxs-lookup"><span data-stu-id="78504-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="78504-104">Таблица Мсисфкбипасс содержит список файлов, которые должны обходить защиту файлов Windows при установке файлов в Microsoft Windows Me.</span><span class="sxs-lookup"><span data-stu-id="78504-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="78504-105">Таблица Мсисфкбипасс содержит следующий столбец.</span><span class="sxs-lookup"><span data-stu-id="78504-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="78504-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="78504-106">Column</span></span> | <span data-ttu-id="78504-107">Type</span><span class="sxs-lookup"><span data-stu-id="78504-107">Type</span></span>                         | <span data-ttu-id="78504-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="78504-108">Key</span></span> | <span data-ttu-id="78504-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="78504-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="78504-110">Файл\_</span><span class="sxs-lookup"><span data-stu-id="78504-110">File\_</span></span> | [<span data-ttu-id="78504-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="78504-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="78504-112">Да</span><span class="sxs-lookup"><span data-stu-id="78504-112">Y</span></span>   | <span data-ttu-id="78504-113">Нет</span><span class="sxs-lookup"><span data-stu-id="78504-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="78504-114">Столбцы</span><span class="sxs-lookup"><span data-stu-id="78504-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="78504-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="78504-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="78504-116">Внешний ключ к [таблице файлов](file-table.md) , указывающий файл, который должен обходить защиту файлов Windows при установке файла в Windows Me.</span><span class="sxs-lookup"><span data-stu-id="78504-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



