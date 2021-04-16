---
description: Возвращает атрибуты исправления.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'Метод ID3DXPatchMesh:: Жетпатчинфо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664987"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a><span data-ttu-id="339af-103">Метод ID3DXPatchMesh:: Жетпатчинфо</span><span class="sxs-lookup"><span data-stu-id="339af-103">ID3DXPatchMesh::GetPatchInfo method</span></span>

<span data-ttu-id="339af-104">Возвращает атрибуты исправления.</span><span class="sxs-lookup"><span data-stu-id="339af-104">Gets the attributes of the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="339af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="339af-105">Syntax</span></span>


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a><span data-ttu-id="339af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="339af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="339af-107">*Патчинфо* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="339af-107">*PatchInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="339af-108">Тип: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="339af-108">Type: **[**LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span></span>

<span data-ttu-id="339af-109">Указатель на структуры, содержащие атрибуты исправления.</span><span class="sxs-lookup"><span data-stu-id="339af-109">Pointer to the structures containing the patch attributes.</span></span> <span data-ttu-id="339af-110">Дополнительные сведения об атрибутах исправления см. в разделе [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="339af-110">For more information about patch attributes, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="339af-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="339af-111">Return value</span></span>

<span data-ttu-id="339af-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="339af-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="339af-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="339af-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="339af-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="339af-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="339af-115">Требования</span><span class="sxs-lookup"><span data-stu-id="339af-115">Requirements</span></span>



| <span data-ttu-id="339af-116">Требование</span><span class="sxs-lookup"><span data-stu-id="339af-116">Requirement</span></span> | <span data-ttu-id="339af-117">Значение</span><span class="sxs-lookup"><span data-stu-id="339af-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="339af-118">Header</span><span class="sxs-lookup"><span data-stu-id="339af-118">Header</span></span><br/>  | <dl> <span data-ttu-id="339af-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="339af-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="339af-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="339af-120">Library</span></span><br/> | <dl> <span data-ttu-id="339af-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="339af-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="339af-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="339af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339af-123">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="339af-123">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




