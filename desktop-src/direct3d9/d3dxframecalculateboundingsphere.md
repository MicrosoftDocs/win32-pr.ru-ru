---
description: Выполняет вычисление ограничивающей сферы всех сеток в иерархии фреймов.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Функция D3DXFrameCalculateBoundingSphere (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703789"
---
# <a name="d3dxframecalculateboundingsphere-function"></a><span data-ttu-id="790cc-103">Функция D3DXFrameCalculateBoundingSphere</span><span class="sxs-lookup"><span data-stu-id="790cc-103">D3DXFrameCalculateBoundingSphere function</span></span>

<span data-ttu-id="790cc-104">Выполняет вычисление ограничивающей сферы всех сеток в иерархии фреймов.</span><span class="sxs-lookup"><span data-stu-id="790cc-104">Computes the bounding sphere of all the meshes in the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="790cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="790cc-105">Syntax</span></span>


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a><span data-ttu-id="790cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="790cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790cc-107">*пфрамерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="790cc-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="790cc-108">Тип: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="790cc-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="790cc-109">Указатель на корневой узел.</span><span class="sxs-lookup"><span data-stu-id="790cc-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="790cc-110">*побжектцентер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="790cc-110">*pObjectCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="790cc-111">Тип: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="790cc-111">Type: **[**LPD3DXVECTOR3**](d3dxvector3.md)**</span></span>

<span data-ttu-id="790cc-112">Возвращает центр ограничивающей сферы.</span><span class="sxs-lookup"><span data-stu-id="790cc-112">Returns the center of the bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="790cc-113">*побжектрадиус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="790cc-113">*pObjectRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="790cc-114">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="790cc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="790cc-115">Возвращает радиус ограничивающей сферы.</span><span class="sxs-lookup"><span data-stu-id="790cc-115">Returns the radius of the bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790cc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="790cc-116">Return value</span></span>

<span data-ttu-id="790cc-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="790cc-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="790cc-118">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="790cc-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="790cc-119">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="790cc-119">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="790cc-120">Требования</span><span class="sxs-lookup"><span data-stu-id="790cc-120">Requirements</span></span>



| <span data-ttu-id="790cc-121">Требование</span><span class="sxs-lookup"><span data-stu-id="790cc-121">Requirement</span></span> | <span data-ttu-id="790cc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="790cc-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="790cc-123">Header</span><span class="sxs-lookup"><span data-stu-id="790cc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="790cc-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="790cc-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="790cc-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="790cc-125">Library</span></span><br/> | <dl> <span data-ttu-id="790cc-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="790cc-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="790cc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="790cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790cc-128">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="790cc-128">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
