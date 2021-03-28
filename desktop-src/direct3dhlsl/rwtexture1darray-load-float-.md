---
title: 'Функция RWTexture1DArray:: Load (int)'
description: 'Считывает данные текстуры. | Функция RWTexture1DArray:: Load (int)'
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986281"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="2e563-105">Функция RWTexture1DArray:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="2e563-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="2e563-106">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="2e563-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e563-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e563-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="2e563-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e563-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e563-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e563-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e563-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="2e563-110">Type: **int**</span></span>

<span data-ttu-id="2e563-111">Расположение текстуры.</span><span class="sxs-lookup"><span data-stu-id="2e563-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e563-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e563-112">Return value</span></span>

<span data-ttu-id="2e563-113">Тип:</span><span class="sxs-lookup"><span data-stu-id="2e563-113">Type:</span></span>

<span data-ttu-id="2e563-114">Возвращаемый тип соответствует типу в объявлении для объекта [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="2e563-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e563-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e563-115">Remarks</span></span>

<span data-ttu-id="2e563-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2e563-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2e563-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="2e563-117">Vertex</span></span> | <span data-ttu-id="2e563-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2e563-118">Hull</span></span> | <span data-ttu-id="2e563-119">Домен</span><span class="sxs-lookup"><span data-stu-id="2e563-119">Domain</span></span> | <span data-ttu-id="2e563-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2e563-120">Geometry</span></span> | <span data-ttu-id="2e563-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2e563-121">Pixel</span></span> | <span data-ttu-id="2e563-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2e563-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2e563-123">x</span><span class="sxs-lookup"><span data-stu-id="2e563-123">x</span></span>     | <span data-ttu-id="2e563-124">x</span><span class="sxs-lookup"><span data-stu-id="2e563-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2e563-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e563-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e563-126">Методы Load</span><span class="sxs-lookup"><span data-stu-id="2e563-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




