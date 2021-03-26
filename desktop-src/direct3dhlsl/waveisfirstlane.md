---
title: Функция Вавеисфирстлане
description: Возвращает значение true только для активной полосы в текущем волне с наименьшим индексом.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Функция Вавеисфирстлане HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339661"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="3974a-104">Функция Вавеисфирстлане</span><span class="sxs-lookup"><span data-stu-id="3974a-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="3974a-105">Возвращает значение true только для активной полосы в текущем волне с наименьшим индексом.</span><span class="sxs-lookup"><span data-stu-id="3974a-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3974a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3974a-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="3974a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3974a-107">Parameters</span></span>

<span data-ttu-id="3974a-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="3974a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3974a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3974a-109">Return value</span></span>

<span data-ttu-id="3974a-110">Значение true только для активной полосы в текущей волны с наименьшим индексом.</span><span class="sxs-lookup"><span data-stu-id="3974a-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="3974a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3974a-111">Remarks</span></span>

<span data-ttu-id="3974a-112">Эта функция может использоваться для определения операций, выполняемых только один раз для каждой волны.</span><span class="sxs-lookup"><span data-stu-id="3974a-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="3974a-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="3974a-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="3974a-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="3974a-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="3974a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3974a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3974a-116">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="3974a-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="3974a-117">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="3974a-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




