---
title: Функция Вавеактивесум
description: Суммирует значение выражения по всем активным желобам в текущей волновой записи и реплицирует его во все дорожки в текущей волн.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Функция Вавеактивесум HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103987989"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="57451-104">Функция Вавеактивесум</span><span class="sxs-lookup"><span data-stu-id="57451-104">WaveActiveSum function</span></span>

<span data-ttu-id="57451-105">Суммирует значение выражения по всем активным желобам в текущей волновой записи и реплицирует его во все дорожки в текущей волн.</span><span class="sxs-lookup"><span data-stu-id="57451-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="57451-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57451-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="57451-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="57451-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57451-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="57451-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="57451-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="57451-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57451-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57451-110">Return value</span></span>

<span data-ttu-id="57451-111">Значение Sum.</span><span class="sxs-lookup"><span data-stu-id="57451-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57451-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="57451-112">Remarks</span></span>

<span data-ttu-id="57451-113">Порядок операций не определен.</span><span class="sxs-lookup"><span data-stu-id="57451-113">The order of operations is undefined.</span></span>

<span data-ttu-id="57451-114">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="57451-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="57451-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="57451-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="57451-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57451-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57451-117">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="57451-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="57451-118">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="57451-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




