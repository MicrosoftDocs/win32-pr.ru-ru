---
title: Direct2D политики обработки ошибок
description: В этом разделе описываются политики обработки ошибок Direct2D. В него входят следующие разделы.
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, обработка ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987794"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="9645a-105">Direct2D политики обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="9645a-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="9645a-106">В этом разделе описываются политики обработки ошибок Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9645a-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="9645a-107">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="9645a-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="9645a-108">Использование HRESULT</span><span class="sxs-lookup"><span data-stu-id="9645a-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="9645a-109">Возвращаемое значение пакетных функций</span><span class="sxs-lookup"><span data-stu-id="9645a-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="9645a-110">Недопустимые входные данные</span><span class="sxs-lookup"><span data-stu-id="9645a-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="9645a-111">Указатель вывода</span><span class="sxs-lookup"><span data-stu-id="9645a-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="9645a-112">Обязательный параметр</span><span class="sxs-lookup"><span data-stu-id="9645a-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="9645a-113">NaN и плохо упорядоченные входные ПРЯМОУГОЛЬНИКи</span><span class="sxs-lookup"><span data-stu-id="9645a-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="9645a-114">NaN в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="9645a-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="9645a-115">Плохо упорядоченные входные ПРЯМОУГОЛЬНИКи</span><span class="sxs-lookup"><span data-stu-id="9645a-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="9645a-116">Использование HRESULT</span><span class="sxs-lookup"><span data-stu-id="9645a-116">Use of HRESULT</span></span>

<span data-ttu-id="9645a-117">Если функция не пакетирована и может иметь сбой во время выполнения, она должна возвращать **HRESULT** , чтобы указать на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9645a-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="9645a-118">Сбой во время выполнения — это любая ошибка, которую невозможно избежать во время разработки, например нехваткой памяти.</span><span class="sxs-lookup"><span data-stu-id="9645a-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="9645a-119">Возвращаемое значение пакетных функций</span><span class="sxs-lookup"><span data-stu-id="9645a-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="9645a-120">Пакетные функции в Direct2D — это функции, которые обрабатываются как единое целое при вызове [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="9645a-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="9645a-121">Они являются командами рисования между [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) и **EndDraw** или командами в [**жеометрисинк**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="9645a-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="9645a-122">Для этих функций в момент завершения пакета выводятся ошибки.</span><span class="sxs-lookup"><span data-stu-id="9645a-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="9645a-123">Ошибка возвращается после **EndDraw** для команд рисования и после **закрытия** для **жеометрисинк**.</span><span class="sxs-lookup"><span data-stu-id="9645a-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="9645a-124">Рендертаржетс прерывать прорисовку, если задано состояние ошибки, но приложение может вызвать [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) для сброса состояния ошибки и возобновления рисования.</span><span class="sxs-lookup"><span data-stu-id="9645a-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="9645a-125">Функции **Get** и **Set** не имеют возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9645a-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="9645a-126">Однако если функция **набора** содержит недопустимые входные данные, отладочный слой создает сообщение.</span><span class="sxs-lookup"><span data-stu-id="9645a-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="9645a-127">В этом случае состояние ошибки не задано и функция **Set** не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="9645a-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="9645a-128">Недопустимые входные данные</span><span class="sxs-lookup"><span data-stu-id="9645a-128">Invalid Input</span></span>

<span data-ttu-id="9645a-129">Direct2D разыменование указателей вывода и обязательных параметров, которые приводят к нарушениям прав доступа, если указатели являются недопустимыми или **равны NULL**.</span><span class="sxs-lookup"><span data-stu-id="9645a-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="9645a-130">Указатель вывода</span><span class="sxs-lookup"><span data-stu-id="9645a-130">Output Pointer</span></span>

<span data-ttu-id="9645a-131">Direct2D разыменование выходного указателя и присваивает его **значению NULL** сразу после ввода функции.</span><span class="sxs-lookup"><span data-stu-id="9645a-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="9645a-132">Это вызывает нарушение прав доступа, если вызывающий объект передает значение **null** в качестве указателя на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="9645a-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="9645a-133">Эта политика также применяется к массивам указателей.</span><span class="sxs-lookup"><span data-stu-id="9645a-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="9645a-134">Для других выходных параметров, таких как структура, разыменование происходит позже, а также приводит к нарушению прав доступа.</span><span class="sxs-lookup"><span data-stu-id="9645a-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="9645a-135">Однако существуют некоторые методы с необязательными выходными указателями (т. е. [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)), которые не вызывают нарушение прав доступа.</span><span class="sxs-lookup"><span data-stu-id="9645a-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="9645a-136">Обязательный параметр</span><span class="sxs-lookup"><span data-stu-id="9645a-136">Required Parameter</span></span>

<span data-ttu-id="9645a-137">Если **значение NULL** передается любой функции, для которой требуется допустимое значение, функция разыменование неверного указателя на ранних этапах, что приводит к нарушению прав доступа.</span><span class="sxs-lookup"><span data-stu-id="9645a-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="9645a-138">Для необязательных входных параметров значение **null** является допустимым значением, что приводит к некоторым разумным значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9645a-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="9645a-139">NaN и плохо упорядоченные входные ПРЯМОУГОЛЬНИКи</span><span class="sxs-lookup"><span data-stu-id="9645a-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="9645a-140">В Direct2D значение NaN считается допустимым входным и плохо упорядоченным входным ПРЯМОУГОЛЬНИКом.</span><span class="sxs-lookup"><span data-stu-id="9645a-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="9645a-141">NaN в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="9645a-141">NaN as Input</span></span>

<span data-ttu-id="9645a-142">NaN считается допустимым входом, хотя обычно он приводит к примитиву, содержащему нерисовку NaN.</span><span class="sxs-lookup"><span data-stu-id="9645a-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="9645a-143">API Direct2D не предоставляет явную фильтрацию NaN для проверки входных данных.</span><span class="sxs-lookup"><span data-stu-id="9645a-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="9645a-144">Плохо упорядоченные входные ПРЯМОУГОЛЬНИКи</span><span class="sxs-lookup"><span data-stu-id="9645a-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="9645a-145">Плохо упорядоченные входные ПРЯМОУГОЛЬНИКи сортируются так, чтобы они правильно указали верхние, левые и нижние углы.</span><span class="sxs-lookup"><span data-stu-id="9645a-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="9645a-146">Для выходных данных пустые прямоугольники выглядят следующим образом: {Infinity, Infinity, Флоатмакс, Флоатмакс}.</span><span class="sxs-lookup"><span data-stu-id="9645a-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 