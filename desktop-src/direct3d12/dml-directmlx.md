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
# <a name="directmlx"></a>DirectMLX

Директмлкс — это вспомогательная библиотека C++, предназначенная только для заголовков для Директмл, призванная упростить создание отдельных операторов в графах.

Директмлкс предоставляет удобные оболочки для всех типов операторов Директмл (DML), а также интуитивно понятные перегрузки операторов, что упрощает создание экземпляров DML-операторов и их привязку к сложным графикам.

## <a name="where-to-find-directmlxh"></a>Где найти `DirectMLX.h`

`DirectMLX.h` распространяется в рамках лицензии MIT по с открытым исходным кодом. Последнюю версию можно найти на сайте [Директмл GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).

## <a name="tensor-constraints"></a>Ограничения тензорные

Для Директмлкс требуется версия Директмл 1.4.0 или более новая (см. [Журнал версий директмл](dml-version-history.md#version-table)). Более старые версии Директмл не поддерживаются.

Директмлкс. h требует компилятора с поддержкой C + +11, включая (но не ограничиваясь им):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Обратите внимание, что рекомендуется использовать компилятор C++ 17 (или более поздней версии). Компиляция для C++ 11 возможна, но она требует использования сторонних библиотек (например, [GSL](https://github.com/microsoft/GSL) и [абсеил](https://github.com/abseil/abseil-cpp)) для замены отсутствующих функциональных возможностей стандартной библиотеки.

Если у вас есть конфигурация, которую не удается скомпилировать `DirectMLX.h` , запросите [вопрос на сайте GitHub](https://github.com/microsoft/DirectML/issues).

## <a name="basic-usage"></a>Основное использование

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

Вот еще один пример, который создает граф Директмл, способный вычислить [формулу квадратичного квадрата](https://en.wikipedia.org/wiki/Quadratic_formula).

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

## <a name="more-examples"></a>Дополнительные примеры

Полные примеры использования Директмлкс можно найти в [репозитории Директмл GitHub](https://github.com/microsoft/DirectML/tree/master/Samples).

## <a name="compile-time-options"></a>Параметры времени компиляции

Директмлкс поддерживает #define времени компиляции для настройки различных частей заголовка.

|Параметр|Описание|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Если #define, то вызовет ошибку, `std::abort` а не создает исключение. Это значение определяется по умолчанию, если исключения недоступны (например, если в параметрах компилятора отключены исключения).|
|**DMLX_USE_WIL**|Если #define, то исключения вызываются с помощью типов исключений [библиотеки реализации Windows](https://github.com/microsoft/wil) . В противном случае вместо них используются стандартные типы исключений (например, `std::runtime_error` ). Этот параметр не действует, если определен **DMLX_NO_EXCEPTIONS** .|
|**DMLX_USE_ABSEIL**|Если #define, использует [абсеил](https://github.com/abseil/abseil-cpp) в качестве отбрасывания замен для типов стандартных библиотек, недоступных в c++ 11. К этим типам относятся `absl::optional` (вместо `std::optional` ), `absl::Span` (вместо `std::span` ) и `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Определяет, следует ли использовать [GSL](https://github.com/microsoft/GSL) в качестве замены для `std::span` . Если #define, то использование `std::span` методов заменяется `gsl::span` на компиляторы без собственных `std::span` реализаций. В противном случае вместо нее предоставляется встроенная реализация. Обратите внимание, что этот параметр используется только при компиляции в компиляторе pre-C + 20 без поддержки `std::span` , а также при отсутствии других замещающих замещения стандартной библиотеки (например, абсеил).|

## <a name="controlling-tensor-layout"></a>Управление макетом тензорные

Для большинства операторов Директмлкс выполняет вычисление свойств выходных десятков оператора от вашего имени. Например, при выполнении `dml::Reduce` по осям `{ 0, 2, 3 }` с входными тензорныеами размеров `{ 3, 4, 5, 6 }` директмлкс автоматически вычислит свойства выходного тензорные, включая правильную форму `{ 1, 4, 1, 1 }` .

Однако другие свойства выходного тензорные включают в себя *шаг*, *тоталтенсорсизеинбитес* и *гуарантидбасеоффсеталигнмент*. По умолчанию Директмлкс устанавливает эти свойства таким образом, что тензорные не имеет стридинг, не гарантирует выравнивание базового смещения, а общий размер тензорные в байтах, вычисленный [дмлкалкбуффертенсорсизе](./dml-helper-functions.md#dmlcalcbuffertensorsize).

Директмлкс поддерживает возможность настройки этих выходных свойств тензорные с помощью объектов, известных как *политики тензорные*. **Тенсорполици** — это настраиваемый обратный вызов, который вызывается директмлкс и возвращает выходные свойства тензорные по заданному типу, флагам и размерам данных тензорные.

Политики тензорные могут быть установлены для объекта **DML:: Graph** и будут использоваться для всех последующих операторов на этом графе. Политики тензорные также можно задать непосредственно при создании **тенсордеск**.

Таким образом, макет десятков, созданных Директмлкс, можно контролировать путем установки **тенсорполици** , устанавливающего соответствующий шаг на его десятках.

### <a name="example-1"></a>Пример 1

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

### <a name="example-2"></a>Пример 2

Директмлкс также предоставляет некоторые альтернативные политики тензорные, встроенные в. Например, политика **интерлеаведчаннел** предоставляется для удобства и может использоваться для создания десятков с шагами таким образом, чтобы они были написаны в нхвк порядке.

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>См. также раздел

* [Директмл GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Пример yolov4 Директмлкс](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Использование STRIDE для выражения заполнения и макета памяти](./dml-strides.md)
* [Структура DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc)