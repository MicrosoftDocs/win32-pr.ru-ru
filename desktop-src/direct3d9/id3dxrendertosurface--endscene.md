---
description: Завершает сцену.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'Метод ID3DXRenderToSurface:: Ендсцене (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821013"
---
# <a name="id3dxrendertosurfaceendscene-method"></a><span data-ttu-id="07d30-103">Метод ID3DXRenderToSurface:: Ендсцене</span><span class="sxs-lookup"><span data-stu-id="07d30-103">ID3DXRenderToSurface::EndScene method</span></span>

<span data-ttu-id="07d30-104">Завершает сцену.</span><span class="sxs-lookup"><span data-stu-id="07d30-104">Ends a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07d30-105">Syntax</span></span>


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="07d30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d30-107">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07d30-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d30-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07d30-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07d30-109">Параметры фильтра, перечисленные в [ \_ фильтре D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="07d30-109">Filter options, enumerated in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d30-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07d30-110">Return value</span></span>

<span data-ttu-id="07d30-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07d30-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07d30-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="07d30-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07d30-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="07d30-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d30-114">Требования</span><span class="sxs-lookup"><span data-stu-id="07d30-114">Requirements</span></span>



| <span data-ttu-id="07d30-115">Требование</span><span class="sxs-lookup"><span data-stu-id="07d30-115">Requirement</span></span> | <span data-ttu-id="07d30-116">Значение</span><span class="sxs-lookup"><span data-stu-id="07d30-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07d30-117">Header</span><span class="sxs-lookup"><span data-stu-id="07d30-117">Header</span></span><br/>  | <dl> <span data-ttu-id="07d30-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d30-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="07d30-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07d30-119">Library</span></span><br/> | <dl> <span data-ttu-id="07d30-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07d30-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07d30-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07d30-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d30-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="07d30-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="07d30-123">**ID3DXRenderToSurface:: Бегинсцене**</span><span class="sxs-lookup"><span data-stu-id="07d30-123">**ID3DXRenderToSurface::BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
