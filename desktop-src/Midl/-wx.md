---
title: Параметр/WX
description: Параметр/WX предписывает компилятору MIDL обрабатывал все ошибки на заданном уровне предупреждения как ошибки.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- MIDL с параметром/WX
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889739"
---
# <a name="wx-switch"></a><span data-ttu-id="983e9-104">Параметр/WX</span><span class="sxs-lookup"><span data-stu-id="983e9-104">/WX switch</span></span>

<span data-ttu-id="983e9-105">Параметр **/WX** предписывает КОМПИЛЯТОРу MIDL обрабатывал все ошибки на заданном уровне предупреждения как ошибки.</span><span class="sxs-lookup"><span data-stu-id="983e9-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="983e9-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="983e9-106">Switch Options</span></span>

<span data-ttu-id="983e9-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="983e9-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="983e9-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="983e9-108">Remarks</span></span>

<span data-ttu-id="983e9-109">Если указан параметр **/WX** и не указан параметр [**/w**](-w.md)*n* , все предупреждения на уровне по умолчанию (уровень 1) обрабатываются как ошибки.</span><span class="sxs-lookup"><span data-stu-id="983e9-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="983e9-110">Параметр [**/w**](-w.md)*n* указывает компилятору отображать все предупреждения на уровне *n* и **/WX** , чтобы компилятор обрабатывал все предупреждения как ошибки.</span><span class="sxs-lookup"><span data-stu-id="983e9-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="983e9-111">Сочетание этих двух параметров указывает компилятору на то, что все предупреждения на уровне *n* обрабатывались как ошибки.</span><span class="sxs-lookup"><span data-stu-id="983e9-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="983e9-112">Ошибки отличаются от предупреждений.</span><span class="sxs-lookup"><span data-stu-id="983e9-112">Errors are different from warnings.</span></span> <span data-ttu-id="983e9-113">Ошибки приводят к остановке обработки IDL-файла компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="983e9-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="983e9-114">Предупреждения вызывают вывод информационного сообщения компилятором MIDL и продолжение обработки IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="983e9-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="983e9-115">Предупреждение. нулевой уровень (0) указывает компилятору MIDL отключить сведения о предупреждениях.</span><span class="sxs-lookup"><span data-stu-id="983e9-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="983e9-116">При объединении ключей **/W0** и **/WX** компилятор MIDL подавляет все сведения о предупреждениях.</span><span class="sxs-lookup"><span data-stu-id="983e9-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="983e9-117">В этом случае параметр **/WX** не действует.</span><span class="sxs-lookup"><span data-stu-id="983e9-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="983e9-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="983e9-118">Examples</span></span>

<span data-ttu-id="983e9-119">**MIDL/WX filename. idl**</span><span class="sxs-lookup"><span data-stu-id="983e9-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="983e9-120">**MIDL/W3/WX filename. idl**</span><span class="sxs-lookup"><span data-stu-id="983e9-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="983e9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="983e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983e9-122">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="983e9-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="983e9-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="983e9-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 




