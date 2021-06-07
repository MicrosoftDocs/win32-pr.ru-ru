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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417460"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>Структура DML_RANDOM_GENERATOR_OPERATOR_DESC (директмл. h)

Заполняет выходной тензорные с помощью детерминированно сформированных псевдослучайных и единообразно распределенных битов. Этот оператор также может выводить обновленное внутреннее состояние генератора, которое можно использовать при последующих выполнениях оператора.

Этот оператор является детерминированным и ведет себя так, как если бы он был чистой функцией, &mdash; т. е. ее выполнение не дает никаких побочных эффектов и не использует глобальное состояние. Выходные данные псевдо-Random, создаваемые этим оператором, зависят только от значений, предоставленных в *инпутстатетенсор*.

Генераторы, реализованные этим оператором, не защищают криптографически. Поэтому этот оператор не следует использовать для шифрования, создания ключа или других приложений, которым требуется криптографически защищенное формирование случайных чисел.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>Участники

`InputStateTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные, содержащий внутреннее состояние генератора. Размер и формат этого входного тензорные зависит от [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).

Для **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** этот тензорные должен иметь тип **UINT32** и иметь размеры `{1,1,1,6}` . Первые 4 32-битные значения содержат монотонно увеличивающийся 128-разрядный счетчик. Последние 2 32-битные значения содержат 64-разрядное значение ключа для генератора.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

При первой инициализации входного состояния генератора, как правило, 128-разрядный счетчик (первые 4 32-разрядные значения UINT32) должен быть инициализирован равным 0. Ключ можно произвольно выбрать; различные значения ключа будут формировать различные последовательности чисел. Значение для ключа обычно создается с помощью предоставленного пользователем *начального значения*.

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий результирующие псевдо-случайные значения. Этот тензорные может иметь любой размер.

`OutputStateTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный выходной тензорные, содержащий обновленное состояние внутреннего генератора. Если оно указано, этот оператор использует *инпутстатетенсор* для вычисления соответствующего обновленного состояния генератора и записывает результат в *аутпутстатетенсор*. Как правило, вызывающие объекты сохраняют этот результат и передают его в качестве входного состояния при последующем выполнении этого оператора.

`Type`

Тип: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Одно из значений перечисления [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , указывающее тип используемого генератора. В настоящее время единственным допустимым значением является **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, которое создает псевдо-случайные числа в соответствии с [алгоритмом филокс 4X32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).

## <a name="remarks"></a>Remarks
При каждом выполнении этого оператора необходимо увеличить 128-разрядный счетчик. Если указан параметр *аутпутстатетенсор* , этот оператор увеличивает значение счетчика с правильным значением от вашего имени и записывает результат в *аутпутстатетенсор*. Объем, на который он должен увеличиваться, зависит от числа формируемых 32-разрядных выходных элементов и типа генератора.

Для **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10** значение счетчика 128-bit должно увеличиваться при `ceil(outputSize / 4)` каждом выполнении, где `outputSize` — число элементов в *аутпуттенсор*.

Рассмотрим пример, где значение счетчика 128-разрядов в настоящее время равно `0x48656c6c'6f46726f'6d536561'74746c65` , а размер аутпуттенсор — `{3,3,20,7219}` . После однократного выполнения этого оператора счетчик должен увеличиваться на 324 855 (число элементов вывода, формируемых на 4, округляя вверх), в результате чего получается значение счетчика `0x48656c6c'6f46726f'6d536561'746f776e` . Это обновленное значение затем должно быть указано в качестве входных данных для следующего выполнения этого оператора.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
`InputStateTensor` и `OutputStateTensor` должны иметь одинаковые *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Измерения | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| инпутстатетенсор | Входные данные | {1, 1, 1, 6} | 4 | ЗНАЧЕНИЕМ |
| аутпуттенсор | Выходные данные | {D0, D1, D2, D3} | 4 | ЗНАЧЕНИЕМ |
| аутпутстатетенсор | Необязательный вывод | {1, 1, 1, 6} | 4 | ЗНАЧЕНИЕМ |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |