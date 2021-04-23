---
title: Константы DirectML
description: Следующие константы объявляются в `DirectML.h` .
keywords:
- Константы
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803413"
---
# <a name="directml-constants"></a><span data-ttu-id="2b9b5-104">Константы DirectML</span><span class="sxs-lookup"><span data-stu-id="2b9b5-104">DirectML constants</span></span>

<span data-ttu-id="2b9b5-105">Следующие константы объявляются в `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="2b9b5-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="2b9b5-106">Константа</span><span class="sxs-lookup"><span data-stu-id="2b9b5-106">Constant</span></span> | <span data-ttu-id="2b9b5-107">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9b5-107">Value</span></span> | <span data-ttu-id="2b9b5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2b9b5-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="2b9b5-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="2b9b5-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="2b9b5-110">5</span><span class="sxs-lookup"><span data-stu-id="2b9b5-110">5</span></span> | <span data-ttu-id="2b9b5-111">Десятки Директмл поддерживают не более 5 измерений для DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="2b9b5-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="2b9b5-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="2b9b5-113">8</span><span class="sxs-lookup"><span data-stu-id="2b9b5-113">8</span></span> | <span data-ttu-id="2b9b5-114">Десятки Директмл поддерживают не более 8 измерений для DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="2b9b5-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="2b9b5-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="2b9b5-116">256</span><span class="sxs-lookup"><span data-stu-id="2b9b5-116">256</span></span> | <span data-ttu-id="2b9b5-117">Временные и постоянные буферы должны иметь базовый адрес, выравниваемая до 256 байт.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="2b9b5-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="2b9b5-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="2b9b5-119">256</span><span class="sxs-lookup"><span data-stu-id="2b9b5-119">256</span></span> | <span data-ttu-id="2b9b5-120">Временные и постоянные буферы должны иметь базовый адрес, выравниваемая до 256 байт.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="2b9b5-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="2b9b5-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="2b9b5-122">16</span><span class="sxs-lookup"><span data-stu-id="2b9b5-122">16</span></span> | <span data-ttu-id="2b9b5-123">Для десятков буферов минимальным требованием выравнивания по базовому адресу является 16 байт.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="2b9b5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2b9b5-124">Requirements</span></span>

| <span data-ttu-id="2b9b5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2b9b5-125">Requirement</span></span> | <span data-ttu-id="2b9b5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9b5-126">Value</span></span> |
|-|-|
| <span data-ttu-id="2b9b5-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b9b5-127">Header</span></span> | <span data-ttu-id="2b9b5-128">Директмл. h</span><span class="sxs-lookup"><span data-stu-id="2b9b5-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="2b9b5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b9b5-129">See also</span></span>

* [<span data-ttu-id="2b9b5-130">Справочник по DirectML</span><span class="sxs-lookup"><span data-stu-id="2b9b5-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="2b9b5-131">Справочник по коду</span><span class="sxs-lookup"><span data-stu-id="2b9b5-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="2b9b5-132">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2b9b5-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
