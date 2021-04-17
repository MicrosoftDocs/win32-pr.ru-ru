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
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664955"
---
# <a name="directml-constants"></a><span data-ttu-id="db65a-104">Константы DirectML</span><span class="sxs-lookup"><span data-stu-id="db65a-104">DirectML constants</span></span>

<span data-ttu-id="db65a-105">Следующие константы объявляются в `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="db65a-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="db65a-106">Константа</span><span class="sxs-lookup"><span data-stu-id="db65a-106">Constant</span></span> | <span data-ttu-id="db65a-107">Значение</span><span class="sxs-lookup"><span data-stu-id="db65a-107">Value</span></span> | <span data-ttu-id="db65a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="db65a-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="db65a-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="db65a-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="db65a-110">5</span><span class="sxs-lookup"><span data-stu-id="db65a-110">5</span></span> | <span data-ttu-id="db65a-111">Десятки Директмл поддерживают не более 5 измерений для DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="db65a-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="db65a-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="db65a-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="db65a-113">8</span><span class="sxs-lookup"><span data-stu-id="db65a-113">8</span></span> | <span data-ttu-id="db65a-114">Десятки Директмл поддерживают не более 8 измерений для DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="db65a-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="db65a-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="db65a-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="db65a-116">256</span><span class="sxs-lookup"><span data-stu-id="db65a-116">256</span></span> | <span data-ttu-id="db65a-117">Временные и постоянные буферы должны иметь базовый адрес, выравниваемая до 256 байт.</span><span class="sxs-lookup"><span data-stu-id="db65a-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="db65a-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="db65a-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="db65a-119">256</span><span class="sxs-lookup"><span data-stu-id="db65a-119">256</span></span> | <span data-ttu-id="db65a-120">Временные и постоянные буферы должны иметь базовый адрес, выравниваемая до 256 байт.</span><span class="sxs-lookup"><span data-stu-id="db65a-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="db65a-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="db65a-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="db65a-122">16</span><span class="sxs-lookup"><span data-stu-id="db65a-122">16</span></span> | <span data-ttu-id="db65a-123">Для десятков буферов минимальным требованием выравнивания по базовому адресу является 16 байт.</span><span class="sxs-lookup"><span data-stu-id="db65a-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="db65a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="db65a-124">Requirements</span></span>

| <span data-ttu-id="db65a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="db65a-125">Requirement</span></span> | <span data-ttu-id="db65a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="db65a-126">Value</span></span> |
|-|-|
| <span data-ttu-id="db65a-127">Header</span><span class="sxs-lookup"><span data-stu-id="db65a-127">Header</span></span> | <span data-ttu-id="db65a-128">D3D12. h</span><span class="sxs-lookup"><span data-stu-id="db65a-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="db65a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db65a-129">See also</span></span>

* [<span data-ttu-id="db65a-130">Справочник по DirectML</span><span class="sxs-lookup"><span data-stu-id="db65a-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="db65a-131">Справочник по коду</span><span class="sxs-lookup"><span data-stu-id="db65a-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="db65a-132">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="db65a-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
