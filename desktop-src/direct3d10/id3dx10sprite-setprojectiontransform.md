---
description: Установите матрицу проекции для всех спрайтов.
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: 'Метод ID3DX10Sprite:: Сетпрожектионтрансформ (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c49fb570f87c8c86313e1f4adcf1560fee909433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548143"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a><span data-ttu-id="dbc59-103">Метод ID3DX10Sprite:: Сетпрожектионтрансформ</span><span class="sxs-lookup"><span data-stu-id="dbc59-103">ID3DX10Sprite::SetProjectionTransform method</span></span>

<span data-ttu-id="dbc59-104">Установите матрицу проекции для всех спрайтов.</span><span class="sxs-lookup"><span data-stu-id="dbc59-104">Set the projection matrix for all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbc59-105">Syntax</span></span>


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="dbc59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbc59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc59-107">*ппрожектионтрансформ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbc59-107">*pProjectionTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc59-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbc59-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dbc59-109">Матрица проекции, используемая для всех спрайтов.</span><span class="sxs-lookup"><span data-stu-id="dbc59-109">The projection matrix to be used on all sprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc59-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbc59-110">Return value</span></span>

<span data-ttu-id="dbc59-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbc59-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbc59-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dbc59-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc59-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dbc59-113">Requirements</span></span>



| <span data-ttu-id="dbc59-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dbc59-114">Requirement</span></span> | <span data-ttu-id="dbc59-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc59-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc59-116">Header</span><span class="sxs-lookup"><span data-stu-id="dbc59-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dbc59-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc59-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbc59-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbc59-118">Library</span></span><br/> | <dl> <span data-ttu-id="dbc59-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbc59-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc59-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbc59-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc59-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="dbc59-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="dbc59-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="dbc59-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
