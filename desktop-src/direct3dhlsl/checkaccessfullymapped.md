---
title: Функция Чеккакцессфуллимаппед
description: Определяет, все ли значения из операции выборки, сбора или загрузки обращаются к сопоставленным плиткам в мозаичном ресурсе.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Функция Чеккакцессфуллимаппед HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793177"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="35b02-104">Функция Чеккакцессфуллимаппед</span><span class="sxs-lookup"><span data-stu-id="35b02-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="35b02-105">Определяет, все ли значения из операции **выборки**, **сбора** или **загрузки** обращаются к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="35b02-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="35b02-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35b02-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="35b02-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="35b02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b02-108">*состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35b02-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b02-109">Тип: **\_ только uint**</span><span class="sxs-lookup"><span data-stu-id="35b02-109">Type: **uint\_only**</span></span>

<span data-ttu-id="35b02-110">Значение состояния, возвращаемое из операции **выборки**, **сбора** или **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="35b02-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="35b02-111">Так как вы не можете получить доступ к этому значению состояния напрямую, необходимо передать его в **чеккакцессфуллимаппед**.</span><span class="sxs-lookup"><span data-stu-id="35b02-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b02-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35b02-112">Return value</span></span>

<span data-ttu-id="35b02-113">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="35b02-113">Type: **bool**</span></span>

<span data-ttu-id="35b02-114">Возвращает **логическое** значение, указывающее, были ли в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features)доступны сопоставленные плитки из операции **выборки**, **сбора** или **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="35b02-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="35b02-115">Возвращает **значение true** , если все значения из операции обращаются к сопоставленным плиткам; в противном случае возвращает **значение false** , если какие бы то ни было значения были взяты из несопоставленной плитки.</span><span class="sxs-lookup"><span data-stu-id="35b02-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="35b02-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="35b02-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="35b02-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35b02-117">Minimum Shader Model</span></span>

<span data-ttu-id="35b02-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="35b02-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="35b02-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35b02-119">Shader Model</span></span>                                                                | <span data-ttu-id="35b02-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="35b02-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="35b02-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="35b02-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="35b02-122">да</span><span class="sxs-lookup"><span data-stu-id="35b02-122">yes</span></span>       |



 

<span data-ttu-id="35b02-123">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="35b02-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="35b02-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="35b02-124">Vertex</span></span> | <span data-ttu-id="35b02-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="35b02-125">Hull</span></span> | <span data-ttu-id="35b02-126">Домен</span><span class="sxs-lookup"><span data-stu-id="35b02-126">Domain</span></span> | <span data-ttu-id="35b02-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="35b02-127">Geometry</span></span> | <span data-ttu-id="35b02-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="35b02-128">Pixel</span></span> | <span data-ttu-id="35b02-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="35b02-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="35b02-130">x</span><span class="sxs-lookup"><span data-stu-id="35b02-130">x</span></span>     | <span data-ttu-id="35b02-131">x</span><span class="sxs-lookup"><span data-stu-id="35b02-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="35b02-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35b02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b02-133">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="35b02-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 