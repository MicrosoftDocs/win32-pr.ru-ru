---
description: Проецирует функцию, представленную в сопоставлении кубов, в сферические гармонические колебания.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Функция D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685004"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="d597d-103">Функция D3DX10SHProjectCubeMap</span><span class="sxs-lookup"><span data-stu-id="d597d-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="d597d-104">Проецирует функцию, представленную в сопоставлении кубов, в сферические гармонические колебания.</span><span class="sxs-lookup"><span data-stu-id="d597d-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="d597d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d597d-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="d597d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d597d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d597d-107">*Заказ*</span><span class="sxs-lookup"><span data-stu-id="d597d-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="d597d-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d597d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d597d-109">Порядок оценки SH, создание заказа ^ 2 коефс, degree — Order-1.</span><span class="sxs-lookup"><span data-stu-id="d597d-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="d597d-110">*пкубемап*</span><span class="sxs-lookup"><span data-stu-id="d597d-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="d597d-111">Тип: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="d597d-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="d597d-112">Кубической карты, который планируется прогнозировать на сферические гармонические колебания.</span><span class="sxs-lookup"><span data-stu-id="d597d-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="d597d-113">См. [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="d597d-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="d597d-114">*праут*</span><span class="sxs-lookup"><span data-stu-id="d597d-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="d597d-115">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d597d-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d597d-116">Выходной вектор SH для Red.</span><span class="sxs-lookup"><span data-stu-id="d597d-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="d597d-117">*пгаут*</span><span class="sxs-lookup"><span data-stu-id="d597d-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="d597d-118">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d597d-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d597d-119">Выходной вектор SH для зеленого цвета.</span><span class="sxs-lookup"><span data-stu-id="d597d-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="d597d-120">*пбаут*</span><span class="sxs-lookup"><span data-stu-id="d597d-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="d597d-121">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d597d-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d597d-122">Выходной вектор SH для синего.</span><span class="sxs-lookup"><span data-stu-id="d597d-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d597d-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d597d-123">Return value</span></span>

<span data-ttu-id="d597d-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d597d-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d597d-125">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d597d-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d597d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d597d-126">Requirements</span></span>



| <span data-ttu-id="d597d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d597d-127">Requirement</span></span> | <span data-ttu-id="d597d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d597d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d597d-129">Header</span><span class="sxs-lookup"><span data-stu-id="d597d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d597d-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d597d-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d597d-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d597d-131">Library</span></span><br/> | <dl> <span data-ttu-id="d597d-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d597d-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d597d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d597d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d597d-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d597d-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
