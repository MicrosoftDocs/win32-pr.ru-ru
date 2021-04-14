---
description: Ограничьте число костей, которые могут повлиять на вершину и/или ограничить объем влияния на кость на вершину.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Метод ID3DX10SkinInfo:: Compact (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424358"
---
# <a name="id3dx10skininfocompact-method"></a><span data-ttu-id="9acc4-103">Метод ID3DX10SkinInfo:: Compact</span><span class="sxs-lookup"><span data-stu-id="9acc4-103">ID3DX10SkinInfo::Compact method</span></span>

<span data-ttu-id="9acc4-104">Ограничьте число костей, которые могут повлиять на вершину и/или ограничить объем влияния на кость на вершину.</span><span class="sxs-lookup"><span data-stu-id="9acc4-104">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9acc4-105">Syntax</span></span>


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a><span data-ttu-id="9acc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9acc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9acc4-107">*Макспервертексинфлуенцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9acc4-107">*MaxPerVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9acc4-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9acc4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9acc4-109">Максимальное число костей, которые могут повлиять на любую заданную вершину.</span><span class="sxs-lookup"><span data-stu-id="9acc4-109">The maximum number of bones that can influence any given vertex.</span></span> <span data-ttu-id="9acc4-110">Это значение пропускается, если оно больше значения, возвращенного [**ID3DX10SkinInfo:: жетмаксбонеинфлуенцес**](id3dx10skininfo-getmaxboneinfluences.md).</span><span class="sxs-lookup"><span data-stu-id="9acc4-110">This value is ignored if it is greater than the value returned by [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span></span>

</dd> <dt>

<span data-ttu-id="9acc4-111">*ScaleMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9acc4-111">*ScaleMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9acc4-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9acc4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9acc4-113">Флаг, описывающий, как масштабировать оставшиеся веса в заданной вершине после того, как некоторые из них были удалены с помощью Минвеигхт.</span><span class="sxs-lookup"><span data-stu-id="9acc4-113">A flag describing how to scale the remaining weights on a given vertex after some have been chopped off by MinWeight.</span></span> <span data-ttu-id="9acc4-114">Если D3DX10 \_ скининфо \_ не \_ указано масштабирование, весовые коэффициенты не будут масштабироваться вообще.</span><span class="sxs-lookup"><span data-stu-id="9acc4-114">If D3DX10\_SKININFO\_NO\_SCALING is specified, the weights will not be scaled at all.</span></span> <span data-ttu-id="9acc4-115">Если \_ \_ указан параметр D3DX10 скининфо Scale \_ to \_ 1, то весовые коэффициенты, превышающие минвеигхт, будут масштабироваться до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9acc4-115">If D3DX10\_SKININFO\_SCALE\_TO\_1 is specified, the weights greater than MinWeight will be scaled up so that they add up to 1.0.</span></span> <span data-ttu-id="9acc4-116">Если указан параметр D3DX10 \_ скининфо \_ Scale for \_ \_ Total, то весовые коэффициенты, превышающие минвеигхт, будут масштабироваться, чтобы они добавлялись к исходному итогу.</span><span class="sxs-lookup"><span data-stu-id="9acc4-116">If D3DX10\_SKININFO\_SCALE\_TO\_TOTAL is specified, the weights greater than MinWeight will be scaled up so that they add up to the original total.</span></span>

</dd> <dt>

<span data-ttu-id="9acc4-117">*Минвеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9acc4-117">*MinWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9acc4-118">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9acc4-118">Type: **float**</span></span>

<span data-ttu-id="9acc4-119">Минимальный процент влияния или веса, который может иметь любая кость на любой вершине.</span><span class="sxs-lookup"><span data-stu-id="9acc4-119">The minimum percentage of influence, or weight, that any bone can have on any vertex.</span></span> <span data-ttu-id="9acc4-120">Это значение должно находиться в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="9acc4-120">This value must be between 0 and 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9acc4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9acc4-121">Return value</span></span>

<span data-ttu-id="9acc4-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9acc4-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9acc4-123">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="9acc4-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9acc4-124">Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY или e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9acc4-124">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="9acc4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9acc4-125">Requirements</span></span>



| <span data-ttu-id="9acc4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9acc4-126">Requirement</span></span> | <span data-ttu-id="9acc4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9acc4-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9acc4-128">Header</span><span class="sxs-lookup"><span data-stu-id="9acc4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9acc4-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9acc4-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9acc4-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9acc4-130">Library</span></span><br/> | <dl> <span data-ttu-id="9acc4-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9acc4-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9acc4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9acc4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9acc4-133">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="9acc4-133">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="9acc4-134">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="9acc4-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
