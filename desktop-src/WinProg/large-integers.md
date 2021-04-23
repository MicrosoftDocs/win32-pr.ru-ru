---
title: Большие целые числа
description: Большие целочисленные функции и структуры изначально поддерживали 64-разрядные значения в 32-разрядной версии Windows.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- большие целые числа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700921"
---
# <a name="large-integers"></a><span data-ttu-id="40118-104">Большие целые числа</span><span class="sxs-lookup"><span data-stu-id="40118-104">Large Integers</span></span>

<span data-ttu-id="40118-105">Большие целочисленные функции и структуры изначально поддерживали 64-разрядные значения в 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="40118-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="40118-106">Теперь компилятор C может поддерживать 64-разрядные целые числа в собственном коде.</span><span class="sxs-lookup"><span data-stu-id="40118-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="40118-107">Например, Microsoft Visual C++ поддерживает целочисленный тип с размером [**\_ \_ Int64**](/windows/desktop/Midl/--int64) .</span><span class="sxs-lookup"><span data-stu-id="40118-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="40118-108">Дополнительные сведения см. в документации, входящей в состав компилятора C.</span><span class="sxs-lookup"><span data-stu-id="40118-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="40118-109">Сведения о 64-разрядных целых числах в 64-разрядной версии Windows см. [в разделе новые типы данных](/windows/desktop/WinProg64/the-new-data-types).</span><span class="sxs-lookup"><span data-stu-id="40118-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="40118-110">Операции с большими целочисленными значениями</span><span class="sxs-lookup"><span data-stu-id="40118-110">Large Integer Operations</span></span>

<span data-ttu-id="40118-111">Приложения могут умножить 32-разрядные целые числа со знаком или без знака, создавая 64-разрядные результаты с помощью функций [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) и [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="40118-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="40118-112">Приложения могут сдвинуть биты в 64-битных значениях влево или вправо с помощью функций [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)и [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) .</span><span class="sxs-lookup"><span data-stu-id="40118-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="40118-113">Эти функции обеспечивают логическую и арифметическую смену.</span><span class="sxs-lookup"><span data-stu-id="40118-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="40118-114">Приложения также могут умножить и разделить 32-битные значения в одной операции с помощью функции [**мулдив**](/windows/desktop/api/Winbase/nf-winbase-muldiv) .</span><span class="sxs-lookup"><span data-stu-id="40118-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="40118-115">Хотя результатом операции является 32-разрядное значение, функция сохраняет промежуточный результат в виде 64-разрядного значения, чтобы информация не была потеряна при умножении и разделении больших 32-разрядных значений.</span><span class="sxs-lookup"><span data-stu-id="40118-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="40118-116">Ссылка на большое целое число</span><span class="sxs-lookup"><span data-stu-id="40118-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="40118-117">Большие целочисленные функции</span><span class="sxs-lookup"><span data-stu-id="40118-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="40118-118">Структуры больших целых чисел</span><span class="sxs-lookup"><span data-stu-id="40118-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 