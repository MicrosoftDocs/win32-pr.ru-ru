---
description: Эта рекомендация предназначена для создания установщик Windows пакета, содержащего более 32767 файлов.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Создание большого пакета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662942"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="177f5-103">Создание большого пакета</span><span class="sxs-lookup"><span data-stu-id="177f5-103">Authoring a Large Package</span></span>

<span data-ttu-id="177f5-104">Эта рекомендация предназначена для создания установщик Windows пакета, содержащего более 32767 файлов.</span><span class="sxs-lookup"><span data-stu-id="177f5-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="177f5-105">Если пакет установщик Windows содержит более 32767 файлов, необходимо изменить схему базы данных, чтобы увеличить предельный размер следующих столбцов:</span><span class="sxs-lookup"><span data-stu-id="177f5-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="177f5-106">Столбец последовательности [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="177f5-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="177f5-107">Столбец Ластсекуенце [таблицы Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="177f5-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="177f5-108">Столбец последовательности [таблицы Patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="177f5-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="177f5-109">Дополнительные сведения см. в разделе [Формат определения столбца](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="177f5-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="177f5-110">**Увеличение предела столбца базы данных**</span><span class="sxs-lookup"><span data-stu-id="177f5-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="177f5-111">Экспортируйте таблицу в файл IDT.</span><span class="sxs-lookup"><span data-stu-id="177f5-111">Export the table to an .idt file.</span></span> <span data-ttu-id="177f5-112">Дополнительные сведения см. в разделе [Msidb.exe](msidb-exe.md), [Экспорт файлов](export-files.md), [Импорт и экспорт](importing-and-exporting.md).</span><span class="sxs-lookup"><span data-stu-id="177f5-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="177f5-113">Измените файл IDT, чтобы изменить тип столбца с I2 на I4 или с I2 на i4.</span><span class="sxs-lookup"><span data-stu-id="177f5-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="177f5-114">Экспортируйте таблицу [ \_ проверки](-validation-table.md) в файл IDT.</span><span class="sxs-lookup"><span data-stu-id="177f5-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="177f5-115">Измените файл IDT, чтобы изменить значения в столбце MaxValue таблицы [ \_ проверки](-validation-table.md) , чтобы они соответствовали увеличенной ширине столбцов.</span><span class="sxs-lookup"><span data-stu-id="177f5-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="177f5-116">Импортируйте файлы IDT обратно в базу данных.</span><span class="sxs-lookup"><span data-stu-id="177f5-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="177f5-117">Обратите внимание, что преобразования и исправления не могут быть созданы между двумя пакетами с разными типами столбцов.</span><span class="sxs-lookup"><span data-stu-id="177f5-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



