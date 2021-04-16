---
description: '\_Таблица Columns — это системная таблица только для чтения, содержащая каталог столбцов. В нем перечислены столбцы для всех таблиц. Можно выполнить запрос к этой таблице, чтобы выяснить, существует ли данный столбец.'
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Таблица _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662990"
---
# <a name="_columns-table"></a><span data-ttu-id="dd34d-105">\_Таблица Columns</span><span class="sxs-lookup"><span data-stu-id="dd34d-105">\_Columns Table</span></span>

<span data-ttu-id="dd34d-106">\_Таблица Columns — это системная таблица только для чтения, содержащая каталог столбцов.</span><span class="sxs-lookup"><span data-stu-id="dd34d-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="dd34d-107">В нем перечислены столбцы для всех таблиц.</span><span class="sxs-lookup"><span data-stu-id="dd34d-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="dd34d-108">Можно выполнить запрос к этой таблице, чтобы выяснить, существует ли данный столбец.</span><span class="sxs-lookup"><span data-stu-id="dd34d-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="dd34d-109">\_Таблица Columns содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="dd34d-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="dd34d-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="dd34d-110">Column</span></span> | <span data-ttu-id="dd34d-111">Type</span><span class="sxs-lookup"><span data-stu-id="dd34d-111">Type</span></span>                   | <span data-ttu-id="dd34d-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="dd34d-112">Key</span></span> | <span data-ttu-id="dd34d-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="dd34d-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="dd34d-114">Таблица</span><span class="sxs-lookup"><span data-stu-id="dd34d-114">Table</span></span>  | [<span data-ttu-id="dd34d-115">Text</span><span class="sxs-lookup"><span data-stu-id="dd34d-115">Text</span></span>](text.md)       | <span data-ttu-id="dd34d-116">Да</span><span class="sxs-lookup"><span data-stu-id="dd34d-116">Y</span></span>   | <span data-ttu-id="dd34d-117">Нет</span><span class="sxs-lookup"><span data-stu-id="dd34d-117">N</span></span>        |
| <span data-ttu-id="dd34d-118">Число</span><span class="sxs-lookup"><span data-stu-id="dd34d-118">Number</span></span> | [<span data-ttu-id="dd34d-119">Integer</span><span class="sxs-lookup"><span data-stu-id="dd34d-119">Integer</span></span>](integer.md) | <span data-ttu-id="dd34d-120">Да</span><span class="sxs-lookup"><span data-stu-id="dd34d-120">Y</span></span>   | <span data-ttu-id="dd34d-121">Нет</span><span class="sxs-lookup"><span data-stu-id="dd34d-121">N</span></span>        |
| <span data-ttu-id="dd34d-122">Имя</span><span class="sxs-lookup"><span data-stu-id="dd34d-122">Name</span></span>   | [<span data-ttu-id="dd34d-123">Text</span><span class="sxs-lookup"><span data-stu-id="dd34d-123">Text</span></span>](text.md)       | <span data-ttu-id="dd34d-124">Нет</span><span class="sxs-lookup"><span data-stu-id="dd34d-124">N</span></span>   | <span data-ttu-id="dd34d-125">Нет</span><span class="sxs-lookup"><span data-stu-id="dd34d-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="dd34d-126">Столбцы</span><span class="sxs-lookup"><span data-stu-id="dd34d-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="dd34d-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="dd34d-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="dd34d-128">Имя таблицы, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="dd34d-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="dd34d-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Нумерация</span><span class="sxs-lookup"><span data-stu-id="dd34d-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="dd34d-130">Порядок столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="dd34d-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="dd34d-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="dd34d-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="dd34d-132">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="dd34d-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd34d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd34d-133">Remarks</span></span>

<span data-ttu-id="dd34d-134">Поскольку \_ Таблица Columns является системной таблицей, которая не может быть изменена с помощью SQL-запросов, вы не можете получить первичные ключи с помощью функции [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) или [**Свойства примарикэйс**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="dd34d-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="dd34d-135">В таблице Columns хранятся только постоянные столбцы \_ .</span><span class="sxs-lookup"><span data-stu-id="dd34d-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="dd34d-136">Чтобы определить, существует ли временный столбец, необходимо создать представление с помощью инструкции SELECT для \* таблицы, а затем перебрать все поля в записи, возвращаемой функцией [**мсивиевжетколумнинфо**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) , с \_ параметром мсиколинфо Names.</span><span class="sxs-lookup"><span data-stu-id="dd34d-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



