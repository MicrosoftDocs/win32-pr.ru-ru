---
description: Возвращает описание функции.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'Метод ID3DXBaseEffect:: Жетфунктиондеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703994"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="73bbd-103">Метод ID3DXBaseEffect:: Жетфунктиондеск</span><span class="sxs-lookup"><span data-stu-id="73bbd-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="73bbd-104">Возвращает описание функции.</span><span class="sxs-lookup"><span data-stu-id="73bbd-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="73bbd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73bbd-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="73bbd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73bbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73bbd-107">*хфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73bbd-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73bbd-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="73bbd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="73bbd-109">Маркер функции.</span><span class="sxs-lookup"><span data-stu-id="73bbd-109">Function handle.</span></span> <span data-ttu-id="73bbd-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="73bbd-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="73bbd-111">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73bbd-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73bbd-112">Тип: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="73bbd-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="73bbd-113">Возвращает описание функции.</span><span class="sxs-lookup"><span data-stu-id="73bbd-113">Returns a description of the function.</span></span> <span data-ttu-id="73bbd-114">См. [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md).</span><span class="sxs-lookup"><span data-stu-id="73bbd-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73bbd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73bbd-115">Return value</span></span>

<span data-ttu-id="73bbd-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73bbd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73bbd-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="73bbd-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="73bbd-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="73bbd-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="73bbd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="73bbd-119">Requirements</span></span>



| <span data-ttu-id="73bbd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="73bbd-120">Requirement</span></span> | <span data-ttu-id="73bbd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="73bbd-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73bbd-122">Header</span><span class="sxs-lookup"><span data-stu-id="73bbd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="73bbd-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="73bbd-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="73bbd-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73bbd-124">Library</span></span><br/> | <dl> <span data-ttu-id="73bbd-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73bbd-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="73bbd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73bbd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bbd-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="73bbd-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




