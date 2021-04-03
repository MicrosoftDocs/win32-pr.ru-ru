---
title: pragma - атрибут
description: Директива \ pragma MIDL \_ echo указывает MIDL на вывод указанной строки без кавычек в создаваемый файл заголовка.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma Attribute MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986885"
---
# <a name="pragma-attribute"></a><span data-ttu-id="313b6-104">pragma - атрибут</span><span class="sxs-lookup"><span data-stu-id="313b6-104">pragma attribute</span></span>

<span data-ttu-id="313b6-105">\#Директива **pragma MIDL \_ echo** предписывает MIDL выдавать указанную строку без кавычек в создаваемый файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="313b6-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="313b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="313b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313b6-107">*string*</span><span class="sxs-lookup"><span data-stu-id="313b6-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="313b6-108">Указывает строку, которая вставляется в создаваемый файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="313b6-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="313b6-109">Кавычки удаляются во время процесса вставки.</span><span class="sxs-lookup"><span data-stu-id="313b6-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="313b6-110">*последовательность токенов*</span><span class="sxs-lookup"><span data-stu-id="313b6-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="313b6-111">Задает последовательность токенов, которые вставляются в созданный файл заголовка как часть директивы **\# pragma** без обработки компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="313b6-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="313b6-112">*n*</span><span class="sxs-lookup"><span data-stu-id="313b6-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="313b6-113">Указывает текущий размер пакета.</span><span class="sxs-lookup"><span data-stu-id="313b6-113">Specifies the current pack size.</span></span> <span data-ttu-id="313b6-114">Допустимые значения: 1, 2, 4, 8 и 16.</span><span class="sxs-lookup"><span data-stu-id="313b6-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="313b6-115">*id*</span><span class="sxs-lookup"><span data-stu-id="313b6-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="313b6-116">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="313b6-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="313b6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="313b6-117">Remarks</span></span>

<span data-ttu-id="313b6-118">Директивы предварительной обработки языка c, которые отображаются в IDL-файле, обрабатываются препроцессором компилятора C.</span><span class="sxs-lookup"><span data-stu-id="313b6-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="313b6-119">Директивы **\# define** в IDL-файле доступны во время компиляции MIDL, хотя и не в компиляторе C.</span><span class="sxs-lookup"><span data-stu-id="313b6-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="313b6-120">Например, когда препроцессор встречает директиву " \# define Windows 4", препроцессор заменяет все вхождения "Windows" в IDL-файле на "4".</span><span class="sxs-lookup"><span data-stu-id="313b6-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="313b6-121">Символ "WINDOWS" недоступен во время компиляции C.</span><span class="sxs-lookup"><span data-stu-id="313b6-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="313b6-122">Чтобы разрешить определениям макросов C-препроцессор проходить через компилятор MIDL к компилятору C, используйте директиву **\# pragma MIDL \_ echo** или [**cpp \_ quote**](cpp-quote.md) .</span><span class="sxs-lookup"><span data-stu-id="313b6-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="313b6-123">Эти директивы предписывает компилятору MIDL создать файл заголовка, содержащий строку параметра с удаленными кавычками.</span><span class="sxs-lookup"><span data-stu-id="313b6-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="313b6-124">Директивы **\# pragma MIDL \_ echo** и **cpp- \_ кавычки** эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="313b6-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="313b6-125">Директива **\# pragma pack** используется компилятором MIDL для управления упаковкой структур.</span><span class="sxs-lookup"><span data-stu-id="313b6-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="313b6-126">Он переопределяет параметр командной строки [**/Zp**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="313b6-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="313b6-127">Параметр Pack (*n*) устанавливает для текущего размера пакета определенное значение: 1, 2, 4, 8 или 16.</span><span class="sxs-lookup"><span data-stu-id="313b6-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="313b6-128">Параметры Pack (Push) и Pack (POP) имеют следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="313b6-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="313b6-129">Компилятор поддерживает стек упаковки.</span><span class="sxs-lookup"><span data-stu-id="313b6-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="313b6-130">Элементы стека упаковки содержат размер пакета и необязательный *идентификатор*. Стек ограничен только доступной памятью с текущим размером пакета в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="313b6-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="313b6-131">Pack (Push) приводит к получению текущего размера пакета, отправленного в стек упаковки.</span><span class="sxs-lookup"><span data-stu-id="313b6-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="313b6-132">Стек ограничивается доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="313b6-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="313b6-133">Pack (Push,*n*) совпадает с Pack (Push), за которым следует Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="313b6-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="313b6-134">Pack (Push, *ID*) также передает *идентификатор* в стек упаковки вместе с размером пакета.</span><span class="sxs-lookup"><span data-stu-id="313b6-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="313b6-135">Pack (Push, *ID*, *n*) совпадает с Pack (Push, *ID*), за которым следует Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="313b6-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="313b6-136">Пакет (POP) приводит к извлечению стека упаковки.</span><span class="sxs-lookup"><span data-stu-id="313b6-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="313b6-137">Несбалансированные POP приводят к предупреждениям и устанавливают текущий размер пакета в значение командной строки.</span><span class="sxs-lookup"><span data-stu-id="313b6-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="313b6-138">Если указан пакет (POP, *ID*, *n*), то *n* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="313b6-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="313b6-139">Компилятор MIDL помещает строки, указанные в директивах [**\\ cpp \_**](cpp-quote.md) и **pragma** в файле заголовка, в последовательности, в которой они указаны в IDL-файле и относительно других компонентов интерфейса в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="313b6-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="313b6-140">Строки обычно должны присутствовать в разделе Interface-Body файла IDL после всех операций [**импорта**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="313b6-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="313b6-141">Компилятор MIDL не пытается обработать директивы **\# pragma** , которые не начинаются с префикса MIDL \_ .</span><span class="sxs-lookup"><span data-stu-id="313b6-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="313b6-142">Другие директивы **\# pragma** в IDL-файле передаются в созданный файл заголовка без изменений.</span><span class="sxs-lookup"><span data-stu-id="313b6-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="313b6-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="313b6-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="313b6-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="313b6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313b6-145">**\_цитата cpp**</span><span class="sxs-lookup"><span data-stu-id="313b6-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="313b6-146">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="313b6-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="313b6-147">**импортиру**</span><span class="sxs-lookup"><span data-stu-id="313b6-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="313b6-148">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="313b6-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




