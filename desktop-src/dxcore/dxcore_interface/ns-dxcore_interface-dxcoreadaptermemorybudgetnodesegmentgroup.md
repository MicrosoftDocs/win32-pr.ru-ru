---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Описывает группу сегментов памяти для адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413105"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="7fb31-103">Структура Дкскореадаптермеморибуджетнодесегментграуп</span><span class="sxs-lookup"><span data-stu-id="7fb31-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="7fb31-104">Описывает группу сегментов памяти для адаптера.</span><span class="sxs-lookup"><span data-stu-id="7fb31-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fb31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fb31-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="7fb31-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7fb31-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="7fb31-107">нодеиндекс</span><span class="sxs-lookup"><span data-stu-id="7fb31-107">nodeIndex</span></span>

<span data-ttu-id="7fb31-108">Тип: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="7fb31-108">Type: **uint32_t**</span></span>

<span data-ttu-id="7fb31-109">Указывает физический адаптер устройства, для которого запрашиваются сведения о памяти адаптера.</span><span class="sxs-lookup"><span data-stu-id="7fb31-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="7fb31-110">Для операции с одним адаптером задайте для этого параметра значение 0.</span><span class="sxs-lookup"><span data-stu-id="7fb31-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="7fb31-111">Если имеется несколько узлов адаптеров, задайте для этого индекса узел (физический адаптер устройства), для которого требуется запросить сведения о памяти адаптера (см. раздел [многоадаптеровые системы](../../direct3d12/multi-engine.md)).</span><span class="sxs-lookup"><span data-stu-id="7fb31-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="7fb31-112">сегментграуп</span><span class="sxs-lookup"><span data-stu-id="7fb31-112">segmentGroup</span></span>

<span data-ttu-id="7fb31-113">Тип: **[дкскоресегментграуп](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb31-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="7fb31-114">Указывает группирование сегмента памяти адаптера, о котором необходимо выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="7fb31-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fb31-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fb31-115">See also</span></span>

[<span data-ttu-id="7fb31-116">Справочник по Дкскоре</span><span class="sxs-lookup"><span data-stu-id="7fb31-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="7fb31-117">Перечисление адаптеров с использованием DXCore</span><span class="sxs-lookup"><span data-stu-id="7fb31-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="7fb31-118">Системы с несколькими адаптерами</span><span class="sxs-lookup"><span data-stu-id="7fb31-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)