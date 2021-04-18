---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Переупорядочивает (пермутес) данные из глубины в блоки пространственных данных. Оператор выводит копию входного тензорные, где значения из измерения глубины перемещаются в пространственные блоки в измерения высоты и ширины.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 639bda0b8d398d24b01649635d3cfcbd2301a211
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105720001"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="78842-104">Структура DML_DEPTH_TO_SPACE1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="78842-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="78842-105">Переупорядочивает (пермутес) данные из глубины в блоки пространственных данных.</span><span class="sxs-lookup"><span data-stu-id="78842-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="78842-106">Оператор выводит копию входного тензорные, где значения из измерения глубины перемещаются в пространственные блоки в измерения высоты и ширины.</span><span class="sxs-lookup"><span data-stu-id="78842-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="78842-107">Это обратное преобразование [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="78842-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78842-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="78842-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="78842-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="78842-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78842-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78842-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="78842-111">Члены</span><span class="sxs-lookup"><span data-stu-id="78842-111">Members</span></span>

`InputTensor`

<span data-ttu-id="78842-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78842-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78842-113">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="78842-113">The tensor to read from.</span></span> <span data-ttu-id="78842-114">К измерениям входного тензорные присвоено значение `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="78842-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="78842-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78842-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78842-116">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="78842-116">The tensor to write the results to.</span></span> <span data-ttu-id="78842-117">Размеры выходных тензорные равны `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , где:</span><span class="sxs-lookup"><span data-stu-id="78842-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="78842-118">Аутпутчаннелкаунт вычислено как Инпутчаннелкаунт/( `BlockSize`  \*  `BlockSize` )</span><span class="sxs-lookup"><span data-stu-id="78842-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="78842-119">Аутпусеигхт вычислено как Инпусеигхт \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="78842-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="78842-120">Аутпутвидс вычислено как Инпутвидс \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="78842-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="78842-121">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="78842-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="78842-122">Ширина и высота перемещаемых блоков.</span><span class="sxs-lookup"><span data-stu-id="78842-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="78842-123">Тип: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="78842-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="78842-124">См. [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="78842-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="78842-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="78842-125">Examples</span></span>

<span data-ttu-id="78842-126">В примерах, приведенных в этом разделе, используются следующие входные данные.</span><span class="sxs-lookup"><span data-stu-id="78842-126">The examples in this section all use the input below.</span></span>

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="78842-127">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="78842-127">Example 1.</span></span> <span data-ttu-id="78842-128">Порядок строк в столбцах</span><span class="sxs-lookup"><span data-stu-id="78842-128">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="78842-129">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="78842-129">Example 2.</span></span> <span data-ttu-id="78842-130">Порядок столбцов в строках</span><span class="sxs-lookup"><span data-stu-id="78842-130">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="78842-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78842-131">Remarks</span></span>
<span data-ttu-id="78842-132">Если для параметра *Order* задано значение [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** эквивалентно [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="78842-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="78842-133">Доступность</span><span class="sxs-lookup"><span data-stu-id="78842-133">Availability</span></span>
<span data-ttu-id="78842-134">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="78842-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="78842-135">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="78842-135">Tensor constraints</span></span>
<span data-ttu-id="78842-136">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="78842-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="78842-137">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="78842-137">Tensor support</span></span>
| <span data-ttu-id="78842-138">Тензорные</span><span class="sxs-lookup"><span data-stu-id="78842-138">Tensor</span></span> | <span data-ttu-id="78842-139">Вид</span><span class="sxs-lookup"><span data-stu-id="78842-139">Kind</span></span> | <span data-ttu-id="78842-140">Измерения</span><span class="sxs-lookup"><span data-stu-id="78842-140">Dimensions</span></span> | <span data-ttu-id="78842-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="78842-141">Supported dimension counts</span></span> | <span data-ttu-id="78842-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="78842-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="78842-143">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="78842-143">InputTensor</span></span> | <span data-ttu-id="78842-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="78842-144">Input</span></span> | <span data-ttu-id="78842-145">{Батчкаунт, Инпутчаннелкаунт, Инпусеигхт, Инпутвидс}</span><span class="sxs-lookup"><span data-stu-id="78842-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="78842-146">4</span><span class="sxs-lookup"><span data-stu-id="78842-146">4</span></span> | <span data-ttu-id="78842-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="78842-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="78842-148">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="78842-148">OutputTensor</span></span> | <span data-ttu-id="78842-149">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="78842-149">Output</span></span> | <span data-ttu-id="78842-150">{Батчкаунт, Аутпутчаннелкаунт, Аутпусеигхт, Аутпутвидс}</span><span class="sxs-lookup"><span data-stu-id="78842-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="78842-151">4</span><span class="sxs-lookup"><span data-stu-id="78842-151">4</span></span> | <span data-ttu-id="78842-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="78842-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="78842-153">Требования</span><span class="sxs-lookup"><span data-stu-id="78842-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="78842-154">**Header**</span><span class="sxs-lookup"><span data-stu-id="78842-154">**Header**</span></span> | <span data-ttu-id="78842-155">директмл. h</span><span class="sxs-lookup"><span data-stu-id="78842-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="78842-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78842-156">See also</span></span>

* [<span data-ttu-id="78842-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="78842-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="78842-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="78842-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)