---
description: Запрашивает освобождение объекта контейнера сетки.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: 'ID3DXAllocateHierarchy: метод:D Естроймешконтаинер (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548119"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a><span data-ttu-id="727d8-103">ID3DXAllocateHierarchy: метод:D Естроймешконтаинер</span><span class="sxs-lookup"><span data-stu-id="727d8-103">ID3DXAllocateHierarchy::DestroyMeshContainer method</span></span>

<span data-ttu-id="727d8-104">Запрашивает освобождение объекта контейнера сетки.</span><span class="sxs-lookup"><span data-stu-id="727d8-104">Requests deallocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="727d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="727d8-105">Syntax</span></span>


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a><span data-ttu-id="727d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="727d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727d8-107">*пмешконтаинертофри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="727d8-107">*pMeshContainerToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727d8-108">Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="727d8-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="727d8-109">Указатель на объект контейнера сетки, который будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="727d8-109">Pointer to the mesh container object to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="727d8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="727d8-110">Return value</span></span>

<span data-ttu-id="727d8-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="727d8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="727d8-112">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="727d8-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="727d8-113">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="727d8-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="727d8-114">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="727d8-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="727d8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="727d8-115">Requirements</span></span>



| <span data-ttu-id="727d8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="727d8-116">Requirement</span></span> | <span data-ttu-id="727d8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="727d8-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="727d8-118">Header</span><span class="sxs-lookup"><span data-stu-id="727d8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="727d8-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="727d8-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="727d8-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="727d8-120">Library</span></span><br/> | <dl> <span data-ttu-id="727d8-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="727d8-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="727d8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="727d8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727d8-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="727d8-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




