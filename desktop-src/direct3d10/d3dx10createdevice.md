---
description: Создайте наилучшее устройство Direct3D 10, представляющее видеоадаптер. Если можно создать совместимое с Direct3D 10,1 устройство, вы сможете получить указатель интерфейса ID3D10Device1 из возвращенного указателя интерфейса устройства.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Функция D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713906"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="9bf45-104">Функция D3DX10CreateDevice</span><span class="sxs-lookup"><span data-stu-id="9bf45-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="9bf45-105">Создайте наилучшее устройство Direct3D 10, представляющее видеоадаптер.</span><span class="sxs-lookup"><span data-stu-id="9bf45-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="9bf45-106">Если можно создать совместимое с Direct3D 10,1 устройство, вы сможете получить указатель [**интерфейса ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) из возвращенного указателя интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="9bf45-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf45-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bf45-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="9bf45-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bf45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bf45-109">*падаптер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bf45-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf45-110">Тип: **[ **идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="9bf45-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="9bf45-111">Указатель на адаптер дисплея (см. интерфейс [**идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) при создании аппаратного устройства; в противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9bf45-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="9bf45-112">Если при создании аппаратного устройства указано **значение NULL** , Direct3D будет использовать первый адаптер, перечисленный интерфейсом [**идксгифактори**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="9bf45-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9bf45-113">*Дривертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bf45-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf45-114">Тип: **[ **D3D10 \_ \_ Тип драйвера**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="9bf45-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="9bf45-115">Тип драйвера устройства (см. раздел перечисление [**\_ \_ типов драйверов D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ).</span><span class="sxs-lookup"><span data-stu-id="9bf45-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="9bf45-116">Тип драйвера определяется типом создаваемого устройства.</span><span class="sxs-lookup"><span data-stu-id="9bf45-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="9bf45-117">*Программное обеспечение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bf45-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf45-118">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bf45-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bf45-119">Маркер загруженного модуля, который реализует драйвер программного обеспечения (например, D3D10Ref.dll).</span><span class="sxs-lookup"><span data-stu-id="9bf45-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="9bf45-120">Чтобы получить маркер, вызовите функцию [Ошибка GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="9bf45-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="9bf45-121">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bf45-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf45-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bf45-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bf45-123">Флаги создания устройства (см. раздел перечисление [**D3D10 \_ Создание \_ \_ флага устройства**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) ), включающее [уровни API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="9bf45-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="9bf45-124">Эти флаги могут быть побитовыми или объединенными.</span><span class="sxs-lookup"><span data-stu-id="9bf45-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="9bf45-125">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9bf45-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf45-126">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="9bf45-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="9bf45-127">Адрес указателя на созданное устройство (см. интерфейс [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="9bf45-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bf45-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bf45-128">Return value</span></span>

<span data-ttu-id="9bf45-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bf45-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bf45-130">Эта функция возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9bf45-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf45-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bf45-131">Remarks</span></span>

<span data-ttu-id="9bf45-132">Эта функция пытается создать наилучшее устройство для оборудования.</span><span class="sxs-lookup"><span data-stu-id="9bf45-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="9bf45-133">Во-первых, функция пытается создать устройство 10,1.</span><span class="sxs-lookup"><span data-stu-id="9bf45-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="9bf45-134">Если не удается создать устройство 10,1, функция пытается создать устройство 10,0.</span><span class="sxs-lookup"><span data-stu-id="9bf45-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="9bf45-135">Если ни одно из устройств не было успешно создано, функция возвращает \_ ошибку E.</span><span class="sxs-lookup"><span data-stu-id="9bf45-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="9bf45-136">Если приложению нужно создать только устройство 10,1 или только устройство 10,0, используйте следующие функции:</span><span class="sxs-lookup"><span data-stu-id="9bf45-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="9bf45-137">Используйте функцию [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) , чтобы создать только устройство Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="9bf45-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="9bf45-138">Используйте функцию [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) , чтобы создать только устройство Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="9bf45-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="9bf45-139">Используйте функцию [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) для получения указателя интерфейса [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) из указателя интерфейса [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="9bf45-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="9bf45-140">Устройство Direct3D 10,1 можно создать только на компьютерах под управлением Windows Vista с пакетом обновления 1 (SP1) или более поздней версии и с установленным Direct3D 10,1-совместимым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="9bf45-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="9bf45-141">Однако допускается вызов этой функции на компьютерах под управлением любой версии Windows с установленной библиотекой DLL D3DX10.</span><span class="sxs-lookup"><span data-stu-id="9bf45-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf45-142">Требования</span><span class="sxs-lookup"><span data-stu-id="9bf45-142">Requirements</span></span>



| <span data-ttu-id="9bf45-143">Требование</span><span class="sxs-lookup"><span data-stu-id="9bf45-143">Requirement</span></span> | <span data-ttu-id="9bf45-144">Значение</span><span class="sxs-lookup"><span data-stu-id="9bf45-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf45-145">Header</span><span class="sxs-lookup"><span data-stu-id="9bf45-145">Header</span></span><br/> | <dl> <span data-ttu-id="9bf45-146"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bf45-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf45-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bf45-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf45-148">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="9bf45-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
