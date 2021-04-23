---
title: 'Функция Рвструктуредбуффер:: Load (int, uint)'
description: 'Считывает данные буфера и возвращает сведения о состоянии операции. | Функция Рвструктуредбуффер:: Load (int, uint)'
ms.assetid: 19FAA031-F31E-4B73-BC69-489CDF0CF184
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
ms.openlocfilehash: 74a153d4b56ec16b80dec180287005666747d259
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986285"
---
# <a name="rwstructuredbufferloadintuint-function"></a><span data-ttu-id="e5859-105">Функция Рвструктуредбуффер:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="e5859-105">RWStructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="e5859-106">Считывает данные буфера и возвращает сведения о состоянии операции.</span><span class="sxs-lookup"><span data-stu-id="e5859-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5859-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5859-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="e5859-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5859-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5859-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5859-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5859-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="e5859-110">Type: **int**</span></span>

<span data-ttu-id="e5859-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="e5859-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e5859-112">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5859-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5859-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e5859-113">Type: **uint**</span></span>

<span data-ttu-id="e5859-114">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="e5859-114">The status of the operation.</span></span> <span data-ttu-id="e5859-115">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e5859-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e5859-116">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e5859-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e5859-117">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e5859-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5859-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5859-118">Return value</span></span>

<span data-ttu-id="e5859-119">Тип:</span><span class="sxs-lookup"><span data-stu-id="e5859-119">Type:</span></span>

<span data-ttu-id="e5859-120">Возвращаемый тип соответствует типу в объявлении для объекта [**рвструктуредбуффер**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e5859-120">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5859-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5859-121">Remarks</span></span>

<span data-ttu-id="e5859-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e5859-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e5859-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="e5859-123">Vertex</span></span> | <span data-ttu-id="e5859-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e5859-124">Hull</span></span> | <span data-ttu-id="e5859-125">Домен</span><span class="sxs-lookup"><span data-stu-id="e5859-125">Domain</span></span> | <span data-ttu-id="e5859-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e5859-126">Geometry</span></span> | <span data-ttu-id="e5859-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e5859-127">Pixel</span></span> | <span data-ttu-id="e5859-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e5859-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e5859-129">x</span><span class="sxs-lookup"><span data-stu-id="e5859-129">x</span></span>      | <span data-ttu-id="e5859-130">x</span><span class="sxs-lookup"><span data-stu-id="e5859-130">x</span></span>    | <span data-ttu-id="e5859-131">x</span><span class="sxs-lookup"><span data-stu-id="e5859-131">x</span></span>      | <span data-ttu-id="e5859-132">x</span><span class="sxs-lookup"><span data-stu-id="e5859-132">x</span></span>        | <span data-ttu-id="e5859-133">x</span><span class="sxs-lookup"><span data-stu-id="e5859-133">x</span></span>     | <span data-ttu-id="e5859-134">x</span><span class="sxs-lookup"><span data-stu-id="e5859-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e5859-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5859-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5859-136">Методы Load</span><span class="sxs-lookup"><span data-stu-id="e5859-136">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 
