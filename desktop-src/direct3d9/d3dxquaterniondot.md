---
description: Возвращает скалярное произведение двух кватернионов.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: Функция D3DXQuaternionDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355520"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="dbad6-103">Функция D3DXQuaternionDot</span><span class="sxs-lookup"><span data-stu-id="dbad6-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="dbad6-104">Возвращает скалярное произведение двух кватернионов.</span><span class="sxs-lookup"><span data-stu-id="dbad6-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbad6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbad6-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="dbad6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbad6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbad6-107">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbad6-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbad6-108">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="dbad6-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dbad6-109">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="dbad6-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dbad6-110">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbad6-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbad6-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="dbad6-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dbad6-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="dbad6-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbad6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbad6-113">Return value</span></span>

<span data-ttu-id="dbad6-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbad6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbad6-115">Скалярное произведение двух кватернионов.</span><span class="sxs-lookup"><span data-stu-id="dbad6-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbad6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbad6-116">Remarks</span></span>

<span data-ttu-id="dbad6-117">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="dbad6-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbad6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dbad6-118">Requirements</span></span>



| <span data-ttu-id="dbad6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dbad6-119">Requirement</span></span> | <span data-ttu-id="dbad6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dbad6-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbad6-121">Header</span><span class="sxs-lookup"><span data-stu-id="dbad6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dbad6-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbad6-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dbad6-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbad6-123">Library</span></span><br/> | <dl> <span data-ttu-id="dbad6-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbad6-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dbad6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbad6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbad6-126">Математические функции</span><span class="sxs-lookup"><span data-stu-id="dbad6-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
