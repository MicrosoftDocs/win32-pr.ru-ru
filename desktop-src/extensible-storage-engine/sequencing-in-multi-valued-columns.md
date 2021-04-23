---
description: Дополнительные сведения см. в статье Виртуализация в столбцах с несколькими значениями.
title: Последовательность в столбцах с несколькими значениями
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569029"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="9a0c5-103">Последовательность в столбцах с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="9a0c5-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="9a0c5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9a0c5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="9a0c5-105">Последовательность в столбцах с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="9a0c5-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="9a0c5-106">Значения в столбце с несколькими значениями идентифицируются по номеру индекса, который называется *итагсекуенце*.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="9a0c5-107">Это число является ссылкой на одно значение столбца.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="9a0c5-108">Этот номер используется, когда новые значения задаются, извлекаются или перечисляются в столбце.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="9a0c5-109">*Итагсекуенце* используется в различных структурах, включая:</span><span class="sxs-lookup"><span data-stu-id="9a0c5-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="9a0c5-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="9a0c5-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="9a0c5-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="9a0c5-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="9a0c5-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="9a0c5-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="9a0c5-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="9a0c5-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="9a0c5-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="9a0c5-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="9a0c5-115">Этот *итагсекуенце* начинается с 1 для каждого значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="9a0c5-116">Порядковый номер увеличивается при добавлении новых значений в столбец.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="9a0c5-117">Установка значения в столбце с параметром *итагсекуенце* , равным 0, означает, что значение будет добавлено к набору значений, уже наданных в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="9a0c5-118">Использование *итагсекуенце* больше, чем количество значений, заданных для столбца, будет иметь одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="9a0c5-119">Если указать *итагсекуенце* существующего значения, это значение будет перезаписано без вставки нового значения.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="9a0c5-120">Установка существующего значения равным NULL приведет к удалению этого значения из набора значений, уже наданных в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="9a0c5-121">Все последующие значения в столбце будут переноситься вниз на один слот, что последующий доступ к этим значениям с помощью *итагсекуенце* будет иметь номер, который еще не использовался ранее.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="9a0c5-122">На следующей диаграмме показана *итагсекуенце* в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="9a0c5-123">Столбец с именем ColA имеет три записи: val1, val2 и Val3 с *итагсекуенце* 1, 2 и 3 соответственно.</span><span class="sxs-lookup"><span data-stu-id="9a0c5-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="9a0c5-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="9a0c5-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
