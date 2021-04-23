---
title: Функция D2DGetInput (D2d1effecthelpers. h)
description: Возвращает цвет входных данных N во входной координате. Доступно только для простых входных данных.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Функция D2DGetInput Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657826"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="1304d-105">Функция D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="1304d-105">D2DGetInput function</span></span>

<span data-ttu-id="1304d-106">Возвращает цвет входных данных N во входной координате.</span><span class="sxs-lookup"><span data-stu-id="1304d-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="1304d-107">Доступно только для простых входных данных.</span><span class="sxs-lookup"><span data-stu-id="1304d-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1304d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1304d-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="1304d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1304d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1304d-110">*N* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1304d-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1304d-111">Входной номер.</span><span class="sxs-lookup"><span data-stu-id="1304d-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1304d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1304d-112">Return value</span></span>

<span data-ttu-id="1304d-113">Функция возвращает **float4**, СОДЕРЖАЩУЮ цвет RGBA в формате инпутн.</span><span class="sxs-lookup"><span data-stu-id="1304d-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="1304d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1304d-114">Remarks</span></span>

<span data-ttu-id="1304d-115">В следующем примере показана функция, используемая как часть арифметического составного действия.</span><span class="sxs-lookup"><span data-stu-id="1304d-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="1304d-116">Другой пример использования этой функции см. в разделе Примечания для [ \_ \_ записи D2D PS](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="1304d-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1304d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1304d-117">Requirements</span></span>



| <span data-ttu-id="1304d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1304d-118">Requirement</span></span> | <span data-ttu-id="1304d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1304d-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1304d-120">Header</span><span class="sxs-lookup"><span data-stu-id="1304d-120">Header</span></span><br/> | <dl> <span data-ttu-id="1304d-121"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="1304d-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="1304d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1304d-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="1304d-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1304d-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="1304d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1304d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1304d-125">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="1304d-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="1304d-126">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="1304d-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





