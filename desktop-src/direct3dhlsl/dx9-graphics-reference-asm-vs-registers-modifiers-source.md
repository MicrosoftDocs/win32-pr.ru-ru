---
title: Модификаторы исходного регистра исходных шейдеров вершин
description: Модификаторы источника можно применять для изменения данных, считанных из исходного регистра, до того, как данные будут использоваться инструкцией.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411160"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="97cdc-103">Модификаторы исходного регистра исходных шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="97cdc-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="97cdc-104">Модификаторы источника можно применять для изменения данных, считанных из исходного регистра, до того, как данные будут использоваться инструкцией.</span><span class="sxs-lookup"><span data-stu-id="97cdc-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="97cdc-105">Negate</span><span class="sxs-lookup"><span data-stu-id="97cdc-105">Negate</span></span>

<span data-ttu-id="97cdc-106">Инвертирует содержимое регистра источника.</span><span class="sxs-lookup"><span data-stu-id="97cdc-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="97cdc-107">Модификатор компонента</span><span class="sxs-lookup"><span data-stu-id="97cdc-107">Component modifier</span></span> | <span data-ttu-id="97cdc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="97cdc-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="97cdc-109">\- Cерверный</span><span class="sxs-lookup"><span data-stu-id="97cdc-109">\- r</span></span>               | <span data-ttu-id="97cdc-110">Отрицание источника</span><span class="sxs-lookup"><span data-stu-id="97cdc-110">Source negation</span></span> |



 

<span data-ttu-id="97cdc-111">Модификатор отрицания не может использоваться во втором регистре источника следующих инструкций: [m3x2-VS](m3x2---vs.md), [m3x3-VS](m3x3---vs.md), [m3x4-VS](m3x4---vs.md), [m4x3-VS](m4x3---vs.md), [m4x4-VS](m4x4---vs.md).</span><span class="sxs-lookup"><span data-stu-id="97cdc-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="97cdc-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="97cdc-112">Vertex shader versions</span></span> | <span data-ttu-id="97cdc-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="97cdc-113">1\_1</span></span> | <span data-ttu-id="97cdc-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cdc-114">2\_0</span></span> | <span data-ttu-id="97cdc-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="97cdc-115">2\_x</span></span> | <span data-ttu-id="97cdc-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="97cdc-116">2\_sw</span></span> | <span data-ttu-id="97cdc-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cdc-117">3\_0</span></span> | <span data-ttu-id="97cdc-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="97cdc-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="97cdc-119">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-119">x</span></span>    | <span data-ttu-id="97cdc-120">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-120">x</span></span>    | <span data-ttu-id="97cdc-121">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-121">x</span></span>    | <span data-ttu-id="97cdc-122">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-122">x</span></span>     | <span data-ttu-id="97cdc-123">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-123">x</span></span>    | <span data-ttu-id="97cdc-124">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="97cdc-125">Абсолютное значение</span><span class="sxs-lookup"><span data-stu-id="97cdc-125">Absolute Value</span></span>

<span data-ttu-id="97cdc-126">Получение абсолютного значения регистра.</span><span class="sxs-lookup"><span data-stu-id="97cdc-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="97cdc-127">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="97cdc-127">Vertex shader versions</span></span> | <span data-ttu-id="97cdc-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="97cdc-128">1\_1</span></span> | <span data-ttu-id="97cdc-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cdc-129">2\_0</span></span> | <span data-ttu-id="97cdc-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="97cdc-130">2\_x</span></span> | <span data-ttu-id="97cdc-131">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="97cdc-131">2\_sw</span></span> | <span data-ttu-id="97cdc-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97cdc-132">3\_0</span></span> | <span data-ttu-id="97cdc-133">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="97cdc-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="97cdc-134">abs</span><span class="sxs-lookup"><span data-stu-id="97cdc-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="97cdc-135">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-135">x</span></span>    | <span data-ttu-id="97cdc-136">x</span><span class="sxs-lookup"><span data-stu-id="97cdc-136">x</span></span>     |



 

<span data-ttu-id="97cdc-137">Если шейдер версии 3 считывает из одного или нескольких регистров с плавающей запятой (c \# ), одно из следующих должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="97cdc-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="97cdc-138">Все константные регистры с плавающей запятой должны использовать модификатор ABS.</span><span class="sxs-lookup"><span data-stu-id="97cdc-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="97cdc-139">Ни один из постоянных регистров с плавающей запятой не может использовать модификатор ABS.</span><span class="sxs-lookup"><span data-stu-id="97cdc-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97cdc-140">См. также</span><span class="sxs-lookup"><span data-stu-id="97cdc-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97cdc-141">Модификаторы регистра для шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="97cdc-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




