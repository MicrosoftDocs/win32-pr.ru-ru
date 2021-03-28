---
title: Функция Вавеактивеаллекуал
description: Возвращает значение true, если выражение одинаково для каждой активной полосы в текущем звуковом поле (и, таким образом, единообразно в нем).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Функция Вавеактивеаллекуал HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797250"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="f89d1-104">Функция Вавеактивеаллекуал</span><span class="sxs-lookup"><span data-stu-id="f89d1-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="f89d1-105">Возвращает значение true, если выражение одинаково для каждой активной полосы в текущем звуковом поле (и, таким образом, единообразно в нем).</span><span class="sxs-lookup"><span data-stu-id="f89d1-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="f89d1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f89d1-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="f89d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f89d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89d1-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="f89d1-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="f89d1-109">Выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="f89d1-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89d1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f89d1-110">Return value</span></span>

<span data-ttu-id="f89d1-111">Значение true, если выражение одинаково для каждой активной полосы в текущем волна.</span><span class="sxs-lookup"><span data-stu-id="f89d1-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89d1-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f89d1-112">Remarks</span></span>

<span data-ttu-id="f89d1-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="f89d1-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="f89d1-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f89d1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89d1-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="f89d1-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="f89d1-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="f89d1-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




