---
title: 'Функция Рвбуффер:: Load (int, uint)'
description: 'Считывает данные буфера и возвращает состояние операции. | Функция Рвбуффер:: Load (int, uint)'
ms.assetid: 90C9ECE8-2068-47C7-B87A-941B2D4F221D
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
ms.openlocfilehash: 81d23d67b0d02ed375e07f310089067d6a7bbd67
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157063"
---
# <a name="rwbufferloadintuint-function"></a><span data-ttu-id="417d5-105">Функция Рвбуффер:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="417d5-105">RWBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="417d5-106">Считывает данные буфера и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="417d5-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="417d5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="417d5-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="417d5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="417d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417d5-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="417d5-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="417d5-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="417d5-110">Type: **int**</span></span>

<span data-ttu-id="417d5-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="417d5-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="417d5-112">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="417d5-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="417d5-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="417d5-113">Type: **uint**</span></span>

<span data-ttu-id="417d5-114">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="417d5-114">The status of the operation.</span></span> <span data-ttu-id="417d5-115">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="417d5-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="417d5-116">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="417d5-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="417d5-117">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="417d5-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417d5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="417d5-118">Return value</span></span>

<span data-ttu-id="417d5-119">Тип:</span><span class="sxs-lookup"><span data-stu-id="417d5-119">Type:</span></span>

<span data-ttu-id="417d5-120">Возвращаемый тип соответствует типу в объявлении для объекта [**рвбуффер**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="417d5-120">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="417d5-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="417d5-121">Remarks</span></span>

<span data-ttu-id="417d5-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="417d5-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="417d5-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="417d5-123">Vertex</span></span> | <span data-ttu-id="417d5-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="417d5-124">Hull</span></span> | <span data-ttu-id="417d5-125">Домен</span><span class="sxs-lookup"><span data-stu-id="417d5-125">Domain</span></span> | <span data-ttu-id="417d5-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="417d5-126">Geometry</span></span> | <span data-ttu-id="417d5-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="417d5-127">Pixel</span></span> | <span data-ttu-id="417d5-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="417d5-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="417d5-129">x</span><span class="sxs-lookup"><span data-stu-id="417d5-129">x</span></span>      | <span data-ttu-id="417d5-130">x</span><span class="sxs-lookup"><span data-stu-id="417d5-130">x</span></span>    | <span data-ttu-id="417d5-131">x</span><span class="sxs-lookup"><span data-stu-id="417d5-131">x</span></span>      | <span data-ttu-id="417d5-132">x</span><span class="sxs-lookup"><span data-stu-id="417d5-132">x</span></span>        | <span data-ttu-id="417d5-133">x</span><span class="sxs-lookup"><span data-stu-id="417d5-133">x</span></span>     | <span data-ttu-id="417d5-134">x</span><span class="sxs-lookup"><span data-stu-id="417d5-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="417d5-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="417d5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417d5-136">Методы Load</span><span class="sxs-lookup"><span data-stu-id="417d5-136">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 
