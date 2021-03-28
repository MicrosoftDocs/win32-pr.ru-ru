---
title: 'Функция Рвструктуредбуффер:: Load (int)'
description: 'Считывает данные буфера. | Функция Рвструктуредбуффер:: Load (int)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
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
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998050"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="ec32e-105">Функция Рвструктуредбуффер:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="ec32e-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="ec32e-106">Считывает данные буфера.</span><span class="sxs-lookup"><span data-stu-id="ec32e-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec32e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec32e-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="ec32e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec32e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec32e-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec32e-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec32e-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="ec32e-110">Type: **int**</span></span>

<span data-ttu-id="ec32e-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="ec32e-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec32e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec32e-112">Return value</span></span>

<span data-ttu-id="ec32e-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="ec32e-113">Type:</span></span>

<span data-ttu-id="ec32e-114">Возвращаемый тип соответствует типу в объявлении для объекта [**рвструктуредбуффер**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec32e-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec32e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec32e-115">Remarks</span></span>

<span data-ttu-id="ec32e-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ec32e-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ec32e-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="ec32e-117">Vertex</span></span> | <span data-ttu-id="ec32e-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ec32e-118">Hull</span></span> | <span data-ttu-id="ec32e-119">Домен</span><span class="sxs-lookup"><span data-stu-id="ec32e-119">Domain</span></span> | <span data-ttu-id="ec32e-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ec32e-120">Geometry</span></span> | <span data-ttu-id="ec32e-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ec32e-121">Pixel</span></span> | <span data-ttu-id="ec32e-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ec32e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ec32e-123">x</span><span class="sxs-lookup"><span data-stu-id="ec32e-123">x</span></span>      | <span data-ttu-id="ec32e-124">x</span><span class="sxs-lookup"><span data-stu-id="ec32e-124">x</span></span>    | <span data-ttu-id="ec32e-125">x</span><span class="sxs-lookup"><span data-stu-id="ec32e-125">x</span></span>      | <span data-ttu-id="ec32e-126">x</span><span class="sxs-lookup"><span data-stu-id="ec32e-126">x</span></span>        | <span data-ttu-id="ec32e-127">x</span><span class="sxs-lookup"><span data-stu-id="ec32e-127">x</span></span>     | <span data-ttu-id="ec32e-128">x</span><span class="sxs-lookup"><span data-stu-id="ec32e-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ec32e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec32e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec32e-130">Методы Load</span><span class="sxs-lookup"><span data-stu-id="ec32e-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




