---
title: cpp_quote - атрибут
description: '\_Ключевое слово Quote в формате cpp предписывает компилятору MIDL выводить указанную строку без кавычек в создаваемый файл заголовка.'
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote атрибута MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069122"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="a7796-104">\_атрибут Quote в cpp</span><span class="sxs-lookup"><span data-stu-id="a7796-104">cpp\_quote attribute</span></span>

<span data-ttu-id="a7796-105">Ключевое слово **\_ quote** в формате cpp предписывает компилятору MIDL выводить указанную строку без кавычек в создаваемый файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="a7796-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="a7796-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7796-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7796-107">*string*</span><span class="sxs-lookup"><span data-stu-id="a7796-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="a7796-108">Указывает строку в кавычках, которая создается в созданном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="a7796-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="a7796-109">Строка должна быть заключена в кавычки, чтобы не допустить расширения препроцессором C.</span><span class="sxs-lookup"><span data-stu-id="a7796-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7796-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7796-110">Remarks</span></span>

<span data-ttu-id="a7796-111">Директивы предварительной обработки языка c, которые отображаются в IDL-файле, обрабатываются препроцессором компилятора C.</span><span class="sxs-lookup"><span data-stu-id="a7796-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="a7796-112">Директивы **\# define** в IDL-файле доступны во время компиляции MIDL, но недоступны компилятору C.</span><span class="sxs-lookup"><span data-stu-id="a7796-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="a7796-113">Например, когда препроцессор встречает директиву " \# define Windows 4", препроцессор заменяет все вхождения "Windows" в IDL-файле на "4".</span><span class="sxs-lookup"><span data-stu-id="a7796-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="a7796-114">Символ "WINDOWS" недоступен во время компиляции C-Language.</span><span class="sxs-lookup"><span data-stu-id="a7796-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="a7796-115">Чтобы разрешить определениям макросов C-препроцессор проходить через компилятор MIDL к компилятору C, используйте директиву **\# pragma MIDL \_ echo** или **cpp \_ quote** .</span><span class="sxs-lookup"><span data-stu-id="a7796-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="a7796-116">Эти директивы предписывает компилятору MIDL создать файл заголовка, содержащий строку параметра с удаленными кавычками.</span><span class="sxs-lookup"><span data-stu-id="a7796-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="a7796-117">Директивы **\# pragma MIDL \_ echo** и **cpp- \_ кавычки** эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="a7796-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="a7796-118">Компилятор MIDL помещает строки, указанные в директивах **cpp \_** и [**pragma**](pragma.md) , в файл заголовка в последовательности, в которой они указаны в IDL-файле, и относительно других компонентов интерфейса в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="a7796-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="a7796-119">Строки обычно отображаются в разделе тела IDL-файла после всех операций [**импорта**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="a7796-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="a7796-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="a7796-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="a7796-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7796-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7796-122">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="a7796-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a7796-123">**импортиру**</span><span class="sxs-lookup"><span data-stu-id="a7796-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="a7796-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="a7796-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




