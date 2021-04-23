---
title: Средства
description: В этом разделе описываются средства, которые можно использовать для подготовки приложения 64-bit. Windows 10 доступна для процессоров на базе x64 и ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- 64-разрядное руководством по программированию для Windows, 64-разрядное программирование для Windows, средства
- средства 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411240"
---
# <a name="the-tools"></a><span data-ttu-id="a3292-106">Средства</span><span class="sxs-lookup"><span data-stu-id="a3292-106">The Tools</span></span>

<span data-ttu-id="a3292-107">В этом разделе описываются средства, которые можно использовать для подготовки приложения 64-bit.</span><span class="sxs-lookup"><span data-stu-id="a3292-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="a3292-108">Windows 10 доступна для процессоров на базе x64 и ARM64.</span><span class="sxs-lookup"><span data-stu-id="a3292-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="a3292-109">Включение файлов</span><span class="sxs-lookup"><span data-stu-id="a3292-109">Include Files</span></span>

<span data-ttu-id="a3292-110">Элементы API практически идентичны в пределах между 32 и 64-разрядными окнами.</span><span class="sxs-lookup"><span data-stu-id="a3292-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="a3292-111">Файлы заголовков Windows были изменены так, чтобы их можно было использовать как для 32, так и для 64-разрядного кода.</span><span class="sxs-lookup"><span data-stu-id="a3292-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="a3292-112">Новые 64-разрядные типы и макросы определяются в новом файле заголовка Басетсд. h, который находится в наборе файлов заголовков, включенных в Windows. h.</span><span class="sxs-lookup"><span data-stu-id="a3292-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="a3292-113">Басетсд. h содержит новые определения типов данных, которые помогают сделать размер слова исходного кода независимым от него.</span><span class="sxs-lookup"><span data-stu-id="a3292-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="a3292-114">Новые типы данных</span><span class="sxs-lookup"><span data-stu-id="a3292-114">New Data Types</span></span>

<span data-ttu-id="a3292-115">Файлы заголовков Windows содержат новые типы данных.</span><span class="sxs-lookup"><span data-stu-id="a3292-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="a3292-116">Эти типы в основном предназначены для совместимости типов с 32-разрядными типами данных.</span><span class="sxs-lookup"><span data-stu-id="a3292-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="a3292-117">Новые типы предоставляют точно такую же типизацию, что и существующие типы, в то же время обеспечивая поддержку 64-разрядных Windows.</span><span class="sxs-lookup"><span data-stu-id="a3292-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="a3292-118">Дополнительные сведения см. [в разделе новые типы данных](the-new-data-types.md) или файл заголовка басетсд. h.</span><span class="sxs-lookup"><span data-stu-id="a3292-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="a3292-119">Предустановленный макрос</span><span class="sxs-lookup"><span data-stu-id="a3292-119">Predefined Macros</span></span>

<span data-ttu-id="a3292-120">Компилятор определяет следующие макросы для определения платформы.</span><span class="sxs-lookup"><span data-stu-id="a3292-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="a3292-121">Макрос</span><span class="sxs-lookup"><span data-stu-id="a3292-121">Macro</span></span>   | <span data-ttu-id="a3292-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a3292-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3292-123">\_ПЛАТФОРМЕ</span><span class="sxs-lookup"><span data-stu-id="a3292-123">\_WIN64</span></span> | <span data-ttu-id="a3292-124">64-разрядная платформа.</span><span class="sxs-lookup"><span data-stu-id="a3292-124">A 64-bit platform.</span></span> <span data-ttu-id="a3292-125">Сюда входят x64 и ARM64.</span><span class="sxs-lookup"><span data-stu-id="a3292-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="a3292-126">\_Платформа</span><span class="sxs-lookup"><span data-stu-id="a3292-126">\_WIN32</span></span> | <span data-ttu-id="a3292-127">32-разрядная платформа.</span><span class="sxs-lookup"><span data-stu-id="a3292-127">A 32-bit platform.</span></span> <span data-ttu-id="a3292-128">Это значение также определяется в 64-разрядном компиляторе для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="a3292-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="a3292-129">\_ПЛАТФОРМЕ</span><span class="sxs-lookup"><span data-stu-id="a3292-129">\_WIN16</span></span> | <span data-ttu-id="a3292-130">16-разрядная платформа</span><span class="sxs-lookup"><span data-stu-id="a3292-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="a3292-131">Следующие макросы относятся к архитектуре.</span><span class="sxs-lookup"><span data-stu-id="a3292-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="a3292-132">Макрос</span><span class="sxs-lookup"><span data-stu-id="a3292-132">Macro</span></span>      | <span data-ttu-id="a3292-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a3292-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="a3292-134">\_M \_ ia64</span><span class="sxs-lookup"><span data-stu-id="a3292-134">\_M\_IA64</span></span>  | <span data-ttu-id="a3292-135">Платформа Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="a3292-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="a3292-136">\_M \_ IX86</span><span class="sxs-lookup"><span data-stu-id="a3292-136">\_M\_IX86</span></span>  | <span data-ttu-id="a3292-137">Платформа x86</span><span class="sxs-lookup"><span data-stu-id="a3292-137">x86 platform</span></span>           |
| <span data-ttu-id="a3292-138">\_M \_ x64</span><span class="sxs-lookup"><span data-stu-id="a3292-138">\_M\_X64</span></span>   | <span data-ttu-id="a3292-139">Платформа x64</span><span class="sxs-lookup"><span data-stu-id="a3292-139">x64 platform</span></span>           |
| <span data-ttu-id="a3292-140">\_M \_ ARM64</span><span class="sxs-lookup"><span data-stu-id="a3292-140">\_M\_ARM64</span></span> | <span data-ttu-id="a3292-141">Платформа ARM64</span><span class="sxs-lookup"><span data-stu-id="a3292-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="a3292-142">Не используйте эти макросы, за исключением кода, зависящего от архитектуры. вместо этого используйте \_ Win64, \_ Win32 и \_ WIN16, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="a3292-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="a3292-143">Вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="a3292-143">Helper Functions</span></span>

<span data-ttu-id="a3292-144">Следующие встроенные функции (определенные в Басетсд. h) позволяют безопасно преобразовывать значения из одного типа в другой.</span><span class="sxs-lookup"><span data-stu-id="a3292-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="a3292-145">Знак **инттоптр** расширяет значение **int** , **уинттоптр** ноль — расширяет значение **неподписанного целого** числа, **лонгтоптр** знак **длинного** типа, а **улонгтоптр** нуля расширяет значение **без знака** .</span><span class="sxs-lookup"><span data-stu-id="a3292-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="a3292-146">64-разрядный компилятор</span><span class="sxs-lookup"><span data-stu-id="a3292-146">64-bit Compiler</span></span>

<span data-ttu-id="a3292-147">64-разрядные компиляторы можно использовать для выявления усечения указателя, неправильного приведения типов и других проблем, связанных с 64.</span><span class="sxs-lookup"><span data-stu-id="a3292-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="a3292-148">При первом запуске компилятора, возможно, будет создано много усечений указателя или предупреждений о несоответствии типов, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="a3292-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="a3292-149">Используйте эти предупреждения в качестве рекомендации, чтобы сделать код более надежным.</span><span class="sxs-lookup"><span data-stu-id="a3292-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="a3292-150">Рекомендуется устранить все предупреждения, особенно предупреждения усечения указателей.</span><span class="sxs-lookup"><span data-stu-id="a3292-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="a3292-151">64-разрядные коммутаторы и предупреждения компилятора</span><span class="sxs-lookup"><span data-stu-id="a3292-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="a3292-152">Обратите внимание, что этот компилятор включает модель данных LLP64.</span><span class="sxs-lookup"><span data-stu-id="a3292-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="a3292-153">Существует параметр предупреждения, помогающий перенестися в LLP64.</span><span class="sxs-lookup"><span data-stu-id="a3292-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="a3292-154">Параметр-Wp64-W3 включает следующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3292-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="a3292-155">C4305: предупреждение усечения.</span><span class="sxs-lookup"><span data-stu-id="a3292-155">C4305: Truncation warning.</span></span> <span data-ttu-id="a3292-156">Например, "return": усечение из "без знака Int64" в "Long".</span><span class="sxs-lookup"><span data-stu-id="a3292-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="a3292-157">C4311: предупреждение усечения.</span><span class="sxs-lookup"><span data-stu-id="a3292-157">C4311: Truncation warning.</span></span> <span data-ttu-id="a3292-158">Например, "приведение типа": усечение указателя из "int \* \_ ptr64" в "int".</span><span class="sxs-lookup"><span data-stu-id="a3292-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="a3292-159">C4312: преобразование в предупреждение о большем размере.</span><span class="sxs-lookup"><span data-stu-id="a3292-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="a3292-160">Например, "приведение типов": преобразование "int" в "int \* \_ ptr64" большего размера.</span><span class="sxs-lookup"><span data-stu-id="a3292-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="a3292-161">C4318: передача нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="a3292-161">C4318: Passing zero length.</span></span> <span data-ttu-id="a3292-162">Например, передача нулевой константы в качестве длины функции **memset** .</span><span class="sxs-lookup"><span data-stu-id="a3292-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="a3292-163">C4319: оператор NOT.</span><span class="sxs-lookup"><span data-stu-id="a3292-163">C4319: Not operator.</span></span> <span data-ttu-id="a3292-164">Например, "~": нулевое расширение "без знака Long" до "неподписанный \_ Int64" большего размера.</span><span class="sxs-lookup"><span data-stu-id="a3292-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="a3292-165">C4313: вызов семейства функций **printf** с конфликтующими спецификаторами и аргументами типа преобразования.</span><span class="sxs-lookup"><span data-stu-id="a3292-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="a3292-166">Например, "printf": "% p" в строке формата конфликтует с аргументом 2 типа " \_ Int64".</span><span class="sxs-lookup"><span data-stu-id="a3292-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="a3292-167">Другим примером является функция printf ("% x", значение указателя \_ ), что приводит к усечению верхних 32 бит.</span><span class="sxs-lookup"><span data-stu-id="a3292-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="a3292-168">Правильный вызов — printf ("% p", значение указателя \_ ).</span><span class="sxs-lookup"><span data-stu-id="a3292-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="a3292-169">Предупреждение C4244: то же, что и у существующего предупреждения C4242.</span><span class="sxs-lookup"><span data-stu-id="a3292-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="a3292-170">Например, return: преобразование из " \_ Int64" в "без знака int", возможна потери данных.</span><span class="sxs-lookup"><span data-stu-id="a3292-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="a3292-171">64-разрядный компоновщик и библиотеки</span><span class="sxs-lookup"><span data-stu-id="a3292-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="a3292-172">Для создания приложений используйте компоновщик и библиотеки, предоставляемые Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a3292-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="a3292-173">Большинство 32-разрядных библиотек имеют соответствующую 64-разрядную версию, но некоторые устаревшие библиотеки доступны только в 32-разрядных версиях.</span><span class="sxs-lookup"><span data-stu-id="a3292-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="a3292-174">Код, который вызывает эти библиотеки, не будет связываться при создании приложения для 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="a3292-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 





