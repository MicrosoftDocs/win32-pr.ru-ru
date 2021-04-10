---
description: Поскольку установщик использует реляционную базу данных, существуют функции для выполнения запросов язык SQL (SQL) к базе данных. В следующей процедуре описывается использование SQL для запроса к базе данных.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Работа с запросами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998736"
---
# <a name="working-with-queries"></a><span data-ttu-id="b7b3f-104">Работа с запросами</span><span class="sxs-lookup"><span data-stu-id="b7b3f-104">Working with Queries</span></span>

<span data-ttu-id="b7b3f-105">Поскольку установщик использует реляционную базу данных, существуют функции для выполнения запросов язык SQL (SQL) к базе данных.</span><span class="sxs-lookup"><span data-stu-id="b7b3f-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="b7b3f-106">В следующей процедуре описывается использование SQL для запроса к базе данных.</span><span class="sxs-lookup"><span data-stu-id="b7b3f-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="b7b3f-107">**Запрос базы данных с помощью SQL**</span><span class="sxs-lookup"><span data-stu-id="b7b3f-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="b7b3f-108">Откройте объект [**представления**](view-object.md) с соответствующей инструкцией SQL, вызвав функцию [**мсидатабасеопенвиев**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="b7b3f-109">Объект [**представления**](view-object.md) — это логическая таблица, созданная путем применения запроса к набору таблиц.</span><span class="sxs-lookup"><span data-stu-id="b7b3f-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="b7b3f-110">SQL запросы должны соответствовать [синтаксису SQL](sql-syntax.md) , предоставленному установщиком.</span><span class="sxs-lookup"><span data-stu-id="b7b3f-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="b7b3f-111">Эта инструкция SQL может содержать маркеры параметров, которые не указаны, пока не будет запущен объект **представления** .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="b7b3f-112">Запустите объект [**представления**](view-object.md) , вызвав функцию [**мсивиевексекуте**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="b7b3f-113">Получите следующую запись из объекта [**представления**](view-object.md) , вызвав функцию [**мсивиевфетч**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="b7b3f-114">Измените объект [**представления**](view-object.md) , вызвав функцию [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="b7b3f-115">Можно также проверить данные с помощью [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , передав соответствующие флаги.</span><span class="sxs-lookup"><span data-stu-id="b7b3f-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="b7b3f-116">Если **мсивиевмодифи** возвращает ошибку \_ недопустимых \_ данных из запроса на проверку, базовые данные повреждены.</span><span class="sxs-lookup"><span data-stu-id="b7b3f-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="b7b3f-117">Получите подробные сведения об ошибке для объекта [**представления**](view-object.md) , вызвав функцию [**мсивиевжетеррор**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="b7b3f-118">Закройте объект [**представления**](view-object.md) , вызвав функцию [**мсивиевклосе**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .</span><span class="sxs-lookup"><span data-stu-id="b7b3f-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="b7b3f-119">Дополнительные сведения см. в разделе [примеры запросов к базам данных с помощью SQL и скрипта](examples-of-database-queries-using-sql-and-script.md).</span><span class="sxs-lookup"><span data-stu-id="b7b3f-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



