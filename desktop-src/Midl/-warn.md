---
title: Параметр/warn
description: Параметр/warn указывает уровень предупреждений компилятора MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- Параметр/warn MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783735"
---
# <a name="warn-switch"></a><span data-ttu-id="c2090-104">Параметр/warn</span><span class="sxs-lookup"><span data-stu-id="c2090-104">/warn switch</span></span>

<span data-ttu-id="c2090-105">Параметр **/warn** указывает уровень предупреждений компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="c2090-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="c2090-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="c2090-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c2090-107">*level*</span><span class="sxs-lookup"><span data-stu-id="c2090-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="c2090-108">Задает уровень предупреждений — целое число в диапазоне от 0 до 4.</span><span class="sxs-lookup"><span data-stu-id="c2090-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="c2090-109">Между параметром **/warn** нет пробелов и цифр, указывающих на значение уровня предупреждения.</span><span class="sxs-lookup"><span data-stu-id="c2090-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2090-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2090-110">Remarks</span></span>

<span data-ttu-id="c2090-111">Уровень предупреждения указывает на серьезность предупреждения.</span><span class="sxs-lookup"><span data-stu-id="c2090-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="c2090-112">Уровни предупреждений находятся в диапазоне от 1 до 4 и имеют нулевое значение для вывода сведений о предупреждении.</span><span class="sxs-lookup"><span data-stu-id="c2090-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="c2090-113">Самым высоким уровнем серьезности предупреждения является уровень 1.</span><span class="sxs-lookup"><span data-stu-id="c2090-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="c2090-114">В следующей таблице описаны предупреждения для каждого уровня предупреждений.</span><span class="sxs-lookup"><span data-stu-id="c2090-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="c2090-115">Уровень предупреждений</span><span class="sxs-lookup"><span data-stu-id="c2090-115">Warning level</span></span> | <span data-ttu-id="c2090-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c2090-116">Description</span></span>                                             | <span data-ttu-id="c2090-117">Пример</span><span class="sxs-lookup"><span data-stu-id="c2090-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c2090-118">0</span><span class="sxs-lookup"><span data-stu-id="c2090-118">0</span></span>             | <span data-ttu-id="c2090-119">Нет предупреждений.</span><span class="sxs-lookup"><span data-stu-id="c2090-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="c2090-120">1</span><span class="sxs-lookup"><span data-stu-id="c2090-120">1</span></span>             | <span data-ttu-id="c2090-121">Серьезные предупреждения, которые могут вызвать ошибки приложения.</span><span class="sxs-lookup"><span data-stu-id="c2090-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="c2090-122">Не заданы обработчики привязки, неатрибуты указатели, конфликтующие переключатели.</span><span class="sxs-lookup"><span data-stu-id="c2090-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="c2090-123">2</span><span class="sxs-lookup"><span data-stu-id="c2090-123">2</span></span>             | <span data-ttu-id="c2090-124">Может вызвать проблемы в операционной среде пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2090-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="c2090-125">Длина идентификатора превышает 31 символ.</span><span class="sxs-lookup"><span data-stu-id="c2090-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="c2090-126">Не указана ARM объединения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2090-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="c2090-127">3</span><span class="sxs-lookup"><span data-stu-id="c2090-127">3</span></span>             | <span data-ttu-id="c2090-128">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c2090-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="c2090-129">4</span><span class="sxs-lookup"><span data-stu-id="c2090-129">4</span></span>             | <span data-ttu-id="c2090-130">Самый низкий уровень предупреждений.</span><span class="sxs-lookup"><span data-stu-id="c2090-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="c2090-131">Конструкции C, отличные от ANSI.</span><span class="sxs-lookup"><span data-stu-id="c2090-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="c2090-132">Предупреждения отличаются от ошибок.</span><span class="sxs-lookup"><span data-stu-id="c2090-132">Warnings are different from errors.</span></span> <span data-ttu-id="c2090-133">Ошибки приводят к остановке обработки IDL-файла компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="c2090-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="c2090-134">Предупреждения вызывают вывод информационного сообщения компилятором MIDL и продолжение обработки IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="c2090-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="c2090-135">Уровень предупреждений, заданный параметром **/warn** , можно использовать с параметром [**WX**](-wx.md) , чтобы компилятор MIDL мог остановить обработку IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="c2090-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="c2090-136">Параметр **/warn** ведет себя так же, как параметр [**/w**](-w.md) .</span><span class="sxs-lookup"><span data-stu-id="c2090-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="c2090-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="c2090-137">Examples</span></span>

<span data-ttu-id="c2090-138">**MIDL/warn2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c2090-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="c2090-139">**MIDL/warn4 Bar. idl**</span><span class="sxs-lookup"><span data-stu-id="c2090-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c2090-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2090-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2090-141">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="c2090-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




