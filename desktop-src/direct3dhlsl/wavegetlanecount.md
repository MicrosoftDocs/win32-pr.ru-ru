---
title: Функция Вавежетланекаунт
description: Возвращает количество желобов в волне на этой архитектуре.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Функция Вавежетланекаунт HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414156"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="07f5d-104">Функция Вавежетланекаунт</span><span class="sxs-lookup"><span data-stu-id="07f5d-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="07f5d-105">Возвращает количество желобов в волне на этой архитектуре.</span><span class="sxs-lookup"><span data-stu-id="07f5d-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f5d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07f5d-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="07f5d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="07f5d-107">Parameters</span></span>

<span data-ttu-id="07f5d-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="07f5d-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07f5d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07f5d-109">Return value</span></span>

<span data-ttu-id="07f5d-110">Результат будет составлять от 4 до 128 и включает все волны: активные, неактивные и (или) вспомогательные желобы.</span><span class="sxs-lookup"><span data-stu-id="07f5d-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="07f5d-111">Результат, возвращаемый этой функцией, может значительно различаться в зависимости от реализации драйвера.</span><span class="sxs-lookup"><span data-stu-id="07f5d-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f5d-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="07f5d-112">Remarks</span></span>

<span data-ttu-id="07f5d-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="07f5d-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="07f5d-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="07f5d-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="07f5d-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07f5d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f5d-116">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="07f5d-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="07f5d-117">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="07f5d-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




