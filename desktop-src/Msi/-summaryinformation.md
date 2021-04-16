---
description: '\_Таблица SummaryInformation — это специальная таблица, используемая в потоке сводных данных. Можно получить или задать поток сводных данных установщик Windows базы данных путем экспорта или импорта текстового файла архива с именем \_ SummaryInformation. IDT.'
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650750"
---
# <a name="_summaryinformation"></a><span data-ttu-id="524fd-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="524fd-104">\_SummaryInformation</span></span>

<span data-ttu-id="524fd-105">\_Таблица SummaryInformation — это специальная таблица, используемая в [потоке сводных данных](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="524fd-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="524fd-106">Можно получить или задать поток сводных данных установщик Windows базы данных путем экспорта или импорта [текстового файла архива](text-archive-files.md) с именем \_ SummaryInformation. IDT.</span><span class="sxs-lookup"><span data-stu-id="524fd-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="524fd-107">Файл IDT экспортированной \_ таблицы SummaryInformation имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="524fd-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="524fd-108">Первая строка содержит имена столбцов таблицы, разделенные символами табуляции: PropertyId и value.</span><span class="sxs-lookup"><span data-stu-id="524fd-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="524fd-109">Список свойств и их идентификаторов см. в разделе [Сводные сведения о наборе свойств потока](summary-information-stream-property-set.md) .</span><span class="sxs-lookup"><span data-stu-id="524fd-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="524fd-110">Вторая строка содержит определения столбцов, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="524fd-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="524fd-111">Определения столбцов задаются так же, как и в стандартном [формате файлового архива](archive-file-format.md). IDT.</span><span class="sxs-lookup"><span data-stu-id="524fd-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="524fd-112">Столбец PropertyId может быть коротким целым числом, не допускающим значения NULL.</span><span class="sxs-lookup"><span data-stu-id="524fd-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="524fd-113">Столбец значения может быть локализованной строкой 255, не допускающей значения NULL.</span><span class="sxs-lookup"><span data-stu-id="524fd-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="524fd-114">Третья строка представляет собой имя таблицы и имя первичного ключевого столбца, разделенные вкладками: \_ SummaryInformation и PropertyId.</span><span class="sxs-lookup"><span data-stu-id="524fd-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="524fd-115">Остальные строки в файле представляют идентификатор процесса и связанное значение, разделенные символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="524fd-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="524fd-116">Дата и время в \_ SummaryInformation имеют формат: гггг/мм/дд чч:: мм:: СС.</span><span class="sxs-lookup"><span data-stu-id="524fd-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="524fd-117">Например, 1999/03/22 15:25:45.</span><span class="sxs-lookup"><span data-stu-id="524fd-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="524fd-118">Ниже приведен пример [сводного информационного потока](summary-information-stream.md) базы данных в формате IDT.</span><span class="sxs-lookup"><span data-stu-id="524fd-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="524fd-119">При использовании [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) или метода [Import](database-import.md) объекта [**базы данных**](database-object.md) для импорта таблицы текстовых архивов с именем \_ SummaryInformation в базу данных установщика вы пишете поток "05SummaryInformation" в базу данных.</span><span class="sxs-lookup"><span data-stu-id="524fd-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



