---
description: Получите матрицу проекции спрайта, которая применяется ко всем спрайтам.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'Метод ID3DX10Sprite:: Жетпрожектионтрансформ (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821532"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a><span data-ttu-id="e0bc2-103">Метод ID3DX10Sprite:: Жетпрожектионтрансформ</span><span class="sxs-lookup"><span data-stu-id="e0bc2-103">ID3DX10Sprite::GetProjectionTransform method</span></span>

<span data-ttu-id="e0bc2-104">Получите матрицу проекции спрайта, которая применяется ко всем спрайтам.</span><span class="sxs-lookup"><span data-stu-id="e0bc2-104">Get the sprite projection matrix that is applied to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0bc2-105">Syntax</span></span>


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="e0bc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0bc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0bc2-107">*ппрожектионтрансформ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0bc2-107">*pProjectionTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0bc2-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0bc2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e0bc2-109">Указатель на [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) , для которого будет задана матрица проекции спрайта.</span><span class="sxs-lookup"><span data-stu-id="e0bc2-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the sprite's projection matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0bc2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0bc2-110">Return value</span></span>

<span data-ttu-id="e0bc2-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0bc2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0bc2-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e0bc2-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0bc2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e0bc2-113">Requirements</span></span>



| <span data-ttu-id="e0bc2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e0bc2-114">Requirement</span></span> | <span data-ttu-id="e0bc2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e0bc2-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0bc2-116">Header</span><span class="sxs-lookup"><span data-stu-id="e0bc2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0bc2-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0bc2-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0bc2-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0bc2-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0bc2-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0bc2-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0bc2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0bc2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0bc2-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="e0bc2-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="e0bc2-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="e0bc2-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
