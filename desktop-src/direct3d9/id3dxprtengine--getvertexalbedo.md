---
description: Получает значения албедо вершин сетки.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'Метод ID3DXPRTEngine:: Жетвертексалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7926f6393221552107667c9209ef2b4c51945ab8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703956"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a><span data-ttu-id="252d4-103">Метод ID3DXPRTEngine:: Жетвертексалбедо</span><span class="sxs-lookup"><span data-stu-id="252d4-103">ID3DXPRTEngine::GetVertexAlbedo method</span></span>

<span data-ttu-id="252d4-104">Получает значения албедо вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="252d4-104">Retrieves albedo values of the mesh vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="252d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="252d4-105">Syntax</span></span>


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a><span data-ttu-id="252d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="252d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="252d4-107">*пвертколорс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="252d4-107">*pVertColors* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="252d4-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="252d4-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="252d4-109">Указатель на массив назначения албедо значений вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="252d4-109">Pointer to a destination array of albedo values of the mesh vertices.</span></span> <span data-ttu-id="252d4-110">См. [**D3DXCOLOR**](d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="252d4-110">See [**D3DXCOLOR**](d3dxcolor.md).</span></span>

</dd> <dt>

<span data-ttu-id="252d4-111">*Нумвертс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="252d4-111">*NumVerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="252d4-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="252d4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="252d4-113">Число вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="252d4-113">Number of vertices in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="252d4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="252d4-114">Return value</span></span>

<span data-ttu-id="252d4-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="252d4-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="252d4-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="252d4-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="252d4-117">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="252d4-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="252d4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="252d4-118">Requirements</span></span>



| <span data-ttu-id="252d4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="252d4-119">Requirement</span></span> | <span data-ttu-id="252d4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="252d4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="252d4-121">Header</span><span class="sxs-lookup"><span data-stu-id="252d4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="252d4-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="252d4-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="252d4-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="252d4-123">Library</span></span><br/> | <dl> <span data-ttu-id="252d4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="252d4-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="252d4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="252d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252d4-126">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="252d4-126">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
