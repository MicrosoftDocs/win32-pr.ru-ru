---
description: Изменение того, какие кости влияют на вершины.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'Метод ID3DX10SkinInfo:: Ремапбонес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713706"
---
# <a name="id3dx10skininforemapbones-method"></a><span data-ttu-id="db7d3-103">Метод ID3DX10SkinInfo:: Ремапбонес</span><span class="sxs-lookup"><span data-stu-id="db7d3-103">ID3DX10SkinInfo::RemapBones method</span></span>

<span data-ttu-id="db7d3-104">Изменение того, какие кости влияют на вершины.</span><span class="sxs-lookup"><span data-stu-id="db7d3-104">Change which bones influence which vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db7d3-105">Syntax</span></span>


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a><span data-ttu-id="db7d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db7d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7d3-107">*Невбонекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db7d3-107">*NewBoneCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db7d3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db7d3-109">Новое число костей.</span><span class="sxs-lookup"><span data-stu-id="db7d3-109">The new number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="db7d3-110">*пбонеремап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db7d3-110">*pBoneRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="db7d3-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db7d3-112">Указатель на массив индексов костей, описывающих повторное сопоставление.</span><span class="sxs-lookup"><span data-stu-id="db7d3-112">A pointer to an array of bone indices, which describe the remapping.</span></span> <span data-ttu-id="db7d3-113">Например, пусть Скининфо содержит несколько костей, таких, что bone0 сопоставляется с v0, bone1 — v1 и bone2 — v2, а массив с 2, 1, 0 — для Пбонеремап.</span><span class="sxs-lookup"><span data-stu-id="db7d3-113">For example, say SkinInfo contains some bones such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="db7d3-114">Это приведет к сопоставлению bone0 с v2, bone1 – v1, а bone2 — v0.</span><span class="sxs-lookup"><span data-stu-id="db7d3-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7d3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db7d3-115">Return value</span></span>

<span data-ttu-id="db7d3-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db7d3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db7d3-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="db7d3-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="db7d3-118">Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY или e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="db7d3-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7d3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="db7d3-119">Requirements</span></span>



| <span data-ttu-id="db7d3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="db7d3-120">Requirement</span></span> | <span data-ttu-id="db7d3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="db7d3-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db7d3-122">Header</span><span class="sxs-lookup"><span data-stu-id="db7d3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="db7d3-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7d3-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="db7d3-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db7d3-124">Library</span></span><br/> | <dl> <span data-ttu-id="db7d3-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db7d3-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db7d3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db7d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7d3-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="db7d3-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="db7d3-128">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="db7d3-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
