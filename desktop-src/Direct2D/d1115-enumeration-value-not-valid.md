---
title: Недопустимое значение перечисления D1115
description: Недопустимое значение перечисления D1115
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Недопустимое значение перечисления D1115 Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105649169"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="84c4b-104">D1115: недопустимое значение перечисления</span><span class="sxs-lookup"><span data-stu-id="84c4b-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="84c4b-105">Параметр параметра \[  \] со \[ *значением* \] *интерфейса*::*method* не является допустимым значением перечисления.</span><span class="sxs-lookup"><span data-stu-id="84c4b-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="84c4b-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="84c4b-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="84c4b-107"><span id="parameter"></span><span id="PARAMETER"></span>*параметр*</span><span class="sxs-lookup"><span data-stu-id="84c4b-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="84c4b-108">Имя параметра, получившего непредвиденный тип.</span><span class="sxs-lookup"><span data-stu-id="84c4b-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="84c4b-109"><span id="value"></span><span id="VALUE"></span>*значений*</span><span class="sxs-lookup"><span data-stu-id="84c4b-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="84c4b-110">Недопустимое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="84c4b-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="84c4b-111"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="84c4b-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="84c4b-112">Имя интерфейса, которому принадлежит *метод* .</span><span class="sxs-lookup"><span data-stu-id="84c4b-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="84c4b-113"><span id="method"></span><span id="METHOD"></span>*Method*</span><span class="sxs-lookup"><span data-stu-id="84c4b-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="84c4b-114">Имя метода, получившего недопустимое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="84c4b-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="84c4b-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="84c4b-115">Examples</span></span>

<span data-ttu-id="84c4b-116">В следующем примере задается значение перечисления [**\_ \_ \_ типа целевого объекта отрисовки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) , равное 30, которое находится за пределами ожидаемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="84c4b-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="84c4b-117">В этом примере создается следующее сообщение отладки:</span><span class="sxs-lookup"><span data-stu-id="84c4b-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="84c4b-118">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="84c4b-118">Possible Causes</span></span>

<span data-ttu-id="84c4b-119">Параметр использовал недопустимое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="84c4b-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="84c4b-120">Исправления</span><span class="sxs-lookup"><span data-stu-id="84c4b-120">Fixes</span></span>

<span data-ttu-id="84c4b-121">Используйте допустимое значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="84c4b-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="84c4b-122">В настоящее время слой отладки проверяет только отдельные значения перечисления. Он не проверяет, является ли побитовое сочетание допустимым.</span><span class="sxs-lookup"><span data-stu-id="84c4b-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 
