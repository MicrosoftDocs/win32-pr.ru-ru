---
title: Интерфейс ID3D12DeviceDownlevel
description: Предоставляет запрос статистики памяти, относящийся к Windows 7.
keywords:
- Интерфейс ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720867"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="d7b74-104">Интерфейс ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="d7b74-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="d7b74-105">Доступ к этому интерфейсу можно получить через **QueryInterface** с [устройства Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) при использовании [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="d7b74-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="d7b74-106">Он предоставляет запрос статистики памяти, относящийся к Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d7b74-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="d7b74-107">Методы</span><span class="sxs-lookup"><span data-stu-id="d7b74-107">Methods</span></span>

<span data-ttu-id="d7b74-108">Интерфейс **ID3D12DeviceDownlevel** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d7b74-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="d7b74-109">Метод</span><span class="sxs-lookup"><span data-stu-id="d7b74-109">Method</span></span> | <span data-ttu-id="d7b74-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d7b74-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="d7b74-111">**куеривидеомеморинфо**</span><span class="sxs-lookup"><span data-stu-id="d7b74-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="d7b74-112">Предоставляет статистику памяти в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d7b74-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d7b74-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d7b74-113">Requirements</span></span>

| <span data-ttu-id="d7b74-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d7b74-114">Requirement</span></span> | <span data-ttu-id="d7b74-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b74-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="d7b74-116">Header</span><span class="sxs-lookup"><span data-stu-id="d7b74-116">Header</span></span> | <span data-ttu-id="d7b74-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="d7b74-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="d7b74-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b74-118">DLL</span></span>    | <span data-ttu-id="d7b74-119">D3D12.dll (только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="d7b74-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d7b74-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7b74-120">See also</span></span>
* [<span data-ttu-id="d7b74-121">Интерфейсы Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7b74-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="d7b74-122">Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="d7b74-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="d7b74-123">Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7b74-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
