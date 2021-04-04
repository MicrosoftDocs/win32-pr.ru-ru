---
description: Таблица Tables \_ является системной таблицей только для чтения, в которой перечислены все таблицы в базе данных. Запросите эту таблицу, чтобы узнать, существует ли таблица.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Таблица _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909163"
---
# <a name="_tables-table"></a><span data-ttu-id="35956-104">\_Таблица таблиц</span><span class="sxs-lookup"><span data-stu-id="35956-104">\_Tables Table</span></span>

<span data-ttu-id="35956-105">Таблица Tables \_ является системной таблицей только для чтения, в которой перечислены все таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="35956-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="35956-106">Запросите эту таблицу, чтобы узнать, существует ли таблица.</span><span class="sxs-lookup"><span data-stu-id="35956-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="35956-107">Таблица Tables \_ содержит следующий столбец.</span><span class="sxs-lookup"><span data-stu-id="35956-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="35956-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="35956-108">Column</span></span> | <span data-ttu-id="35956-109">Type</span><span class="sxs-lookup"><span data-stu-id="35956-109">Type</span></span>             | <span data-ttu-id="35956-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="35956-110">Key</span></span> | <span data-ttu-id="35956-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="35956-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="35956-112">Имя</span><span class="sxs-lookup"><span data-stu-id="35956-112">Name</span></span>   | [<span data-ttu-id="35956-113">Text</span><span class="sxs-lookup"><span data-stu-id="35956-113">Text</span></span>](text.md) | <span data-ttu-id="35956-114">Да</span><span class="sxs-lookup"><span data-stu-id="35956-114">Y</span></span>   | <span data-ttu-id="35956-115">Нет</span><span class="sxs-lookup"><span data-stu-id="35956-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="35956-116">Столбец</span><span class="sxs-lookup"><span data-stu-id="35956-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="35956-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="35956-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="35956-118">Имя одной из таблиц.</span><span class="sxs-lookup"><span data-stu-id="35956-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35956-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35956-119">Remarks</span></span>

<span data-ttu-id="35956-120">Поскольку \_ Таблица таблиц является системной таблицей, которая не может быть изменена с помощью SQL-запросов, вы не можете получить первичные ключи с помощью функции [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) или [**Свойства примарикэйс**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="35956-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



