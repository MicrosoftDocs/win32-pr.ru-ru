---
description: В этом разделе определяются \_ константы ИНЕГ локали \* , используемые NLS.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: Константы LOCALE_INEG *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343992"
---
# <a name="locale_ineg-constants"></a><span data-ttu-id="9679e-103">\_Константы ИНЕГ языкового стандарта \*</span><span class="sxs-lookup"><span data-stu-id="9679e-103">LOCALE\_INEG\* Constants</span></span>

<span data-ttu-id="9679e-104">В этом разделе определяются \_ константы ИНЕГ локали \* , используемые NLS.</span><span class="sxs-lookup"><span data-stu-id="9679e-104">This topic defines the LOCALE\_INEG\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9679e-105">Значение</span><span class="sxs-lookup"><span data-stu-id="9679e-105">Value</span></span></th>
<th><span data-ttu-id="9679e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9679e-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9679e-107">LOCALE_INEGCURR</span><span class="sxs-lookup"><span data-stu-id="9679e-107">LOCALE_INEGCURR</span></span></td>
<td><span data-ttu-id="9679e-108">Режим отрицательной валюты.</span><span class="sxs-lookup"><span data-stu-id="9679e-108">Negative currency mode.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9679e-109">Режим</span><span class="sxs-lookup"><span data-stu-id="9679e-109">Mode</span></span></th>
<th><span data-ttu-id="9679e-110">Формат для отрицательной валюты</span><span class="sxs-lookup"><span data-stu-id="9679e-110">Format for negative currency</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9679e-111">0</span><span class="sxs-lookup"><span data-stu-id="9679e-111">0</span></span></td>
<td><span data-ttu-id="9679e-112">Левая круглая скобка, символ денежной суммы, число, правая круглая скобка; Например, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="9679e-112">Left parenthesis, monetary symbol, number, right parenthesis; for example, ($1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-113">1</span><span class="sxs-lookup"><span data-stu-id="9679e-113">1</span></span></td>
<td><span data-ttu-id="9679e-114">Отрицательный знак, денежный символ, число; Например,-$1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-114">Negative sign, monetary symbol, number; for example, -$1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-115">2</span><span class="sxs-lookup"><span data-stu-id="9679e-115">2</span></span></td>
<td><span data-ttu-id="9679e-116">Символ денежной суммы, знак минус, число; Например, $-1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-116">Monetary symbol, negative sign, number; for example, $-1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-117">3</span><span class="sxs-lookup"><span data-stu-id="9679e-117">3</span></span></td>
<td><span data-ttu-id="9679e-118">Символ денежной суммы, число, знак минус; Например, $1,1-</span><span class="sxs-lookup"><span data-stu-id="9679e-118">Monetary symbol, number, negative sign; for example, $1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-119">4</span><span class="sxs-lookup"><span data-stu-id="9679e-119">4</span></span></td>
<td><span data-ttu-id="9679e-120">Открывающая круглая скобка, цифра, денежный символ, правая круглая скобка; Например, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="9679e-120">Left parenthesis, number, monetary symbol, right parenthesis; for example, (1.1$)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-121">5</span><span class="sxs-lookup"><span data-stu-id="9679e-121">5</span></span></td>
<td><span data-ttu-id="9679e-122">Отрицательный знак, число, денежный символ; Например,-$1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-122">Negative sign, number, monetary symbol; for example, -1.1$</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-123">6</span><span class="sxs-lookup"><span data-stu-id="9679e-123">6</span></span></td>
<td><span data-ttu-id="9679e-124">Число, знак минуса, символ денежной суммы; Например, 1,1-$</span><span class="sxs-lookup"><span data-stu-id="9679e-124">Number, negative sign, monetary symbol; for example, 1.1-$</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-125">7</span><span class="sxs-lookup"><span data-stu-id="9679e-125">7</span></span></td>
<td><span data-ttu-id="9679e-126">Число, денежный символ, знак отрицательного числа; Например, $1,1-</span><span class="sxs-lookup"><span data-stu-id="9679e-126">Number, monetary symbol, negative sign; for example, 1.1$-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-127">8</span><span class="sxs-lookup"><span data-stu-id="9679e-127">8</span></span></td>
<td><span data-ttu-id="9679e-128">Отрицательный знак, число, пробел, денежный символ (например, #5, но с пробелом до символа денежной суммы); Например,-$1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-128">Negative sign, number, space, monetary symbol (like #5, but with a space before the monetary symbol); for example, -1.1 $</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-129">9</span><span class="sxs-lookup"><span data-stu-id="9679e-129">9</span></span></td>
<td><span data-ttu-id="9679e-130">Отрицательный знак, денежный символ, пробел, число (например, #1, но с пробелом после символа денежной суммы); Например,-$1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-130">Negative sign, monetary symbol, space, number (like #1, but with a space after the monetary symbol); for example, -$ 1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-131">10</span><span class="sxs-lookup"><span data-stu-id="9679e-131">10</span></span></td>
<td><span data-ttu-id="9679e-132">Число, пробел, денежный символ, знак минуса (например, #7, но с пробелом до символа денежной суммы); Например, $1,1-</span><span class="sxs-lookup"><span data-stu-id="9679e-132">Number, space, monetary symbol, negative sign (like #7, but with a space before the monetary symbol); for example, 1.1 $-</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-133">11</span><span class="sxs-lookup"><span data-stu-id="9679e-133">11</span></span></td>
<td><span data-ttu-id="9679e-134">Символ денежной суммы, пробел, число, знак минуса (например, #3, но с пробелом после символа денежной суммы); Например, $1,1-</span><span class="sxs-lookup"><span data-stu-id="9679e-134">Monetary symbol, space, number, negative sign (like #3, but with a space after the monetary symbol); for example, $ 1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-135">12</span><span class="sxs-lookup"><span data-stu-id="9679e-135">12</span></span></td>
<td><span data-ttu-id="9679e-136">Символ денежной суммы, пробел, знак минуса, число (например, #2, но с пробелом после символа денежной суммы); Например, $-1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-136">Monetary symbol, space, negative sign, number (like #2, but with a space after the monetary symbol); for example, $ -1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-137">13</span><span class="sxs-lookup"><span data-stu-id="9679e-137">13</span></span></td>
<td><span data-ttu-id="9679e-138">Число, отрицательный знак, пробел, денежный символ (например, #6, но с пробелом до символа денежной суммы); Например, 1,1-$</span><span class="sxs-lookup"><span data-stu-id="9679e-138">Number, negative sign, space, monetary symbol (like #6, but with a space before the monetary symbol); for example, 1.1- $</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-139">14</span><span class="sxs-lookup"><span data-stu-id="9679e-139">14</span></span></td>
<td><span data-ttu-id="9679e-140">Открывающая круглая скобка, символ денежной суммы, пробел, число, правая круглая скобка (например, #0, но с пробелом после символа денежной суммы); Например, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="9679e-140">Left parenthesis, monetary symbol, space, number, right parenthesis (like #0, but with a space after the monetary symbol); for example, ($ 1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-141">15</span><span class="sxs-lookup"><span data-stu-id="9679e-141">15</span></span></td>
<td><span data-ttu-id="9679e-142">Левая круглая скобка, число, пробел, символ денежной суммы, правая круглая скобка (например, #4, но с пробелом перед символом денежной суммы); Например, ($1,1)</span><span class="sxs-lookup"><span data-stu-id="9679e-142">Left parenthesis, number, space, monetary symbol, right parenthesis (like #4, but with a space before the monetary symbol); for example, (1.1 $)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-143">LOCALE_INEGNUMBER</span><span class="sxs-lookup"><span data-stu-id="9679e-143">LOCALE_INEGNUMBER</span></span></td>
<td><span data-ttu-id="9679e-144">Режим отрицательного числа, то есть формат отрицательного числа.</span><span class="sxs-lookup"><span data-stu-id="9679e-144">Negative number mode, that is, the format for a negative number.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9679e-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9679e-145">Value</span></span></th>
<th><span data-ttu-id="9679e-146">Формат</span><span class="sxs-lookup"><span data-stu-id="9679e-146">Format</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9679e-147">0</span><span class="sxs-lookup"><span data-stu-id="9679e-147">0</span></span></td>
<td><span data-ttu-id="9679e-148">Левая круглая скобка, число, правая круглая скобка; Например, (1,1)</span><span class="sxs-lookup"><span data-stu-id="9679e-148">Left parenthesis, number, right parenthesis; for example, (1.1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-149">1</span><span class="sxs-lookup"><span data-stu-id="9679e-149">1</span></span></td>
<td><span data-ttu-id="9679e-150">Отрицательный знак, число; Например,-1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-150">Negative sign, number; for example, -1.1</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-151">2</span><span class="sxs-lookup"><span data-stu-id="9679e-151">2</span></span></td>
<td><span data-ttu-id="9679e-152">Отрицательный знак, пробел, число; Например,-1,1</span><span class="sxs-lookup"><span data-stu-id="9679e-152">Negative sign, space, number; for example, - 1.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-153">3</span><span class="sxs-lookup"><span data-stu-id="9679e-153">3</span></span></td>
<td><span data-ttu-id="9679e-154">Число, знак минус; Например, 1,1-</span><span class="sxs-lookup"><span data-stu-id="9679e-154">Number, negative sign; for example, 1.1-</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-155">4</span><span class="sxs-lookup"><span data-stu-id="9679e-155">4</span></span></td>
<td><span data-ttu-id="9679e-156">Число, пробел, знак минус; Например, 1,1-</span><span class="sxs-lookup"><span data-stu-id="9679e-156">Number, space, negative sign; for example, 1.1 -</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-157">LOCALE_INEGSEPBYSPACE</span><span class="sxs-lookup"><span data-stu-id="9679e-157">LOCALE_INEGSEPBYSPACE</span></span></td>
<td><span data-ttu-id="9679e-158">Разделение отрицательного знака на денежное значение.</span><span class="sxs-lookup"><span data-stu-id="9679e-158">Separation of the negative sign in a monetary value.</span></span> <span data-ttu-id="9679e-159">Это значение равно 1, если символ денежной суммы отделяется пробелом от отрицательного значения или 0, если это не так.</span><span class="sxs-lookup"><span data-stu-id="9679e-159">This value is 1 if the monetary symbol is separated by a space from the negative amount, or 0 if it is not.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-160">LOCALE_INEGSIGNPOSN</span><span class="sxs-lookup"><span data-stu-id="9679e-160">LOCALE_INEGSIGNPOSN</span></span></td>
<td><span data-ttu-id="9679e-161">Индекс форматирования для отрицательных значений денежного знака.</span><span class="sxs-lookup"><span data-stu-id="9679e-161">Formatting index for the negative sign in currency values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9679e-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9679e-162">Value</span></span></th>
<th><span data-ttu-id="9679e-163">Значение</span><span class="sxs-lookup"><span data-stu-id="9679e-163">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9679e-164">0</span><span class="sxs-lookup"><span data-stu-id="9679e-164">0</span></span></td>
<td><span data-ttu-id="9679e-165">В скобках заключается сумма и символ денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="9679e-165">Parentheses surround the amount and the monetary symbol.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-166">1</span><span class="sxs-lookup"><span data-stu-id="9679e-166">1</span></span></td>
<td><span data-ttu-id="9679e-167">Знак перед числом.</span><span class="sxs-lookup"><span data-stu-id="9679e-167">The sign precedes the number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-168">2</span><span class="sxs-lookup"><span data-stu-id="9679e-168">2</span></span></td>
<td><span data-ttu-id="9679e-169">Знак соответствует номеру.</span><span class="sxs-lookup"><span data-stu-id="9679e-169">The sign follows the number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9679e-170">3</span><span class="sxs-lookup"><span data-stu-id="9679e-170">3</span></span></td>
<td><span data-ttu-id="9679e-171">Знак предшествует символу денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="9679e-171">The sign precedes the monetary symbol.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-172">4</span><span class="sxs-lookup"><span data-stu-id="9679e-172">4</span></span></td>
<td><span data-ttu-id="9679e-173">Знак соответствует символу денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="9679e-173">The sign follows the monetary symbol.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9679e-174">LOCALE_INEGSYMPRECEDES</span><span class="sxs-lookup"><span data-stu-id="9679e-174">LOCALE_INEGSYMPRECEDES</span></span></td>
<td><span data-ttu-id="9679e-175">Расположение символа денежной суммы в отрицательном денежном значении.</span><span class="sxs-lookup"><span data-stu-id="9679e-175">Position of the monetary symbol in a negative monetary value.</span></span> <span data-ttu-id="9679e-176">Это значение равно 1, если символ денежной суммы предшествует отрицательному значению, или 0, если символ соответствует сумме.</span><span class="sxs-lookup"><span data-stu-id="9679e-176">This value is 1 if the monetary symbol precedes the negative amount, or 0 if the symbol follows the amount.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



