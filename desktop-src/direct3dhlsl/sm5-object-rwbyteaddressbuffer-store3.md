---
title: 'Функция Рвбитеаддрессбуффер:: Store3'
description: Задает три значения.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Функция Store3 HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335088"
---
# <a name="store3-function"></a><span data-ttu-id="ed158-104">Функция Store3</span><span class="sxs-lookup"><span data-stu-id="ed158-104">Store3 function</span></span>

<span data-ttu-id="ed158-105">Задает три значения.</span><span class="sxs-lookup"><span data-stu-id="ed158-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed158-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed158-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="ed158-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed158-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed158-108">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed158-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed158-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ed158-109">Type: **uint**</span></span>

<span data-ttu-id="ed158-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="ed158-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="ed158-111">*значения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed158-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed158-112">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="ed158-112">Type: **uint3**</span></span>

<span data-ttu-id="ed158-113">Три входных значения.</span><span class="sxs-lookup"><span data-stu-id="ed158-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed158-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed158-114">Return value</span></span>

<span data-ttu-id="ed158-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ed158-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed158-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed158-116">Remarks</span></span>

<span data-ttu-id="ed158-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ed158-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ed158-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="ed158-118">Vertex</span></span> | <span data-ttu-id="ed158-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ed158-119">Hull</span></span> | <span data-ttu-id="ed158-120">Домен</span><span class="sxs-lookup"><span data-stu-id="ed158-120">Domain</span></span> | <span data-ttu-id="ed158-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ed158-121">Geometry</span></span> | <span data-ttu-id="ed158-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ed158-122">Pixel</span></span> | <span data-ttu-id="ed158-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ed158-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ed158-124">x</span><span class="sxs-lookup"><span data-stu-id="ed158-124">x</span></span>     | <span data-ttu-id="ed158-125">x</span><span class="sxs-lookup"><span data-stu-id="ed158-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ed158-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed158-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed158-127">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="ed158-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="ed158-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ed158-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




