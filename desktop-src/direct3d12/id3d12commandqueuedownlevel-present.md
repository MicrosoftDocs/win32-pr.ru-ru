---
title: 'ID3D12CommandQueueDownlevel: метод повторной отправки:P'
description: 'Копирует содержимое из ресурса Texture2D Direct3D 12 в окно. | ID3D12CommandQueueDownlevel: метод повторной отправки:P'
keywords:
- Метод Present
- Метод Present, интерфейс ID3D12CommandQueueDownlevel
- Интерфейс ID3D12CommandQueueDownlevel, метод Present
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720922"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="e2785-107">ID3D12CommandQueueDownlevel: метод повторной отправки:P</span><span class="sxs-lookup"><span data-stu-id="e2785-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="e2785-108">Копирует содержимое из ресурса Texture2D Direct3D 12 в окно.</span><span class="sxs-lookup"><span data-stu-id="e2785-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2785-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2785-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="e2785-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2785-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="e2785-111">Тип: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="e2785-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="e2785-112">Список открытых команд, который Direct3D 12 помещает в очередь на текущую команду, а затем закрывается и отправляется.</span><span class="sxs-lookup"><span data-stu-id="e2785-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="e2785-113">Тип: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="e2785-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="e2785-114">Ресурс, содержащий необходимое содержимое для показа, с измерением [**ресурса измерения D3D12 \_ \_ \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)и форматом, который является одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="e2785-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="e2785-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="e2785-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="e2785-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2785-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="e2785-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2785-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="e2785-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="e2785-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="e2785-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2785-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="e2785-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2785-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="e2785-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2785-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="e2785-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="e2785-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="e2785-123">Тип: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2785-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2785-124">Маркер окна, в котором должно отображаться содержимое.</span><span class="sxs-lookup"><span data-stu-id="e2785-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="e2785-125">Тип: **[ \_ \_ \_ Флаги представления нижнего уровня D3D12](d3d12_downlevel_present_flags.md)**</span><span class="sxs-lookup"><span data-stu-id="e2785-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="e2785-126">Флаги для изменения **текущей** операции.</span><span class="sxs-lookup"><span data-stu-id="e2785-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2785-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2785-127">Return value</span></span>

<span data-ttu-id="e2785-128">Возвращает **S_OK** при успешном выполнении или в случае сбоя HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e2785-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2785-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e2785-129">Requirements</span></span>

| <span data-ttu-id="e2785-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e2785-130">Requirement</span></span> | <span data-ttu-id="e2785-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e2785-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="e2785-132">Header</span><span class="sxs-lookup"><span data-stu-id="e2785-132">Header</span></span> | <span data-ttu-id="e2785-133">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="e2785-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="e2785-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e2785-134">DLL</span></span>    | <span data-ttu-id="e2785-135">D3D12.dll (только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e2785-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e2785-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2785-136">See also</span></span>
* [<span data-ttu-id="e2785-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="e2785-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="e2785-138">Интерфейсы Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2785-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="e2785-139">Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="e2785-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="e2785-140">Direct3D 12 в Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2785-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
