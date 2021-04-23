---
title: шум
description: Создает случайное значение с помощью алгоритма Perl-Noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- шум HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414197"
---
# <a name="noise"></a><span data-ttu-id="70021-104">шум</span><span class="sxs-lookup"><span data-stu-id="70021-104">noise</span></span>

<span data-ttu-id="70021-105">Создает случайное значение с помощью алгоритма Perl-Noise.</span><span class="sxs-lookup"><span data-stu-id="70021-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="70021-106">*RET* шум (*x*)</span><span class="sxs-lookup"><span data-stu-id="70021-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="70021-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="70021-107">Parameters</span></span>



| <span data-ttu-id="70021-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="70021-108">Item</span></span>                                                   | <span data-ttu-id="70021-109">Описание</span><span class="sxs-lookup"><span data-stu-id="70021-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="70021-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="70021-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="70021-111">\[в \] векторе с плавающей точкой, из которого создается шум Perl.</span><span class="sxs-lookup"><span data-stu-id="70021-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="70021-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70021-112">Return Value</span></span>

<span data-ttu-id="70021-113">Значение шума Perl в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="70021-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="70021-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="70021-114">Remarks</span></span>

<span data-ttu-id="70021-115">Значения шума в Perl плавно меняются от одной точки к другой, создавая естественно выглядящие значения, создаваемые случайным образом.</span><span class="sxs-lookup"><span data-stu-id="70021-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="70021-116">Можно использовать Perl для создания процедурных текстур для таких эффектов, как «формирование состояния» и «пожар».</span><span class="sxs-lookup"><span data-stu-id="70021-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="70021-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="70021-117">Type Description</span></span>



| <span data-ttu-id="70021-118">Имя</span><span class="sxs-lookup"><span data-stu-id="70021-118">Name</span></span>  | [<span data-ttu-id="70021-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="70021-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="70021-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="70021-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="70021-121">Размер</span><span class="sxs-lookup"><span data-stu-id="70021-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="70021-122">*x*</span><span class="sxs-lookup"><span data-stu-id="70021-122">*x*</span></span>   | [<span data-ttu-id="70021-123">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="70021-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="70021-124">**float**</span><span class="sxs-lookup"><span data-stu-id="70021-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="70021-125">any</span><span class="sxs-lookup"><span data-stu-id="70021-125">any</span></span>  |
| <span data-ttu-id="70021-126">*обратно*</span><span class="sxs-lookup"><span data-stu-id="70021-126">*ret*</span></span> | [<span data-ttu-id="70021-127">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="70021-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="70021-128">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="70021-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="70021-129">1</span><span class="sxs-lookup"><span data-stu-id="70021-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="70021-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="70021-130">Minimum Shader Model</span></span>

<span data-ttu-id="70021-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="70021-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="70021-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="70021-132">Shader Model</span></span>                                                                       | <span data-ttu-id="70021-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="70021-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="70021-134">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="70021-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="70021-135">Нет</span><span class="sxs-lookup"><span data-stu-id="70021-135">no</span></span>                  |
| [<span data-ttu-id="70021-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70021-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="70021-137">Да (только для TX \_ 1 \_ 0)</span><span class="sxs-lookup"><span data-stu-id="70021-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="70021-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70021-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70021-139">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="70021-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

