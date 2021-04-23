---
title: 'Функция Рвбуффер:: Load (int)'
description: 'Считывает данные буфера. | Функция Рвбуффер:: Load (int)'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820612"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="354d5-105">Функция Рвбуффер:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="354d5-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="354d5-106">Считывает данные буфера.</span><span class="sxs-lookup"><span data-stu-id="354d5-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="354d5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="354d5-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="354d5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="354d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354d5-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="354d5-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="354d5-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="354d5-110">Type: **int**</span></span>

<span data-ttu-id="354d5-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="354d5-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354d5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="354d5-112">Return value</span></span>

<span data-ttu-id="354d5-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="354d5-113">Type:</span></span>

<span data-ttu-id="354d5-114">Возвращаемый тип соответствует типу в объявлении для объекта [**рвбуффер**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="354d5-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="354d5-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="354d5-115">Remarks</span></span>

<span data-ttu-id="354d5-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="354d5-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="354d5-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="354d5-117">Vertex</span></span> | <span data-ttu-id="354d5-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="354d5-118">Hull</span></span> | <span data-ttu-id="354d5-119">Домен</span><span class="sxs-lookup"><span data-stu-id="354d5-119">Domain</span></span> | <span data-ttu-id="354d5-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="354d5-120">Geometry</span></span> | <span data-ttu-id="354d5-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="354d5-121">Pixel</span></span> | <span data-ttu-id="354d5-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="354d5-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="354d5-123">x</span><span class="sxs-lookup"><span data-stu-id="354d5-123">x</span></span>      | <span data-ttu-id="354d5-124">x</span><span class="sxs-lookup"><span data-stu-id="354d5-124">x</span></span>    | <span data-ttu-id="354d5-125">x</span><span class="sxs-lookup"><span data-stu-id="354d5-125">x</span></span>      | <span data-ttu-id="354d5-126">x</span><span class="sxs-lookup"><span data-stu-id="354d5-126">x</span></span>        | <span data-ttu-id="354d5-127">x</span><span class="sxs-lookup"><span data-stu-id="354d5-127">x</span></span>     | <span data-ttu-id="354d5-128">x</span><span class="sxs-lookup"><span data-stu-id="354d5-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="354d5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="354d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354d5-130">Методы Load</span><span class="sxs-lookup"><span data-stu-id="354d5-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




