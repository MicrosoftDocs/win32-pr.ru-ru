---
title: Функция D2DGetScenePosition (D2d1effecthelpers. h)
description: Возвращает значение расположения входной сцены \_ . Доступно только в том \_ случае \_ \_ , если в исходном файле объявлено, что для D2D требуется указать расположение сцены.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Функция D2DGetScenePosition Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657933"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="b7683-105">Функция D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="b7683-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="b7683-106">Возвращает значение расположения входной сцены \_ .</span><span class="sxs-lookup"><span data-stu-id="b7683-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="b7683-107">Доступно только в том \_ случае \_ \_ , если в исходном файле объявлено, что для D2D требуется указать расположение сцены.</span><span class="sxs-lookup"><span data-stu-id="b7683-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7683-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7683-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="b7683-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7683-109">Parameters</span></span>

<span data-ttu-id="b7683-110">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="b7683-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7683-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7683-111">Return value</span></span>

<span data-ttu-id="b7683-112">Функция возвращает **float4** в положении сцены формата \_ .</span><span class="sxs-lookup"><span data-stu-id="b7683-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7683-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7683-113">Remarks</span></span>

<span data-ttu-id="b7683-114">В следующем примере показано использование функции при формировании шаблона разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="b7683-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="b7683-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b7683-115">Requirements</span></span>



| <span data-ttu-id="b7683-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b7683-116">Requirement</span></span> | <span data-ttu-id="b7683-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b7683-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7683-118">Header</span><span class="sxs-lookup"><span data-stu-id="b7683-118">Header</span></span><br/> | <dl> <span data-ttu-id="b7683-119"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="b7683-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="b7683-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b7683-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="b7683-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7683-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="b7683-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7683-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7683-123">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="b7683-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="b7683-124">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="b7683-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





