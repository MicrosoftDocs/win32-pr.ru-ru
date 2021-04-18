---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Определяет константы, указывающие направление операции вдоль заданной оси для оператора (например, суммирование, выбор элементов Top-k, выбор минимального элемента).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_AXIS_DIRECTION
ms.openlocfilehash: 18cd2189f88378245be0824e0a68e5f618008bc7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719922"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="63fe5-103">Перечисление DML_AXIS_DIRECTION (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="63fe5-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="63fe5-104">Определяет константы, указывающие направление операции вдоль заданной оси для оператора (например, суммирование, выбор элементов Top-k, выбор минимального элемента).</span><span class="sxs-lookup"><span data-stu-id="63fe5-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63fe5-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="63fe5-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="63fe5-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="63fe5-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63fe5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63fe5-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="63fe5-108">Константы</span><span class="sxs-lookup"><span data-stu-id="63fe5-108">Constants</span></span>

| <span data-ttu-id="63fe5-109">Имя</span><span class="sxs-lookup"><span data-stu-id="63fe5-109">Name</span></span> | <span data-ttu-id="63fe5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="63fe5-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="63fe5-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="63fe5-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="63fe5-112">Задает увеличение порядка (от нижнего индекса до индекса High).</span><span class="sxs-lookup"><span data-stu-id="63fe5-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="63fe5-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="63fe5-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="63fe5-114">Задает понижение порядка (от верхнего индекса до нижнего индекса).</span><span class="sxs-lookup"><span data-stu-id="63fe5-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="63fe5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="63fe5-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="63fe5-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="63fe5-116">**Header**</span></span> | <span data-ttu-id="63fe5-117">директмл. h</span><span class="sxs-lookup"><span data-stu-id="63fe5-117">directml.h</span></span> |