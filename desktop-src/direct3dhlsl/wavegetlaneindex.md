---
title: Функция Вавежетланеиндекс
description: Возвращает индекс текущей полосы в пределах текущей волны.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Функция Вавежетланеиндекс HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997175"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="26774-104">Функция Вавежетланеиндекс</span><span class="sxs-lookup"><span data-stu-id="26774-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="26774-105">Возвращает индекс текущей полосы в пределах текущей волны.</span><span class="sxs-lookup"><span data-stu-id="26774-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="26774-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26774-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="26774-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="26774-107">Parameters</span></span>

<span data-ttu-id="26774-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="26774-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26774-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26774-109">Return value</span></span>

<span data-ttu-id="26774-110">Текущий индекс полосы.</span><span class="sxs-lookup"><span data-stu-id="26774-110">The current lane index.</span></span> <span data-ttu-id="26774-111">Результат будет находиться в диапазоне от 0 до результата, возвращенного из [**вавежетланекаунт**](wavegetlanecount.md).</span><span class="sxs-lookup"><span data-stu-id="26774-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26774-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="26774-112">Remarks</span></span>

<span data-ttu-id="26774-113">Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="26774-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="26774-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26774-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26774-115">Общие сведения о модели шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="26774-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="26774-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="26774-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




