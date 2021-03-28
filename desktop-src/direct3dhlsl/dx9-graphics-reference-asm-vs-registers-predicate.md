---
title: Регистр предикатов (Справочник по HLSL VS)
description: Этот выходной регистр шейдера вершин содержит логическое значение для каждого канала.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104069396"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="52da1-103">Регистр предикатов (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="52da1-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="52da1-104">Этот выходной регистр шейдера вершин содержит логическое значение для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="52da1-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="52da1-105">Регистр предикатов поддерживается следующими версиями.</span><span class="sxs-lookup"><span data-stu-id="52da1-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="52da1-106">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="52da1-106">Vertex shader versions</span></span> | <span data-ttu-id="52da1-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="52da1-107">1\_1</span></span> | <span data-ttu-id="52da1-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52da1-108">2\_0</span></span> | <span data-ttu-id="52da1-109">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="52da1-109">2\_sw</span></span> | <span data-ttu-id="52da1-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="52da1-110">2\_x</span></span> | <span data-ttu-id="52da1-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52da1-111">3\_0</span></span> | <span data-ttu-id="52da1-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="52da1-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="52da1-113">Регистр предиката</span><span class="sxs-lookup"><span data-stu-id="52da1-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="52da1-114">x</span><span class="sxs-lookup"><span data-stu-id="52da1-114">x</span></span>    | <span data-ttu-id="52da1-115">x</span><span class="sxs-lookup"><span data-stu-id="52da1-115">x</span></span>    | <span data-ttu-id="52da1-116">x</span><span class="sxs-lookup"><span data-stu-id="52da1-116">x</span></span>     |



 

<span data-ttu-id="52da1-117">Ниже приведены свойства регистра.</span><span class="sxs-lookup"><span data-stu-id="52da1-117">Here are the register properties.</span></span>



| <span data-ttu-id="52da1-118">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="52da1-118">Register type</span></span> | <span data-ttu-id="52da1-119">Count</span><span class="sxs-lookup"><span data-stu-id="52da1-119">Count</span></span> | <span data-ttu-id="52da1-120">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="52da1-120">R/W</span></span> | <span data-ttu-id="52da1-121">\# Чтение портов</span><span class="sxs-lookup"><span data-stu-id="52da1-121">\# Read ports</span></span> | <span data-ttu-id="52da1-122">\# Операций чтения и inst</span><span class="sxs-lookup"><span data-stu-id="52da1-122">\# Reads/inst</span></span> | <span data-ttu-id="52da1-123">Измерение</span><span class="sxs-lookup"><span data-stu-id="52da1-123">Dimension</span></span> | <span data-ttu-id="52da1-124">реладдр</span><span class="sxs-lookup"><span data-stu-id="52da1-124">RelAddr</span></span> | <span data-ttu-id="52da1-125">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="52da1-125">Defaults</span></span> | <span data-ttu-id="52da1-126">Требуется ДКЛ</span><span class="sxs-lookup"><span data-stu-id="52da1-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="52da1-127">Предикат (p)</span><span class="sxs-lookup"><span data-stu-id="52da1-127">Predicate(p)</span></span>  | <span data-ttu-id="52da1-128">1</span><span class="sxs-lookup"><span data-stu-id="52da1-128">1</span></span>     | <span data-ttu-id="52da1-129">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="52da1-129">R/W</span></span> | <span data-ttu-id="52da1-130">1</span><span class="sxs-lookup"><span data-stu-id="52da1-130">1</span></span>             | <span data-ttu-id="52da1-131">1</span><span class="sxs-lookup"><span data-stu-id="52da1-131">1</span></span>             | <span data-ttu-id="52da1-132">4</span><span class="sxs-lookup"><span data-stu-id="52da1-132">4</span></span>         | <span data-ttu-id="52da1-133">Н/Д</span><span class="sxs-lookup"><span data-stu-id="52da1-133">N/A</span></span>     | <span data-ttu-id="52da1-134">Отсутствуют</span><span class="sxs-lookup"><span data-stu-id="52da1-134">None</span></span>     | <span data-ttu-id="52da1-135">Нет</span><span class="sxs-lookup"><span data-stu-id="52da1-135">N</span></span>            |



 

<span data-ttu-id="52da1-136">Регистр предикатов можно изменить с помощью [сетп \_ comp-VS](setp-comp---vs.md). Для этого регистра нет значений по умолчанию. приложению необходимо задать регистр перед его использованием.</span><span class="sxs-lookup"><span data-stu-id="52da1-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52da1-137">См. также</span><span class="sxs-lookup"><span data-stu-id="52da1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52da1-138">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="52da1-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




