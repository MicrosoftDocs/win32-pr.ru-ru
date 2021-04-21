---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Определяет константы, управляющие преобразованием, применяемым в операторах Директмл [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) и **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803538"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="8b609-103">Перечисление DML_DEPTH_SPACE_ORDER (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="8b609-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="8b609-104">Определяет константы, управляющие преобразованием, применяемым в операторах Директмл [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) и **DML_OPERATOR_SPACE_TO_DEPTH1**.</span><span class="sxs-lookup"><span data-stu-id="8b609-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="8b609-105">Они используются в структурах [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="8b609-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b609-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="8b609-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8b609-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8b609-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b609-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b609-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="8b609-109">Константы</span><span class="sxs-lookup"><span data-stu-id="8b609-109">Constants</span></span>

| <span data-ttu-id="8b609-110">Имя</span><span class="sxs-lookup"><span data-stu-id="8b609-110">Name</span></span> | <span data-ttu-id="8b609-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8b609-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="8b609-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="8b609-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="8b609-113">Приводит к тому, что десятки, используемые в [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) , будут интерпретироваться в следующих макетах, где измерения в круглых скобках будут выровнены вместе.</span><span class="sxs-lookup"><span data-stu-id="8b609-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="8b609-114">- **Версия глубины**: [Пакетная, (Блоккхеигхт, Блокквидс, каналы), высота, ширина]</span><span class="sxs-lookup"><span data-stu-id="8b609-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="8b609-115">- **Версия пространства**: [Пакетная, каналы, (высота, блоккхеигхт), (ширина, блокквидс)]</span><span class="sxs-lookup"><span data-stu-id="8b609-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="8b609-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="8b609-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="8b609-117">Приводит к тому, что десятки, используемые в [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) , будут интерпретироваться в следующих макетах, где измерения в круглых скобках будут выровнены вместе.</span><span class="sxs-lookup"><span data-stu-id="8b609-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="8b609-118">- **Версия глубины**: [Пакетная, (каналы, Блоккхеигхт, блокквидс), высота, ширина]</span><span class="sxs-lookup"><span data-stu-id="8b609-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="8b609-119">- **Версия пространства**: [Пакетная, каналы, (высота, блоккхеигхт), (ширина, блокквидс)]</span><span class="sxs-lookup"><span data-stu-id="8b609-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="8b609-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b609-120">Remarks</span></span>

<span data-ttu-id="8b609-121">Примеры, демонстрирующие последствия этих значений, см. в документации по [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="8b609-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b609-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8b609-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8b609-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="8b609-123">**Header**</span></span> | <span data-ttu-id="8b609-124">директмл. h</span><span class="sxs-lookup"><span data-stu-id="8b609-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="8b609-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b609-125">See also</span></span>

* [<span data-ttu-id="8b609-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="8b609-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="8b609-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="8b609-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="8b609-128">Доступность</span><span class="sxs-lookup"><span data-stu-id="8b609-128">Availability</span></span>
<span data-ttu-id="8b609-129">Это перечисление было представлено в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8b609-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>