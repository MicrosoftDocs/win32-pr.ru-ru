---
description: 'Дополнительные сведения: Добавление таблиц в базу данных'
title: Добавление таблиц в базу данных
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990852"
---
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="25418-103">Добавление таблиц в базу данных</span><span class="sxs-lookup"><span data-stu-id="25418-103">Adding Tables to the Database</span></span>


<span data-ttu-id="25418-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25418-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="25418-105">Добавление таблиц в базу данных</span><span class="sxs-lookup"><span data-stu-id="25418-105">Adding Tables to the Database</span></span>

<span data-ttu-id="25418-106">Таблицы представляют собой разнородную коллекцию записей, которые физически и логически группируют данные в базе данных.</span><span class="sxs-lookup"><span data-stu-id="25418-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="25418-107">Таблицы уникально идентифицируются по имени.</span><span class="sxs-lookup"><span data-stu-id="25418-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="25418-108">Идентификатор таблицы ([JET_TABLEID](./jet-tableid.md)) — это указатель на курсор, который используется для обновления таблиц и перехода по ним.</span><span class="sxs-lookup"><span data-stu-id="25418-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="25418-109">Вы можете открыть несколько [JET_TABLEID](./jet-tableid.md) в одной таблице.</span><span class="sxs-lookup"><span data-stu-id="25418-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="25418-110">Существующая таблица открывается в вызове [жетопентабле](./jetopentable-function.md), а новая таблица создается без строк или столбцов с [жеткреатетабле](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="25418-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="25418-111">Чтобы атомарным образом создать таблицу с начальным набором столбцов и индексов, вызовите [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md) или [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="25418-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="25418-112">Исходный размер таблицы указывается в параметре *лпажес* в [жеткреатетабле](./jetcreatetable-function.md) или в элементе **улпажес** структуры [JET_TABLECREATE](./jet-tablecreate-structure.md) в вызове [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="25418-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="25418-113">Таблицы автоматически увеличиваются при добавлении данных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="25418-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="25418-114">Рост пропорционально начальному размеру таблицы.</span><span class="sxs-lookup"><span data-stu-id="25418-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="25418-115">Столбцы могут быть добавлены в таблицу в любое время с помощью [жетаддколумн](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="25418-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="25418-116">Если приложению больше не требуется доступ к таблице, курсор можно закрыть с помощью [жетклосетабле](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="25418-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="25418-117">Таблицу можно удалить с помощью вызова [жетделететабле](./jetdeletetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="25418-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="25418-118">Операции с таблицами должны выполняться в контексте транзакции.</span><span class="sxs-lookup"><span data-stu-id="25418-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="25418-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="25418-119">See Also</span></span>

[<span data-ttu-id="25418-120">Транзакции</span><span class="sxs-lookup"><span data-stu-id="25418-120">Transactions</span></span>](./transactions.md)
