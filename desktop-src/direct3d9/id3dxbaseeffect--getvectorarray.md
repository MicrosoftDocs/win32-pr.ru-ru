---
description: Возвращает массив векторов.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'Метод ID3DXBaseEffect:: Жетвектораррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354123"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="46517-103">Метод ID3DXBaseEffect:: Жетвектораррай</span><span class="sxs-lookup"><span data-stu-id="46517-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="46517-104">Возвращает массив векторов.</span><span class="sxs-lookup"><span data-stu-id="46517-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="46517-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46517-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="46517-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="46517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46517-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46517-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46517-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="46517-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="46517-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="46517-109">Unique identifier.</span></span> <span data-ttu-id="46517-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="46517-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="46517-111">*пвектор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46517-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46517-112">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="46517-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="46517-113">Возвращает массив векторов с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="46517-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="46517-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46517-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46517-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46517-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46517-116">Количество векторов в массиве.</span><span class="sxs-lookup"><span data-stu-id="46517-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46517-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46517-117">Return value</span></span>

<span data-ttu-id="46517-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46517-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46517-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="46517-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46517-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="46517-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="46517-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46517-121">Remarks</span></span>

<span data-ttu-id="46517-122">Если векторы назначения больше, чем исходные векторы, будут заполнены только исходные компоненты каждого целевого вектора, а остальные компоненты вектора назначения будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="46517-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="46517-123">Требования</span><span class="sxs-lookup"><span data-stu-id="46517-123">Requirements</span></span>



| <span data-ttu-id="46517-124">Требование</span><span class="sxs-lookup"><span data-stu-id="46517-124">Requirement</span></span> | <span data-ttu-id="46517-125">Значение</span><span class="sxs-lookup"><span data-stu-id="46517-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46517-126">Header</span><span class="sxs-lookup"><span data-stu-id="46517-126">Header</span></span><br/>  | <dl> <span data-ttu-id="46517-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="46517-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="46517-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46517-128">Library</span></span><br/> | <dl> <span data-ttu-id="46517-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46517-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="46517-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46517-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46517-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="46517-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="46517-132">**сетвектораррай**</span><span class="sxs-lookup"><span data-stu-id="46517-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
