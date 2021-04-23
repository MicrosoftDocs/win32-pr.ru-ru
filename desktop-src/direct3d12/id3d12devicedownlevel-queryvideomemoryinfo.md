---
title: 'Метод ID3D12DeviceDownlevel:: Куеривидеомеморинфо'
description: 'Копирует содержимое из ресурса Texture2D Direct3D 12 в окно. | Метод ID3D12DeviceDownlevel:: Куеривидеомеморинфо'
keywords:
- Метод Куеривидеомеморинфо
- Метод Куеривидеомеморинфо, интерфейс ID3D12DeviceDownlevel
- Интерфейс ID3D12DeviceDownlevel, метод Куеривидеомеморинфо
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720921"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="11006-107">Метод ID3D12DeviceDownlevel:: Куеривидеомеморинфо</span><span class="sxs-lookup"><span data-stu-id="11006-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="11006-108">Предоставляет статистику памяти в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11006-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="11006-109">Этот метод эквивалентен [IDXGIAdapter3:: куеривидеомеморинфо](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), который недоступен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11006-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="11006-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11006-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="11006-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="11006-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="11006-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="11006-112">Type: **UINT**</span></span>

<span data-ttu-id="11006-113">Указывает физический адаптер устройства, для которого запрашиваются данные видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="11006-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="11006-114">Для операции с одним GPU установите значение 0.</span><span class="sxs-lookup"><span data-stu-id="11006-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="11006-115">Если имеется несколько узлов GPU, задайте для него индекс узла (физического адаптера устройства), для которого запрашиваются данные видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="11006-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="11006-116">См. раздел [многоадаптеровые системы](multi-engine.md).</span><span class="sxs-lookup"><span data-stu-id="11006-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="11006-117">Тип: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="11006-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="11006-118">Указывает **DXGI_MEMORY_SEGMENT_GROUP** , определяющий группу как локальную или нелокальную.</span><span class="sxs-lookup"><span data-stu-id="11006-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="11006-119">Тип: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="11006-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="11006-120">Заполняет структуру **DXGI_QUERY_VIDEO_MEMORY_INFO** текущими значениями.</span><span class="sxs-lookup"><span data-stu-id="11006-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="11006-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11006-121">Return value</span></span>

<span data-ttu-id="11006-122">Возвращает **S_OK** при успешном выполнении или в случае сбоя HRESULT.</span><span class="sxs-lookup"><span data-stu-id="11006-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="11006-123">Требования</span><span class="sxs-lookup"><span data-stu-id="11006-123">Requirements</span></span>

| <span data-ttu-id="11006-124">Требование</span><span class="sxs-lookup"><span data-stu-id="11006-124">Requirement</span></span> | <span data-ttu-id="11006-125">Значение</span><span class="sxs-lookup"><span data-stu-id="11006-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="11006-126">Header</span><span class="sxs-lookup"><span data-stu-id="11006-126">Header</span></span> | <span data-ttu-id="11006-127">d3d12downlevel. h и dxgi1_4. h</span><span class="sxs-lookup"><span data-stu-id="11006-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="11006-128">DLL</span><span class="sxs-lookup"><span data-stu-id="11006-128">DLL</span></span>    | <span data-ttu-id="11006-129">D3D12.dll (только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="11006-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="11006-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11006-130">See also</span></span>
* [<span data-ttu-id="11006-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="11006-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="11006-132">Интерфейсы Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="11006-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="11006-133">Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="11006-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="11006-134">Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="11006-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
