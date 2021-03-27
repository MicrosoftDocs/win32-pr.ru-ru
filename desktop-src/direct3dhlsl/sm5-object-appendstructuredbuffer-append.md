---
title: 'Функция Аппендструктуредбуффер:: Append'
description: Добавляет значение в конец буфера.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Функция append HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "103987039"
---
# <a name="append-function"></a><span data-ttu-id="47aaf-104">Функция append</span><span class="sxs-lookup"><span data-stu-id="47aaf-104">Append function</span></span>

<span data-ttu-id="47aaf-105">Добавляет значение в конец буфера.</span><span class="sxs-lookup"><span data-stu-id="47aaf-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="47aaf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47aaf-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="47aaf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="47aaf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47aaf-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47aaf-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47aaf-109">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="47aaf-109">Type: **T**</span></span>

<span data-ttu-id="47aaf-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="47aaf-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47aaf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47aaf-111">Return value</span></span>

<span data-ttu-id="47aaf-112">None</span><span class="sxs-lookup"><span data-stu-id="47aaf-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="47aaf-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="47aaf-113">Remarks</span></span>

<span data-ttu-id="47aaf-114">T может быть любым типом данных, включая структуры.</span><span class="sxs-lookup"><span data-stu-id="47aaf-114">T can be any data type including structures.</span></span>

<span data-ttu-id="47aaf-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="47aaf-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="47aaf-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="47aaf-116">Vertex</span></span> | <span data-ttu-id="47aaf-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="47aaf-117">Hull</span></span> | <span data-ttu-id="47aaf-118">Домен</span><span class="sxs-lookup"><span data-stu-id="47aaf-118">Domain</span></span> | <span data-ttu-id="47aaf-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="47aaf-119">Geometry</span></span> | <span data-ttu-id="47aaf-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="47aaf-120">Pixel</span></span> | <span data-ttu-id="47aaf-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="47aaf-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="47aaf-122">x</span><span class="sxs-lookup"><span data-stu-id="47aaf-122">x</span></span>      | <span data-ttu-id="47aaf-123">x</span><span class="sxs-lookup"><span data-stu-id="47aaf-123">x</span></span>    | <span data-ttu-id="47aaf-124">x</span><span class="sxs-lookup"><span data-stu-id="47aaf-124">x</span></span>      | <span data-ttu-id="47aaf-125">x</span><span class="sxs-lookup"><span data-stu-id="47aaf-125">x</span></span>        | <span data-ttu-id="47aaf-126">x</span><span class="sxs-lookup"><span data-stu-id="47aaf-126">x</span></span>     | <span data-ttu-id="47aaf-127">x</span><span class="sxs-lookup"><span data-stu-id="47aaf-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="47aaf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47aaf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47aaf-129">аппендструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="47aaf-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="47aaf-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="47aaf-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




