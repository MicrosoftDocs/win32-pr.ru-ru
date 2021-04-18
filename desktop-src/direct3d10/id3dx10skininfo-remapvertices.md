---
description: Изменение вершин, на которые влияют эти кости.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'Метод ID3DX10SkinInfo:: Ремапвертицес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713705"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="ddf95-103">Метод ID3DX10SkinInfo:: Ремапвертицес</span><span class="sxs-lookup"><span data-stu-id="ddf95-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="ddf95-104">Изменение вершин, на которые влияют эти кости.</span><span class="sxs-lookup"><span data-stu-id="ddf95-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddf95-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="ddf95-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddf95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf95-107">*Неввертекскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddf95-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddf95-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddf95-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ddf95-109">Новое число вершин.</span><span class="sxs-lookup"><span data-stu-id="ddf95-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="ddf95-110">*пвертексремап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddf95-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddf95-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddf95-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ddf95-112">Указатель на массив индексов вершин, описывающих повторное сопоставление.</span><span class="sxs-lookup"><span data-stu-id="ddf95-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="ddf95-113">Например, пусть Скининфо содержит несколько вершин, таких, что bone0 сопоставляется с v0, bone1 — v1 и bone2 — v2, а массив с 2, 1, 0 — для Пбонеремап.</span><span class="sxs-lookup"><span data-stu-id="ddf95-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="ddf95-114">Это приведет к сопоставлению bone0 с v2, bone1 – v1, а bone2 — v0.</span><span class="sxs-lookup"><span data-stu-id="ddf95-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf95-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddf95-115">Return value</span></span>

<span data-ttu-id="ddf95-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddf95-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddf95-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ddf95-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ddf95-118">Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY или e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ddf95-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddf95-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ddf95-119">Requirements</span></span>



| <span data-ttu-id="ddf95-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ddf95-120">Requirement</span></span> | <span data-ttu-id="ddf95-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ddf95-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf95-122">Header</span><span class="sxs-lookup"><span data-stu-id="ddf95-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ddf95-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf95-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddf95-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ddf95-124">Library</span></span><br/> | <dl> <span data-ttu-id="ddf95-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddf95-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf95-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddf95-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf95-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="ddf95-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="ddf95-128">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ddf95-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
