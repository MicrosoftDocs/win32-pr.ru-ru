---
description: Извлекает параметры поверхности рендеринга.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'Метод ID3DXRenderToSurface:: desc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273952"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="da369-103">Метод ID3DXRenderToSurface:: DESC</span><span class="sxs-lookup"><span data-stu-id="da369-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="da369-104">Извлекает параметры поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="da369-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="da369-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da369-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="da369-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da369-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da369-107">*ппараметерс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="da369-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da369-108">Тип: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="da369-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="da369-109">Указатель на структуру [**\_ DESC D3DXRTS**](d3dxrts-desc.md) , описывающую параметры поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="da369-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da369-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da369-110">Return value</span></span>

<span data-ttu-id="da369-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da369-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da369-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="da369-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da369-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="da369-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="da369-114">Требования</span><span class="sxs-lookup"><span data-stu-id="da369-114">Requirements</span></span>



| <span data-ttu-id="da369-115">Требование</span><span class="sxs-lookup"><span data-stu-id="da369-115">Requirement</span></span> | <span data-ttu-id="da369-116">Значение</span><span class="sxs-lookup"><span data-stu-id="da369-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da369-117">Header</span><span class="sxs-lookup"><span data-stu-id="da369-117">Header</span></span><br/>  | <dl> <span data-ttu-id="da369-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="da369-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="da369-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da369-119">Library</span></span><br/> | <dl> <span data-ttu-id="da369-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da369-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da369-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da369-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da369-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="da369-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 




