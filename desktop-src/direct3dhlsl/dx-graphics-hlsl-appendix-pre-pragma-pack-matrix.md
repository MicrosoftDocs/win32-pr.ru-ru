---
title: Директива pragma pack_matrix
description: Директива pragma, задающая выравнивание упаковки для матриц.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix директивы pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068999"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="bed5a-104">\_директива pragma матрицы Pack</span><span class="sxs-lookup"><span data-stu-id="bed5a-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="bed5a-105">Директива pragma, задающая выравнивание упаковки для матриц.</span><span class="sxs-lookup"><span data-stu-id="bed5a-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="bed5a-106">\#\_Матрица pragma pack ( *Выравнивание* )</span><span class="sxs-lookup"><span data-stu-id="bed5a-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="bed5a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bed5a-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bed5a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="bed5a-108">Item</span></span></th>
<th><span data-ttu-id="bed5a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bed5a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bed5a-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>Выравнивание</em></span><span class="sxs-lookup"><span data-stu-id="bed5a-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="bed5a-111">Выравнивание, устанавливаемое для матриц.</span><span class="sxs-lookup"><span data-stu-id="bed5a-111">Alignment to set for matrices.</span></span> <span data-ttu-id="bed5a-112">Этот параметр может принимать одно из значений, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bed5a-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bed5a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="bed5a-113">Value</span></span></th>
<th><span data-ttu-id="bed5a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bed5a-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bed5a-115">column_major</span><span class="sxs-lookup"><span data-stu-id="bed5a-115">column_major</span></span></td>
<td><span data-ttu-id="bed5a-116">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bed5a-116">Default.</span></span> <span data-ttu-id="bed5a-117">Задает для выравнивания упаковки матрицы значение столбца Major.</span><span class="sxs-lookup"><span data-stu-id="bed5a-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed5a-118">row_major</span><span class="sxs-lookup"><span data-stu-id="bed5a-118">row_major</span></span></td>
<td><span data-ttu-id="bed5a-119">Задает выравнивание упаковки матрицы по строке основной.</span><span class="sxs-lookup"><span data-stu-id="bed5a-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="bed5a-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="bed5a-120">Examples</span></span>

<span data-ttu-id="bed5a-121">В следующем примере устанавливается выравнивание упаковки матрицы в строку Major.</span><span class="sxs-lookup"><span data-stu-id="bed5a-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="bed5a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bed5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed5a-123">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bed5a-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="bed5a-124">\#Директива pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bed5a-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





