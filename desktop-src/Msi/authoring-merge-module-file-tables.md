---
description: Таблица файлов необходима в каждом модуле слияния и должна иметь запись для каждого файла, который доставляется в целевой пакет установки модулем слияния.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Создание таблиц файлов модулей слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080682"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="237b6-103">Создание таблиц файлов модулей слияния</span><span class="sxs-lookup"><span data-stu-id="237b6-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="237b6-104">[Таблица файлов](file-table.md) необходима в каждом модуле слияния и должна иметь запись для каждого файла, который доставляется в целевой пакет установки модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="237b6-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="237b6-105">При слиянии модуля слияния в MSI-файл каждый файл в таблице файла модуля слияния сохраняется в [*CAB*](c-gly.md) -файле в файле MSM.</span><span class="sxs-lookup"><span data-stu-id="237b6-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="237b6-106">Имя CAB-файла в модуле слияния всегда является следующим: MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="237b6-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="237b6-107">Дополнительные сведения см. в разделе [Создание CAB-файлов MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="237b6-108">Поскольку файлы модуля слияния всегда хранятся внутри CAB-файла, нет необходимости задавать битовые флаги **мсидбфилеаттрибутеснонкомпрессед** или **Мсидбфилеаттрибутескомпрессед** в столбце Attributes [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="237b6-109">Имена файлов в MergeModule.CABinet должны совпадать с первичным ключом в [таблице файлов](file-table.md)модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="237b6-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="237b6-110">Столбец File является первичным ключом [таблицы File](file-table.md) , а записи в этом поле должны соответствовать соглашению, описанному в разделе [именование первичных ключей в базах данных модулей слияния](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="237b6-111">Порядковые номера файлов указываются в столбце Sequence [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="237b6-112">Файлы должны быть перечислены в [таблице файлов](file-table.md) модуля слияния в той же последовательности, в которой они хранятся в MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="237b6-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="237b6-113">Порядковые номера файлов не должны быть последовательными, но они должны следовать той же последовательности, что и файлы, хранящиеся в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="237b6-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="237b6-114">Например, первый, второй и третий файлы, хранящиеся в CAB-файле, могут иметь порядковые номера 100, 200 и 300.</span><span class="sxs-lookup"><span data-stu-id="237b6-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="237b6-115">Установщик пропускает дополнительные файлы, включенные в MergeModule.CABINET, которые не перечислены в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="237b6-116">Один CAB-файл может содержать все файлы, необходимые для модуля слияния, который поддерживает несколько языков с помощью преобразований.</span><span class="sxs-lookup"><span data-stu-id="237b6-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="237b6-117">Всем языковым файлам можно предоставить уникальный порядковый номер в CAB-файле, а затем преобразование может добавлять или удалять файлы из [таблицы File](file-table.md) , если это необходимо для конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="237b6-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="237b6-118">Дополнительные сведения см. в разделе [Создание модулей слияния для нескольких языков](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="237b6-119">Дополнительные сведения см. в разделе [Файловая таблица](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="237b6-119">For more information, see [File Table](file-table.md).</span></span>

 

 



