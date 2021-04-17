---
title: Параметр/w
description: Параметр/W указывает уровень предупреждений компилятора MIDL. Уровень предупреждения указывает на серьезность предупреждения.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- Параметр/w MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681542"
---
# <a name="w-switch"></a><span data-ttu-id="6d439-105">Параметр/w</span><span class="sxs-lookup"><span data-stu-id="6d439-105">/W switch</span></span>

<span data-ttu-id="6d439-106">Параметр **/w** указывает уровень предупреждений компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="6d439-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="6d439-107">Уровень предупреждения указывает на серьезность предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6d439-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="6d439-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="6d439-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6d439-109">*level*</span><span class="sxs-lookup"><span data-stu-id="6d439-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="6d439-110">Задает уровень предупреждений — целое число в диапазоне от 0 до 4.</span><span class="sxs-lookup"><span data-stu-id="6d439-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="6d439-111">Между параметром **/w** нет пробелов и цифрой, указывающей на значение уровня предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6d439-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d439-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d439-112">Remarks</span></span>

<span data-ttu-id="6d439-113">Уровни предупреждений находятся в диапазоне от 1 до 4 и имеют нулевое значение для вывода сведений о предупреждении.</span><span class="sxs-lookup"><span data-stu-id="6d439-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="6d439-114">Предупреждение о наивысшей серьезности имеет уровень 1.</span><span class="sxs-lookup"><span data-stu-id="6d439-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="6d439-115">В следующей таблице описаны предупреждения для каждого уровня предупреждений.</span><span class="sxs-lookup"><span data-stu-id="6d439-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="6d439-116">Уровень предупреждений</span><span class="sxs-lookup"><span data-stu-id="6d439-116">Warning level</span></span> | <span data-ttu-id="6d439-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6d439-117">Description</span></span>                                             | <span data-ttu-id="6d439-118">Пример</span><span class="sxs-lookup"><span data-stu-id="6d439-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6d439-119">W0</span><span class="sxs-lookup"><span data-stu-id="6d439-119">W0</span></span>            | <span data-ttu-id="6d439-120">Нет предупреждений.</span><span class="sxs-lookup"><span data-stu-id="6d439-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="6d439-121">W1</span><span class="sxs-lookup"><span data-stu-id="6d439-121">W1</span></span>            | <span data-ttu-id="6d439-122">Серьезные предупреждения, которые могут вызвать ошибки приложения.</span><span class="sxs-lookup"><span data-stu-id="6d439-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="6d439-123">Не заданы обработчики привязки, неатрибуты указатели, конфликтующие переключатели.</span><span class="sxs-lookup"><span data-stu-id="6d439-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="6d439-124">W2</span><span class="sxs-lookup"><span data-stu-id="6d439-124">W2</span></span>            | <span data-ttu-id="6d439-125">Может вызвать проблемы в операционной среде пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d439-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="6d439-126">Длина идентификатора превышает 31 символ.</span><span class="sxs-lookup"><span data-stu-id="6d439-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="6d439-127">Не указана ARM объединения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d439-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="6d439-128">W3</span><span class="sxs-lookup"><span data-stu-id="6d439-128">W3</span></span>            | <span data-ttu-id="6d439-129">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="6d439-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="6d439-130">W4</span><span class="sxs-lookup"><span data-stu-id="6d439-130">W4</span></span>            | <span data-ttu-id="6d439-131">Самый низкий уровень предупреждений.</span><span class="sxs-lookup"><span data-stu-id="6d439-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="6d439-132">Конструкции C, отличные от ANSI.</span><span class="sxs-lookup"><span data-stu-id="6d439-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="6d439-133">Предупреждения отличаются от ошибок.</span><span class="sxs-lookup"><span data-stu-id="6d439-133">Warnings are different from errors.</span></span> <span data-ttu-id="6d439-134">Ошибки приводят к остановке обработки IDL-файла компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="6d439-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="6d439-135">Предупреждения вызывают вывод информационного сообщения компилятором MIDL и продолжение обработки IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="6d439-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="6d439-136">Уровень предупреждений, заданный параметром **/w** , можно использовать с параметром [**/WX**](-wx.md) , чтобы компилятор MIDL приостановить обработку IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="6d439-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="6d439-137">Параметр **/w** ведет себя так же, как параметр [**/warn**](-warn.md) .</span><span class="sxs-lookup"><span data-stu-id="6d439-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="6d439-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="6d439-138">Examples</span></span>

<span data-ttu-id="6d439-139">**MIDL/W2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="6d439-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="6d439-140">**MIDL/W4 Bar. idl**</span><span class="sxs-lookup"><span data-stu-id="6d439-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6d439-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d439-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d439-142">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="6d439-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6d439-143">**/warn**</span><span class="sxs-lookup"><span data-stu-id="6d439-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




