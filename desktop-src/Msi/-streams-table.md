---
description: В \_ таблице Streams перечислены внедренные потоки данных OLE. Это временная таблица, созданная только в том случае, если на нее ссылается инструкция SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Таблица _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662987"
---
# <a name="_streams-table"></a><span data-ttu-id="0860e-104">\_Таблица потоков</span><span class="sxs-lookup"><span data-stu-id="0860e-104">\_Streams Table</span></span>

<span data-ttu-id="0860e-105">В \_ таблице Streams перечислены внедренные потоки данных OLE.</span><span class="sxs-lookup"><span data-stu-id="0860e-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="0860e-106">Это временная таблица, созданная только в том случае, если на нее ссылается инструкция SQL.</span><span class="sxs-lookup"><span data-stu-id="0860e-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="0860e-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="0860e-107">Column</span></span> | <span data-ttu-id="0860e-108">Type</span><span class="sxs-lookup"><span data-stu-id="0860e-108">Type</span></span>                 | <span data-ttu-id="0860e-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="0860e-109">Key</span></span> | <span data-ttu-id="0860e-110">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="0860e-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="0860e-111">Имя</span><span class="sxs-lookup"><span data-stu-id="0860e-111">Name</span></span>   | [<span data-ttu-id="0860e-112">Text</span><span class="sxs-lookup"><span data-stu-id="0860e-112">Text</span></span>](text.md)     | <span data-ttu-id="0860e-113">Да</span><span class="sxs-lookup"><span data-stu-id="0860e-113">Y</span></span>   | <span data-ttu-id="0860e-114">Нет</span><span class="sxs-lookup"><span data-stu-id="0860e-114">N</span></span>        |
| <span data-ttu-id="0860e-115">Данные</span><span class="sxs-lookup"><span data-stu-id="0860e-115">Data</span></span>   | [<span data-ttu-id="0860e-116">Двоичный</span><span class="sxs-lookup"><span data-stu-id="0860e-116">Binary</span></span>](binary.md) | <span data-ttu-id="0860e-117">Нет</span><span class="sxs-lookup"><span data-stu-id="0860e-117">N</span></span>   | <span data-ttu-id="0860e-118">Да</span><span class="sxs-lookup"><span data-stu-id="0860e-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0860e-119">Столбцы</span><span class="sxs-lookup"><span data-stu-id="0860e-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0860e-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="0860e-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="0860e-121">Уникальный ключ, определяющий поток.</span><span class="sxs-lookup"><span data-stu-id="0860e-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="0860e-122">Максимальная длина имени — 62 символов.</span><span class="sxs-lookup"><span data-stu-id="0860e-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="0860e-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="0860e-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="0860e-124">Неформатированные двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="0860e-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0860e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0860e-125">Remarks</span></span>

<span data-ttu-id="0860e-126">Чтобы скопировать поток данных OLE (например, объект типа [binary](binary.md) данных) из файла в базу данных, создайте запись в \_ таблице Streams и введите имя потока данных в столбец имя этой записи и скопируйте данные из файла в столбец данных с помощью [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span><span class="sxs-lookup"><span data-stu-id="0860e-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="0860e-127">Используйте [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) для вставки новой записи в таблицу.</span><span class="sxs-lookup"><span data-stu-id="0860e-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="0860e-128">Для чтения потока двоичных данных, внедренного в базу данных, используйте SQL-запрос для поиска и получения записи, содержащей двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="0860e-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="0860e-129">Используйте [**мсирекордреадстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) для считывания двоичных данных в буфер.</span><span class="sxs-lookup"><span data-stu-id="0860e-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="0860e-130">Чтобы переместить поток двоичных данных из одной базы данных в другую, сначала экспортируйте данные в файл.</span><span class="sxs-lookup"><span data-stu-id="0860e-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="0860e-131">Используйте SQL-запрос для поиска потока данных в файле и используйте [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) для копирования данных из файла в столбец данных \_ таблицы Streams второй базы данных.</span><span class="sxs-lookup"><span data-stu-id="0860e-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="0860e-132">Это гарантирует, что каждая база данных будет иметь собственную копию двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="0860e-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="0860e-133">Вы не можете перемещать двоичные данные из одной базы данных в другую, просто получая запись с данными из первой базы данных и вставляя ее во вторую базу данных.</span><span class="sxs-lookup"><span data-stu-id="0860e-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="0860e-134">Чтобы удалить поток данных, выберите запись и задайте для столбца данных значение null, прежде чем обновлять запись.</span><span class="sxs-lookup"><span data-stu-id="0860e-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="0860e-135">Другой способ — удалить запись из таблицы, удалив ее с помощью [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) или простого SQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="0860e-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="0860e-136">Поток не следует получать в записи, если поток удаляется из таблицы.</span><span class="sxs-lookup"><span data-stu-id="0860e-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="0860e-137">Чтобы переименовать поток данных OLE, обновите столбец "имя" записи.</span><span class="sxs-lookup"><span data-stu-id="0860e-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="0860e-138">Если для этой таблицы размещается удержание с помощью SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="0860e-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="0860e-139">УДЕРЖАНИЕ) или добавление столбца с УДЕРЖАНИЕм, таблица должна быть освобождена с помощью функции FREE.</span><span class="sxs-lookup"><span data-stu-id="0860e-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="0860e-140">Потоки не записываются, пока таблица не будет освобождена или зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="0860e-140">Streams are not written until the table has been released or committed.</span></span>

 

 



