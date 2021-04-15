---
title: Перечисление Додовнлоадкостполици
description: Указывает идентификатор параметров политик затрат, связанных со свойством **DODownloadProperty_CostPolicy** .
keywords:
- Перечисление Додовнлоадкостполици, Додовнлоадкостполици
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414873"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="9c1c6-104">Перечисление Додовнлоадкостполици</span><span class="sxs-lookup"><span data-stu-id="9c1c6-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="9c1c6-105">Перечисление **додовнлоадкостполици** указывает идентификатор параметров политик затрат, связанных со свойством **DODownloadProperty_CostPolicy** .</span><span class="sxs-lookup"><span data-stu-id="9c1c6-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c1c6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c1c6-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="9c1c6-107">Константы</span><span class="sxs-lookup"><span data-stu-id="9c1c6-107">Constants</span></span>

| <span data-ttu-id="9c1c6-108">Требование</span><span class="sxs-lookup"><span data-stu-id="9c1c6-108">Requirement</span></span> | <span data-ttu-id="9c1c6-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9c1c6-109">Value</span></span> |
|-|-|
| <span data-ttu-id="9c1c6-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="9c1c6-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="9c1c6-111">Загрузка выполняется независимо от стоимости.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="9c1c6-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="9c1c6-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="9c1c6-113">Загрузка выполняется, если не накладывает затраты или лимиты трафика.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="9c1c6-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="9c1c6-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="9c1c6-115">Загрузка выполняется, если не взимается ни плата, ни исчерпание.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="9c1c6-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="9c1c6-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="9c1c6-117">Загрузка выполняется, если в связи с нагрузкой не взимается плата за роуминг.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="9c1c6-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="9c1c6-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="9c1c6-119">Загрузка выполняется, если не взимается плата.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="9c1c6-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="9c1c6-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="9c1c6-121">Загрузка выполняется, если сеть не подключена к сотовой сети.</span><span class="sxs-lookup"><span data-stu-id="9c1c6-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="9c1c6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9c1c6-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9c1c6-123">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="9c1c6-123">**Minimum supported client**</span></span> | <span data-ttu-id="9c1c6-124">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="9c1c6-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="9c1c6-125">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="9c1c6-125">**Minimum supported server**</span></span> | <span data-ttu-id="9c1c6-126">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="9c1c6-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="9c1c6-127">**Header**</span><span class="sxs-lookup"><span data-stu-id="9c1c6-127">**Header**</span></span> | <span data-ttu-id="9c1c6-128">Деливерйоптимизатиондовнлоадтипес. h</span><span class="sxs-lookup"><span data-stu-id="9c1c6-128">DeliveryOptimizationDownloadTypes.h</span></span> |
