---
description: Вызывается шейдером пересечения для сообщения пересечения лучей.
ms.assetid: ''
title: Функция ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701271"
---
# <a name="reporthit-function"></a><span data-ttu-id="eda94-103">Функция ReportHit</span><span class="sxs-lookup"><span data-stu-id="eda94-103">ReportHit function</span></span>

<span data-ttu-id="eda94-104">Вызывается [шейдером пересечения](intersection-shader.md) для сообщения пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="eda94-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eda94-105">Syntax</span></span>
<span data-ttu-id="eda94-106">Это встроенное определение функции эквивалентно следующему шаблону функции:</span><span class="sxs-lookup"><span data-stu-id="eda94-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="eda94-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eda94-107">Parameters</span></span>

`THit`

<span data-ttu-id="eda94-108">Значение с плавающей запятой, задающее параметр параметрической расстояния пересечения.</span><span class="sxs-lookup"><span data-stu-id="eda94-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="eda94-109">Целое число без знака, определяющее тип произошедших попаданий.</span><span class="sxs-lookup"><span data-stu-id="eda94-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="eda94-110">Это заданное пользователем значение в диапазоне 0-127.</span><span class="sxs-lookup"><span data-stu-id="eda94-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="eda94-111">Значение может быть считано [любыми](any-hit-shader.md) [ближайшими шейдерами попадания](closest-hit-shader.md) с встроенной функцией **хиткинд** .</span><span class="sxs-lookup"><span data-stu-id="eda94-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="eda94-112">Определяемая пользователем структура [**структуры атрибута пересечения**](intersection-attributes.md) , указывающая атрибуты пересечения.</span><span class="sxs-lookup"><span data-stu-id="eda94-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="eda94-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eda94-113">Return Value</span></span>

<span data-ttu-id="eda94-114">**bool (логическое** ) Значение true, если попадание было принято.</span><span class="sxs-lookup"><span data-stu-id="eda94-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="eda94-115">Попадание отклоняется, если *сит* находится за пределами текущего интервала лучей или любой шейдер попадания вызывает [**игнорехит**](ignorehit-function.md).</span><span class="sxs-lookup"><span data-stu-id="eda94-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="eda94-116">Текущий интервал лучей определяется **райтмин** и **райткуррент**.</span><span class="sxs-lookup"><span data-stu-id="eda94-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eda94-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eda94-117">Remarks</span></span>

<span data-ttu-id="eda94-118">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="eda94-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="eda94-119">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="eda94-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="eda94-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eda94-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda94-121">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eda94-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




