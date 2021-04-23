---
description: 'Дополнительные сведения: индексирование в таблице'
title: Индексирование в таблице
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080383"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="7dd47-103">Индексирование в таблице</span><span class="sxs-lookup"><span data-stu-id="7dd47-103">Indexing in the Table</span></span>


<span data-ttu-id="7dd47-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7dd47-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="7dd47-105">Индексирование в таблице</span><span class="sxs-lookup"><span data-stu-id="7dd47-105">Indexing in the Table</span></span>

<span data-ttu-id="7dd47-106">Индекс — это набор ключевых столбцов, которые определяют постоянный порядок записей в таблице.</span><span class="sxs-lookup"><span data-stu-id="7dd47-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="7dd47-107">Записи — это индексные записи в первичном индексе.</span><span class="sxs-lookup"><span data-stu-id="7dd47-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="7dd47-108">Один первичный индекс и несколько вторичных индексов можно определить для создания различных заказов данных в таблице.</span><span class="sxs-lookup"><span data-stu-id="7dd47-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="7dd47-109">Хотя можно определить несколько индексов, записи физически хранятся в деревьях B + в порядке, указанном первичным индексом.</span><span class="sxs-lookup"><span data-stu-id="7dd47-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="7dd47-110">Первичный индекс всегда является кластеризованным индексом и также должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="7dd47-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="7dd47-111">Первичный индекс должен быть объявлен перед первой обновлением таблицы для сохранения порядка индексов.</span><span class="sxs-lookup"><span data-stu-id="7dd47-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="7dd47-112">Если в приложении не определен первичный индекс, данные сохраняются в том порядке, в котором записи добавляются в таблицу.</span><span class="sxs-lookup"><span data-stu-id="7dd47-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="7dd47-113">Этот особый индекс называется последовательным индексом.</span><span class="sxs-lookup"><span data-stu-id="7dd47-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="7dd47-114">Отдельные деревья B + используются для упорядочивания записей в соответствии с вторичным индексом.</span><span class="sxs-lookup"><span data-stu-id="7dd47-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="7dd47-115">Элементы индекса во вторичном индексе содержат указатели на данные, хранимые в соответствии с первичным индексом.</span><span class="sxs-lookup"><span data-stu-id="7dd47-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="7dd47-116">Записи индекса для записей в первичном индексе должны быть уникальными, так как вторичный индекс указывает на запись, используя первичный ключ записи.</span><span class="sxs-lookup"><span data-stu-id="7dd47-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="7dd47-117">Вторичные индексы могут иметь или не иметь ограничений уникальности.</span><span class="sxs-lookup"><span data-stu-id="7dd47-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="7dd47-118">Дополнительные сведения см. в разделе " [Обзор базы данных](./database-overview.md) ".</span><span class="sxs-lookup"><span data-stu-id="7dd47-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
