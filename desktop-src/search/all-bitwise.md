---
description: ВСЕ БИТОВЫЕ и БИТОВЫЕ ключевые слова используются для проверки битов в целочисленном типе.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ВСЕ побитовое и побитовое
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540655"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="347c1-103">ВСЕ побитовое и побитовое</span><span class="sxs-lookup"><span data-stu-id="347c1-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="347c1-104">**Все битовые** и **битовые** ключевые слова используются для проверки битов в целочисленном типе.</span><span class="sxs-lookup"><span data-stu-id="347c1-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="347c1-105">Если все биты в свойстве соответствуют маске, **все ПОбитовое** значение равно true.</span><span class="sxs-lookup"><span data-stu-id="347c1-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="347c1-106">Если хотя бы один из наборов битов в свойстве соответствует маске, **ПОбитовое** значение равно true.</span><span class="sxs-lookup"><span data-stu-id="347c1-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="347c1-107">Операторы можно применять как к скалярным свойствам (с одним значением), так и к свойствам Vector (несколько значений).</span><span class="sxs-lookup"><span data-stu-id="347c1-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="347c1-108">В следующем примере кода показано, как проверить значения свойств, используя **все ПОбитовое** и **побитовое**.</span><span class="sxs-lookup"><span data-stu-id="347c1-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="347c1-109">Операторы сравнения</span><span class="sxs-lookup"><span data-stu-id="347c1-109">Comparison Operators</span></span>

<span data-ttu-id="347c1-110">В следующей таблице перечислены поддерживаемые операторы сравнения для побитовых тестов.</span><span class="sxs-lookup"><span data-stu-id="347c1-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="347c1-111">Оператор сравнения</span><span class="sxs-lookup"><span data-stu-id="347c1-111">Comparison operator</span></span> | <span data-ttu-id="347c1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="347c1-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="347c1-113">Равно</span><span class="sxs-lookup"><span data-stu-id="347c1-113">Equal to</span></span>     |
| <span data-ttu-id="347c1-114">! = или <></span><span class="sxs-lookup"><span data-stu-id="347c1-114">!= or <></span></span>      | <span data-ttu-id="347c1-115">Не равно</span><span class="sxs-lookup"><span data-stu-id="347c1-115">Not equal to</span></span> |



 

<span data-ttu-id="347c1-116">Логика побитовых тестов приведена в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="347c1-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="347c1-117">Побитовый оператор теста и сравнения</span><span class="sxs-lookup"><span data-stu-id="347c1-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="347c1-118">Логика</span><span class="sxs-lookup"><span data-stu-id="347c1-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="347c1-119">= ВСЕ ПОБИТОВОЕ</span><span class="sxs-lookup"><span data-stu-id="347c1-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="347c1-120">Свойство & маска = маска</span><span class="sxs-lookup"><span data-stu-id="347c1-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="347c1-121">= НЕКОТОРОЕ ПОБИТОВОЕ</span><span class="sxs-lookup"><span data-stu-id="347c1-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="347c1-122">Свойство & Mask! = 0</span><span class="sxs-lookup"><span data-stu-id="347c1-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="347c1-123"><> ВСЕ ПОБИТОВЫЕ</span><span class="sxs-lookup"><span data-stu-id="347c1-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="347c1-124">Свойство & маска! = маска</span><span class="sxs-lookup"><span data-stu-id="347c1-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="347c1-125"><> ПОБИТОВОГО</span><span class="sxs-lookup"><span data-stu-id="347c1-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="347c1-126">Свойство & Mask = 0</span><span class="sxs-lookup"><span data-stu-id="347c1-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="347c1-127">Следующая таблица истинности использует примеры двоичных и шестнадцатеричных значений для демонстате логики побитовых тестов.</span><span class="sxs-lookup"><span data-stu-id="347c1-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="347c1-128">Свойство в двоичном формате (шестнадцатеричное)</span><span class="sxs-lookup"><span data-stu-id="347c1-128">Property in binary (hex)</span></span> | <span data-ttu-id="347c1-129">Маска в двоичном формате (HEX)</span><span class="sxs-lookup"><span data-stu-id="347c1-129">Mask in binary (hex)</span></span> | <span data-ttu-id="347c1-130">Свойство & Mask = двоичное (шестнадцатеричное)</span><span class="sxs-lookup"><span data-stu-id="347c1-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="347c1-131">= НЕКОТОРОЕ ПОБИТОВОЕ</span><span class="sxs-lookup"><span data-stu-id="347c1-131">= SOME BITWISE</span></span> | <span data-ttu-id="347c1-132">= ВСЕ ПОБИТОВОЕ</span><span class="sxs-lookup"><span data-stu-id="347c1-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="347c1-133">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-133">0001 (0x1)</span></span>               | <span data-ttu-id="347c1-134">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-134">0001 (0x1)</span></span>           | <span data-ttu-id="347c1-135">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-135">0001 (0x1)</span></span>                     | <span data-ttu-id="347c1-136">True</span><span class="sxs-lookup"><span data-stu-id="347c1-136">True</span></span>           | <span data-ttu-id="347c1-137">True</span><span class="sxs-lookup"><span data-stu-id="347c1-137">True</span></span>          |
| <span data-ttu-id="347c1-138">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-138">0001 (0x1)</span></span>               | <span data-ttu-id="347c1-139">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="347c1-139">0011 (0x3)</span></span>           | <span data-ttu-id="347c1-140">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-140">0001 (0x1)</span></span>                     | <span data-ttu-id="347c1-141">True</span><span class="sxs-lookup"><span data-stu-id="347c1-141">True</span></span>           | <span data-ttu-id="347c1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="347c1-142">False</span></span>         |
| <span data-ttu-id="347c1-143">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="347c1-143">0011 (0x3)</span></span>               | <span data-ttu-id="347c1-144">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-144">0001 (0x1)</span></span>           | <span data-ttu-id="347c1-145">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-145">0001 (0x1)</span></span>                     | <span data-ttu-id="347c1-146">True</span><span class="sxs-lookup"><span data-stu-id="347c1-146">True</span></span>           | <span data-ttu-id="347c1-147">True</span><span class="sxs-lookup"><span data-stu-id="347c1-147">True</span></span>          |
| <span data-ttu-id="347c1-148">0010 (0x2)</span><span class="sxs-lookup"><span data-stu-id="347c1-148">0010 (0x2)</span></span>               | <span data-ttu-id="347c1-149">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347c1-149">0001 (0x1)</span></span>           | <span data-ttu-id="347c1-150">0000 (0x0)</span><span class="sxs-lookup"><span data-stu-id="347c1-150">0000 (0x0)</span></span>                     | <span data-ttu-id="347c1-151">Неверно</span><span class="sxs-lookup"><span data-stu-id="347c1-151">False</span></span>          | <span data-ttu-id="347c1-152">False</span><span class="sxs-lookup"><span data-stu-id="347c1-152">False</span></span>         |
| <span data-ttu-id="347c1-153">11110000 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="347c1-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="347c1-154">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="347c1-154">00000011 (0x03)</span></span>      | <span data-ttu-id="347c1-155">00000000 (0x00)</span><span class="sxs-lookup"><span data-stu-id="347c1-155">00000000 (0x00)</span></span>                | <span data-ttu-id="347c1-156">Неверно</span><span class="sxs-lookup"><span data-stu-id="347c1-156">False</span></span>          | <span data-ttu-id="347c1-157">False</span><span class="sxs-lookup"><span data-stu-id="347c1-157">False</span></span>         |
| <span data-ttu-id="347c1-158">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="347c1-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="347c1-159">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="347c1-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="347c1-160">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="347c1-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="347c1-161">True</span><span class="sxs-lookup"><span data-stu-id="347c1-161">True</span></span>           | <span data-ttu-id="347c1-162">True</span><span class="sxs-lookup"><span data-stu-id="347c1-162">True</span></span>          |
| <span data-ttu-id="347c1-163">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="347c1-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="347c1-164">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="347c1-164">00000011 (0x03)</span></span>      | <span data-ttu-id="347c1-165">00000010 (0x02)</span><span class="sxs-lookup"><span data-stu-id="347c1-165">00000010 (0x02)</span></span>                | <span data-ttu-id="347c1-166">True</span><span class="sxs-lookup"><span data-stu-id="347c1-166">True</span></span>           | <span data-ttu-id="347c1-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="347c1-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="347c1-168">Пример</span><span class="sxs-lookup"><span data-stu-id="347c1-168">Example</span></span>

<span data-ttu-id="347c1-169">Ниже приведен пример **ПОбитового** предиката ALL.</span><span class="sxs-lookup"><span data-stu-id="347c1-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="347c1-170">См. также</span><span class="sxs-lookup"><span data-stu-id="347c1-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="347c1-171">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="347c1-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="347c1-172">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="347c1-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="347c1-173">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="347c1-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



