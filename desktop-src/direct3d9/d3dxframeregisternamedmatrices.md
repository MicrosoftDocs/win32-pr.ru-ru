---
description: При наличии иерархии фреймов регистрирует все именованные матрицы в микшере анимации.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: Функция D3DXFrameRegisterNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713684"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="bcbd3-103">Функция D3DXFrameRegisterNamedMatrices</span><span class="sxs-lookup"><span data-stu-id="bcbd3-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="bcbd3-104">При наличии иерархии фреймов регистрирует все именованные матрицы в микшере анимации.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbd3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcbd3-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="bcbd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcbd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbd3-107">*пфрамерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcbd3-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd3-108">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="bcbd3-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="bcbd3-109">Узел верхнего уровня в иерархии фреймов.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd3-110">*панимконтроллер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcbd3-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd3-111">Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="bcbd3-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="bcbd3-112">Указатель на объект контроллера анимации.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcbd3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcbd3-113">Return value</span></span>

<span data-ttu-id="bcbd3-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bcbd3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bcbd3-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bcbd3-116">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bcbd3-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbd3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bcbd3-117">Requirements</span></span>



| <span data-ttu-id="bcbd3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bcbd3-118">Requirement</span></span> | <span data-ttu-id="bcbd3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bcbd3-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbd3-120">Header</span><span class="sxs-lookup"><span data-stu-id="bcbd3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bcbd3-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd3-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bcbd3-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bcbd3-122">Library</span></span><br/> | <dl> <span data-ttu-id="bcbd3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd3-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bcbd3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcbd3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbd3-125">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="bcbd3-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




