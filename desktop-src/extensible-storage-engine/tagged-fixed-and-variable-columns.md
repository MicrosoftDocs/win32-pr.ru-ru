---
description: 'Дополнительные сведения: помеченные, фиксированные и переменные столбцы'
title: Столбцы с тегами, фиксированными и переменными
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497406"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="c9f6a-103">Столбцы с тегами, фиксированными и переменными</span><span class="sxs-lookup"><span data-stu-id="c9f6a-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="c9f6a-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c9f6a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="c9f6a-105">Столбцы с тегами, фиксированными и переменными</span><span class="sxs-lookup"><span data-stu-id="c9f6a-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="c9f6a-106">Столбцы с тегами, фиксированными и переменными длиной являются первичными типами столбцов, поддерживаемыми ESE.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="c9f6a-107">Помеченные столбцы отсутствуют в записи, если данные не сохранены в столбце и могут быть фиксированной или переменной длиной.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="c9f6a-108">Помеченные столбцы также могут содержать несколько значений в одной записи.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="c9f6a-109">Фиксированные столбцы получают одинаковый объем пространства в каждой строке и для представления значения NULL требуется 1 бит.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="c9f6a-110">Для столбцов переменной длины требуется 2 байта, представляющие размер и значение NULL, и занимают переменный объем пространства в каждой записи.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="c9f6a-111">Дополнительные сведения об помеченных и фиксированных столбцах см. в разделе Jet_bitColumnTagged и Jet_bitColumnFixed в элементе **грбит** структуры [JET_COLUMNDEF](./jet-columndef-structure.md) , используемой при вызове [жетаддколумн](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="c9f6a-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="c9f6a-112">Столбцы переменной длины определяются типом столбца, установленным в параметре *колтип* в вызове [жетаддколумн](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="c9f6a-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="c9f6a-113">Следующие типы столбцов могут быть фиксированными или переменными длиной в зависимости от того, установлен ли параметр Jet_bitColumnFixed:</span><span class="sxs-lookup"><span data-stu-id="c9f6a-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="c9f6a-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="c9f6a-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="c9f6a-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="c9f6a-115">JET_coltypText</span></span>

  - <span data-ttu-id="c9f6a-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="c9f6a-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="c9f6a-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="c9f6a-117">JET_coltypLongText</span></span>

<span data-ttu-id="c9f6a-118">Как правило, данные в записи хранятся с фиксированным диапазоном, сначала с переменным диапазоном, а также с диапазоном с тегами, сохраненным последним.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="c9f6a-119">На следующей схеме показано, как записи хранятся в таблице.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="c9f6a-120">Как показано на схеме, диапазон с тегами может содержать столбцы с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="c9f6a-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="c9f6a-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="c9f6a-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
