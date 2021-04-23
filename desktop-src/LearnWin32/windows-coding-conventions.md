---
title: Соглашения о написании кода Windows
description: Если вы не знакомы с программированием для Windows, это можно сделать при первом просмотре программы Windows.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672261"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="242d2-103">Соглашения о написании кода Windows</span><span class="sxs-lookup"><span data-stu-id="242d2-103">Windows Coding Conventions</span></span>

<span data-ttu-id="242d2-104">Если вы не знакомы с программированием для Windows, это можно сделать при первом просмотре программы Windows.</span><span class="sxs-lookup"><span data-stu-id="242d2-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="242d2-105">Код заполняется нестранными определениями типов, такими как **DWORD \_ ptr** и **лпрект**, а переменные имеют такие имена, как *HWND* и *пвсз* (называемые венгерской нотацией).</span><span class="sxs-lookup"><span data-stu-id="242d2-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="242d2-106">Стоит потратить немного времени, чтобы изучить некоторые соглашения о написании кода Windows.</span><span class="sxs-lookup"><span data-stu-id="242d2-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="242d2-107">Большинство API-интерфейсов Windows состоят из функций или интерфейсов модели COM.</span><span class="sxs-lookup"><span data-stu-id="242d2-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="242d2-108">В качестве классов C++ предоставляются очень мало API Windows.</span><span class="sxs-lookup"><span data-stu-id="242d2-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="242d2-109">(Важным исключением является GDI+, один из API-интерфейсов двухмерной графики.)</span><span class="sxs-lookup"><span data-stu-id="242d2-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="242d2-110">Определения типов</span><span class="sxs-lookup"><span data-stu-id="242d2-110">Typedefs</span></span>

<span data-ttu-id="242d2-111">Заголовки Windows содержат множество определений типов.</span><span class="sxs-lookup"><span data-stu-id="242d2-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="242d2-112">Многие из них определены в файле заголовка Виндеф. h.</span><span class="sxs-lookup"><span data-stu-id="242d2-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="242d2-113">Ниже приведены некоторые из них, которые часто встречаются.</span><span class="sxs-lookup"><span data-stu-id="242d2-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="242d2-114">Целочисленные типы</span><span class="sxs-lookup"><span data-stu-id="242d2-114">Integer types</span></span>



| <span data-ttu-id="242d2-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="242d2-115">Data type</span></span>     | <span data-ttu-id="242d2-116">Размер</span><span class="sxs-lookup"><span data-stu-id="242d2-116">Size</span></span>    | <span data-ttu-id="242d2-117">Входил?</span><span class="sxs-lookup"><span data-stu-id="242d2-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="242d2-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="242d2-118">**BYTE**</span></span>      | <span data-ttu-id="242d2-119">8 бит</span><span class="sxs-lookup"><span data-stu-id="242d2-119">8 bits</span></span>  | <span data-ttu-id="242d2-120">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-120">Unsigned</span></span> |
| <span data-ttu-id="242d2-121">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="242d2-121">**DWORD**</span></span>     | <span data-ttu-id="242d2-122">32 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-122">32 bits</span></span> | <span data-ttu-id="242d2-123">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-123">Unsigned</span></span> |
| <span data-ttu-id="242d2-124">**INT32**</span><span class="sxs-lookup"><span data-stu-id="242d2-124">**INT32**</span></span>     | <span data-ttu-id="242d2-125">32 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-125">32 bits</span></span> | <span data-ttu-id="242d2-126">Со знаком</span><span class="sxs-lookup"><span data-stu-id="242d2-126">Signed</span></span>   |
| <span data-ttu-id="242d2-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="242d2-127">**INT64**</span></span>     | <span data-ttu-id="242d2-128">64 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-128">64 bits</span></span> | <span data-ttu-id="242d2-129">Со знаком</span><span class="sxs-lookup"><span data-stu-id="242d2-129">Signed</span></span>   |
| <span data-ttu-id="242d2-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="242d2-130">**LONG**</span></span>      | <span data-ttu-id="242d2-131">32 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-131">32 bits</span></span> | <span data-ttu-id="242d2-132">Со знаком</span><span class="sxs-lookup"><span data-stu-id="242d2-132">Signed</span></span>   |
| <span data-ttu-id="242d2-133">**лонглонг**</span><span class="sxs-lookup"><span data-stu-id="242d2-133">**LONGLONG**</span></span>  | <span data-ttu-id="242d2-134">64 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-134">64 bits</span></span> | <span data-ttu-id="242d2-135">Со знаком</span><span class="sxs-lookup"><span data-stu-id="242d2-135">Signed</span></span>   |
| <span data-ttu-id="242d2-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="242d2-136">**UINT32**</span></span>    | <span data-ttu-id="242d2-137">32 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-137">32 bits</span></span> | <span data-ttu-id="242d2-138">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-138">Unsigned</span></span> |
| <span data-ttu-id="242d2-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="242d2-139">**UINT64**</span></span>    | <span data-ttu-id="242d2-140">64 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-140">64 bits</span></span> | <span data-ttu-id="242d2-141">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-141">Unsigned</span></span> |
| <span data-ttu-id="242d2-142">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="242d2-142">**ULONG**</span></span>     | <span data-ttu-id="242d2-143">32 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-143">32 bits</span></span> | <span data-ttu-id="242d2-144">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-144">Unsigned</span></span> |
| <span data-ttu-id="242d2-145">**улонглонг**</span><span class="sxs-lookup"><span data-stu-id="242d2-145">**ULONGLONG**</span></span> | <span data-ttu-id="242d2-146">64 бита</span><span class="sxs-lookup"><span data-stu-id="242d2-146">64 bits</span></span> | <span data-ttu-id="242d2-147">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-147">Unsigned</span></span> |
| <span data-ttu-id="242d2-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="242d2-148">**WORD**</span></span>      | <span data-ttu-id="242d2-149">16 бит</span><span class="sxs-lookup"><span data-stu-id="242d2-149">16 bits</span></span> | <span data-ttu-id="242d2-150">Без знака</span><span class="sxs-lookup"><span data-stu-id="242d2-150">Unsigned</span></span> |



 

<span data-ttu-id="242d2-151">Как видите, в этих определениях типов имеется определенный объем избыточности.</span><span class="sxs-lookup"><span data-stu-id="242d2-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="242d2-152">Часть этого перекрывается просто из-за истории интерфейсов API Windows.</span><span class="sxs-lookup"><span data-stu-id="242d2-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="242d2-153">Перечисленные типы имеют фиксированный размер, а размеры одинаковы в 32-и 64-приложениях.</span><span class="sxs-lookup"><span data-stu-id="242d2-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="242d2-154">Например, тип **DWORD** всегда 32 бит в ширину.</span><span class="sxs-lookup"><span data-stu-id="242d2-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="242d2-155">Логический тип</span><span class="sxs-lookup"><span data-stu-id="242d2-155">Boolean Type</span></span>

<span data-ttu-id="242d2-156">**Bool** — это typedef для целочисленного значения, используемого в логическом контексте.</span><span class="sxs-lookup"><span data-stu-id="242d2-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="242d2-157">Файл заголовка Виндеф. h также определяет два значения для использования с **bool**.</span><span class="sxs-lookup"><span data-stu-id="242d2-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="242d2-158">Несмотря на это определение **true**, большинство функций, возвращающих тип **bool** , могут возвращать любое ненулевое значение, обозначающее логическую истинность.</span><span class="sxs-lookup"><span data-stu-id="242d2-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="242d2-159">Поэтому всегда следует писать следующее:</span><span class="sxs-lookup"><span data-stu-id="242d2-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="242d2-160">и не так:</span><span class="sxs-lookup"><span data-stu-id="242d2-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="242d2-161">Помните, что **bool** является целочисленным типом и не является взаимозаменяемым с типом **bool** C++.</span><span class="sxs-lookup"><span data-stu-id="242d2-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="242d2-162">Типы указателей</span><span class="sxs-lookup"><span data-stu-id="242d2-162">Pointer Types</span></span>

<span data-ttu-id="242d2-163">Windows определяет множество типов данных *указателя на X*.</span><span class="sxs-lookup"><span data-stu-id="242d2-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="242d2-164">Они обычно имеют префикс *P-* или *LP-* в имени.</span><span class="sxs-lookup"><span data-stu-id="242d2-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="242d2-165">Например, **лпрект** является указателем на [**Rect**](/previous-versions//dd162897(v=vs.85)), где **Rect** — это структура, описывающая прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="242d2-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="242d2-166">Следующие объявления переменных эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="242d2-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="242d2-167">Исторически, *P* означает "указатель", а *LP* — "длинный указатель".</span><span class="sxs-lookup"><span data-stu-id="242d2-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="242d2-168">Длинные указатели (также называемые *дальнеимися указателями*) являются наследие из 16-разрядных окон, когда они были необходимы для адресации диапазонов памяти за пределами текущего сегмента.</span><span class="sxs-lookup"><span data-stu-id="242d2-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="242d2-169">Префикс *LP* был сохранен, чтобы упростить перенос 16-разрядного кода в 32-разрядную версию Windows.</span><span class="sxs-lookup"><span data-stu-id="242d2-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="242d2-170">На сегодняшний день нет различий — указатель является указателем.</span><span class="sxs-lookup"><span data-stu-id="242d2-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="242d2-171">Типы точности указателей</span><span class="sxs-lookup"><span data-stu-id="242d2-171">Pointer Precision Types</span></span>

<span data-ttu-id="242d2-172">Следующие типы данных всегда имеют размер указателя, то есть 32 бит в 32-разрядных приложениях и 64 бит на уровне в 64-разрядных приложениях.</span><span class="sxs-lookup"><span data-stu-id="242d2-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="242d2-173">Размер определяется во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="242d2-173">The size is determined at compile time.</span></span> <span data-ttu-id="242d2-174">Если 32-разрядное приложение выполняется в 64-разрядной версии Windows, эти типы данных по-прежнему имеют ширину 4 байта.</span><span class="sxs-lookup"><span data-stu-id="242d2-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="242d2-175">(64-разрядное приложение не может работать в 32-разрядной версии Windows, поэтому обратная ситуация не возникает.)</span><span class="sxs-lookup"><span data-stu-id="242d2-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="242d2-176">**DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="242d2-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="242d2-177">**INT \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="242d2-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="242d2-178">**LONG \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="242d2-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="242d2-179">**ULONG- \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="242d2-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="242d2-180">**UINT \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="242d2-180">**UINT\_PTR**</span></span>

<span data-ttu-id="242d2-181">Эти типы используются в ситуациях, когда целочисленное значение может быть приведено к указателю.</span><span class="sxs-lookup"><span data-stu-id="242d2-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="242d2-182">Они также используются для определения переменных для арифметических операций с указателями и для определения счетчиков циклов, которые просматривают весь диапазон байтов в буферах памяти.</span><span class="sxs-lookup"><span data-stu-id="242d2-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="242d2-183">В общем случае они появляются в местах, где существующее 32-разрядное значение было расширено до 64 бит в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="242d2-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="242d2-184">Венгерская нотация</span><span class="sxs-lookup"><span data-stu-id="242d2-184">Hungarian Notation</span></span>

<span data-ttu-id="242d2-185">*Венгерская нотация* — это практика добавления префиксов к именам переменных для предоставления дополнительных сведений о переменной.</span><span class="sxs-lookup"><span data-stu-id="242d2-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="242d2-186">(Инвентаризация в нотации, Чарльз Симони, была венгерской, поэтому ее имя).</span><span class="sxs-lookup"><span data-stu-id="242d2-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="242d2-187">В исходной форме нотация Венгерская информация предоставляет *семантическую* информацию о переменной, которая сообщает вам о предполагаемом использовании.</span><span class="sxs-lookup"><span data-stu-id="242d2-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="242d2-188">Например, *я* обозначает индекс, *CB* означает размер в байтах ("количество байт"), а значения строк и столбцов для значений *RW* и *Col* .</span><span class="sxs-lookup"><span data-stu-id="242d2-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="242d2-189">Эти префиксы предназначены для того, чтобы избежать случайного использования переменной в неправильном контексте.</span><span class="sxs-lookup"><span data-stu-id="242d2-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="242d2-190">Например, если вы видели выражение `rwPosition +  cbTable` , вы узнаете, что к размеру добавляется номер строки, что почти наверняка является ошибкой в коде.</span><span class="sxs-lookup"><span data-stu-id="242d2-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="242d2-191">Более распространенная форма венгерской нотации использует префиксы для предоставления сведений о *типе* , например *DW* для **DWORD** и *w* для **Word**.</span><span class="sxs-lookup"><span data-stu-id="242d2-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="242d2-192">При поиске в Интернете по «венгерской нотации» вы найдете множество мнений о том, хорошо ли Венгерская нотация.</span><span class="sxs-lookup"><span data-stu-id="242d2-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="242d2-193">Некоторые программисты имеют сильная отличие от венгерской нотации.</span><span class="sxs-lookup"><span data-stu-id="242d2-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="242d2-194">Другие считают это полезным.</span><span class="sxs-lookup"><span data-stu-id="242d2-194">Others find it helpful.</span></span> <span data-ttu-id="242d2-195">Независимо от многих примеров кода на MSDN используется Венгерская нотация, но вам не нужно запоминать префиксы для понимания кода.</span><span class="sxs-lookup"><span data-stu-id="242d2-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="242d2-196">Следующая</span><span class="sxs-lookup"><span data-stu-id="242d2-196">Next</span></span>

[<span data-ttu-id="242d2-197">Работа со строками</span><span class="sxs-lookup"><span data-stu-id="242d2-197">Working with Strings</span></span>](working-with-strings.md)

 

 