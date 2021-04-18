---
description: Получение суммы влияния на заданную кость на заданную вершину.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'Метод ID3DX10SkinInfo:: Жетбонеинфлуенце (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713840"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a><span data-ttu-id="319d0-103">Метод ID3DX10SkinInfo:: Жетбонеинфлуенце</span><span class="sxs-lookup"><span data-stu-id="319d0-103">ID3DX10SkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="319d0-104">Получение суммы влияния на заданную кость на заданную вершину.</span><span class="sxs-lookup"><span data-stu-id="319d0-104">Get the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="319d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="319d0-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a><span data-ttu-id="319d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="319d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="319d0-107">*Бонеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="319d0-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="319d0-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="319d0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="319d0-109">Индекс, указывающий существующую кость.</span><span class="sxs-lookup"><span data-stu-id="319d0-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="319d0-110">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="319d0-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="319d0-111">*Инфлуенцеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="319d0-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="319d0-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="319d0-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="319d0-113">Индекс в списке вершин, на которые она влияет.</span><span class="sxs-lookup"><span data-stu-id="319d0-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="319d0-114">*пвеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="319d0-114">*pWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="319d0-115">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="319d0-115">Type: **float\***</span></span>

<span data-ttu-id="319d0-116">Величина влияния (от 0 до 1), на которую кость поверх вершины.</span><span class="sxs-lookup"><span data-stu-id="319d0-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="319d0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="319d0-117">Return value</span></span>

<span data-ttu-id="319d0-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="319d0-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="319d0-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="319d0-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="319d0-120">В случае сбоя метода возвращаемое значение может быть равно E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="319d0-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="319d0-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="319d0-121">Remarks</span></span>

<span data-ttu-id="319d0-122">Используйте ID3DX10SkinInfo:: Жетбонеинфлуенцекаунт, чтобы узнать, сколько вершин влияет на кость.</span><span class="sxs-lookup"><span data-stu-id="319d0-122">Use ID3DX10SkinInfo::GetBoneInfluenceCount to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="319d0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="319d0-123">Requirements</span></span>



| <span data-ttu-id="319d0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="319d0-124">Requirement</span></span> | <span data-ttu-id="319d0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="319d0-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="319d0-126">Header</span><span class="sxs-lookup"><span data-stu-id="319d0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="319d0-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="319d0-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="319d0-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="319d0-128">Library</span></span><br/> | <dl> <span data-ttu-id="319d0-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="319d0-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="319d0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="319d0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="319d0-131">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="319d0-131">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="319d0-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="319d0-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
