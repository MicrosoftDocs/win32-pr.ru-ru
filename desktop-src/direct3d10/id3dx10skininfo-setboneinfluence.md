---
description: Установка объема влияния на заданную кость на заданную вершину.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'Метод ID3DX10SkinInfo:: Сетбонеинфлуенце (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713839"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="40740-103">Метод ID3DX10SkinInfo:: Сетбонеинфлуенце</span><span class="sxs-lookup"><span data-stu-id="40740-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="40740-104">Установка объема влияния на заданную кость на заданную вершину.</span><span class="sxs-lookup"><span data-stu-id="40740-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="40740-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40740-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="40740-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="40740-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40740-107">*Бонеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40740-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40740-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40740-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40740-109">Индекс, указывающий существующую кость.</span><span class="sxs-lookup"><span data-stu-id="40740-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="40740-110">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="40740-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="40740-111">*Инфлуенцеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40740-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40740-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40740-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40740-113">Индекс в списке вершин, на которые она влияет.</span><span class="sxs-lookup"><span data-stu-id="40740-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="40740-114">*Вес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40740-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40740-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="40740-115">Type: **float**</span></span>

<span data-ttu-id="40740-116">Величина влияния (от 0 до 1), на которую кость поверх вершины.</span><span class="sxs-lookup"><span data-stu-id="40740-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40740-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40740-117">Return value</span></span>

<span data-ttu-id="40740-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40740-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40740-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="40740-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="40740-120">В случае сбоя метода возвращаемое значение может быть равно E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="40740-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="40740-121">Требования</span><span class="sxs-lookup"><span data-stu-id="40740-121">Requirements</span></span>



| <span data-ttu-id="40740-122">Требование</span><span class="sxs-lookup"><span data-stu-id="40740-122">Requirement</span></span> | <span data-ttu-id="40740-123">Значение</span><span class="sxs-lookup"><span data-stu-id="40740-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40740-124">Header</span><span class="sxs-lookup"><span data-stu-id="40740-124">Header</span></span><br/>  | <dl> <span data-ttu-id="40740-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="40740-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="40740-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="40740-126">Library</span></span><br/> | <dl> <span data-ttu-id="40740-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40740-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40740-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40740-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40740-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="40740-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="40740-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="40740-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
