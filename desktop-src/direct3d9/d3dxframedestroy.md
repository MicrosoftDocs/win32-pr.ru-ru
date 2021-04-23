---
description: Уничтожает поддерево фреймов в корне, включая корень.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: Функция D3DXFrameDestroy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713687"
---
# <a name="d3dxframedestroy-function"></a><span data-ttu-id="0ee4b-103">Функция D3DXFrameDestroy</span><span class="sxs-lookup"><span data-stu-id="0ee4b-103">D3DXFrameDestroy function</span></span>

<span data-ttu-id="0ee4b-104">Уничтожает поддерево фреймов в корне, включая корень.</span><span class="sxs-lookup"><span data-stu-id="0ee4b-104">Destroys the subtree of frames under the root, including the root.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ee4b-105">Syntax</span></span>


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="0ee4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ee4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee4b-107">*пфрамерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ee4b-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee4b-108">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="0ee4b-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="0ee4b-109">Указатель на корневой узел.</span><span class="sxs-lookup"><span data-stu-id="0ee4b-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="0ee4b-110">*паллок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ee4b-110">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee4b-111">Тип: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="0ee4b-111">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="0ee4b-112">Интерфейс выделения, используемый для освобождения узлов иерархии фреймов.</span><span class="sxs-lookup"><span data-stu-id="0ee4b-112">Allocation interface used to deallocate nodes of the frame hierarchy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee4b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ee4b-113">Return value</span></span>

<span data-ttu-id="0ee4b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ee4b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ee4b-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0ee4b-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ee4b-116">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0ee4b-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee4b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee4b-117">Requirements</span></span>



| <span data-ttu-id="0ee4b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee4b-118">Requirement</span></span> | <span data-ttu-id="0ee4b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee4b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee4b-120">Header</span><span class="sxs-lookup"><span data-stu-id="0ee4b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0ee4b-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee4b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0ee4b-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ee4b-122">Library</span></span><br/> | <dl> <span data-ttu-id="0ee4b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ee4b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ee4b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ee4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee4b-125">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="0ee4b-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




