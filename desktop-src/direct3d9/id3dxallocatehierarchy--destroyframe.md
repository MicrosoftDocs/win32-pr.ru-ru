---
description: Запрашивает освобождение объекта Frame.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: 'ID3DXAllocateHierarchy: метод:D Естройфраме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4a394501b9967d3f7cb6d3f6b2f30db168438278
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424510"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a><span data-ttu-id="0fc3a-103">ID3DXAllocateHierarchy: метод:D Естройфраме</span><span class="sxs-lookup"><span data-stu-id="0fc3a-103">ID3DXAllocateHierarchy::DestroyFrame method</span></span>

<span data-ttu-id="0fc3a-104">Запрашивает освобождение объекта Frame.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-104">Requests deallocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fc3a-105">Syntax</span></span>


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a><span data-ttu-id="0fc3a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fc3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc3a-107">*пфраметофри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fc3a-107">*pFrameToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc3a-108">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="0fc3a-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="0fc3a-109">Указатель на рамку, которую необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-109">Pointer to the frame to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc3a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fc3a-110">Return value</span></span>

<span data-ttu-id="0fc3a-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0fc3a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0fc3a-112">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0fc3a-113">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0fc3a-114">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="0fc3a-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fc3a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0fc3a-115">Requirements</span></span>



| <span data-ttu-id="0fc3a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0fc3a-116">Requirement</span></span> | <span data-ttu-id="0fc3a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0fc3a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc3a-118">Header</span><span class="sxs-lookup"><span data-stu-id="0fc3a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0fc3a-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fc3a-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0fc3a-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0fc3a-120">Library</span></span><br/> | <dl> <span data-ttu-id="0fc3a-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fc3a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0fc3a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fc3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc3a-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="0fc3a-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




