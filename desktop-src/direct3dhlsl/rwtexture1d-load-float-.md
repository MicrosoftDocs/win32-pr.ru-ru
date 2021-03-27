---
title: 'Функция RWTexture1D:: Load (int)'
description: 'Считывает данные текстуры. | Функция RWTexture1D:: Load (int)'
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353115"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="92d8e-105">Функция RWTexture1D:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="92d8e-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="92d8e-106">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="92d8e-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92d8e-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="92d8e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92d8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92d8e-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92d8e-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92d8e-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="92d8e-110">Type: **int**</span></span>

<span data-ttu-id="92d8e-111">Расположение текстуры.</span><span class="sxs-lookup"><span data-stu-id="92d8e-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92d8e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92d8e-112">Return value</span></span>

<span data-ttu-id="92d8e-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="92d8e-113">Type:</span></span>

<span data-ttu-id="92d8e-114">Возвращаемый тип соответствует типу в объявлении для объекта [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="92d8e-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="92d8e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="92d8e-115">Remarks</span></span>

<span data-ttu-id="92d8e-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="92d8e-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="92d8e-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="92d8e-117">Vertex</span></span> | <span data-ttu-id="92d8e-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="92d8e-118">Hull</span></span> | <span data-ttu-id="92d8e-119">Домен</span><span class="sxs-lookup"><span data-stu-id="92d8e-119">Domain</span></span> | <span data-ttu-id="92d8e-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="92d8e-120">Geometry</span></span> | <span data-ttu-id="92d8e-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="92d8e-121">Pixel</span></span> | <span data-ttu-id="92d8e-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="92d8e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="92d8e-123">x</span><span class="sxs-lookup"><span data-stu-id="92d8e-123">x</span></span>     | <span data-ttu-id="92d8e-124">x</span><span class="sxs-lookup"><span data-stu-id="92d8e-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="92d8e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92d8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92d8e-126">Методы Load</span><span class="sxs-lookup"><span data-stu-id="92d8e-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




