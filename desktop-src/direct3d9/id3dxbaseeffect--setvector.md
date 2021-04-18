---
description: Задает вектор.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'Метод ID3DXBaseEffect:: Сетвектор (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714009"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="37d40-103">Метод ID3DXBaseEffect:: Сетвектор</span><span class="sxs-lookup"><span data-stu-id="37d40-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="37d40-104">Задает вектор.</span><span class="sxs-lookup"><span data-stu-id="37d40-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37d40-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="37d40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37d40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37d40-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37d40-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d40-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="37d40-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="37d40-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="37d40-109">Unique identifier.</span></span> <span data-ttu-id="37d40-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="37d40-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="37d40-111">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37d40-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d40-112">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="37d40-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="37d40-113">Указатель на вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="37d40-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37d40-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37d40-114">Return value</span></span>

<span data-ttu-id="37d40-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37d40-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37d40-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="37d40-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="37d40-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="37d40-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="37d40-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37d40-118">Remarks</span></span>

<span data-ttu-id="37d40-119">Если вектор назначения меньше, чем исходный вектор, дополнительные компоненты исходного вектора будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="37d40-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d40-120">Требования</span><span class="sxs-lookup"><span data-stu-id="37d40-120">Requirements</span></span>



| <span data-ttu-id="37d40-121">Требование</span><span class="sxs-lookup"><span data-stu-id="37d40-121">Requirement</span></span> | <span data-ttu-id="37d40-122">Значение</span><span class="sxs-lookup"><span data-stu-id="37d40-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d40-123">Header</span><span class="sxs-lookup"><span data-stu-id="37d40-123">Header</span></span><br/>  | <dl> <span data-ttu-id="37d40-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="37d40-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="37d40-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37d40-125">Library</span></span><br/> | <dl> <span data-ttu-id="37d40-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37d40-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="37d40-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37d40-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d40-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="37d40-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="37d40-129">**Вектор**</span><span class="sxs-lookup"><span data-stu-id="37d40-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




