---
description: Возвращает описание этапа.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'Метод ID3DXBaseEffect:: Жетпассдеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713992"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="6abc0-103">Метод ID3DXBaseEffect:: Жетпассдеск</span><span class="sxs-lookup"><span data-stu-id="6abc0-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="6abc0-104">Возвращает описание этапа.</span><span class="sxs-lookup"><span data-stu-id="6abc0-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6abc0-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6abc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6abc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abc0-107">*хпасс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6abc0-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6abc0-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6abc0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6abc0-109">Передача маркера.</span><span class="sxs-lookup"><span data-stu-id="6abc0-109">Pass handle.</span></span> <span data-ttu-id="6abc0-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6abc0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6abc0-111">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6abc0-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6abc0-112">Тип: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="6abc0-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="6abc0-113">Возвращает описание указанного прохода.</span><span class="sxs-lookup"><span data-stu-id="6abc0-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="6abc0-114">См. [**D3DXPASS \_ DESC**](d3dxpass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="6abc0-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6abc0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6abc0-115">Return value</span></span>

<span data-ttu-id="6abc0-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6abc0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6abc0-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="6abc0-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6abc0-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="6abc0-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6abc0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6abc0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6abc0-120">Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), этот метод возвращает в функции шейдера указатели **null** (в [**D3DXPASS \_ DESC**](d3dxpass-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="6abc0-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6abc0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6abc0-121">Requirements</span></span>



| <span data-ttu-id="6abc0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6abc0-122">Requirement</span></span> | <span data-ttu-id="6abc0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6abc0-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6abc0-124">Header</span><span class="sxs-lookup"><span data-stu-id="6abc0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6abc0-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6abc0-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6abc0-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6abc0-126">Library</span></span><br/> | <dl> <span data-ttu-id="6abc0-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6abc0-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6abc0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6abc0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abc0-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6abc0-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




