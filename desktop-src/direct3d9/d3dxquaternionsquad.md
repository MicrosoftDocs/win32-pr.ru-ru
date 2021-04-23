---
description: Интерполяция между кватернионми с использованием сферической куадрангле интерполяции.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Функция D3DXQuaternionSquad (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694126"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="12216-103">Функция D3DXQuaternionSquad (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="12216-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="12216-104">Интерполяция между кватернионми с использованием сферической куадрангле интерполяции.</span><span class="sxs-lookup"><span data-stu-id="12216-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="12216-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12216-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="12216-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12216-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12216-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="12216-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12216-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="12216-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12216-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="12216-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="12216-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12216-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12216-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="12216-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12216-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="12216-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="12216-113">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12216-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12216-114">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="12216-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12216-115">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="12216-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="12216-116">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12216-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12216-117">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="12216-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12216-118">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="12216-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="12216-119">*ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12216-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12216-120">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="12216-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12216-121">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="12216-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="12216-122">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="12216-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12216-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12216-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12216-124">Параметр, который указывает, насколько проинтерполируются между кватернионми.</span><span class="sxs-lookup"><span data-stu-id="12216-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12216-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12216-125">Return value</span></span>

<span data-ttu-id="12216-126">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="12216-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12216-127">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом сферической куадрангле интерполяции.</span><span class="sxs-lookup"><span data-stu-id="12216-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="12216-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12216-128">Remarks</span></span>

<span data-ttu-id="12216-129">Эта функция использует следующую последовательность сферческих операций интерполяции:</span><span class="sxs-lookup"><span data-stu-id="12216-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="12216-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="12216-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="12216-131">Таким образом, функция **D3DXQuaternionSquad** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="12216-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="12216-132">Пример интерполяции между кватернионами см. в примере Скиннедмеш.</span><span class="sxs-lookup"><span data-stu-id="12216-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="12216-133">Вы можете получить этот пример и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="12216-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="12216-134">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="12216-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="12216-135">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="12216-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="12216-136">Требования</span><span class="sxs-lookup"><span data-stu-id="12216-136">Requirements</span></span>



| <span data-ttu-id="12216-137">Требование</span><span class="sxs-lookup"><span data-stu-id="12216-137">Requirement</span></span> | <span data-ttu-id="12216-138">Значение</span><span class="sxs-lookup"><span data-stu-id="12216-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12216-139">Header</span><span class="sxs-lookup"><span data-stu-id="12216-139">Header</span></span><br/>  | <dl> <span data-ttu-id="12216-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12216-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="12216-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="12216-141">Library</span></span><br/> | <dl> <span data-ttu-id="12216-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12216-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12216-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12216-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12216-144">Математические функции</span><span class="sxs-lookup"><span data-stu-id="12216-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="12216-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="12216-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="12216-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="12216-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="12216-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="12216-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
