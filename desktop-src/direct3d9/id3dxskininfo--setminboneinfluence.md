---
description: Устанавливает минимальную влияние на кость. Влияние значений меньше этого значения не учитывается.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'Метод ID3DXSkinInfo:: Сетминбонеинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713444"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="bb62e-104">Метод ID3DXSkinInfo:: Сетминбонеинфлуенце</span><span class="sxs-lookup"><span data-stu-id="bb62e-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="bb62e-105">Устанавливает минимальную влияние на кость.</span><span class="sxs-lookup"><span data-stu-id="bb62e-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="bb62e-106">Влияние значений меньше этого значения не учитывается.</span><span class="sxs-lookup"><span data-stu-id="bb62e-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb62e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb62e-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="bb62e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb62e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb62e-109">*Мининфл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb62e-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb62e-110">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb62e-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb62e-111">Минимальное значение влияния.</span><span class="sxs-lookup"><span data-stu-id="bb62e-111">Minimum influence value.</span></span> <span data-ttu-id="bb62e-112">Влияние значений меньше этого значения не учитывается.</span><span class="sxs-lookup"><span data-stu-id="bb62e-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb62e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-113">Return value</span></span>

<span data-ttu-id="bb62e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb62e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb62e-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bb62e-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb62e-116">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="bb62e-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb62e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bb62e-117">Requirements</span></span>



| <span data-ttu-id="bb62e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bb62e-118">Requirement</span></span> | <span data-ttu-id="bb62e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb62e-120">Header</span><span class="sxs-lookup"><span data-stu-id="bb62e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bb62e-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb62e-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb62e-122">Library</span></span><br/> | <dl> <span data-ttu-id="bb62e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb62e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb62e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb62e-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="bb62e-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="bb62e-126">**ID3DXSkinInfo:: Жетминбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bb62e-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
