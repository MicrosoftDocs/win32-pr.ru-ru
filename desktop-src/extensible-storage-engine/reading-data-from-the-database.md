---
description: 'Дополнительные сведения: чтение данных из базы данных'
title: Чтение данных из базы данных
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683584"
---
# <a name="reading-data-from-the-database"></a><span data-ttu-id="d92ca-103">Чтение данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="d92ca-103">Reading Data from the Database</span></span>


<span data-ttu-id="d92ca-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d92ca-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="d92ca-105">Чтение данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="d92ca-105">Reading Data from the Database</span></span>

<span data-ttu-id="d92ca-106">Чтение данных из базы данных должно выполняться в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="d92ca-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="d92ca-107">В следующей процедуре показано, как выполнить простую операцию чтения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d92ca-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="d92ca-108">Чтение данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="d92ca-108">To read data from a database</span></span>

1.  <span data-ttu-id="d92ca-109">Вызовите [жетбегинтрансактион](./jetbegintransaction-function.md) или [JetBeginTransaction2](./jetbegintransaction2-function.md) с идентификатором сеанса, чтобы начать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="d92ca-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="d92ca-110">Переместите курсор к нужной записи, вызвав [жетмове](./jetmove-function.md) с JET_MoveFirst в параметре *CRowset* .</span><span class="sxs-lookup"><span data-stu-id="d92ca-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="d92ca-111">Дополнительные сведения о том, как переместить курсор, см. в статье [индексирование в разделе таблицы](./indexing-in-the-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d92ca-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="d92ca-112">Вызовите [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) для текущей записи с JET_ColInfo, указанным в параметре *инфолевел* , чтобы получить идентификатор столбца для столбца.</span><span class="sxs-lookup"><span data-stu-id="d92ca-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="d92ca-113">Идентификатор столбца возвращается в структуре [JET_COLUMNDEF](./jet-columndef-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="d92ca-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="d92ca-114">Прочтите данные из столбца, вызвав [жетретриевеколумн](./jetretrievecolumn-function.md) с идентификатором столбца, полученным на шаге 3 в параметре columnid.</span><span class="sxs-lookup"><span data-stu-id="d92ca-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="d92ca-115">Параметр *пвдата* содержит тип данных, указанных в структуре [JET_COLUMNDEF](./jet-columndef-structure.md) , полученной на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="d92ca-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="d92ca-116">Вызовите [жеткоммиттрансактион](./jetcommittransaction-function.md) , чтобы зафиксировать транзакцию в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d92ca-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
