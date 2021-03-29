---
title: Функция Вавереадланефирст
description: Возвращает значение выражения для активной полосы текущего волна с наименьшим индексом.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- Функция Вавереадланефирст HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984104"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="3e681-104">Функция Вавереадланефирст</span><span class="sxs-lookup"><span data-stu-id="3e681-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="3e681-105">Возвращает значение выражения для активной полосы текущего волна с наименьшим индексом.</span><span class="sxs-lookup"><span data-stu-id="3e681-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e681-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e681-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="3e681-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e681-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e681-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="3e681-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="3e681-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="3e681-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e681-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e681-110">Return value</span></span>

<span data-ttu-id="3e681-111">Полученное значение равномерно распределяется по волнам.</span><span class="sxs-lookup"><span data-stu-id="3e681-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e681-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e681-112">Remarks</span></span>

<span data-ttu-id="3e681-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="3e681-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="3e681-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e681-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e681-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="3e681-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="3e681-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="3e681-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




