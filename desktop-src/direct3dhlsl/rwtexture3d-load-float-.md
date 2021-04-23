---
title: 'Функция RWTexture3D:: Load (int)'
description: 'Считывает данные текстуры. | Функция RWTexture3D:: Load (int)'
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353102"
---
# <a name="rwtexture3dloadint-function"></a><span data-ttu-id="6a33d-105">Функция RWTexture3D:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="6a33d-105">RWTexture3D::Load(int) function</span></span>

<span data-ttu-id="6a33d-106">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="6a33d-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a33d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a33d-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="6a33d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a33d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a33d-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6a33d-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a33d-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="6a33d-110">Type: **int**</span></span>

<span data-ttu-id="6a33d-111">Расположение текстуры.</span><span class="sxs-lookup"><span data-stu-id="6a33d-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a33d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a33d-112">Return value</span></span>

<span data-ttu-id="6a33d-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="6a33d-113">Type:</span></span>

<span data-ttu-id="6a33d-114">Возвращаемый тип соответствует типу в объявлении для объекта [**RWTexture3D**](sm5-object-rwtexture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="6a33d-114">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a33d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a33d-115">Remarks</span></span>

<span data-ttu-id="6a33d-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="6a33d-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6a33d-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="6a33d-117">Vertex</span></span> | <span data-ttu-id="6a33d-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="6a33d-118">Hull</span></span> | <span data-ttu-id="6a33d-119">Домен</span><span class="sxs-lookup"><span data-stu-id="6a33d-119">Domain</span></span> | <span data-ttu-id="6a33d-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="6a33d-120">Geometry</span></span> | <span data-ttu-id="6a33d-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="6a33d-121">Pixel</span></span> | <span data-ttu-id="6a33d-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="6a33d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6a33d-123">x</span><span class="sxs-lookup"><span data-stu-id="6a33d-123">x</span></span>     | <span data-ttu-id="6a33d-124">x</span><span class="sxs-lookup"><span data-stu-id="6a33d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6a33d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a33d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a33d-126">Методы Load</span><span class="sxs-lookup"><span data-stu-id="6a33d-126">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 




