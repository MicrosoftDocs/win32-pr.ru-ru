---
description: В MOF числа — это цифры, описывающие числовые значения. MOF предоставляет разнообразные типы данных, которые преобразуются в автоматизацию, а также позволяют использовать эти числа в разных форматах. В следующей таблице перечислены числовые значения, поддерживаемые MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Числа (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701344"
---
# <a name="numbers-wmi"></a><span data-ttu-id="3b3f7-105">Числа (WMI)</span><span class="sxs-lookup"><span data-stu-id="3b3f7-105">Numbers (WMI)</span></span>

<span data-ttu-id="3b3f7-106">В MOF числа — это цифры, описывающие числовые значения.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="3b3f7-107">MOF предоставляет разнообразные типы данных, которые преобразуются в автоматизацию, а также позволяют использовать эти числа в разных форматах.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="3b3f7-108">В следующей таблице перечислены числовые значения, поддерживаемые MOF.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="3b3f7-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3b3f7-109">Data type</span></span>  | <span data-ttu-id="3b3f7-110">Тип автоматизации</span><span class="sxs-lookup"><span data-stu-id="3b3f7-110">Automation type</span></span> | <span data-ttu-id="3b3f7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3b3f7-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3f7-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-112">**sint8**</span></span>  | <span data-ttu-id="3b3f7-113">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-113">**VT\_I2**</span></span>      | <span data-ttu-id="3b3f7-114">8-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="3b3f7-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-115">**sint16**</span></span> | <span data-ttu-id="3b3f7-116">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-116">**VT\_I2**</span></span>      | <span data-ttu-id="3b3f7-117">16-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="3b3f7-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-118">**sint32**</span></span> | <span data-ttu-id="3b3f7-119">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3b3f7-119">VT\_I4</span></span>          | <span data-ttu-id="3b3f7-120">32-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="3b3f7-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-121">**sint64**</span></span> | <span data-ttu-id="3b3f7-122">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="3b3f7-123">64-разрядное целое число со знаком в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="3b3f7-124">Этот тип соответствует шестнадцатеричному или десятичному формату в соответствии с правилами Американский национальный институт стандартов (ANSI) (ANSI) C.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="3b3f7-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-125">**real32**</span></span> | <span data-ttu-id="3b3f7-126">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-126">**VT\_R4**</span></span>      | <span data-ttu-id="3b3f7-127">4-байтовое значение с плавающей запятой, которое соответствует институту стандартов электрических и электронных электроники, Inc. (IEEE).</span><span class="sxs-lookup"><span data-stu-id="3b3f7-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="3b3f7-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-128">**real64**</span></span> | <span data-ttu-id="3b3f7-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-129">**VT\_R8**</span></span>      | <span data-ttu-id="3b3f7-130">8-байтовое значение с плавающей запятой, следующее за стандартом IEEE.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="3b3f7-131">**uint8**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-131">**uint8**</span></span>  | <span data-ttu-id="3b3f7-132">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-132">**VT\_UI1**</span></span>     | <span data-ttu-id="3b3f7-133">8-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3b3f7-134">**uint16**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-134">**uint16**</span></span> | <span data-ttu-id="3b3f7-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-135">**VT\_I4**</span></span>      | <span data-ttu-id="3b3f7-136">16-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="3b3f7-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-137">**uint32**</span></span> | <span data-ttu-id="3b3f7-138">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-138">**VT\_I4**</span></span>      | <span data-ttu-id="3b3f7-139">32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="3b3f7-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-140">**uint64**</span></span> | <span data-ttu-id="3b3f7-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="3b3f7-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="3b3f7-142">64-разрядное целое число без знака в форме строки.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="3b3f7-143">Этот тип следует шестнадцатеричному или десятичному формату в соответствии с правилами ANSI C.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="3b3f7-144">Хотя при работе со службой автоматизации в коде MOF возникают некоторые изменения:</span><span class="sxs-lookup"><span data-stu-id="3b3f7-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="3b3f7-145">В качестве строк необходимо кодировать 64-разрядные целые числа.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="3b3f7-146">Автоматизация не поддерживает 64-разрядный целочисленный тип.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="3b3f7-147">Типы автоматизации не всегда соответствуют типам данных, равным bit.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="3b3f7-148">Например, Автоматизация использует VT \_ I4 для возврата 16-разрядного значения без знака.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="3b3f7-149">Это несоответствие существует из-за проблем с расширением знака.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="3b3f7-150">Если автоматизация использовала VT \_ I2 вместо VT \_ I4, 65 536 будет выглядеть как значение 1, что приведет к проблемам с типами и диапазонами.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="3b3f7-151">Аналогичным образом, Автоматизация представляет тип **UInt32** как VT \_ I4, так как для него не существует целочисленного типа, содержащего **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="3b3f7-152">Нет необходимости изменять представление для 8-разрядных чисел.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="3b3f7-153">Автоматизация поддерживает VT \_ UI1, 8-разрядный тип без знака.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="3b3f7-154">MOF поддерживает длинные константы.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-154">MOF supports long constants.</span></span> <span data-ttu-id="3b3f7-155">Вы объявляете длинную константу, используя простую последовательность цифр с необязательным отрицательным знаком.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="3b3f7-156">Длинная константа не может превышать размер переменной, объявленной для ее хранения.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="3b3f7-157">Некоторые примеры длинных констант — 1000 и 12310.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="3b3f7-158">MOF также поддерживает альтернативные числовые форматы.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="3b3f7-159">В следующей таблице перечислены специальные символы, которые необходимо использовать для описания шестнадцатеричных, двоичных и восьмеричных констант.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="3b3f7-160">Константа</span><span class="sxs-lookup"><span data-stu-id="3b3f7-160">Constant</span></span>               | <span data-ttu-id="3b3f7-161">Специальный символ</span><span class="sxs-lookup"><span data-stu-id="3b3f7-161">Special character</span></span>     | <span data-ttu-id="3b3f7-162">Пример</span><span class="sxs-lookup"><span data-stu-id="3b3f7-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="3b3f7-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="3b3f7-163">Decimal</span></span><br/>     | <span data-ttu-id="3b3f7-164">Нет</span><span class="sxs-lookup"><span data-stu-id="3b3f7-164">None</span></span><br/>       | <span data-ttu-id="3b3f7-165">Val = 65</span><span class="sxs-lookup"><span data-stu-id="3b3f7-165">val = 65</span></span><br/>       |
| <span data-ttu-id="3b3f7-166">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3b3f7-166">Hexadecimal</span></span><br/> | <span data-ttu-id="3b3f7-167">префикс 0x</span><span class="sxs-lookup"><span data-stu-id="3b3f7-167">0x prefix</span></span><br/>  | <span data-ttu-id="3b3f7-168">Val = 0x41 влево</span><span class="sxs-lookup"><span data-stu-id="3b3f7-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="3b3f7-169">Восьмеричн</span><span class="sxs-lookup"><span data-stu-id="3b3f7-169">Octal</span></span><br/>       | <span data-ttu-id="3b3f7-170">Ведущие 0</span><span class="sxs-lookup"><span data-stu-id="3b3f7-170">Leading 0</span></span><br/>  | <span data-ttu-id="3b3f7-171">Val = 0101</span><span class="sxs-lookup"><span data-stu-id="3b3f7-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="3b3f7-172">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="3b3f7-172">Binary</span></span><br/>      | <span data-ttu-id="3b3f7-173">Конец B</span><span class="sxs-lookup"><span data-stu-id="3b3f7-173">Trailing B</span></span><br/> | <span data-ttu-id="3b3f7-174">Val = 1000001B</span><span class="sxs-lookup"><span data-stu-id="3b3f7-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="3b3f7-175">Константу с плавающей запятой можно использовать для представления экспоненциальной нотации, а также дробей, как показано далее:</span><span class="sxs-lookup"><span data-stu-id="3b3f7-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="3b3f7-176">WMI считает константы с плавающей запятой как типы **VT \_ R8** для автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="3b3f7-177">В следующем примере описываются объявления классов и экземпляров, демонстрирующие использование каждого из числовых типов данных для задания свойств.</span><span class="sxs-lookup"><span data-stu-id="3b3f7-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




