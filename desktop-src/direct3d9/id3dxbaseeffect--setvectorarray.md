---
description: Задает массив векторов.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: 'Метод ID3DXBaseEffect:: Сетвектораррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4c5deace65608ee547b8fdcc4fb236b11d38c810
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000436"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a><span data-ttu-id="528fb-103">Метод ID3DXBaseEffect:: Сетвектораррай</span><span class="sxs-lookup"><span data-stu-id="528fb-103">ID3DXBaseEffect::SetVectorArray method</span></span>

<span data-ttu-id="528fb-104">Задает массив векторов.</span><span class="sxs-lookup"><span data-stu-id="528fb-104">Sets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="528fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="528fb-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="528fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="528fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="528fb-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="528fb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="528fb-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="528fb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="528fb-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="528fb-109">Unique identifier.</span></span> <span data-ttu-id="528fb-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="528fb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="528fb-111">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="528fb-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="528fb-112">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="528fb-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="528fb-113">Массив векторов с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="528fb-113">Array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="528fb-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="528fb-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="528fb-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="528fb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="528fb-116">Количество векторов в массиве.</span><span class="sxs-lookup"><span data-stu-id="528fb-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="528fb-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="528fb-117">Return value</span></span>

<span data-ttu-id="528fb-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="528fb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="528fb-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="528fb-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="528fb-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="528fb-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="528fb-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="528fb-121">Remarks</span></span>

<span data-ttu-id="528fb-122">Если векторы назначения меньше, чем исходные векторы, дополнительные компоненты исходных векторов будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="528fb-122">If the destination vectors are smaller than the source vectors, the additional components of the source vectors will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="528fb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="528fb-123">Requirements</span></span>



| <span data-ttu-id="528fb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="528fb-124">Requirement</span></span> | <span data-ttu-id="528fb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="528fb-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="528fb-126">Header</span><span class="sxs-lookup"><span data-stu-id="528fb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="528fb-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="528fb-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="528fb-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="528fb-128">Library</span></span><br/> | <dl> <span data-ttu-id="528fb-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="528fb-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="528fb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="528fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528fb-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="528fb-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="528fb-132">**жетвектораррай**</span><span class="sxs-lookup"><span data-stu-id="528fb-132">**GetVectorArray**</span></span>](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
