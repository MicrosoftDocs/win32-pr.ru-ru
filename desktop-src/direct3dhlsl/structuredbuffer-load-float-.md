---
title: 'Функция Структуредбуффер:: Load (int)'
description: 'Считывает данные буфера. | Функция Структуредбуффер:: Load (int)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986609"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="5db33-105">Функция Структуредбуффер:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="5db33-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="5db33-106">Считывает данные буфера.</span><span class="sxs-lookup"><span data-stu-id="5db33-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db33-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5db33-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="5db33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5db33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db33-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db33-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db33-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="5db33-110">Type: **int**</span></span>

<span data-ttu-id="5db33-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="5db33-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db33-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5db33-112">Return value</span></span>

<span data-ttu-id="5db33-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="5db33-113">Type:</span></span>

<span data-ttu-id="5db33-114">Возвращаемый тип соответствует типу в объявлении для объекта [**структуредбуффер**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5db33-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5db33-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="5db33-115">Remarks</span></span>

<span data-ttu-id="5db33-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5db33-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5db33-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="5db33-117">Vertex</span></span> | <span data-ttu-id="5db33-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5db33-118">Hull</span></span> | <span data-ttu-id="5db33-119">Домен</span><span class="sxs-lookup"><span data-stu-id="5db33-119">Domain</span></span> | <span data-ttu-id="5db33-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5db33-120">Geometry</span></span> | <span data-ttu-id="5db33-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5db33-121">Pixel</span></span> | <span data-ttu-id="5db33-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5db33-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5db33-123">x</span><span class="sxs-lookup"><span data-stu-id="5db33-123">x</span></span>     | <span data-ttu-id="5db33-124">x</span><span class="sxs-lookup"><span data-stu-id="5db33-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5db33-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5db33-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db33-126">Методы Load</span><span class="sxs-lookup"><span data-stu-id="5db33-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




