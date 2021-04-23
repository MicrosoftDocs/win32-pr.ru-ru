---
title: Функция Граупмеморибарриер
description: Блокирует выполнение всех потоков в группе до тех пор, пока не завершится общий доступ к группе.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- Функция Граупмеморибарриер HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54a140a892b0e9144ef23fc0290ca3bb3747e90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068722"
---
# <a name="groupmemorybarrier-function"></a><span data-ttu-id="aabfb-104">Функция Граупмеморибарриер</span><span class="sxs-lookup"><span data-stu-id="aabfb-104">GroupMemoryBarrier function</span></span>

<span data-ttu-id="aabfb-105">Блокирует выполнение всех потоков в группе до тех пор, пока не завершится общий доступ к группе.</span><span class="sxs-lookup"><span data-stu-id="aabfb-105">Blocks execution of all threads in a group until all group shared accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabfb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aabfb-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="aabfb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aabfb-107">Parameters</span></span>

<span data-ttu-id="aabfb-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="aabfb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aabfb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aabfb-109">Return value</span></span>

<span data-ttu-id="aabfb-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="aabfb-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aabfb-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="aabfb-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="aabfb-112">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="aabfb-112">Minimum Shader Model</span></span>

<span data-ttu-id="aabfb-113">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="aabfb-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aabfb-114">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="aabfb-114">Shader Model</span></span>                                                                | <span data-ttu-id="aabfb-115">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="aabfb-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="aabfb-116">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="aabfb-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="aabfb-117">да</span><span class="sxs-lookup"><span data-stu-id="aabfb-117">yes</span></span>       |



 

<span data-ttu-id="aabfb-118">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="aabfb-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="aabfb-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="aabfb-119">Vertex</span></span> | <span data-ttu-id="aabfb-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="aabfb-120">Hull</span></span> | <span data-ttu-id="aabfb-121">Домен</span><span class="sxs-lookup"><span data-stu-id="aabfb-121">Domain</span></span> | <span data-ttu-id="aabfb-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="aabfb-122">Geometry</span></span> | <span data-ttu-id="aabfb-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="aabfb-123">Pixel</span></span> | <span data-ttu-id="aabfb-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="aabfb-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="aabfb-125">x</span><span class="sxs-lookup"><span data-stu-id="aabfb-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aabfb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aabfb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabfb-127">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="aabfb-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="aabfb-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="aabfb-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




