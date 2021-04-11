---
description: Получение списка вершин, на которые влияет заданная кость, и списка интенсивности влияния этой кости на каждую вершину.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'Метод ID3DX10SkinInfo:: Жетбонеинфлуенцес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273972"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="0bb77-103">Метод ID3DX10SkinInfo:: Жетбонеинфлуенцес</span><span class="sxs-lookup"><span data-stu-id="0bb77-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="0bb77-104">Получение списка вершин, на которые влияет заданная кость, и списка интенсивности влияния этой кости на каждую вершину.</span><span class="sxs-lookup"><span data-stu-id="0bb77-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb77-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bb77-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="0bb77-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bb77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb77-107">*Бонеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bb77-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb77-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bb77-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bb77-109">Индекс, указывающий существующую кость.</span><span class="sxs-lookup"><span data-stu-id="0bb77-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="0bb77-110">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="0bb77-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bb77-111">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bb77-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb77-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bb77-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bb77-113">Смещение от верхнего края списка влияющих вершин.</span><span class="sxs-lookup"><span data-stu-id="0bb77-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="0bb77-114">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетбонеинфлуенцекаунт**](id3dx10skininfo-getboneinfluencecount.md).</span><span class="sxs-lookup"><span data-stu-id="0bb77-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bb77-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bb77-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb77-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bb77-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bb77-117">Число индексов и весов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="0bb77-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="0bb77-118">Значение должно находиться в диапазоне от 0 до значения, возвращаемого ID3DX10SkinInfo:: Жетбонеинфлуенцекаунт.</span><span class="sxs-lookup"><span data-stu-id="0bb77-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="0bb77-119">*пдестиндицес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0bb77-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb77-120">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bb77-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bb77-121">Список индексов в буфере вершин, каждый из которых представляет вершину, на которую влияет кость.</span><span class="sxs-lookup"><span data-stu-id="0bb77-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="0bb77-122">Эти значения соответствуют значениям в Пдествеигхтс, таким, что Пдестиндицес \[ i \] соответствует пдествеигхтс \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="0bb77-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="0bb77-123">*пдествеигхтс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0bb77-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb77-124">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="0bb77-124">Type: **float\***</span></span>

<span data-ttu-id="0bb77-125">Список величин влияния на кость на каждую вершину.</span><span class="sxs-lookup"><span data-stu-id="0bb77-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="0bb77-126">Эти значения соответствуют значениям в Пдестиндицес, таким, что Пдествеигхтс \[ i \] соответствует пдестиндицес \[ i \] . f</span><span class="sxs-lookup"><span data-stu-id="0bb77-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb77-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bb77-127">Return value</span></span>

<span data-ttu-id="0bb77-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bb77-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bb77-129">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="0bb77-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0bb77-130">Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ INVALIDARG или e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0bb77-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb77-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0bb77-131">Requirements</span></span>



| <span data-ttu-id="0bb77-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0bb77-132">Requirement</span></span> | <span data-ttu-id="0bb77-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0bb77-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb77-134">Header</span><span class="sxs-lookup"><span data-stu-id="0bb77-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0bb77-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb77-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0bb77-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0bb77-136">Library</span></span><br/> | <dl> <span data-ttu-id="0bb77-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bb77-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb77-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bb77-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb77-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="0bb77-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="0bb77-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="0bb77-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
