---
description: Получите указатель интерфейса устройства Direct3D 10,1 из указателя интерфейса Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Функция D3DX10GetFeatureLevel1 (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703655"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="19d21-103">Функция D3DX10GetFeatureLevel1</span><span class="sxs-lookup"><span data-stu-id="19d21-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="19d21-104">Получите указатель интерфейса устройства Direct3D 10,1 из указателя интерфейса Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="19d21-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19d21-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="19d21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19d21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d21-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19d21-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d21-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="19d21-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="19d21-109">Указатель на устройство Direct3D 10,0 (см. интерфейс [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="19d21-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="19d21-110">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="19d21-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19d21-111">Тип: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="19d21-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="19d21-112">Указатель на устройство Direct3D 10,1 (см. интерфейс [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).</span><span class="sxs-lookup"><span data-stu-id="19d21-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d21-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19d21-113">Return value</span></span>

<span data-ttu-id="19d21-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19d21-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19d21-115">Эта функция возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="19d21-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="19d21-116">Если можно получить интерфейс устройства Direct3D 10,1, эта функция завершается успешно и передает указатель на интерфейс 10,1 с помощью параметра *ппдевице* .</span><span class="sxs-lookup"><span data-stu-id="19d21-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="19d21-117">Если интерфейс устройства Direct3D 10,1 не может быть получен, эта функция возвращает \_ ошибку E и не возвращает ничего для параметра *ппдевице* .</span><span class="sxs-lookup"><span data-stu-id="19d21-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d21-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19d21-118">Remarks</span></span>

<span data-ttu-id="19d21-119">Чтобы эта функция была выполнена успешно, необходимо получить предоставленный указатель [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) с помощью вызова функции [**D3DX10CreateDevice**](d3dx10createdevice.md) , функции [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , функции [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) или функции [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .</span><span class="sxs-lookup"><span data-stu-id="19d21-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="19d21-120">Можно создать только устройство Direct3D 10,1 на компьютерах под управлением Windows Vista с пакетом обновления 1 (SP1) или более поздней версии и с установленным Direct3D 10,1-совместимым оборудованием.</span><span class="sxs-lookup"><span data-stu-id="19d21-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="19d21-121">Эта функция возвращает «E \_ Fail» на любом компьютере, не отвечающих этим требованиям.</span><span class="sxs-lookup"><span data-stu-id="19d21-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="19d21-122">Однако эту функцию можно вызвать для любой версии Windows с установленной библиотекой DLL D3DX10.</span><span class="sxs-lookup"><span data-stu-id="19d21-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="19d21-123">Требования</span><span class="sxs-lookup"><span data-stu-id="19d21-123">Requirements</span></span>



| <span data-ttu-id="19d21-124">Требование</span><span class="sxs-lookup"><span data-stu-id="19d21-124">Requirement</span></span> | <span data-ttu-id="19d21-125">Значение</span><span class="sxs-lookup"><span data-stu-id="19d21-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d21-126">Header</span><span class="sxs-lookup"><span data-stu-id="19d21-126">Header</span></span><br/> | <dl> <span data-ttu-id="19d21-127"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d21-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d21-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19d21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d21-129">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="19d21-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




