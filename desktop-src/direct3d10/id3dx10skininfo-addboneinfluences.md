---
description: Включите существующую кость, чтобы она влияла на группу вершин, и определите, насколько сильно влияют на эту кость на каждой вершине.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'Метод ID3DX10SkinInfo:: Аддбонеинфлуенцес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273794"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="1b72d-103">Метод ID3DX10SkinInfo:: Аддбонеинфлуенцес</span><span class="sxs-lookup"><span data-stu-id="1b72d-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="1b72d-104">Включите существующую кость, чтобы она влияла на группу вершин, и определите, насколько сильно влияют на эту кость на каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="1b72d-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b72d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b72d-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="1b72d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b72d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b72d-107">*Бонеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b72d-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b72d-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b72d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b72d-109">Индекс, указывающий существующую кость.</span><span class="sxs-lookup"><span data-stu-id="1b72d-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="1b72d-110">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="1b72d-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b72d-111">*Инфлуенцекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b72d-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b72d-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b72d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b72d-113">Число вершин, добавляемых к влиянию на кость.</span><span class="sxs-lookup"><span data-stu-id="1b72d-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="1b72d-114">*пиндицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b72d-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b72d-115">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b72d-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1b72d-116">Указатель на массив индексов вершин.</span><span class="sxs-lookup"><span data-stu-id="1b72d-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="1b72d-117">Каждый элемент этого массива имеет соответствующий элемент в Пвеигхтс, так что Пиндицес \[ i \] соответствует пвеигхтс \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="1b72d-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="1b72d-118">Соответствующее значение в Пвеигхтс \[ i \] определяет, какое влияние на бонеиндекс будет на вершину, индексируемую с помощью пиндицес \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="1b72d-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="1b72d-119">Размер массива Пиндицес должен быть больше или равен Инфлуенцекаунт.</span><span class="sxs-lookup"><span data-stu-id="1b72d-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="1b72d-120">*пвеигхтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b72d-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b72d-121">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="1b72d-121">Type: **float\***</span></span>

<span data-ttu-id="1b72d-122">Указатель на массив весовых коэффициентов костей.</span><span class="sxs-lookup"><span data-stu-id="1b72d-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="1b72d-123">Каждый элемент этого массива имеет соответствующий элемент в Пиндицес, так что Пвеигхтс \[ i \] соответствует пиндицес \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="1b72d-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="1b72d-124">Каждое значение в Пвеигхтс находится в диапазоне от 0 до 1 и определяет величину влияния на кость на каждую вершину.</span><span class="sxs-lookup"><span data-stu-id="1b72d-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="1b72d-125">Размер Пвеигхтс должен быть больше или равен Инфлуенцекаунт.</span><span class="sxs-lookup"><span data-stu-id="1b72d-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b72d-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b72d-126">Return value</span></span>

<span data-ttu-id="1b72d-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b72d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b72d-128">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1b72d-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1b72d-129">Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ INVALIDARG или e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1b72d-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b72d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1b72d-130">Requirements</span></span>



| <span data-ttu-id="1b72d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1b72d-131">Requirement</span></span> | <span data-ttu-id="1b72d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1b72d-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b72d-133">Header</span><span class="sxs-lookup"><span data-stu-id="1b72d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1b72d-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b72d-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b72d-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b72d-135">Library</span></span><br/> | <dl> <span data-ttu-id="1b72d-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b72d-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b72d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b72d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b72d-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="1b72d-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="1b72d-139">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="1b72d-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
