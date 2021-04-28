---
title: Обработка ошибок в COM (начало работы с Win32 и C++)
description: Обработка ошибок в COM (начало работы с Win32 и C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103922"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a><span data-ttu-id="8a66d-103">Обработка ошибок в COM (начало работы с Win32 и C++)</span><span class="sxs-lookup"><span data-stu-id="8a66d-103">Error Handling in COM (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="8a66d-104">COM использует значения **HRESULT** для указания на успешное или неуспешное завершение метода или вызова функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-104">COM uses **HRESULT** values to indicate the success or failure of a method or function call.</span></span> <span data-ttu-id="8a66d-105">Различные заголовки SDK определяют различные константы **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a66d-105">Various SDK headers define various **HRESULT** constants.</span></span> <span data-ttu-id="8a66d-106">Общий набор кодов на уровне системы определяется в файле WinError. h.</span><span class="sxs-lookup"><span data-stu-id="8a66d-106">A common set of system-wide codes is defined in WinError.h.</span></span> <span data-ttu-id="8a66d-107">В следующей таблице показаны некоторые коды возврата для всей системы.</span><span class="sxs-lookup"><span data-stu-id="8a66d-107">The following table shows some of those system-wide return codes.</span></span>



| <span data-ttu-id="8a66d-108">Константа</span><span class="sxs-lookup"><span data-stu-id="8a66d-108">Constant</span></span>            | <span data-ttu-id="8a66d-109">Числовое значение</span><span class="sxs-lookup"><span data-stu-id="8a66d-109">Numeric value</span></span> | <span data-ttu-id="8a66d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8a66d-110">Description</span></span>                                          |
|---------------------|---------------|------------------------------------------------------|
| <span data-ttu-id="8a66d-111">**E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="8a66d-111">**E\_ACCESSDENIED**</span></span> | <span data-ttu-id="8a66d-112">0x80070005</span><span class="sxs-lookup"><span data-stu-id="8a66d-112">0x80070005</span></span>    | <span data-ttu-id="8a66d-113">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="8a66d-113">Access denied.</span></span>                                       |
| <span data-ttu-id="8a66d-114">**\_Ошибка E**</span><span class="sxs-lookup"><span data-stu-id="8a66d-114">**E\_FAIL**</span></span>         | <span data-ttu-id="8a66d-115">0x80004005</span><span class="sxs-lookup"><span data-stu-id="8a66d-115">0x80004005</span></span>    | <span data-ttu-id="8a66d-116">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8a66d-116">Unspecified error.</span></span>                                   |
| <span data-ttu-id="8a66d-117">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="8a66d-117">**E\_INVALIDARG**</span></span>   | <span data-ttu-id="8a66d-118">0x80070057</span><span class="sxs-lookup"><span data-stu-id="8a66d-118">0x80070057</span></span>    | <span data-ttu-id="8a66d-119">Недопустимое значение параметра.</span><span class="sxs-lookup"><span data-stu-id="8a66d-119">Invalid parameter value.</span></span>                             |
| <span data-ttu-id="8a66d-120">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="8a66d-120">**E\_OUTOFMEMORY**</span></span>  | <span data-ttu-id="8a66d-121">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="8a66d-121">0x8007000E</span></span>    | <span data-ttu-id="8a66d-122">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="8a66d-122">Out of memory.</span></span>                                       |
| <span data-ttu-id="8a66d-123">**\_указатель E**</span><span class="sxs-lookup"><span data-stu-id="8a66d-123">**E\_POINTER**</span></span>      | <span data-ttu-id="8a66d-124">0x80004003</span><span class="sxs-lookup"><span data-stu-id="8a66d-124">0x80004003</span></span>    | <span data-ttu-id="8a66d-125">Значение **null** передано неверно для значения указателя.</span><span class="sxs-lookup"><span data-stu-id="8a66d-125">**NULL** was passed incorrectly for a pointer value.</span></span> |
| <span data-ttu-id="8a66d-126">**\_непредвиденная E**</span><span class="sxs-lookup"><span data-stu-id="8a66d-126">**E\_UNEXPECTED**</span></span>   | <span data-ttu-id="8a66d-127">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="8a66d-127">0x8000FFFF</span></span>    | <span data-ttu-id="8a66d-128">Непредвиденное условие.</span><span class="sxs-lookup"><span data-stu-id="8a66d-128">Unexpected condition.</span></span>                                |
| <span data-ttu-id="8a66d-129">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="8a66d-129">**S\_OK**</span></span>           | <span data-ttu-id="8a66d-130">0x0</span><span class="sxs-lookup"><span data-stu-id="8a66d-130">0x0</span></span>           | <span data-ttu-id="8a66d-131">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8a66d-131">Success.</span></span>                                             |
| <span data-ttu-id="8a66d-132">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="8a66d-132">**S\_FALSE**</span></span>        | <span data-ttu-id="8a66d-133">0x1</span><span class="sxs-lookup"><span data-stu-id="8a66d-133">0x1</span></span>           | <span data-ttu-id="8a66d-134">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8a66d-134">Success.</span></span>                                             |



 

<span data-ttu-id="8a66d-135">Все константы с префиксом "E \_ " являются кодами ошибок.</span><span class="sxs-lookup"><span data-stu-id="8a66d-135">All of the constants with the prefix "E\_" are error codes.</span></span> <span data-ttu-id="8a66d-136">Константы **s \_ OK** и **\_ false** имеют оба кода успеха.</span><span class="sxs-lookup"><span data-stu-id="8a66d-136">The constants **S\_OK** and **S\_FALSE** are both success codes.</span></span> <span data-ttu-id="8a66d-137">Вероятно, 99% методов COM возвращают **S \_ ОК** , когда они успешны, но не позволяют этому факту выдать себя.</span><span class="sxs-lookup"><span data-stu-id="8a66d-137">Probably 99% of COM methods return **S\_OK** when they succeed; but do not let this fact mislead you.</span></span> <span data-ttu-id="8a66d-138">Метод может вернуть другие коды успеха, поэтому всегда проверяйте наличие ошибок с помощью макроса Success [**или**](/windows/desktop/api/winerror/nf-winerror-succeeded) [**Failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="8a66d-138">A method might return other success codes, so always test for errors by using the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) or [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="8a66d-139">В следующем примере кода показан неправильный способ и правильный способ проверки успеха вызова функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-139">The following example code shows the wrong way and the right way to test for the success of a function call.</span></span>


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



<span data-ttu-id="8a66d-140">Код успеха " **\_ false** " заслуживает упоминания.</span><span class="sxs-lookup"><span data-stu-id="8a66d-140">The success code **S\_FALSE** deserves mention.</span></span> <span data-ttu-id="8a66d-141">Некоторые методы используют **\_ значение false** для среднего, приблизительного, отрицательного условия, которое не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8a66d-141">Some methods use **S\_FALSE** to mean, roughly, a negative condition that is not a failure.</span></span> <span data-ttu-id="8a66d-142">Он также может указывать на отсутствие операции — метод прошел, но не действовал.</span><span class="sxs-lookup"><span data-stu-id="8a66d-142">It can also indicate a "no-op"—the method succeeded, but had no effect.</span></span> <span data-ttu-id="8a66d-143">Например, функция [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) возвращает **\_ значение S false** , если вы вызываете его второй раз из того же потока.</span><span class="sxs-lookup"><span data-stu-id="8a66d-143">For example, the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function returns **S\_FALSE** if you call it a second time from the same thread.</span></span> <span data-ttu-id="8a66d-144">Если необходимо отличить значения от **s \_ ОК** и **s \_ false** в коде, следует протестировать значение напрямую, но по-прежнему использовать [**неудачные**](/windows/desktop/api/winerror/nf-winerror-failed) или [**успешные**](/windows/desktop/api/winerror/nf-winerror-succeeded) операции для решения оставшихся вариантов, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="8a66d-144">If you need to differentiate between **S\_OK** and **S\_FALSE** in your code, you should test the value directly, but still use [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) or [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) to handle the remaining cases, as shown in the following example code.</span></span>


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



<span data-ttu-id="8a66d-145">Некоторые значения **HRESULT** относятся к определенной функции или подсистеме Windows.</span><span class="sxs-lookup"><span data-stu-id="8a66d-145">Some **HRESULT** values are specific to a particular feature or subsystem of Windows.</span></span> <span data-ttu-id="8a66d-146">Например, графический API Direct2D определяет код ошибки **D2DERR \_ неподдерживаемый \_ \_ Формат пикселей**, то есть программа использовала неподдерживаемый формат пикселей.</span><span class="sxs-lookup"><span data-stu-id="8a66d-146">For example, the Direct2D graphics API defines the error code **D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**, which means that the program used an unsupported pixel format.</span></span> <span data-ttu-id="8a66d-147">В документации MSDN часто содержится список конкретных кодов ошибок, которые может возвращать метод.</span><span class="sxs-lookup"><span data-stu-id="8a66d-147">MSDN documentation often gives a list of specific error codes that a method might return.</span></span> <span data-ttu-id="8a66d-148">Однако не следует думать о том, чтобы эти списки были обвышены.</span><span class="sxs-lookup"><span data-stu-id="8a66d-148">However, you should not consider these lists to be definitive.</span></span> <span data-ttu-id="8a66d-149">Метод всегда может возвращать значение **HRESULT** , не указанное в документации.</span><span class="sxs-lookup"><span data-stu-id="8a66d-149">A method can always return an **HRESULT** value that is not listed in the documentation.</span></span> <span data-ttu-id="8a66d-150">Опять же, используйте макросы [**успешно**](/windows/desktop/api/winerror/nf-winerror-succeeded) и [**Failed**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="8a66d-150">Again, use the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macros.</span></span> <span data-ttu-id="8a66d-151">Если вы тестируете конкретный код ошибки, включите также вариант по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a66d-151">If you test for a specific error code, include a default case as well.</span></span>


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a><span data-ttu-id="8a66d-152">Шаблоны для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="8a66d-152">Patterns for Error Handling</span></span>

<span data-ttu-id="8a66d-153">В этом разделе рассматриваются некоторые закономерности обработки ошибок COM в структурированном виде.</span><span class="sxs-lookup"><span data-stu-id="8a66d-153">This section looks at some patterns for handling COM errors in a structured way.</span></span> <span data-ttu-id="8a66d-154">Каждый шаблон имеет свои преимущества и недостатки.</span><span class="sxs-lookup"><span data-stu-id="8a66d-154">Each pattern has advantages and disadvantages.</span></span> <span data-ttu-id="8a66d-155">В некоторой степени, по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="8a66d-155">To some extent, the choice is a matter of taste.</span></span> <span data-ttu-id="8a66d-156">Если вы работаете над существующим проектом, возможно, у него уже есть рекомендации по написанию кода, проскрибе определенный стиль.</span><span class="sxs-lookup"><span data-stu-id="8a66d-156">If you work on an existing project, it might already have coding guidelines that proscribe a particular style.</span></span> <span data-ttu-id="8a66d-157">Независимо от выбранного шаблона надежный код будет следовать следующим правилам.</span><span class="sxs-lookup"><span data-stu-id="8a66d-157">Regardless of which pattern you adopt, robust code will obey the following rules.</span></span>

-   <span data-ttu-id="8a66d-158">Для каждого метода или функции, возвращающей **HRESULT**, проверьте возвращаемое значение перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="8a66d-158">For every method or function that returns an **HRESULT**, check the return value before proceeding.</span></span>
-   <span data-ttu-id="8a66d-159">Освободите ресурсы после их использования.</span><span class="sxs-lookup"><span data-stu-id="8a66d-159">Release resources after they are used.</span></span>
-   <span data-ttu-id="8a66d-160">Не пытайтесь получить доступ к недопустимым или неинициализированным ресурсам, таким как указатели **null** .</span><span class="sxs-lookup"><span data-stu-id="8a66d-160">Do not attempt to access invalid or uninitialized resources, such as **NULL** pointers.</span></span>
-   <span data-ttu-id="8a66d-161">Не пытайтесь использовать ресурс после его выпуска.</span><span class="sxs-lookup"><span data-stu-id="8a66d-161">Do not try to use a resource after you release it.</span></span>

<span data-ttu-id="8a66d-162">Учитывая эти правила, вот четыре шаблона обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="8a66d-162">With these rules in mind, here are four patterns for handling errors.</span></span>

-   [<span data-ttu-id="8a66d-163">Вложенная IFS</span><span class="sxs-lookup"><span data-stu-id="8a66d-163">Nested ifs</span></span>](#nested-ifs)
-   [<span data-ttu-id="8a66d-164">Каскадная IFS</span><span class="sxs-lookup"><span data-stu-id="8a66d-164">Cascading ifs</span></span>](#cascading-ifs)
-   [<span data-ttu-id="8a66d-165">Сбой перехода</span><span class="sxs-lookup"><span data-stu-id="8a66d-165">Jump on Fail</span></span>](#jump-on-fail)
-   [<span data-ttu-id="8a66d-166">Выдать ошибку при сбое</span><span class="sxs-lookup"><span data-stu-id="8a66d-166">Throw on Fail</span></span>](#throw-on-fail)

### <a name="nested-ifs"></a><span data-ttu-id="8a66d-167">Вложенная IFS</span><span class="sxs-lookup"><span data-stu-id="8a66d-167">Nested ifs</span></span>

<span data-ttu-id="8a66d-168">После каждого вызова, возвращающего **значение HRESULT**, используйте оператор **If** для проверки успешности.</span><span class="sxs-lookup"><span data-stu-id="8a66d-168">After every call that returns an **HRESULT**, use an **if** statement to test for success.</span></span> <span data-ttu-id="8a66d-169">Затем вставьте следующий вызов метода в область оператора **If** .</span><span class="sxs-lookup"><span data-stu-id="8a66d-169">Then, put the next method call within the scope of the **if** statement.</span></span> <span data-ttu-id="8a66d-170">Другие операторы **If** могут быть вложенными при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8a66d-170">More **if** statements can be nested as deeply as needed.</span></span> <span data-ttu-id="8a66d-171">В предыдущих примерах кода в этом модуле используется этот шаблон, но это еще раз:</span><span class="sxs-lookup"><span data-stu-id="8a66d-171">The previous code examples in this module have all used this pattern, but here it is again:</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



<span data-ttu-id="8a66d-172">Преимущества</span><span class="sxs-lookup"><span data-stu-id="8a66d-172">Advantages</span></span>

-   <span data-ttu-id="8a66d-173">Переменные могут быть объявлены с минимальной областью действия.</span><span class="sxs-lookup"><span data-stu-id="8a66d-173">Variables can be declared with minimal scope.</span></span> <span data-ttu-id="8a66d-174">Например, *питем* не объявлен до тех пор, пока не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="8a66d-174">For example, *pItem* is not declared until it is used.</span></span>
-   <span data-ttu-id="8a66d-175">В каждом операторе **If** некоторые инварианты имеют значение true: все предыдущие вызовы успешно выполнены, и все полученные ресурсы остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="8a66d-175">Within each **if** statement, certain invariants are true: All previous calls have succeeded, and all acquired resources are still valid.</span></span> <span data-ttu-id="8a66d-176">В предыдущем примере, когда программа достигает самого внутреннего оператора **If** , известно, что оба *питем* и *пфилеопен* являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="8a66d-176">In the previous example, when the program reaches the innermost **if** statement, both *pItem* and *pFileOpen* are known to be valid.</span></span>
-   <span data-ttu-id="8a66d-177">Ясно, когда следует освобождать указатели интерфейса и другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="8a66d-177">It is clear when to release interface pointers and other resources.</span></span> <span data-ttu-id="8a66d-178">Ресурс освобождается в конце оператора **If** , который сразу же следует за вызовом, получившим ресурс.</span><span class="sxs-lookup"><span data-stu-id="8a66d-178">You release a resource at the end of the **if** statement that immediately follows the call that acquired the resource.</span></span>

<span data-ttu-id="8a66d-179">Недостатки</span><span class="sxs-lookup"><span data-stu-id="8a66d-179">Disadvantages</span></span>

-   <span data-ttu-id="8a66d-180">Некоторые люди находят глубокое вложение, сложное для чтения.</span><span class="sxs-lookup"><span data-stu-id="8a66d-180">Some people find deep nesting hard to read.</span></span>
-   <span data-ttu-id="8a66d-181">Обработка ошибок в сочетании с другими операторами ветвления и циклом.</span><span class="sxs-lookup"><span data-stu-id="8a66d-181">Error handling is mixed in with other branching and looping statements.</span></span> <span data-ttu-id="8a66d-182">Это может усложнить создание всей логики программы.</span><span class="sxs-lookup"><span data-stu-id="8a66d-182">This can make the overall program logic harder to follow.</span></span>

### <a name="cascading-ifs"></a><span data-ttu-id="8a66d-183">Каскадная IFS</span><span class="sxs-lookup"><span data-stu-id="8a66d-183">Cascading ifs</span></span>

<span data-ttu-id="8a66d-184">После каждого вызова метода используйте оператор **If** для проверки успешности.</span><span class="sxs-lookup"><span data-stu-id="8a66d-184">After each method call, use an **if** statement to test for success.</span></span> <span data-ttu-id="8a66d-185">Если метод выполняется, поместите вызов следующего метода внутри блока **If** .</span><span class="sxs-lookup"><span data-stu-id="8a66d-185">If the method succeeds, place the next method call inside the **if** block.</span></span> <span data-ttu-id="8a66d-186">Но вместо того, чтобы вложить последующие операторы **If** , поместите каждый последующий [**удачный**](/windows/desktop/api/winerror/nf-winerror-succeeded) тест после предыдущего блока **If** .</span><span class="sxs-lookup"><span data-stu-id="8a66d-186">But instead of nesting further **if** statements, place each subsequent [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) test after the previous **if** block.</span></span> <span data-ttu-id="8a66d-187">Если какой-либо из методов завершается ошибкой, все оставшиеся **успешно выполненные** тесты просто завершаются сбоем до тех пор, пока не будет достигнут конец функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-187">If any method fails, all the remaining **SUCCEEDED** tests simply fail until the bottom of the function is reached.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="8a66d-188">В этом шаблоне ресурсы освобождаются в самом конце функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-188">In this pattern, you release resources at the very end of the function.</span></span> <span data-ttu-id="8a66d-189">При возникновении ошибки некоторые указатели могут быть недопустимыми при выходе из функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-189">If an error occurs, some pointers might be invalid when the function exits.</span></span> <span data-ttu-id="8a66d-190">Вызов [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) на недопустимом указателе приведет к сбою программы (или хуже), поэтому необходимо инициализировать все указатели на **значение NULL** и проверить, не равны ли они **значению NULL** перед их освобождением.</span><span class="sxs-lookup"><span data-stu-id="8a66d-190">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on an invalid pointer will crash the program (or worse), so you must initialize all pointers to **NULL** and check whether they are **NULL** before releasing them.</span></span> <span data-ttu-id="8a66d-191">В этом примере используется `SafeRelease` функция; смарт-указатели также являются хорошим выбором.</span><span class="sxs-lookup"><span data-stu-id="8a66d-191">This example uses the `SafeRelease` function; smart pointers are also a good choice.</span></span>

<span data-ttu-id="8a66d-192">При использовании этого шаблона необходимо соблюдать осторожность при использовании циклических конструкций.</span><span class="sxs-lookup"><span data-stu-id="8a66d-192">If you use this pattern, you must be careful with loop constructs.</span></span> <span data-ttu-id="8a66d-193">В цикле прерывается в цикле, если происходит сбой любого вызова.</span><span class="sxs-lookup"><span data-stu-id="8a66d-193">Inside a loop, break from the loop if any call fails.</span></span>

<span data-ttu-id="8a66d-194">Преимущества</span><span class="sxs-lookup"><span data-stu-id="8a66d-194">Advantages</span></span>

-   <span data-ttu-id="8a66d-195">Этот шаблон создает меньше вложений, чем шаблон "Nested IFS".</span><span class="sxs-lookup"><span data-stu-id="8a66d-195">This pattern creates less nesting than the "nested ifs" pattern.</span></span>
-   <span data-ttu-id="8a66d-196">Общий поток управления более удобен для просмотра.</span><span class="sxs-lookup"><span data-stu-id="8a66d-196">Overall control flow is easier to see.</span></span>
-   <span data-ttu-id="8a66d-197">Ресурсы освобождаются в одной точке кода.</span><span class="sxs-lookup"><span data-stu-id="8a66d-197">Resources are released at one point in the code.</span></span>

<span data-ttu-id="8a66d-198">Недостатки</span><span class="sxs-lookup"><span data-stu-id="8a66d-198">Disadvantages</span></span>

-   <span data-ttu-id="8a66d-199">Все переменные должны быть объявлены и инициализированы в верхней части функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-199">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="8a66d-200">Если вызов завершается неудачно, функция выполняет несколько ненужных проверок ошибок вместо того, чтобы немедленно выйти из функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-200">If a call fails, the function makes multiple unneeded error checks, instead of exiting the function immediately.</span></span>
-   <span data-ttu-id="8a66d-201">Поскольку поток управления просматривает функцию после сбоя, необходимо соблюдать осторожность во всем тексте функции, чтобы не обращаться к недопустимым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="8a66d-201">Because the flow of control continues through the function after a failure, you must be careful throughout the body of the function not to access invalid resources.</span></span>
-   <span data-ttu-id="8a66d-202">Для ошибок внутри цикла требуется специальный случай.</span><span class="sxs-lookup"><span data-stu-id="8a66d-202">Errors inside a loop require a special case.</span></span>

### <a name="jump-on-fail"></a><span data-ttu-id="8a66d-203">Сбой перехода</span><span class="sxs-lookup"><span data-stu-id="8a66d-203">Jump on Fail</span></span>

<span data-ttu-id="8a66d-204">После каждого вызова метода протестируйте ошибку (не удалось).</span><span class="sxs-lookup"><span data-stu-id="8a66d-204">After each method call, test for failure (not success).</span></span> <span data-ttu-id="8a66d-205">При сбое перейдите к метке в нижней части функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-205">On failure, jump to a label near the bottom of the function.</span></span> <span data-ttu-id="8a66d-206">После метки, но перед выходом из функции Освободите ресурсы.</span><span class="sxs-lookup"><span data-stu-id="8a66d-206">After the label, but before exiting the function, release resources.</span></span>


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



<span data-ttu-id="8a66d-207">Преимущества</span><span class="sxs-lookup"><span data-stu-id="8a66d-207">Advantages</span></span>

-   <span data-ttu-id="8a66d-208">Общий поток управления очень удобен для просмотра.</span><span class="sxs-lookup"><span data-stu-id="8a66d-208">The overall control flow is easy to see.</span></span>
-   <span data-ttu-id="8a66d-209">В любой точке кода после [**неудачной**](/windows/desktop/api/winerror/nf-winerror-failed) проверки, если вы не перейдете к метке, гарантируется, что все предыдущие вызовы были успешно выполнены.</span><span class="sxs-lookup"><span data-stu-id="8a66d-209">At every point in the code after a [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) check, if you have not jumped to the label, it is guaranteed that all the previous calls have succeeded.</span></span>
-   <span data-ttu-id="8a66d-210">Ресурсы освобождаются в одном месте кода.</span><span class="sxs-lookup"><span data-stu-id="8a66d-210">Resources are released at one place in the code.</span></span>

<span data-ttu-id="8a66d-211">Недостатки</span><span class="sxs-lookup"><span data-stu-id="8a66d-211">Disadvantages</span></span>

-   <span data-ttu-id="8a66d-212">Все переменные должны быть объявлены и инициализированы в верхней части функции.</span><span class="sxs-lookup"><span data-stu-id="8a66d-212">All variables must be declared and initialized at the top of the function.</span></span>
-   <span data-ttu-id="8a66d-213">Некоторым программистам не нужно использовать **goto** в своем коде.</span><span class="sxs-lookup"><span data-stu-id="8a66d-213">Some programmers do not like to use **goto** in their code.</span></span> <span data-ttu-id="8a66d-214">(Однако следует отметить, что такое использование **goto** очень структурировано; код никогда не переходит за пределы текущего вызова функции.)</span><span class="sxs-lookup"><span data-stu-id="8a66d-214">(However, it should be noted that this use of **goto** is highly structured; the code never jumps outside the current function call.)</span></span>
-   <span data-ttu-id="8a66d-215">операторы **goto** пропускают инициализаторы.</span><span class="sxs-lookup"><span data-stu-id="8a66d-215">**goto** statements skip initializers.</span></span>

### <a name="throw-on-fail"></a><span data-ttu-id="8a66d-216">Выдать ошибку при сбое</span><span class="sxs-lookup"><span data-stu-id="8a66d-216">Throw on Fail</span></span>

<span data-ttu-id="8a66d-217">Вместо перехода к метке можно вызвать исключение при сбое метода.</span><span class="sxs-lookup"><span data-stu-id="8a66d-217">Rather than jump to a label, you can throw an exception when a method fails.</span></span> <span data-ttu-id="8a66d-218">Это может привести к созданию более идиоматическим стиля C++, если вы используете для написания безопасного кода.</span><span class="sxs-lookup"><span data-stu-id="8a66d-218">This can produce a more idiomatic style of C++ if you are used to writing exception-safe code.</span></span>


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



<span data-ttu-id="8a66d-219">Обратите внимание, что в этом примере для управления указателями интерфейса используется класс **CComPtr** .</span><span class="sxs-lookup"><span data-stu-id="8a66d-219">Notice that this example uses the **CComPtr** class to manage interface pointers.</span></span> <span data-ttu-id="8a66d-220">Как правило, если код создает исключения, следует следовать шаблону RAII (получение ресурсов — инициализация).</span><span class="sxs-lookup"><span data-stu-id="8a66d-220">Generally, if your code throws exceptions, you should follow the RAII (Resource Acquisition is Initialization) pattern.</span></span> <span data-ttu-id="8a66d-221">То есть каждый ресурс должен управляться объектом, деструктор которого гарантирует, что ресурс будет освобожден надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="8a66d-221">That is, every resource should be managed by an object whose destructor guarantees that the resource is correctly released.</span></span> <span data-ttu-id="8a66d-222">При возникновении исключения гарантируется вызов деструктора.</span><span class="sxs-lookup"><span data-stu-id="8a66d-222">If an exception is thrown, the destructor is guaranteed to be invoked.</span></span> <span data-ttu-id="8a66d-223">В противном случае программа может утечек ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a66d-223">Otherwise, your program might leak resources.</span></span>

<span data-ttu-id="8a66d-224">Преимущества</span><span class="sxs-lookup"><span data-stu-id="8a66d-224">Advantages</span></span>

-   <span data-ttu-id="8a66d-225">Совместимо с существующим кодом, использующим обработку исключений.</span><span class="sxs-lookup"><span data-stu-id="8a66d-225">Compatible with existing code that uses exception handling.</span></span>
-   <span data-ttu-id="8a66d-226">Совместимо с библиотеками C++, которые создают исключения, такие как библиотека стандартных шаблонов (STL).</span><span class="sxs-lookup"><span data-stu-id="8a66d-226">Compatible with C++ libraries that throw exceptions, such as the Standard Template Library (STL).</span></span>

<span data-ttu-id="8a66d-227">Недостатки</span><span class="sxs-lookup"><span data-stu-id="8a66d-227">Disadvantages</span></span>

-   <span data-ttu-id="8a66d-228">Требуются объекты C++ для управления ресурсами, такими как память или дескрипторы файлов.</span><span class="sxs-lookup"><span data-stu-id="8a66d-228">Requires C++ objects to manage resources such as memory or file handles.</span></span>
-   <span data-ttu-id="8a66d-229">Необходимо хорошо понимать, как писать код, защищенный с помощью исключений.</span><span class="sxs-lookup"><span data-stu-id="8a66d-229">Requires a good understanding of how to write exception-safe code.</span></span>

## <a name="next"></a><span data-ttu-id="8a66d-230">Следующая</span><span class="sxs-lookup"><span data-stu-id="8a66d-230">Next</span></span>

[<span data-ttu-id="8a66d-231">Модуль 3. Графика Windows</span><span class="sxs-lookup"><span data-stu-id="8a66d-231">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)

 

 
