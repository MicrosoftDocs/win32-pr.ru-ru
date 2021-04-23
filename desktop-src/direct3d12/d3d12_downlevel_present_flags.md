---
title: Перечисление D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Флаги, передаваемые методу ID3D12CommandQueueDownlevel::P повторной попытке.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720872"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="9ba35-103">\_ \_ \_ Перечисление флагов предыдущих версий D3D12</span><span class="sxs-lookup"><span data-stu-id="9ba35-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="9ba35-104">Флаги, передаваемые в функцию повторной отправки [**ID3D12CommandQueueDownlevel::P**](id3d12commandqueuedownlevel-present.md) для изменения поведения.</span><span class="sxs-lookup"><span data-stu-id="9ba35-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ba35-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="9ba35-106">Константы</span><span class="sxs-lookup"><span data-stu-id="9ba35-106">Constants</span></span>

<span data-ttu-id="9ba35-107">**\_Флаг D3D12 нижнего уровня \_ отсутствует \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9ba35-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="9ba35-108">Параметры не выбраны.</span><span class="sxs-lookup"><span data-stu-id="9ba35-108">No options selected.</span></span>

<span data-ttu-id="9ba35-109">**D3D12ный \_ \_ флаг представления предыдущих версий \_ \_ ожидает \_ \_ вбланк**</span><span class="sxs-lookup"><span data-stu-id="9ba35-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="9ba35-110">**Текущая** операция не будет выполнена до тех пор, пока не вертикальной синхронизации с момента последнего выполнения **ED.**</span><span class="sxs-lookup"><span data-stu-id="9ba35-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba35-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9ba35-111">Requirements</span></span>

| <span data-ttu-id="9ba35-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9ba35-112">Requirement</span></span> | <span data-ttu-id="9ba35-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba35-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="9ba35-114">Header</span><span class="sxs-lookup"><span data-stu-id="9ba35-114">Header</span></span> | <span data-ttu-id="9ba35-115">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="9ba35-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="9ba35-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9ba35-116">DLL</span></span>    | <span data-ttu-id="9ba35-117">D3D12.dll (только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9ba35-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="9ba35-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ba35-118">See also</span></span>
* [<span data-ttu-id="9ba35-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="9ba35-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="9ba35-120">Перечисления Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ba35-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="9ba35-121">Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="9ba35-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="9ba35-122">Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ba35-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
