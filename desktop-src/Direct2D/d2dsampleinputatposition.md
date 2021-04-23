---
title: Функция D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: Выборка входных данных N в абсолютной позиции сцены, а не относительно позиции для входа. Доступно только для сложных входных данных.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Функция D2DSampleInputAtPosition Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679894"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="ff684-105">Функция D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="ff684-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="ff684-106">Выборка входных данных N в абсолютной позиции сцены, а не относительно позиции для входа.</span><span class="sxs-lookup"><span data-stu-id="ff684-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="ff684-107">Доступно только для сложных входных данных.</span><span class="sxs-lookup"><span data-stu-id="ff684-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff684-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff684-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="ff684-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff684-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff684-110">*N* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ff684-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff684-111">Входной номер.</span><span class="sxs-lookup"><span data-stu-id="ff684-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="ff684-112">*UV* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff684-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff684-113">Расположение UV.</span><span class="sxs-lookup"><span data-stu-id="ff684-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff684-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff684-114">Return value</span></span>

<span data-ttu-id="ff684-115">Функция возвращает **float4** в формате текскурдн.</span><span class="sxs-lookup"><span data-stu-id="ff684-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff684-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff684-116">Remarks</span></span>

<span data-ttu-id="ff684-117">В следующем примере показана функция, используемая в циклической оболочке.</span><span class="sxs-lookup"><span data-stu-id="ff684-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="ff684-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ff684-118">Requirements</span></span>



| <span data-ttu-id="ff684-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ff684-119">Requirement</span></span> | <span data-ttu-id="ff684-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ff684-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff684-121">Header</span><span class="sxs-lookup"><span data-stu-id="ff684-121">Header</span></span><br/> | <dl> <span data-ttu-id="ff684-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="ff684-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="ff684-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ff684-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="ff684-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff684-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="ff684-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff684-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff684-126">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="ff684-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="ff684-127">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="ff684-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





