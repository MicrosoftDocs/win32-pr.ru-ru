---
UID: NE:directml.DML_RANDOM_GENERATOR_TYPE
title: DML_RANDOM_GENERATOR_TYPE
description: Определяет константы, указывающие типы генератора случайных случайных чисел.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_TYPE
- DML_RANDOM_GENERATOR_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_RANDOM_GENERATOR_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_TYPE, DML_RANDOM_GENERATOR_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
- directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
ms.openlocfilehash: bcb79fe7737e8b9ddb461c8da8a901960a4b23f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105720003"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a><span data-ttu-id="b7cb3-103">Перечисление DML_RANDOM_GENERATOR_TYPE (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="b7cb3-103">DML_RANDOM_GENERATOR_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="b7cb3-104">Определяет константы, указывающие типы генератора случайных случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="b7cb3-104">Defines constants that specify types of random random-number generator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7cb3-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="b7cb3-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b7cb3-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b7cb3-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cb3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7cb3-107">Syntax</span></span>
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a><span data-ttu-id="b7cb3-108">Константы</span><span class="sxs-lookup"><span data-stu-id="b7cb3-108">Constants</span></span>

| <span data-ttu-id="b7cb3-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b7cb3-109">Name</span></span> | <span data-ttu-id="b7cb3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b7cb3-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="b7cb3-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span><span class="sxs-lookup"><span data-stu-id="b7cb3-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span></span> | <span data-ttu-id="b7cb3-112">Указывает генератор для псевдо-случайных чисел в соответствии с [алгоритмом филокс 4x32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span><span class="sxs-lookup"><span data-stu-id="b7cb3-112">Specifies a generator for pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span> |


## <a name="requirements"></a><span data-ttu-id="b7cb3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b7cb3-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b7cb3-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="b7cb3-114">**Header**</span></span> | <span data-ttu-id="b7cb3-115">директмл. h</span><span class="sxs-lookup"><span data-stu-id="b7cb3-115">directml.h</span></span> |