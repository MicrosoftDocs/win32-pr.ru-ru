---
title: Функция D3DX11UnsetAllDeviceObjects (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать метод ссылку ID3D11DeviceContext Клеарстате.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- D3DX11UnsetAllDeviceObjects функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355340"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="3df15-105">Функция D3DX11UnsetAllDeviceObjects</span><span class="sxs-lookup"><span data-stu-id="3df15-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="3df15-106">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="3df15-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="3df15-107">Вместо использования этой функции рекомендуется использовать метод [**ссылку ID3D11DeviceContext:: клеарстате**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .</span><span class="sxs-lookup"><span data-stu-id="3df15-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="3df15-108">Удаляет все ресурсы с устройства, присвоив их указателям **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3df15-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="3df15-109">Этот метод должен вызываться во время завершения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="3df15-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="3df15-110">Это гарантирует, что когда один из них освобождает все ресурсы, которые не привязаны к устройству.</span><span class="sxs-lookup"><span data-stu-id="3df15-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df15-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3df15-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="3df15-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3df15-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df15-113">*пконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3df15-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df15-114">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="3df15-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="3df15-115">Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="3df15-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df15-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3df15-116">Return value</span></span>

<span data-ttu-id="3df15-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3df15-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3df15-118">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3df15-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3df15-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3df15-119">Requirements</span></span>



| <span data-ttu-id="3df15-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3df15-120">Requirement</span></span> | <span data-ttu-id="3df15-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3df15-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3df15-122">Header</span><span class="sxs-lookup"><span data-stu-id="3df15-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3df15-123"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df15-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="3df15-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3df15-124">Library</span></span><br/> | <dl> <span data-ttu-id="3df15-125"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3df15-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3df15-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3df15-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df15-127">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="3df15-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





