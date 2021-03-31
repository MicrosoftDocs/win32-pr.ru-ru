---
description: Добавляет дочерний фрейм в рамку.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: Функция D3DXFrameAppendChild (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273777"
---
# <a name="d3dxframeappendchild-function"></a><span data-ttu-id="862e8-103">Функция D3DXFrameAppendChild</span><span class="sxs-lookup"><span data-stu-id="862e8-103">D3DXFrameAppendChild function</span></span>

<span data-ttu-id="862e8-104">Добавляет дочерний фрейм в рамку.</span><span class="sxs-lookup"><span data-stu-id="862e8-104">Adds a child frame to a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="862e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="862e8-105">Syntax</span></span>


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a><span data-ttu-id="862e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="862e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862e8-107">*пфрамепарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="862e8-107">*pFrameParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="862e8-108">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="862e8-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="862e8-109">Указатель на родительский узел.</span><span class="sxs-lookup"><span data-stu-id="862e8-109">Pointer to the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="862e8-110">*пфрамечилд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="862e8-110">*pFrameChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="862e8-111">Тип: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="862e8-111">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="862e8-112">Указатель на дочерний узел.</span><span class="sxs-lookup"><span data-stu-id="862e8-112">Pointer to the child node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862e8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="862e8-113">Return value</span></span>

<span data-ttu-id="862e8-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="862e8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="862e8-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="862e8-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="862e8-116">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="862e8-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="862e8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="862e8-117">Requirements</span></span>



| <span data-ttu-id="862e8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="862e8-118">Requirement</span></span> | <span data-ttu-id="862e8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="862e8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="862e8-120">Header</span><span class="sxs-lookup"><span data-stu-id="862e8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="862e8-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="862e8-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="862e8-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="862e8-122">Library</span></span><br/> | <dl> <span data-ttu-id="862e8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="862e8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="862e8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="862e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862e8-125">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="862e8-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




