---
title: Регистр предикатов (Справочник по HLSL PS)
description: Этот выходной регистр шейдера пикселей содержит логическое значение для каждого канала.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785067"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="862d7-103">Регистр предикатов (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="862d7-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="862d7-104">Этот выходной регистр шейдера пикселей содержит логическое значение для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="862d7-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="862d7-105">Регистр предикатов поддерживается следующими версиями:</span><span class="sxs-lookup"><span data-stu-id="862d7-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="862d7-106">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="862d7-106">Pixel shader versions</span></span> | <span data-ttu-id="862d7-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="862d7-107">1\_1</span></span> | <span data-ttu-id="862d7-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="862d7-108">1\_2</span></span> | <span data-ttu-id="862d7-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="862d7-109">1\_3</span></span> | <span data-ttu-id="862d7-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="862d7-110">1\_4</span></span> | <span data-ttu-id="862d7-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="862d7-111">2\_0</span></span> | <span data-ttu-id="862d7-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="862d7-112">2\_sw</span></span> | <span data-ttu-id="862d7-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="862d7-113">2\_x</span></span> | <span data-ttu-id="862d7-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="862d7-114">3\_0</span></span> | <span data-ttu-id="862d7-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="862d7-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="862d7-116">Регистр предиката</span><span class="sxs-lookup"><span data-stu-id="862d7-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="862d7-117">x</span><span class="sxs-lookup"><span data-stu-id="862d7-117">x</span></span>    | <span data-ttu-id="862d7-118">x</span><span class="sxs-lookup"><span data-stu-id="862d7-118">x</span></span>    | <span data-ttu-id="862d7-119">x</span><span class="sxs-lookup"><span data-stu-id="862d7-119">x</span></span>     |



 

<span data-ttu-id="862d7-120">Ниже приведены свойства регистра.</span><span class="sxs-lookup"><span data-stu-id="862d7-120">Here are the register properties.</span></span>



| <span data-ttu-id="862d7-121">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="862d7-121">Register type</span></span> | <span data-ttu-id="862d7-122">Count</span><span class="sxs-lookup"><span data-stu-id="862d7-122">Count</span></span> | <span data-ttu-id="862d7-123">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="862d7-123">R/W</span></span> | <span data-ttu-id="862d7-124">\# Чтение портов</span><span class="sxs-lookup"><span data-stu-id="862d7-124">\# Read ports</span></span> | <span data-ttu-id="862d7-125">\# Операций чтения и inst</span><span class="sxs-lookup"><span data-stu-id="862d7-125">\# Reads/inst</span></span> | <span data-ttu-id="862d7-126">Измерение</span><span class="sxs-lookup"><span data-stu-id="862d7-126">Dimension</span></span> | <span data-ttu-id="862d7-127">реладдр</span><span class="sxs-lookup"><span data-stu-id="862d7-127">RelAddr</span></span> | <span data-ttu-id="862d7-128">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="862d7-128">Defaults</span></span> | <span data-ttu-id="862d7-129">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="862d7-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="862d7-130">Предикат (p)</span><span class="sxs-lookup"><span data-stu-id="862d7-130">Predicate(p)</span></span>  | <span data-ttu-id="862d7-131">1</span><span class="sxs-lookup"><span data-stu-id="862d7-131">1</span></span>     | <span data-ttu-id="862d7-132">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="862d7-132">R/W</span></span> | <span data-ttu-id="862d7-133">1</span><span class="sxs-lookup"><span data-stu-id="862d7-133">1</span></span>             | <span data-ttu-id="862d7-134">1</span><span class="sxs-lookup"><span data-stu-id="862d7-134">1</span></span>             | <span data-ttu-id="862d7-135">4</span><span class="sxs-lookup"><span data-stu-id="862d7-135">4</span></span>         | <span data-ttu-id="862d7-136">Н/Д</span><span class="sxs-lookup"><span data-stu-id="862d7-136">N/A</span></span>     | <span data-ttu-id="862d7-137">Отсутствуют</span><span class="sxs-lookup"><span data-stu-id="862d7-137">None</span></span>     | <span data-ttu-id="862d7-138">Нет</span><span class="sxs-lookup"><span data-stu-id="862d7-138">N</span></span>            |



 

<span data-ttu-id="862d7-139">Регистр предиката можно изменить с помощью [сетп \_ comp-PS](setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="862d7-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="862d7-140">Для этого регистра значения по умолчанию отсутствуют. приложению необходимо задать регистр перед его использованием.</span><span class="sxs-lookup"><span data-stu-id="862d7-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="862d7-141">См. также</span><span class="sxs-lookup"><span data-stu-id="862d7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="862d7-142">Регистры</span><span class="sxs-lookup"><span data-stu-id="862d7-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




