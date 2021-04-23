---
title: Интерфейс ID3D12CommandQueueDownlevel
description: Предоставляет механизм присутствия, характерный для Windows 7.
keywords:
- Интерфейс ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720868"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="4a3f3-104">Интерфейс ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="4a3f3-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="4a3f3-105">Доступ к этому интерфейсу можно получить через **QueryInterface** из [очереди команд Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) при использовании [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="4a3f3-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="4a3f3-106">Он предоставляет механизм присутствия, характерный для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="4a3f3-107">Методы</span><span class="sxs-lookup"><span data-stu-id="4a3f3-107">Methods</span></span>

<span data-ttu-id="4a3f3-108">Интерфейс **ID3D12CommandQueueDownlevel** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="4a3f3-109">Метод</span><span class="sxs-lookup"><span data-stu-id="4a3f3-109">Method</span></span> | <span data-ttu-id="4a3f3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4a3f3-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="4a3f3-111">**Настоящее**</span><span class="sxs-lookup"><span data-stu-id="4a3f3-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="4a3f3-112">Копирует содержимое из ресурса D3D12 Texture2D в окно.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="4a3f3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4a3f3-113">Requirements</span></span>

| <span data-ttu-id="4a3f3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4a3f3-114">Requirement</span></span> | <span data-ttu-id="4a3f3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4a3f3-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="4a3f3-116">Header</span><span class="sxs-lookup"><span data-stu-id="4a3f3-116">Header</span></span> | <span data-ttu-id="4a3f3-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="4a3f3-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="4a3f3-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4a3f3-118">DLL</span></span>    | <span data-ttu-id="4a3f3-119">D3D12.dll (только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="4a3f3-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="4a3f3-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a3f3-120">See also</span></span>
* [<span data-ttu-id="4a3f3-121">Интерфейсы Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a3f3-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="4a3f3-122">Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="4a3f3-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="4a3f3-123">Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a3f3-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
