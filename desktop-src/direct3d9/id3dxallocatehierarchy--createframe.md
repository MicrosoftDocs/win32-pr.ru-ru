---
description: Запрашивает выделение объекта Frame.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'Метод ID3DXAllocateHierarchy:: Креатефраме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694238"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="7f45d-103">Метод ID3DXAllocateHierarchy:: Креатефраме</span><span class="sxs-lookup"><span data-stu-id="7f45d-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="7f45d-104">Запрашивает выделение объекта Frame.</span><span class="sxs-lookup"><span data-stu-id="7f45d-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f45d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f45d-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7f45d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f45d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f45d-107">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f45d-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f45d-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f45d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f45d-109">Имя создаваемого фрейма.</span><span class="sxs-lookup"><span data-stu-id="7f45d-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="7f45d-110">*ппневфраме* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7f45d-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7f45d-111">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f45d-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="7f45d-112">Возвращает созданный объект Frame.</span><span class="sxs-lookup"><span data-stu-id="7f45d-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f45d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f45d-113">Return value</span></span>

<span data-ttu-id="7f45d-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f45d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f45d-115">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="7f45d-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7f45d-116">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7f45d-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7f45d-117">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="7f45d-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f45d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7f45d-118">Requirements</span></span>



| <span data-ttu-id="7f45d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7f45d-119">Requirement</span></span> | <span data-ttu-id="7f45d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7f45d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f45d-121">Header</span><span class="sxs-lookup"><span data-stu-id="7f45d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7f45d-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f45d-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7f45d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f45d-123">Library</span></span><br/> | <dl> <span data-ttu-id="7f45d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f45d-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f45d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f45d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f45d-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="7f45d-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
