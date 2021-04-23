---
title: cstruct_out Switch
description: Параметр/cstruct_out изменяет определение COM-интерфейса, которое возвращает структуры в соответствии с интерфейсом ABI, предоставляемым разработчиком C++.
keywords:
- /cstruct_out параметр MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103892858"
---
# <a name="cstruct_out-switch"></a><span data-ttu-id="e3f9a-104">/кструкт \_ out</span><span class="sxs-lookup"><span data-stu-id="e3f9a-104">/cstruct\_out switch</span></span>

<span data-ttu-id="e3f9a-105">Этот параметр изменяет определение C COM-интерфейса, которое возвращает структуры в соответствии с интерфейсом ABI, предоставляемым разработчиком C++.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="e3f9a-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="e3f9a-106">Switch Options</span></span>

<span data-ttu-id="e3f9a-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f9a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3f9a-108">Remarks</span></span>

<span data-ttu-id="e3f9a-109">Некоторые определения интерфейсов (особенно в `d3d12.idl` ) содержат `__stdcall` методы, возвращающие структуры.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="e3f9a-110">C и C++ ABI от КОМПИЛЯТОРОМ MSVC отличаются тем, как они реализуют такие функции:</span><span class="sxs-lookup"><span data-stu-id="e3f9a-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="e3f9a-111">C рассматривает их как обычные функции, которые принимают скрытый `this` указатель в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="e3f9a-112">Компилятор применяет небольшую структуру оптимизации структуры, которая позволяет использовать структуры размером менее 8 байт (или больше, если все значения являются плавающей запятой), возвращаемые в регистрах.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="e3f9a-113">Только крупные структуры продвигаются для использования скрытого параметра и возвращаемого вызывающего объекта значения.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="e3f9a-114">C++ обрабатывает их как функции членов.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-114">C++ treats them as member functions.</span></span> <span data-ttu-id="e3f9a-115">Компилятор *всегда* делает это путем вставки скрытого параметра (указателя на возвращаемое вызывающим объектом значение) в качестве второго параметра после `this` указателя.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="e3f9a-116">Он также возвращает тот же указатель, что и возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="e3f9a-117">Этот параметр заставляет определение C интерфейсов в результирующем заголовке предположить, что разработчик использует C++, а код на языке C должен явно использовать интерфейс ABI C++.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="e3f9a-118">Это означает, что функция включает скрытый параметр для указателя возвращаемого значения и возвращает этот указатель вместо структуры напрямую.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3f9a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3f9a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f9a-120">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="e3f9a-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
