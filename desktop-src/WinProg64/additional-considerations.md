---
title: Дополнительные сведения
description: При переносе кода учитывайте следующие моменты.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Советы по переносу 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105704035"
---
# <a name="additional-considerations"></a><span data-ttu-id="b738b-104">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="b738b-104">Additional Considerations</span></span>

<span data-ttu-id="b738b-105">При переносе кода учитывайте следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="b738b-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="b738b-106">Следующее допущение больше не является допустимым:</span><span class="sxs-lookup"><span data-stu-id="b738b-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="b738b-107">Однако 64-разрядный компилятор определяет \_ Win32 для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="b738b-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="b738b-108">Следующее допущение больше не является допустимым:</span><span class="sxs-lookup"><span data-stu-id="b738b-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="b738b-109">В этом случае предложение else может представлять \_ Win32 или \_ Win64.</span><span class="sxs-lookup"><span data-stu-id="b738b-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="b738b-110">Будьте внимательны при выравнивании типов данных.</span><span class="sxs-lookup"><span data-stu-id="b738b-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="b738b-111">Макрос **\_ выравнивания типа** возвращает требования к выравниванию для типа данных.</span><span class="sxs-lookup"><span data-stu-id="b738b-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="b738b-112">Например: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 на x86, 8 для процессора Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 везде</span><span class="sxs-lookup"><span data-stu-id="b738b-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="b738b-113">Например, код ядра, который в настоящее время выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b738b-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="b738b-114">возможно, следует изменить на:</span><span class="sxs-lookup"><span data-stu-id="b738b-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="b738b-115">Автоматические исправления исключений выравнивания в режиме ядра отключены для систем Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="b738b-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="b738b-116">Будьте внимательны при отсутствии операций.</span><span class="sxs-lookup"><span data-stu-id="b738b-116">Be careful with NOT operations.</span></span> <span data-ttu-id="b738b-117">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="b738b-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="b738b-118">Проблема заключается в том, что ~ (b – 1) создает "Символ 0x0000 0000 XXXX XXXX", а не "0xFFFF FFFF XXXX XXXX".</span><span class="sxs-lookup"><span data-stu-id="b738b-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="b738b-119">Компилятор не определит это.</span><span class="sxs-lookup"><span data-stu-id="b738b-119">The compiler will not detect this.</span></span> <span data-ttu-id="b738b-120">Чтобы устранить эту проблему, измените код следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b738b-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="b738b-121">Будьте внимательны при выполнении неподписанных и подписанных операций.</span><span class="sxs-lookup"><span data-stu-id="b738b-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="b738b-122">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="b738b-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="b738b-123">Результат неожиданно большой.</span><span class="sxs-lookup"><span data-stu-id="b738b-123">The result is unexpectedly large.</span></span> <span data-ttu-id="b738b-124">Правило заключается в том, что если любой из операндов не имеет знака, результат будет неподписанным.</span><span class="sxs-lookup"><span data-stu-id="b738b-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="b738b-125">В предыдущем примере выражение преобразуется в значение без знака, разделенное на b, и результат, хранящийся в c.</span><span class="sxs-lookup"><span data-stu-id="b738b-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="b738b-126">Преобразование не требует числовой обработки.</span><span class="sxs-lookup"><span data-stu-id="b738b-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="b738b-127">В качестве другого примера рассмотрим следующее.</span><span class="sxs-lookup"><span data-stu-id="b738b-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="b738b-128">Проблема возникает, поскольку x не подписан, что делает все выражение неподписанным.</span><span class="sxs-lookup"><span data-stu-id="b738b-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="b738b-129">Это подходит, если y не является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="b738b-129">This works fine unless y is negative.</span></span> <span data-ttu-id="b738b-130">В этом случае y преобразуется в значение без знака, выражение вычисляется с использованием 32-разрядной точности, масштабируется и добавляется в pVar1.</span><span class="sxs-lookup"><span data-stu-id="b738b-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="b738b-131">32-разрядное отрицательное число без знака преобразуется в большое 64-разрядное положительное число, которое дает неверный результат.</span><span class="sxs-lookup"><span data-stu-id="b738b-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="b738b-132">Чтобы устранить эту проблему, объявите x как значение со знаком или явно присвоить его **Long** в выражении.</span><span class="sxs-lookup"><span data-stu-id="b738b-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="b738b-133">Будьте внимательны при выделении распределения размера поэтапного выполнения.</span><span class="sxs-lookup"><span data-stu-id="b738b-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="b738b-134">Пример:</span><span class="sxs-lookup"><span data-stu-id="b738b-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="b738b-135">Следующий код является неправильным, так как компилятор будет размещает структуру с дополнительными 4 байтами для создания 8-байтового выравнивания:</span><span class="sxs-lookup"><span data-stu-id="b738b-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="b738b-136">Следующий код правильный:</span><span class="sxs-lookup"><span data-stu-id="b738b-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="b738b-137">Не передавайте `(HANDLE)0xFFFFFFFF` в такие функции, как [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span><span class="sxs-lookup"><span data-stu-id="b738b-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="b738b-138">Вместо этого используйте **недопустимое \_ \_ значение Handle**.</span><span class="sxs-lookup"><span data-stu-id="b738b-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="b738b-139">При печати строки используйте правильные описатели формата.</span><span class="sxs-lookup"><span data-stu-id="b738b-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="b738b-140">Используйте% p для печати указателей в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="b738b-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="b738b-141">Это лучший вариант для печати указателей.</span><span class="sxs-lookup"><span data-stu-id="b738b-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="b738b-142">Microsoft Visual C++ поддерживает% I для печати данных в виде полиморфизма.</span><span class="sxs-lookup"><span data-stu-id="b738b-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="b738b-143">Visual C++ также поддерживает% I64 для печати значений 64 бит.</span><span class="sxs-lookup"><span data-stu-id="b738b-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 