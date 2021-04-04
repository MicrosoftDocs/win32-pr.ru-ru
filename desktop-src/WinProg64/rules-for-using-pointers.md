---
title: Правила использования указателей
description: Перенос кода для компиляции как 32, так и 64-разрядной версии Microsoft Windows выполняется очень просто. Необходимо выполнить только несколько простых правил для указателей приведения и использовать новые типы данных в коде. Ниже приведены правила обработки указателей.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- Правила использования указателей в 64-разрядном программировании Windows
- Управление указателями 64-разрядное программирование для Windows
- указатели приведения 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103987954"
---
# <a name="rules-for-using-pointers"></a><span data-ttu-id="b31d7-108">Правила использования указателей</span><span class="sxs-lookup"><span data-stu-id="b31d7-108">Rules for Using Pointers</span></span>

<span data-ttu-id="b31d7-109">Перенос кода для компиляции как 32, так и 64-разрядной версии Microsoft Windows выполняется очень просто.</span><span class="sxs-lookup"><span data-stu-id="b31d7-109">Porting your code to compile for both 32- and 64-bit Microsoft Windows is straightforward.</span></span> <span data-ttu-id="b31d7-110">Необходимо выполнить только несколько простых правил для указателей приведения и использовать новые типы данных в коде.</span><span class="sxs-lookup"><span data-stu-id="b31d7-110">You need only follow a few simple rules about casting pointers, and use the new data types in your code.</span></span> <span data-ttu-id="b31d7-111">Ниже приведены правила обработки указателей.</span><span class="sxs-lookup"><span data-stu-id="b31d7-111">The rules for pointer manipulation are as follows.</span></span>

1.  <span data-ttu-id="b31d7-112">Не выведите указатели на **int**, **Long**, **ulong** или **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b31d7-112">Do not cast pointers to **int**, **long**, **ULONG**, or **DWORD**.</span></span>

    <span data-ttu-id="b31d7-113">Если необходимо привести указатель для проверки некоторых битов, задать или очистить биты или иным образом манипулировать его содержимым, используйте тип данных **uint \_ ptr** или **int \_** PTR.</span><span class="sxs-lookup"><span data-stu-id="b31d7-113">If you must cast a pointer to test some bits, set or clear bits, or otherwise manipulate its contents, use the **UINT\_PTR** or **INT\_PTR** type.</span></span> <span data-ttu-id="b31d7-114">Эти типы являются целочисленными типами, которые масштабируются до размера указателя для 32 и 64-разрядных окон (например, **ulong** для 32-bit Windows и \_ Int64 для 64-bit Windows).</span><span class="sxs-lookup"><span data-stu-id="b31d7-114">These types are integral types that scale to the size of a pointer for both 32- and 64-bit Windows (for example, **ULONG** for 32-bit Windows and \_int64 for 64-bit Windows).</span></span> <span data-ttu-id="b31d7-115">Например, предположим, что выполняется перенос следующего кода:</span><span class="sxs-lookup"><span data-stu-id="b31d7-115">For example, assume you are porting the following code:</span></span>

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    <span data-ttu-id="b31d7-116">В рамках процесса переноса вы измените код следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b31d7-116">As a part of the porting process, you would change the code as follows:</span></span>

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    <span data-ttu-id="b31d7-117">Используйте **uint \_ ptr** и **int \_ ptr** там, где это необходимо (и если вы не уверены, являются ли они обязательными, их использование будет невозможным в случае).</span><span class="sxs-lookup"><span data-stu-id="b31d7-117">Use **UINT\_PTR** and **INT\_PTR** where appropriate (and if you are uncertain whether they are required, there is no harm in using them just in case).</span></span> <span data-ttu-id="b31d7-118">Не приведите указатели к типам **ulong**, **Long**, **int**, **uint** или **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b31d7-118">Do not cast your pointers to the types **ULONG**, **LONG**, **INT**, **UINT**, or **DWORD**.</span></span>

    <span data-ttu-id="b31d7-119">Обратите внимание, что **Handle** определяется **как \* void**, поэтому приведение значения **Handle** к значению типа **ulong** для проверки, установки или очистки младших разрядов в 64-разрядной системе является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b31d7-119">Note that **HANDLE** is defined as a **void\***, so typecasting a **HANDLE** value to a **ULONG** value to test, set, or clear the low-order 2 bits is an error on 64-bit Windows.</span></span>

2.  <span data-ttu-id="b31d7-120">Используйте функцию **птртолонг** или **птртаулонг** для усечения указателей.</span><span class="sxs-lookup"><span data-stu-id="b31d7-120">Use the **PtrToLong** or **PtrToUlong** function to truncate pointers.</span></span>

    <span data-ttu-id="b31d7-121">Если необходимо усечь указатель до 32-разрядного значения, используйте функцию **птртолонг** или **птртаулонг** (определенную в басетсд. h).</span><span class="sxs-lookup"><span data-stu-id="b31d7-121">If you must truncate a pointer to a 32-bit value, use the **PtrToLong** or **PtrToUlong** function (defined in Basetsd.h).</span></span> <span data-ttu-id="b31d7-122">Эти функции отключают предупреждение об усечении указателя на время вызова.</span><span class="sxs-lookup"><span data-stu-id="b31d7-122">These functions disable the pointer truncation warning for the duration of the call.</span></span>

    <span data-ttu-id="b31d7-123">Используйте эти функции внимательно.</span><span class="sxs-lookup"><span data-stu-id="b31d7-123">Use these functions carefully.</span></span> <span data-ttu-id="b31d7-124">После преобразования переменной указателя с помощью одной из этих функций никогда не используйте ее в качестве указателя.</span><span class="sxs-lookup"><span data-stu-id="b31d7-124">After you convert a pointer variable using one of these functions, never use it as a pointer again.</span></span> <span data-ttu-id="b31d7-125">Эти функции усекаются верхние 32 бит адреса, которые обычно требуются для доступа к памяти, на которую ссылается указатель.</span><span class="sxs-lookup"><span data-stu-id="b31d7-125">These functions truncate the upper 32 bits of an address, which are usually needed to access the memory originally referenced by pointer.</span></span> <span data-ttu-id="b31d7-126">Использование этих функций без тщательного рассмотрения приводит к ненадежному коду.</span><span class="sxs-lookup"><span data-stu-id="b31d7-126">Using these functions without careful consideration will result in fragile code.</span></span>

3.  <span data-ttu-id="b31d7-127">Будьте внимательны при использовании \_ значений указателя 32 в коде, который может быть скомпилирован в виде 64-разрядного кода.</span><span class="sxs-lookup"><span data-stu-id="b31d7-127">Be careful when using POINTER\_32 values in code that may be compiled as 64-bit code.</span></span> <span data-ttu-id="b31d7-128">Компилятор будет расширять указатель, когда он назначается собственному указателю в 64-разрядном коде, а указатель не расширяется без нуля.</span><span class="sxs-lookup"><span data-stu-id="b31d7-128">The compiler will sign-extend the pointer when it is assigned to a native pointer in 64-bit code, not zero-extend the pointer.</span></span>
4.  <span data-ttu-id="b31d7-129">Будьте внимательны при использовании \_ значений указателя 64 в коде, который может быть скомпилирован в виде 32-разрядного кода.</span><span class="sxs-lookup"><span data-stu-id="b31d7-129">Be careful when using POINTER\_64 values in code that may be compiled as 32-bit code.</span></span> <span data-ttu-id="b31d7-130">Компилятор будет расширять указатель в 32-разрядном коде, не расширяя указатель на ноль.</span><span class="sxs-lookup"><span data-stu-id="b31d7-130">The compiler will sign-extend the pointer in 32-bit code, not zero-extend the pointer.</span></span>
5.  <span data-ttu-id="b31d7-131">Будьте внимательны при использовании параметров OUT.</span><span class="sxs-lookup"><span data-stu-id="b31d7-131">Be careful using OUT parameters.</span></span>

    <span data-ttu-id="b31d7-132">Например, предположим, что имеется функция, определенная следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b31d7-132">For example, suppose you have a function defined as follows:</span></span>

    `void func( OUT PULONG *PointerToUlong );`

    <span data-ttu-id="b31d7-133">Не вызывайте эту функцию, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b31d7-133">Do not call this function as follows.</span></span>

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    <span data-ttu-id="b31d7-134">Вместо этого используйте следующий вызов.</span><span class="sxs-lookup"><span data-stu-id="b31d7-134">Instead, use the following call.</span></span>

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    <span data-ttu-id="b31d7-135">Приведение &UL к **пулонг \*** предотвращает ошибку компилятора, но функция будет записывать 64-битное значение указателя в память в &UL.</span><span class="sxs-lookup"><span data-stu-id="b31d7-135">Typecasting &ul to **PULONG\*** prevents a compiler error, but the function will write a 64-bit pointer value into the memory at &ul.</span></span> <span data-ttu-id="b31d7-136">Этот код работает в 32-разрядной Windows, но приведет к повреждению данных в 64-разрядной версии Windows, и это будет заметное повреждение.</span><span class="sxs-lookup"><span data-stu-id="b31d7-136">This code works on 32-bit Windows, but will cause data corruption on 64-bit Windows and it will be subtle, hard-to-find corruption.</span></span> <span data-ttu-id="b31d7-137">Нижняя строка: не воспроизводить взятия с помощью кода C — простой и простой — лучше.</span><span class="sxs-lookup"><span data-stu-id="b31d7-137">The bottom line: Do not play tricks with the C code—straightforward and simple is better.</span></span>

6.  <span data-ttu-id="b31d7-138">Будьте внимательны с использованием интерфейсов с полиморфизмом.</span><span class="sxs-lookup"><span data-stu-id="b31d7-138">Be careful with polymorphic interfaces.</span></span>

    <span data-ttu-id="b31d7-139">Не создавайте функции, которые принимают параметры **DWORD** для данных с преформациюми.</span><span class="sxs-lookup"><span data-stu-id="b31d7-139">Do not create functions that accept **DWORD** parameters for polymorphic data.</span></span> <span data-ttu-id="b31d7-140">Если данные могут быть указателями или целочисленными значениями, используйте \_ Тип uint PTR или **PVOID** .</span><span class="sxs-lookup"><span data-stu-id="b31d7-140">If the data can be a pointer or an integral value, use the UINT\_PTR or **PVOID** type.</span></span>

    <span data-ttu-id="b31d7-141">Например, не следует создавать функцию, которая принимает массив параметров исключений, типизированных как значения **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b31d7-141">For example, do not create a function that accepts an array of exception parameters typed as **DWORD** values.</span></span> <span data-ttu-id="b31d7-142">Массив должен быть массивом значений типа **DWORD \_** .</span><span class="sxs-lookup"><span data-stu-id="b31d7-142">The array should be an array of **DWORD\_PTR** values.</span></span> <span data-ttu-id="b31d7-143">Таким образом, элементы массива могут содержать адреса или 32-разрядные целочисленные значения.</span><span class="sxs-lookup"><span data-stu-id="b31d7-143">Therefore, the array elements can hold addresses or 32-bit integral values.</span></span> <span data-ttu-id="b31d7-144">(Общее правило состоит в том, что если исходный тип — **DWORD** , и он должен быть шириной указателя, преобразуйте его в значение **типа DWORD \_** .</span><span class="sxs-lookup"><span data-stu-id="b31d7-144">(The general rule is that if the original type is **DWORD** and it needs to be pointer width, convert it to a **DWORD\_PTR** value.</span></span> <span data-ttu-id="b31d7-145">Именно поэтому существуют соответствующие типы точности указателей.) Если у вас есть код, который использует **DWORD**, **ULONG** или другие 32-разрядные типы в полиморфизме (то есть необходимо, чтобы параметр или член структуры содержал адрес), используйте **uint \_ ptr** вместо текущего типа.</span><span class="sxs-lookup"><span data-stu-id="b31d7-145">That is why there are corresponding pointer-precision types.) If you have code that uses **DWORD**, **ULONG**, or other 32-bit types in a polymorphic way (that is, you really want the parameter or structure member to hold an address), use **UINT\_PTR** in place of the current type.</span></span>

7.  <span data-ttu-id="b31d7-146">Используйте новые функции класса Window.</span><span class="sxs-lookup"><span data-stu-id="b31d7-146">Use the new window class functions.</span></span>

    <span data-ttu-id="b31d7-147">Если у вас есть закрытые данные окон или классов, содержащие указатели, в коде потребуется использовать следующие новые функции:</span><span class="sxs-lookup"><span data-stu-id="b31d7-147">If you have window or class private data that contains pointers, your code will need to use the following new functions:</span></span>

    -   [<span data-ttu-id="b31d7-148">**жеткласслонгптр**</span><span class="sxs-lookup"><span data-stu-id="b31d7-148">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [<span data-ttu-id="b31d7-149">**жетвиндовлонгптр**</span><span class="sxs-lookup"><span data-stu-id="b31d7-149">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [<span data-ttu-id="b31d7-150">**сеткласслонгптр**</span><span class="sxs-lookup"><span data-stu-id="b31d7-150">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [<span data-ttu-id="b31d7-151">**сетвиндовлонгптр**</span><span class="sxs-lookup"><span data-stu-id="b31d7-151">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    <span data-ttu-id="b31d7-152">Эти функции можно использовать как в 32, так и в 64-разрядных Windows, но они необходимы для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="b31d7-152">These functions can be used on both 32- and 64-bit Windows, but they are required on 64-bit Windows.</span></span> <span data-ttu-id="b31d7-153">Подготовьтесь к переходу, используя эти функции сейчас.</span><span class="sxs-lookup"><span data-stu-id="b31d7-153">Prepare for the transition by using these functions now.</span></span>

    <span data-ttu-id="b31d7-154">Кроме того, необходимо обращаться к указателям или дескрипторам в закрытых данных класса с помощью новых функций в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="b31d7-154">Additionally, you must access pointers or handles in class private data using the new functions on 64-bit Windows.</span></span> <span data-ttu-id="b31d7-155">Чтобы помочь вам найти эти случаи, следующие индексы не определяются в файле WinUser. h во время компиляции 64-bit:</span><span class="sxs-lookup"><span data-stu-id="b31d7-155">To aid you in finding these cases, the following indexes are not defined in Winuser.h during a 64-bit compile:</span></span>

    -   <span data-ttu-id="b31d7-156">ГВЛ \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="b31d7-156">GWL\_WNDPROC</span></span>
    -   <span data-ttu-id="b31d7-157">ГВЛ \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="b31d7-157">GWL\_HINSTANCE</span></span>
    -   <span data-ttu-id="b31d7-158">ГВЛ \_ хвдпарент</span><span class="sxs-lookup"><span data-stu-id="b31d7-158">GWL\_HWDPARENT</span></span>
    -   <span data-ttu-id="b31d7-159">ГВЛый \_ USERDATA</span><span class="sxs-lookup"><span data-stu-id="b31d7-159">GWL\_USERDATA</span></span>

    <span data-ttu-id="b31d7-160">Вместо этого Winuser. h определяет следующие новые индексы:</span><span class="sxs-lookup"><span data-stu-id="b31d7-160">Instead, Winuser.h defines the following new indexes:</span></span>

    -   <span data-ttu-id="b31d7-161">ГВЛП \_ WndProc</span><span class="sxs-lookup"><span data-stu-id="b31d7-161">GWLP\_WNDPROC</span></span>
    -   <span data-ttu-id="b31d7-162">ГВЛП \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="b31d7-162">GWLP\_HINSTANCE</span></span>
    -   <span data-ttu-id="b31d7-163">ГВЛП \_ хвндпарент</span><span class="sxs-lookup"><span data-stu-id="b31d7-163">GWLP\_HWNDPARENT</span></span>
    -   <span data-ttu-id="b31d7-164">ГВЛПый \_ USERDATA</span><span class="sxs-lookup"><span data-stu-id="b31d7-164">GWLP\_USERDATA</span></span>
    -   <span data-ttu-id="b31d7-165">\_идентификатор гвлп</span><span class="sxs-lookup"><span data-stu-id="b31d7-165">GWLP\_ID</span></span>

    <span data-ttu-id="b31d7-166">Например, следующий код не компилирует:</span><span class="sxs-lookup"><span data-stu-id="b31d7-166">For example, the following code does not compile:</span></span>

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    <span data-ttu-id="b31d7-167">Его следует изменить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b31d7-167">It should be changed as follows:</span></span>

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    <span data-ttu-id="b31d7-168">При задании элемента **кбвндекстра** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) необходимо зарезервировать достаточно места для указателей.</span><span class="sxs-lookup"><span data-stu-id="b31d7-168">When setting the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure, be sure to reserve enough space for pointers.</span></span> <span data-ttu-id="b31d7-169">Например, если в настоящее время выполняется резервирование значения параметра sizeof (DWORD) для указателя, то Зарезервируйте значение в \_ байтах sizeof (DWORD PTR).</span><span class="sxs-lookup"><span data-stu-id="b31d7-169">For example, if you are currently reserving sizeof(DWORD) bytes for a pointer value, reserve sizeof(DWORD\_PTR) bytes.</span></span>

8.  <span data-ttu-id="b31d7-170">Доступ ко всем данным окон и классов с помощью **\_ смещения поля**.</span><span class="sxs-lookup"><span data-stu-id="b31d7-170">Access all window and class data using **FIELD\_OFFSET**.</span></span>

    <span data-ttu-id="b31d7-171">Обычно доступ к данным окна осуществляется с помощью жестко заданных смещений.</span><span class="sxs-lookup"><span data-stu-id="b31d7-171">It is common to access window data using hard-coded offsets.</span></span> <span data-ttu-id="b31d7-172">Эта методика не переносима на 64-разрядную версию Windows.</span><span class="sxs-lookup"><span data-stu-id="b31d7-172">This technique is not portable to 64-bit Windows.</span></span> <span data-ttu-id="b31d7-173">Чтобы сделать код переносимым, получите доступ к данным окна и класса с помощью макроса **\_ смещения поля** .</span><span class="sxs-lookup"><span data-stu-id="b31d7-173">To make your code portable, access your window and class data using the **FIELD\_OFFSET** macro.</span></span> <span data-ttu-id="b31d7-174">Не считайте, что второй указатель имеет смещение 4.</span><span class="sxs-lookup"><span data-stu-id="b31d7-174">Do not assume that the second pointer has an offset of 4.</span></span>

9.  <span data-ttu-id="b31d7-175">Типы **lParam**, **wParam** и **lResult** изменяют размер вместе с платформой.</span><span class="sxs-lookup"><span data-stu-id="b31d7-175">The **LPARAM**, **WPARAM**, and **LRESULT** types change size with the platform.</span></span>

    <span data-ttu-id="b31d7-176">При компиляции 64-разрядного кода эти типы расширяются до 64 бит, так как они обычно содержат указатели или целочисленные типы.</span><span class="sxs-lookup"><span data-stu-id="b31d7-176">When compiling 64-bit code, these types expand to 64 bits, because they typically hold pointers or integral types.</span></span> <span data-ttu-id="b31d7-177">Не следует смешивать эти значения с **DWORD**, **ulong**, **uint**, **int**, **int** или **Long** .</span><span class="sxs-lookup"><span data-stu-id="b31d7-177">Do not mix these values with **DWORD**, **ULONG**, **UINT**, **INT**, **int**, or **long** values.</span></span> <span data-ttu-id="b31d7-178">Изучите использование этих типов и убедитесь, что значения не были случайно усечены.</span><span class="sxs-lookup"><span data-stu-id="b31d7-178">Examine how you use these types and ensure that you do not inadvertently truncate values.</span></span>

 

 