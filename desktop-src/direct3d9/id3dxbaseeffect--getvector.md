---
description: Возвращает вектор.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'Метод ID3DXBaseEffect:: Vector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354130"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="ceff2-103">Метод ID3DXBaseEffect:: Vector</span><span class="sxs-lookup"><span data-stu-id="ceff2-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="ceff2-104">Возвращает вектор.</span><span class="sxs-lookup"><span data-stu-id="ceff2-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceff2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceff2-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="ceff2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceff2-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ceff2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceff2-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ceff2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ceff2-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="ceff2-109">Unique identifier.</span></span> <span data-ttu-id="ceff2-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ceff2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceff2-111">*пвектор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ceff2-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ceff2-112">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ceff2-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ceff2-113">Возвращает вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="ceff2-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceff2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ceff2-114">Return value</span></span>

<span data-ttu-id="ceff2-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ceff2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ceff2-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ceff2-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ceff2-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ceff2-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceff2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ceff2-118">Remarks</span></span>

<span data-ttu-id="ceff2-119">Если вектор назначения больше, чем исходный вектор, будут заполнены только исходные компоненты целевого вектора, а остальные компоненты будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="ceff2-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceff2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ceff2-120">Requirements</span></span>



| <span data-ttu-id="ceff2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ceff2-121">Requirement</span></span> | <span data-ttu-id="ceff2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ceff2-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceff2-123">Header</span><span class="sxs-lookup"><span data-stu-id="ceff2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ceff2-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceff2-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ceff2-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ceff2-125">Library</span></span><br/> | <dl> <span data-ttu-id="ceff2-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ceff2-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ceff2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ceff2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceff2-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ceff2-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ceff2-129">**сетвектор**</span><span class="sxs-lookup"><span data-stu-id="ceff2-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




