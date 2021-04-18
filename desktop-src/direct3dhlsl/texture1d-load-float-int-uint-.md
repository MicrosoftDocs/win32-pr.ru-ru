---
title: 'Функция Texture1D:: Load (int, int, uint)'
description: 'Считывает данные текстуры и возвращает состояние операции. | Функция Texture1D:: Load (int, int, uint)'
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
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
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986469"
---
# <a name="texture1dloadintintuint-function"></a><span data-ttu-id="5a062-105">Функция Texture1D:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="5a062-105">Texture1D::Load(int,int,uint) function</span></span>

<span data-ttu-id="5a062-106">Считывает данные текстуры и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="5a062-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a062-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a062-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="5a062-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a062-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a062-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a062-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a062-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="5a062-110">Type: **int**</span></span>

<span data-ttu-id="5a062-111">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="5a062-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5a062-112">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a062-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a062-113">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="5a062-113">Type: **int**</span></span>

<span data-ttu-id="5a062-114">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="5a062-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="5a062-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5a062-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a062-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="5a062-116">Type: **uint**</span></span>

<span data-ttu-id="5a062-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="5a062-117">The status of the operation.</span></span> <span data-ttu-id="5a062-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5a062-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5a062-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5a062-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5a062-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5a062-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a062-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a062-121">Return value</span></span>

<span data-ttu-id="5a062-122">Тип:</span><span class="sxs-lookup"><span data-stu-id="5a062-122">Type:</span></span>

<span data-ttu-id="5a062-123">Возвращаемый тип соответствует типу в объявлении для объекта [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="5a062-123">The return type matches the type in the declaration for the [**Texture1D**](sm5-object-texture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a062-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a062-124">Remarks</span></span>

<span data-ttu-id="5a062-125">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5a062-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5a062-126">Вершина</span><span class="sxs-lookup"><span data-stu-id="5a062-126">Vertex</span></span> | <span data-ttu-id="5a062-127">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5a062-127">Hull</span></span> | <span data-ttu-id="5a062-128">Домен</span><span class="sxs-lookup"><span data-stu-id="5a062-128">Domain</span></span> | <span data-ttu-id="5a062-129">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5a062-129">Geometry</span></span> | <span data-ttu-id="5a062-130">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5a062-130">Pixel</span></span> | <span data-ttu-id="5a062-131">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5a062-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5a062-132">x</span><span class="sxs-lookup"><span data-stu-id="5a062-132">x</span></span>      | <span data-ttu-id="5a062-133">x</span><span class="sxs-lookup"><span data-stu-id="5a062-133">x</span></span>    | <span data-ttu-id="5a062-134">x</span><span class="sxs-lookup"><span data-stu-id="5a062-134">x</span></span>      | <span data-ttu-id="5a062-135">x</span><span class="sxs-lookup"><span data-stu-id="5a062-135">x</span></span>        | <span data-ttu-id="5a062-136">x</span><span class="sxs-lookup"><span data-stu-id="5a062-136">x</span></span>     | <span data-ttu-id="5a062-137">x</span><span class="sxs-lookup"><span data-stu-id="5a062-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5a062-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a062-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a062-139">Методы Load</span><span class="sxs-lookup"><span data-stu-id="5a062-139">Load methods</span></span>](texture1d-load.md)
</dt> <dt>

[<span data-ttu-id="5a062-140">**Texture1D**</span><span class="sxs-lookup"><span data-stu-id="5a062-140">**Texture1D**</span></span>](sm5-object-texture1d.md)
</dt> </dl>

 

 
