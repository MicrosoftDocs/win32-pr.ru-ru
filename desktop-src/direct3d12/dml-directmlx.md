---
title: DirectMLX
description: Директмлкс — это вспомогательная библиотека C++, предназначенная только для заголовков для Директмл, призванная упростить создание отдельных операторов в графах.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: ba7eca27a39b690f678bdac1ea0feba1991e8b40
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521191"
---
# <a name="directmlx"></a><span data-ttu-id="e3bd7-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="e3bd7-103">DirectMLX</span></span>

<span data-ttu-id="e3bd7-104">Директмлкс — это вспомогательная библиотека C++, предназначенная только для заголовков для Директмл, призванная упростить создание отдельных операторов в графах.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="e3bd7-105">Директмлкс предоставляет удобные оболочки для всех типов операторов Директмл (DML), а также интуитивно понятные перегрузки операторов, что упрощает создание экземпляров DML-операторов и их привязку к сложным графикам.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="e3bd7-106">Где найти `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="e3bd7-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="e3bd7-107">`DirectMLX.h` распространяется в рамках лицензии MIT по с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="e3bd7-108">Последнюю версию можно найти на сайте [Директмл GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e3bd7-109">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e3bd7-109">Tensor constraints</span></span>

<span data-ttu-id="e3bd7-110">Для Директмлкс требуется версия Директмл 1.4.0 или более новая (см. [Журнал версий директмл](dml-version-history.md#version-table)).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="e3bd7-111">Более старые версии Директмл не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="e3bd7-112">Директмлкс. h требует компилятора с поддержкой C + +11, включая (но не ограничиваясь им):</span><span class="sxs-lookup"><span data-stu-id="e3bd7-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="e3bd7-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e3bd7-113">Visual Studio 2017</span></span>
* <span data-ttu-id="e3bd7-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="e3bd7-114">Visual Studio 2019</span></span>
* <span data-ttu-id="e3bd7-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="e3bd7-115">Clang 10</span></span>

<span data-ttu-id="e3bd7-116">Обратите внимание, что рекомендуется использовать компилятор C++ 17 (или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-116">Note that a C++17 (or newer) compiler is the option that we recommend.</span></span> <span data-ttu-id="e3bd7-117">Компиляция для C++ 11 возможна, но она требует использования сторонних библиотек (например, [GSL](https://github.com/microsoft/GSL) и [абсеил](https://github.com/abseil/abseil-cpp)) для замены отсутствующих функциональных возможностей стандартной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="e3bd7-118">Если у вас есть конфигурация, которую не удается скомпилировать `DirectMLX.h` , запросите [вопрос на сайте GitHub](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="e3bd7-119">Основное использование</span><span class="sxs-lookup"><span data-stu-id="e3bd7-119">Basic usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="e3bd7-120">Вот еще один пример, который создает граф Директмл, способный вычислить [формулу квадратичного квадрата](https://en.wikipedia.org/wiki/Quadratic_formula).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="e3bd7-121">Дополнительные примеры</span><span class="sxs-lookup"><span data-stu-id="e3bd7-121">More examples</span></span>

<span data-ttu-id="e3bd7-122">Полные примеры использования Директмлкс можно найти в [репозитории Директмл GitHub](https://github.com/microsoft/DirectML/tree/master/Samples).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="e3bd7-123">Параметры времени компиляции</span><span class="sxs-lookup"><span data-stu-id="e3bd7-123">Compile-time options</span></span>

<span data-ttu-id="e3bd7-124">Директмлкс поддерживает #define времени компиляции для настройки различных частей заголовка.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="e3bd7-125">Параметр</span><span class="sxs-lookup"><span data-stu-id="e3bd7-125">Option</span></span>|<span data-ttu-id="e3bd7-126">Описание</span><span class="sxs-lookup"><span data-stu-id="e3bd7-126">Description</span></span>|
|-|-|
|<span data-ttu-id="e3bd7-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="e3bd7-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="e3bd7-128">Если #define, то вызовет ошибку, `std::abort` а не создает исключение.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="e3bd7-129">Это значение определяется по умолчанию, если исключения недоступны (например, если в параметрах компилятора отключены исключения).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="e3bd7-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="e3bd7-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="e3bd7-131">Если #define, то исключения вызываются с помощью типов исключений [библиотеки реализации Windows](https://github.com/microsoft/wil) .</span><span class="sxs-lookup"><span data-stu-id="e3bd7-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="e3bd7-132">В противном случае вместо них используются стандартные типы исключений (например, `std::runtime_error` ).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="e3bd7-133">Этот параметр не действует, если определен **DMLX_NO_EXCEPTIONS** .</span><span class="sxs-lookup"><span data-stu-id="e3bd7-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="e3bd7-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="e3bd7-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="e3bd7-135">Если #define, использует [абсеил](https://github.com/abseil/abseil-cpp) в качестве отбрасывания замен для типов стандартных библиотек, недоступных в c++ 11.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="e3bd7-136">К этим типам относятся `absl::optional` (вместо `std::optional` ), `absl::Span` (вместо `std::span` ) и `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="e3bd7-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="e3bd7-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="e3bd7-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="e3bd7-138">Определяет, следует ли использовать [GSL](https://github.com/microsoft/GSL) в качестве замены для `std::span` .</span><span class="sxs-lookup"><span data-stu-id="e3bd7-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="e3bd7-139">Если #define, то использование `std::span` методов заменяется `gsl::span` на компиляторы без собственных `std::span` реализаций.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="e3bd7-140">В противном случае вместо нее предоставляется встроенная реализация.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="e3bd7-141">Обратите внимание, что этот параметр используется только при компиляции в компиляторе pre-C + 20 без поддержки `std::span` , а также при отсутствии других замещающих замещения стандартной библиотеки (например, абсеил).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="e3bd7-142">Управление макетом тензорные</span><span class="sxs-lookup"><span data-stu-id="e3bd7-142">Controlling tensor layout</span></span>

<span data-ttu-id="e3bd7-143">Для большинства операторов Директмлкс выполняет вычисление свойств выходных десятков оператора от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="e3bd7-144">Например, при выполнении `dml::Reduce` по осям `{ 0, 2, 3 }` с входными тензорныеами размеров `{ 3, 4, 5, 6 }` директмлкс автоматически вычислит свойства выходного тензорные, включая правильную форму `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="e3bd7-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="e3bd7-145">Однако другие свойства выходного тензорные включают в себя *шаг*, *тоталтенсорсизеинбитес* и *гуарантидбасеоффсеталигнмент*.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="e3bd7-146">По умолчанию Директмлкс устанавливает эти свойства таким образом, что тензорные не имеет стридинг, не гарантирует выравнивание базового смещения, а общий размер тензорные в байтах, вычисленный [дмлкалкбуффертенсорсизе](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span><span class="sxs-lookup"><span data-stu-id="e3bd7-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="e3bd7-147">Директмлкс поддерживает возможность настройки этих выходных свойств тензорные с помощью объектов, известных как *политики тензорные*.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="e3bd7-148">**Тенсорполици** — это настраиваемый обратный вызов, который вызывается директмлкс и возвращает выходные свойства тензорные по заданному типу, флагам и размерам данных тензорные.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="e3bd7-149">Политики тензорные могут быть установлены для объекта **DML:: Graph** и будут использоваться для всех последующих операторов на этом графе.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-149">Tensor policies can be set on the **dml::Graph** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="e3bd7-150">Политики тензорные также можно задать непосредственно при создании **тенсордеск**.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="e3bd7-151">Таким образом, макет десятков, созданных Директмлкс, можно контролировать путем установки **тенсорполици** , устанавливающего соответствующий шаг на его десятках.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="e3bd7-152">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3bd7-152">Example 1</span></span>

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="e3bd7-153">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e3bd7-153">Example 2</span></span>

<span data-ttu-id="e3bd7-154">Директмлкс также предоставляет некоторые альтернативные политики тензорные, встроенные в.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="e3bd7-155">Например, политика **интерлеаведчаннел** предоставляется для удобства и может использоваться для создания десятков с шагами таким образом, чтобы они были написаны в нхвк порядке.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="e3bd7-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3bd7-156">See also</span></span>

* [<span data-ttu-id="e3bd7-157">Директмл GitHub</span><span class="sxs-lookup"><span data-stu-id="e3bd7-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="e3bd7-158">Пример yolov4 Директмлкс</span><span class="sxs-lookup"><span data-stu-id="e3bd7-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="e3bd7-159">Использование STRIDE для выражения заполнения и макета памяти</span><span class="sxs-lookup"><span data-stu-id="e3bd7-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="e3bd7-160">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="e3bd7-160">DML_GRAPH_DESC structure</span></span>](/windows/win32/api/directml/ns-directml-dml_graph_desc)