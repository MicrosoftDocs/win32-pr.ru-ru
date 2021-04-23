---
description: Создайте наилучшее устройство Direct3D и цепочку буферов.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Функция D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355550"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="f1541-103">Функция D3DX10CreateDeviceAndSwapChain</span><span class="sxs-lookup"><span data-stu-id="f1541-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="f1541-104">Создайте наилучшее устройство Direct3D и цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="f1541-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1541-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1541-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="f1541-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1541-107">*падаптер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1541-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-108">Тип: **[ **идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="f1541-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="f1541-109">Указатель на [**идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span><span class="sxs-lookup"><span data-stu-id="f1541-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="f1541-110">*Дривертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1541-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-111">Тип: **[ **D3D10 \_ \_ Тип драйвера**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="f1541-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="f1541-112">Тип драйвера для устройства.</span><span class="sxs-lookup"><span data-stu-id="f1541-112">The type of driver for the device.</span></span> <span data-ttu-id="f1541-113">См. раздел [**\_ \_ Тип драйвера D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span><span class="sxs-lookup"><span data-stu-id="f1541-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="f1541-114">*Программное обеспечение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1541-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-115">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1541-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1541-116">Обработчик для библиотеки DLL, реализующей программное средство прорисовки.</span><span class="sxs-lookup"><span data-stu-id="f1541-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="f1541-117">Должен иметь **значение NULL** , если дривертипе не является программным.</span><span class="sxs-lookup"><span data-stu-id="f1541-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="f1541-118">ХМОДУЛЕ библиотеки DLL можно получить с помощью [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)или [Ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="f1541-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="f1541-119">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1541-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1541-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1541-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f1541-121">Optional.</span></span> <span data-ttu-id="f1541-122">Флаги создания устройств (см. раздел [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)), который включает [уровни API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="f1541-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="f1541-123">Эти флаги могут быть побитовыми или объединенными.</span><span class="sxs-lookup"><span data-stu-id="f1541-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="f1541-124">*псвапчаиндеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1541-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-125">Тип: **[ **\_ \_ цепочка \_ перекачки DXGI**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="f1541-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="f1541-126">Описание цепочки буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="f1541-126">Description of the swap chain.</span></span> <span data-ttu-id="f1541-127">См. раздел " [**\_ \_ цепочка \_ подкачки DXGI**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)".</span><span class="sxs-lookup"><span data-stu-id="f1541-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="f1541-128">*ппсвапчаин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1541-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-129">Тип: **[ **идксгисвапчаин**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1541-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="f1541-130">Адрес указателя на [**идксгисвапчаин**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="f1541-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="f1541-131">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1541-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1541-132">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1541-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="f1541-133">Адрес указателя на [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) , который будет принимать созданное устройство.</span><span class="sxs-lookup"><span data-stu-id="f1541-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1541-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1541-134">Return value</span></span>

<span data-ttu-id="f1541-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1541-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1541-136">Этот метод возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f1541-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1541-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1541-137">Remarks</span></span>

<span data-ttu-id="f1541-138">Для создания наилучшего устройства этот метод реализует несколько вариантов создания устройства.</span><span class="sxs-lookup"><span data-stu-id="f1541-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="f1541-139">Во-первых, метод пытается создать устройство 10,1 (и цепь подкачки).</span><span class="sxs-lookup"><span data-stu-id="f1541-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="f1541-140">Если это не удается, метод пытается создать устройство 10,0.</span><span class="sxs-lookup"><span data-stu-id="f1541-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="f1541-141">Если это не удается, метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f1541-141">If that fails, the method will fail.</span></span> <span data-ttu-id="f1541-142">Если приложению нужно создать только устройство 10,1 или только устройство 10,0, используйте эти API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f1541-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="f1541-143">Используйте [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) , чтобы создать устройство и цепочку подкачки Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="f1541-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="f1541-144">Используйте [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) , чтобы создать устройство и цепочку подкачки Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="f1541-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="f1541-145">Для этого метода требуется Windows Vista с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f1541-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1541-146">Требования</span><span class="sxs-lookup"><span data-stu-id="f1541-146">Requirements</span></span>



| <span data-ttu-id="f1541-147">Требование</span><span class="sxs-lookup"><span data-stu-id="f1541-147">Requirement</span></span> | <span data-ttu-id="f1541-148">Значение</span><span class="sxs-lookup"><span data-stu-id="f1541-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1541-149">Header</span><span class="sxs-lookup"><span data-stu-id="f1541-149">Header</span></span><br/> | <dl> <span data-ttu-id="f1541-150"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1541-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1541-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1541-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1541-152">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="f1541-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
