---
title: " Line, директива"
description: Директива препроцессора, которая задает внутренний хранимый компилятором номер строки и имя файла для указанных значений.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- HLSL Директива line
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411792"
---
# <a name="line-directive"></a><span data-ttu-id="3f736-104">\#Line, директива</span><span class="sxs-lookup"><span data-stu-id="3f736-104">\#line Directive</span></span>

<span data-ttu-id="3f736-105">Директива препроцессора, которая задает внутренний хранимый компилятором номер строки и имя файла для указанных значений.</span><span class="sxs-lookup"><span data-stu-id="3f736-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="3f736-106">\#Line *LineNumber* "*ИмяФайла*"</span><span class="sxs-lookup"><span data-stu-id="3f736-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3f736-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f736-107">Parameters</span></span>



| <span data-ttu-id="3f736-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="3f736-108">Item</span></span>                                                                                                                              | <span data-ttu-id="3f736-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3f736-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f736-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span><span class="sxs-lookup"><span data-stu-id="3f736-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="3f736-111">Номер строки для задания.</span><span class="sxs-lookup"><span data-stu-id="3f736-111">Line number to set.</span></span> <span data-ttu-id="3f736-112">Это может быть любая целочисленная константа.</span><span class="sxs-lookup"><span data-stu-id="3f736-112">This can be any integer constant.</span></span> <span data-ttu-id="3f736-113">Замена макросов может выполняться в токенах предварительной обработки при условии, что результат имеет правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3f736-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="3f736-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*имя файла* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="3f736-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="3f736-115">Имя файла для задания.</span><span class="sxs-lookup"><span data-stu-id="3f736-115">Filename to set.</span></span> <span data-ttu-id="3f736-116">Имя файла может быть любым сочетанием символов и должно быть заключено в двойные кавычки ("").</span><span class="sxs-lookup"><span data-stu-id="3f736-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="3f736-117">Если этот параметр пропущен, предыдущее имя файла остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="3f736-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f736-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f736-118">Remarks</span></span>

<span data-ttu-id="3f736-119">Компилятор использует номер строки и имя файла для ссылки на ошибки, обнаруженные во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="3f736-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="3f736-120">Номер линии обычно указывает на текущую строку входных данных, а имя файла — на текущий входной файл.</span><span class="sxs-lookup"><span data-stu-id="3f736-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="3f736-121">Номер строки увеличивается на единицу после обработки каждой строки.</span><span class="sxs-lookup"><span data-stu-id="3f736-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="3f736-122">Если изменить номер линии и имя файла, компилятор игнорирует предыдущих значений и продолжит обработку с новыми значениями.</span><span class="sxs-lookup"><span data-stu-id="3f736-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="3f736-123">\#Директива line обычно используется генераторами программ, чтобы сообщения об ошибках ссылались на исходный исходный файл, а не на созданную программу.</span><span class="sxs-lookup"><span data-stu-id="3f736-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="3f736-124">Переводчик использует номер строки и имя файла для определения значений предопределенного файла макросов \_ \_ \_ \_ и \_ \_ строки \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3f736-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="3f736-125">С помощью этих макросов можно вставлять в текст программы описательные сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="3f736-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="3f736-126">\_ \_ Файловый \_ \_ макрос разворачивается в строку, содержимое которой является именем файла, заключенное в двойные кавычки ("").</span><span class="sxs-lookup"><span data-stu-id="3f736-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="3f736-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="3f736-127">Examples</span></span>

<span data-ttu-id="3f736-128">В следующем примере номер строки присваивается 151, а имя файла — Copy. c.</span><span class="sxs-lookup"><span data-stu-id="3f736-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="3f736-129">В следующем примере макрос ASSERT использует предопределенную \_ \_ строку \_ \_ и файл макросов \_ \_ \_ \_ для вывода сообщения об ошибке для исходного файла, если указанное утверждение не имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3f736-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="3f736-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f736-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f736-131">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3f736-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





