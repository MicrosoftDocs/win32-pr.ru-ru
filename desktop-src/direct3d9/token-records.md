---
description: В этом разделе описывается формат записей для каждого токена уровня записи. Сведения делятся на следующие разделы.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Записи маркеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710681"
---
# <a name="token-records"></a><span data-ttu-id="b6b97-104">Записи маркеров</span><span class="sxs-lookup"><span data-stu-id="b6b97-104">Token Records</span></span>

<span data-ttu-id="b6b97-105">В этом разделе описывается формат записей для каждого токена уровня записи.</span><span class="sxs-lookup"><span data-stu-id="b6b97-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="b6b97-106">Сведения делятся на следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="b6b97-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="b6b97-107">имя ТОКЕНа \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="b6b97-108">Строка ТОКЕНа \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="b6b97-109">\_целое число токенов</span><span class="sxs-lookup"><span data-stu-id="b6b97-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="b6b97-110">GUID ТОКЕНа \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="b6b97-111">\_список целых чисел токенов \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="b6b97-112">\_список с плавающей лексемой \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="b6b97-113">имя ТОКЕНа \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-113">TOKEN\_NAME</span></span>

<span data-ttu-id="b6b97-114">Запись переменной длины.</span><span class="sxs-lookup"><span data-stu-id="b6b97-114">A variable-length record.</span></span> <span data-ttu-id="b6b97-115">За маркером следует значение Count, указывающее число байтов, следующих за полем имени.</span><span class="sxs-lookup"><span data-stu-id="b6b97-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="b6b97-116">Запись с именем, равным ASCII, завершается.</span><span class="sxs-lookup"><span data-stu-id="b6b97-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="b6b97-117">Поле</span><span class="sxs-lookup"><span data-stu-id="b6b97-117">Field</span></span> | <span data-ttu-id="b6b97-118">Тип</span><span class="sxs-lookup"><span data-stu-id="b6b97-118">Type</span></span>       | <span data-ttu-id="b6b97-119">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b6b97-119">Size (bytes)</span></span> | <span data-ttu-id="b6b97-120">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b6b97-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="b6b97-121">token</span><span class="sxs-lookup"><span data-stu-id="b6b97-121">token</span></span> | <span data-ttu-id="b6b97-122">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-122">WORD</span></span>       | <span data-ttu-id="b6b97-123">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-123">2</span></span>            | <span data-ttu-id="b6b97-124">Имя токена \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-124">token\_name</span></span>                    |
| <span data-ttu-id="b6b97-125">count</span><span class="sxs-lookup"><span data-stu-id="b6b97-125">count</span></span> | <span data-ttu-id="b6b97-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-126">DWORD</span></span>      | <span data-ttu-id="b6b97-127">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-127">4</span></span>            | <span data-ttu-id="b6b97-128">Длина поля имени в байтах</span><span class="sxs-lookup"><span data-stu-id="b6b97-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="b6b97-129">name</span><span class="sxs-lookup"><span data-stu-id="b6b97-129">name</span></span>  | <span data-ttu-id="b6b97-130">Массив БАЙТОВ</span><span class="sxs-lookup"><span data-stu-id="b6b97-130">BYTE array</span></span> | <span data-ttu-id="b6b97-131">count</span><span class="sxs-lookup"><span data-stu-id="b6b97-131">count</span></span>        | <span data-ttu-id="b6b97-132">Имя ASCII</span><span class="sxs-lookup"><span data-stu-id="b6b97-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="b6b97-133">Строка ТОКЕНа \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-133">TOKEN\_STRING</span></span>

<span data-ttu-id="b6b97-134">Запись переменной длины.</span><span class="sxs-lookup"><span data-stu-id="b6b97-134">A variable-length record.</span></span> <span data-ttu-id="b6b97-135">За маркером следует значение Count, указывающее число байтов, следующих за строковым полем.</span><span class="sxs-lookup"><span data-stu-id="b6b97-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="b6b97-136">Строка в кодировке ASCII для счетчика длины сохраняет запись, которая завершается завершающим маркером.</span><span class="sxs-lookup"><span data-stu-id="b6b97-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="b6b97-137">Вариант признака конца определяется синтаксическими проблемами, которые обсуждаются в других местах.</span><span class="sxs-lookup"><span data-stu-id="b6b97-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="b6b97-138">Поле</span><span class="sxs-lookup"><span data-stu-id="b6b97-138">Field</span></span>      | <span data-ttu-id="b6b97-139">Тип</span><span class="sxs-lookup"><span data-stu-id="b6b97-139">Type</span></span>       | <span data-ttu-id="b6b97-140">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b6b97-140">Size (bytes)</span></span> | <span data-ttu-id="b6b97-141">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b6b97-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="b6b97-142">token</span><span class="sxs-lookup"><span data-stu-id="b6b97-142">token</span></span>      | <span data-ttu-id="b6b97-143">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-143">WORD</span></span>       | <span data-ttu-id="b6b97-144">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-144">2</span></span>            | <span data-ttu-id="b6b97-145">Строка токена \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-145">token\_string</span></span>                    |
| <span data-ttu-id="b6b97-146">count</span><span class="sxs-lookup"><span data-stu-id="b6b97-146">count</span></span>      | <span data-ttu-id="b6b97-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-147">DWORD</span></span>      | <span data-ttu-id="b6b97-148">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-148">4</span></span>            | <span data-ttu-id="b6b97-149">Длина строкового поля в байтах</span><span class="sxs-lookup"><span data-stu-id="b6b97-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="b6b97-150">Строка</span><span class="sxs-lookup"><span data-stu-id="b6b97-150">strinG</span></span>     | <span data-ttu-id="b6b97-151">Массив БАЙТОВ</span><span class="sxs-lookup"><span data-stu-id="b6b97-151">BYTE array</span></span> | <span data-ttu-id="b6b97-152">count</span><span class="sxs-lookup"><span data-stu-id="b6b97-152">count</span></span>        | <span data-ttu-id="b6b97-153">строка ASCII</span><span class="sxs-lookup"><span data-stu-id="b6b97-153">ASCII string</span></span>                     |
| <span data-ttu-id="b6b97-154">признак конца</span><span class="sxs-lookup"><span data-stu-id="b6b97-154">terminator</span></span> | <span data-ttu-id="b6b97-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-155">DWORD</span></span>      | <span data-ttu-id="b6b97-156">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-156">4</span></span>            | <span data-ttu-id="b6b97-157">\_разделительная точка с запятой или маркер \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="b6b97-158">\_целое число токенов</span><span class="sxs-lookup"><span data-stu-id="b6b97-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="b6b97-159">Фиксированная длина записи.</span><span class="sxs-lookup"><span data-stu-id="b6b97-159">A fixed length record.</span></span> <span data-ttu-id="b6b97-160">За маркером следует необходимое целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="b6b97-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="b6b97-161">Поле</span><span class="sxs-lookup"><span data-stu-id="b6b97-161">Field</span></span> | <span data-ttu-id="b6b97-162">Тип</span><span class="sxs-lookup"><span data-stu-id="b6b97-162">Type</span></span>  | <span data-ttu-id="b6b97-163">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b6b97-163">Size (bytes)</span></span> | <span data-ttu-id="b6b97-164">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b6b97-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="b6b97-165">token</span><span class="sxs-lookup"><span data-stu-id="b6b97-165">token</span></span> | <span data-ttu-id="b6b97-166">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-166">WORD</span></span>  | <span data-ttu-id="b6b97-167">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-167">2</span></span>            | <span data-ttu-id="b6b97-168">\_целое число токенов</span><span class="sxs-lookup"><span data-stu-id="b6b97-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="b6b97-169">Значений</span><span class="sxs-lookup"><span data-stu-id="b6b97-169">valuE</span></span> | <span data-ttu-id="b6b97-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-170">DWORD</span></span> | <span data-ttu-id="b6b97-171">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-171">4</span></span>            | <span data-ttu-id="b6b97-172">Одно целое</span><span class="sxs-lookup"><span data-stu-id="b6b97-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="b6b97-173">GUID ТОКЕНа \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-173">TOKEN\_GUID</span></span>

<span data-ttu-id="b6b97-174">Запись фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="b6b97-174">A fixed-length record.</span></span> <span data-ttu-id="b6b97-175">За маркером следуют четыре поля данных, определенные стандартом DCE использование.</span><span class="sxs-lookup"><span data-stu-id="b6b97-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="b6b97-176">Поле</span><span class="sxs-lookup"><span data-stu-id="b6b97-176">Field</span></span> | <span data-ttu-id="b6b97-177">Тип</span><span class="sxs-lookup"><span data-stu-id="b6b97-177">Type</span></span>       | <span data-ttu-id="b6b97-178">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b6b97-178">Size (bytes)</span></span> | <span data-ttu-id="b6b97-179">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b6b97-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="b6b97-180">token</span><span class="sxs-lookup"><span data-stu-id="b6b97-180">token</span></span> | <span data-ttu-id="b6b97-181">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-181">WORD</span></span>       | <span data-ttu-id="b6b97-182">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-182">2</span></span>            | <span data-ttu-id="b6b97-183">GUID токена \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="b6b97-184">Файл1</span><span class="sxs-lookup"><span data-stu-id="b6b97-184">Data1</span></span> | <span data-ttu-id="b6b97-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-185">DWORD</span></span>      | <span data-ttu-id="b6b97-186">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-186">4</span></span>            | <span data-ttu-id="b6b97-187">Поле данных UUID 1</span><span class="sxs-lookup"><span data-stu-id="b6b97-187">UUID data field 1</span></span> |
| <span data-ttu-id="b6b97-188">Data2</span><span class="sxs-lookup"><span data-stu-id="b6b97-188">Data2</span></span> | <span data-ttu-id="b6b97-189">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-189">WORD</span></span>       | <span data-ttu-id="b6b97-190">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-190">2</span></span>            | <span data-ttu-id="b6b97-191">Поле данных UUID 2</span><span class="sxs-lookup"><span data-stu-id="b6b97-191">UUID data field 2</span></span> |
| <span data-ttu-id="b6b97-192">Data3</span><span class="sxs-lookup"><span data-stu-id="b6b97-192">Data3</span></span> | <span data-ttu-id="b6b97-193">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-193">WORD</span></span>       | <span data-ttu-id="b6b97-194">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-194">2</span></span>            | <span data-ttu-id="b6b97-195">Поле данных UUID 3</span><span class="sxs-lookup"><span data-stu-id="b6b97-195">UUID data field 3</span></span> |
| <span data-ttu-id="b6b97-196">Data4</span><span class="sxs-lookup"><span data-stu-id="b6b97-196">Data4</span></span> | <span data-ttu-id="b6b97-197">Массив БАЙТОВ</span><span class="sxs-lookup"><span data-stu-id="b6b97-197">BYTE array</span></span> | <span data-ttu-id="b6b97-198">8</span><span class="sxs-lookup"><span data-stu-id="b6b97-198">8</span></span>            | <span data-ttu-id="b6b97-199">Поле данных UUID 4</span><span class="sxs-lookup"><span data-stu-id="b6b97-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="b6b97-200">\_список целых чисел токенов \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="b6b97-201">Запись переменной длины.</span><span class="sxs-lookup"><span data-stu-id="b6b97-201">A variable-length record.</span></span> <span data-ttu-id="b6b97-202">За маркером следует значение Count, указывающее количество целых чисел, следующих за полем списка.</span><span class="sxs-lookup"><span data-stu-id="b6b97-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="b6b97-203">Для повышения эффективности последовательные списки целых чисел должны быть объединены в один список.</span><span class="sxs-lookup"><span data-stu-id="b6b97-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="b6b97-204">Поле</span><span class="sxs-lookup"><span data-stu-id="b6b97-204">Field</span></span> | <span data-ttu-id="b6b97-205">Тип</span><span class="sxs-lookup"><span data-stu-id="b6b97-205">Type</span></span>  | <span data-ttu-id="b6b97-206">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b6b97-206">Size (bytes)</span></span> | <span data-ttu-id="b6b97-207">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b6b97-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="b6b97-208">token</span><span class="sxs-lookup"><span data-stu-id="b6b97-208">token</span></span> | <span data-ttu-id="b6b97-209">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-209">WORD</span></span>  | <span data-ttu-id="b6b97-210">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-210">2</span></span>            | <span data-ttu-id="b6b97-211">\_список целых чисел токенов \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="b6b97-212">count</span><span class="sxs-lookup"><span data-stu-id="b6b97-212">count</span></span> | <span data-ttu-id="b6b97-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-213">DWORD</span></span> | <span data-ttu-id="b6b97-214">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-214">4</span></span>            | <span data-ttu-id="b6b97-215">Число целых чисел в поле списка</span><span class="sxs-lookup"><span data-stu-id="b6b97-215">Number of integers in list field</span></span> |
| <span data-ttu-id="b6b97-216">list</span><span class="sxs-lookup"><span data-stu-id="b6b97-216">list</span></span>  | <span data-ttu-id="b6b97-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-217">DWORD</span></span> | <span data-ttu-id="b6b97-218">4 x число</span><span class="sxs-lookup"><span data-stu-id="b6b97-218">4 x count</span></span>    | <span data-ttu-id="b6b97-219">Список целых чисел</span><span class="sxs-lookup"><span data-stu-id="b6b97-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="b6b97-220">\_список с плавающей лексемой \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="b6b97-221">Запись переменной длины.</span><span class="sxs-lookup"><span data-stu-id="b6b97-221">A variable-length record.</span></span> <span data-ttu-id="b6b97-222">За маркером следует значение Count, которое указывает количество элементов float или Double, следующих за полем списка.</span><span class="sxs-lookup"><span data-stu-id="b6b97-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="b6b97-223">Размер значения с плавающей запятой (float или Double) определяется значением float сизеспеЦифиед в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="b6b97-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="b6b97-224">Для повышения эффективности списки с плавающей точкой с последовательным МАРКЕРом \_ \_ должны быть объединены в один список.</span><span class="sxs-lookup"><span data-stu-id="b6b97-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="b6b97-225">Поле</span><span class="sxs-lookup"><span data-stu-id="b6b97-225">Field</span></span> | <span data-ttu-id="b6b97-226">Тип</span><span class="sxs-lookup"><span data-stu-id="b6b97-226">Type</span></span>               | <span data-ttu-id="b6b97-227">Размер (в байтах)</span><span class="sxs-lookup"><span data-stu-id="b6b97-227">Size (bytes)</span></span>   | <span data-ttu-id="b6b97-228">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b6b97-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="b6b97-229">token</span><span class="sxs-lookup"><span data-stu-id="b6b97-229">token</span></span> | <span data-ttu-id="b6b97-230">WORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-230">WORD</span></span>               | <span data-ttu-id="b6b97-231">2</span><span class="sxs-lookup"><span data-stu-id="b6b97-231">2</span></span>              | <span data-ttu-id="b6b97-232">\_список с плавающей лексемой \_</span><span class="sxs-lookup"><span data-stu-id="b6b97-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="b6b97-233">count</span><span class="sxs-lookup"><span data-stu-id="b6b97-233">count</span></span> | <span data-ttu-id="b6b97-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6b97-234">DWORD</span></span>              | <span data-ttu-id="b6b97-235">4</span><span class="sxs-lookup"><span data-stu-id="b6b97-235">4</span></span>              | <span data-ttu-id="b6b97-236">Число элементов float или Double в поле списка</span><span class="sxs-lookup"><span data-stu-id="b6b97-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="b6b97-237">list</span><span class="sxs-lookup"><span data-stu-id="b6b97-237">list</span></span>  | <span data-ttu-id="b6b97-238">массив float/Double</span><span class="sxs-lookup"><span data-stu-id="b6b97-238">float/double array</span></span> | <span data-ttu-id="b6b97-239">число по 4 или 8 x</span><span class="sxs-lookup"><span data-stu-id="b6b97-239">4 or 8 x count</span></span> | <span data-ttu-id="b6b97-240">Float или Double List</span><span class="sxs-lookup"><span data-stu-id="b6b97-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="b6b97-241">См. также</span><span class="sxs-lookup"><span data-stu-id="b6b97-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6b97-242">Двоичное кодирование</span><span class="sxs-lookup"><span data-stu-id="b6b97-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 
