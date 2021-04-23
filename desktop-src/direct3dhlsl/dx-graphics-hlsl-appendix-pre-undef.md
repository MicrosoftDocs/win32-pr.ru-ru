---
title: " Директива undef"
description: Директива препроцессора, которая удаляет текущее определение константы или макроса, который был ранее определен с помощью директивы \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Директива undef HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334032"
---
# <a name="undef-directive"></a><span data-ttu-id="760bc-104">\#Директива undef</span><span class="sxs-lookup"><span data-stu-id="760bc-104">\#undef Directive</span></span>

<span data-ttu-id="760bc-105">Директива препроцессора, которая удаляет текущее определение константы или макроса, который был ранее определен с помощью директивы [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .</span><span class="sxs-lookup"><span data-stu-id="760bc-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="760bc-106">\#*идентификатор* undef</span><span class="sxs-lookup"><span data-stu-id="760bc-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="760bc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="760bc-107">Parameters</span></span>



| <span data-ttu-id="760bc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="760bc-108">Item</span></span>                                                                              | <span data-ttu-id="760bc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="760bc-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="760bc-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*Идентификатор*</span><span class="sxs-lookup"><span data-stu-id="760bc-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="760bc-111">Идентификатор константы или макроса, определение которых необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="760bc-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="760bc-112">Если вы не определяете макрос, укажите только идентификатор, а не список параметров.</span><span class="sxs-lookup"><span data-stu-id="760bc-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="760bc-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="760bc-113">Remarks</span></span>

<span data-ttu-id="760bc-114">\#Директиву undef можно применить к идентификатору, не имеющему предыдущего определения. Это гарантирует, что идентификатор не определен.</span><span class="sxs-lookup"><span data-stu-id="760bc-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="760bc-115">Замена макросов не выполняется в \# операторах undef.</span><span class="sxs-lookup"><span data-stu-id="760bc-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="760bc-116">\#Директива undef обычно объединяется с директивой [ \# define](dx-graphics-hlsl-appendix-pre-define.md) для создания области в исходной программе, в которой идентификатор имеет специальное значение.</span><span class="sxs-lookup"><span data-stu-id="760bc-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="760bc-117">Например, определенная функция программы-источника может использовать константы манифестов для определения значений среды, которые не влияют на остальные части программы.</span><span class="sxs-lookup"><span data-stu-id="760bc-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="760bc-118">\#Директива undef также работает с директивой [) для управления условной компиляцией исходной программы.</span><span class="sxs-lookup"><span data-stu-id="760bc-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="760bc-119">Константы и макросы могут быть неопределенными из командной строки с помощью параметра/U, за которыми следуют идентификаторы, которые должны быть неопределенными.</span><span class="sxs-lookup"><span data-stu-id="760bc-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="760bc-120">Это эквивалентно добавлению последовательности \# директив undef в начало исходного файла.</span><span class="sxs-lookup"><span data-stu-id="760bc-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="760bc-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="760bc-121">Examples</span></span>

<span data-ttu-id="760bc-122">В следующем примере показано, как использовать \# директиву undef для удаления определений символьной константы и макроса.</span><span class="sxs-lookup"><span data-stu-id="760bc-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="760bc-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="760bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760bc-124">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="760bc-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="760bc-125">\#Директива define (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="760bc-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="760bc-126">\#Если,)</span><span class="sxs-lookup"><span data-stu-id="760bc-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





