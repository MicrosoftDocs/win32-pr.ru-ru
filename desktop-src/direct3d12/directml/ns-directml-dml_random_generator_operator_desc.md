---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Заполняет выходной тензорные с помощью детерминированно сформированных псевдослучайных и единообразно распределенных битов. Этот оператор также может выводить обновленное внутреннее состояние генератора, которое можно использовать при последующих выполнениях оператора.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804068"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="e2eca-104">Структура DML_RANDOM_GENERATOR_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e2eca-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e2eca-105">Заполняет выходной тензорные с помощью детерминированно сформированных псевдослучайных и единообразно распределенных битов.</span><span class="sxs-lookup"><span data-stu-id="e2eca-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="e2eca-106">Этот оператор также может выводить обновленное внутреннее состояние генератора, которое можно использовать при последующих выполнениях оператора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="e2eca-107">Этот оператор является детерминированным и ведет себя так, как если бы он был чистой функцией, &mdash; т. е. ее выполнение не дает никаких побочных эффектов и не использует глобальное состояние.</span><span class="sxs-lookup"><span data-stu-id="e2eca-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="e2eca-108">Выходные данные псевдо-Random, создаваемые этим оператором, зависят только от значений, предоставленных в *инпутстатетенсор*.</span><span class="sxs-lookup"><span data-stu-id="e2eca-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="e2eca-109">Генераторы, реализованные этим оператором, не защищают криптографически. Поэтому этот оператор не следует использовать для шифрования, создания ключа или других приложений, которым требуется криптографически защищенное формирование случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="e2eca-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2eca-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="e2eca-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e2eca-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e2eca-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2eca-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2eca-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="e2eca-113">Члены</span><span class="sxs-lookup"><span data-stu-id="e2eca-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="e2eca-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e2eca-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e2eca-115">Входной тензорные, содержащий внутреннее состояние генератора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="e2eca-116">Размер и формат этого входного тензорные зависит от [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span><span class="sxs-lookup"><span data-stu-id="e2eca-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="e2eca-117">Для **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** этот тензорные должен иметь тип **UINT32** и иметь размеры `{1,1,1,6}` .</span><span class="sxs-lookup"><span data-stu-id="e2eca-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="e2eca-118">Первые 4 32-битные значения содержат монотонно увеличивающийся 128-разрядный счетчик.</span><span class="sxs-lookup"><span data-stu-id="e2eca-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="e2eca-119">Последние 2 32-битные значения содержат 64-разрядное значение ключа для генератора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="e2eca-120">При первой инициализации входного состояния генератора, как правило, 128-разрядный счетчик (первые 4 32-разрядные значения UINT32) должен быть инициализирован равным 0.</span><span class="sxs-lookup"><span data-stu-id="e2eca-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="e2eca-121">Ключ можно произвольно выбрать; различные значения ключа будут формировать различные последовательности чисел.</span><span class="sxs-lookup"><span data-stu-id="e2eca-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="e2eca-122">Значение для ключа обычно создается с помощью предоставленного пользователем *начального значения*.</span><span class="sxs-lookup"><span data-stu-id="e2eca-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="e2eca-123">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e2eca-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e2eca-124">Выходной тензорные, содержащий результирующие псевдо-случайные значения.</span><span class="sxs-lookup"><span data-stu-id="e2eca-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="e2eca-125">Этот тензорные может иметь любой размер.</span><span class="sxs-lookup"><span data-stu-id="e2eca-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="e2eca-126">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e2eca-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e2eca-127">Необязательный выходной тензорные, содержащий обновленное состояние внутреннего генератора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="e2eca-128">Если оно указано, этот оператор использует *инпутстатетенсор* для вычисления соответствующего обновленного состояния генератора и записывает результат в *аутпутстатетенсор*.</span><span class="sxs-lookup"><span data-stu-id="e2eca-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="e2eca-129">Как правило, вызывающие объекты сохраняют этот результат и передают его в качестве входного состояния при последующем выполнении этого оператора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="e2eca-130">Тип: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="e2eca-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="e2eca-131">Одно из значений перечисления [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , указывающее тип используемого генератора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="e2eca-132">В настоящее время единственным допустимым значением является **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, которое создает псевдо-случайные числа в соответствии с [алгоритмом филокс 4X32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span><span class="sxs-lookup"><span data-stu-id="e2eca-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2eca-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2eca-133">Remarks</span></span>
<span data-ttu-id="e2eca-134">При каждом выполнении этого оператора необходимо увеличить 128-разрядный счетчик.</span><span class="sxs-lookup"><span data-stu-id="e2eca-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="e2eca-135">Если указан параметр *аутпутстатетенсор* , этот оператор увеличивает значение счетчика с правильным значением от вашего имени и записывает результат в *аутпутстатетенсор*.</span><span class="sxs-lookup"><span data-stu-id="e2eca-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="e2eca-136">Объем, на который он должен увеличиваться, зависит от числа формируемых 32-разрядных выходных элементов и типа генератора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="e2eca-137">Для **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** значение счетчика 128-bit должно увеличиваться при `ceil(outputSize / 4)` каждом выполнении, где `outputSize` — число элементов в *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e2eca-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="e2eca-138">Рассмотрим пример, где значение счетчика 128-разрядов в настоящее время равно `0x48656c6c'6f46726f'6d536561'74746c65` , а размер аутпуттенсор — `{3,3,20,7219}` .</span><span class="sxs-lookup"><span data-stu-id="e2eca-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="e2eca-139">После однократного выполнения этого оператора счетчик должен увеличиваться на 324 855 (число элементов вывода, формируемых на 4, округляя вверх), в результате чего получается значение счетчика `0x48656c6c'6f46726f'6d536561'746f776e` .</span><span class="sxs-lookup"><span data-stu-id="e2eca-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="e2eca-140">Это обновленное значение затем должно быть указано в качестве входных данных для следующего выполнения этого оператора.</span><span class="sxs-lookup"><span data-stu-id="e2eca-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="e2eca-141">Доступность</span><span class="sxs-lookup"><span data-stu-id="e2eca-141">Availability</span></span>
<span data-ttu-id="e2eca-142">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e2eca-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e2eca-143">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e2eca-143">Tensor constraints</span></span>
<span data-ttu-id="e2eca-144">`InputStateTensor` и `OutputStateTensor` должны иметь одинаковые *размеры*.</span><span class="sxs-lookup"><span data-stu-id="e2eca-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e2eca-145">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e2eca-145">Tensor support</span></span>
| <span data-ttu-id="e2eca-146">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e2eca-146">Tensor</span></span> | <span data-ttu-id="e2eca-147">Вид</span><span class="sxs-lookup"><span data-stu-id="e2eca-147">Kind</span></span> | <span data-ttu-id="e2eca-148">Измерения</span><span class="sxs-lookup"><span data-stu-id="e2eca-148">Dimensions</span></span> | <span data-ttu-id="e2eca-149">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e2eca-149">Supported dimension counts</span></span> | <span data-ttu-id="e2eca-150">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e2eca-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e2eca-151">инпутстатетенсор</span><span class="sxs-lookup"><span data-stu-id="e2eca-151">InputStateTensor</span></span> | <span data-ttu-id="e2eca-152">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e2eca-152">Input</span></span> | <span data-ttu-id="e2eca-153">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="e2eca-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="e2eca-154">4</span><span class="sxs-lookup"><span data-stu-id="e2eca-154">4</span></span> | <span data-ttu-id="e2eca-155">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="e2eca-155">UINT32</span></span> |
| <span data-ttu-id="e2eca-156">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e2eca-156">OutputTensor</span></span> | <span data-ttu-id="e2eca-157">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e2eca-157">Output</span></span> | <span data-ttu-id="e2eca-158">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="e2eca-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="e2eca-159">4</span><span class="sxs-lookup"><span data-stu-id="e2eca-159">4</span></span> | <span data-ttu-id="e2eca-160">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="e2eca-160">UINT32</span></span> |
| <span data-ttu-id="e2eca-161">аутпутстатетенсор</span><span class="sxs-lookup"><span data-stu-id="e2eca-161">OutputStateTensor</span></span> | <span data-ttu-id="e2eca-162">Необязательный вывод</span><span class="sxs-lookup"><span data-stu-id="e2eca-162">Optional output</span></span> | <span data-ttu-id="e2eca-163">{1, 1, 1, 6}</span><span class="sxs-lookup"><span data-stu-id="e2eca-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="e2eca-164">4</span><span class="sxs-lookup"><span data-stu-id="e2eca-164">4</span></span> | <span data-ttu-id="e2eca-165">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="e2eca-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="e2eca-166">Требования</span><span class="sxs-lookup"><span data-stu-id="e2eca-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e2eca-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="e2eca-167">**Header**</span></span> | <span data-ttu-id="e2eca-168">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e2eca-168">directml.h</span></span> |