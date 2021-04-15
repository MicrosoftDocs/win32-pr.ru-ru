---
title: 'Buffer:: Load (int, uint), функция'
description: 'Считывает данные буфера и возвращает состояние операции. | Buffer:: Load (int, uint), функция'
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
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
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986204"
---
# <a name="bufferloadint-uint-function"></a><span data-ttu-id="9fb2b-105">Buffer:: Load (int, uint), функция</span><span class="sxs-lookup"><span data-stu-id="9fb2b-105">Buffer::Load(int, uint) function</span></span>

<span data-ttu-id="9fb2b-106">Считывает данные буфера и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="9fb2b-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb2b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fb2b-107">Syntax</span></span>

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="9fb2b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fb2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb2b-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fb2b-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb2b-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="9fb2b-110">Type: **int**</span></span>

<span data-ttu-id="9fb2b-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="9fb2b-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9fb2b-112">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9fb2b-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb2b-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9fb2b-113">Type: **uint**</span></span>

<span data-ttu-id="9fb2b-114">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="9fb2b-114">The status of the operation.</span></span> <span data-ttu-id="9fb2b-115">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb2b-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9fb2b-116">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9fb2b-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9fb2b-117">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9fb2b-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb2b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fb2b-118">Return value</span></span>

<span data-ttu-id="9fb2b-119">Тип:</span><span class="sxs-lookup"><span data-stu-id="9fb2b-119">Type:</span></span>

<span data-ttu-id="9fb2b-120">Возвращаемый тип соответствует типу в объявлении для объекта [**буфера**](sm5-object-buffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9fb2b-120">The return type matches the type in the declaration for the [**Buffer**](sm5-object-buffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb2b-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fb2b-121">Remarks</span></span>

<span data-ttu-id="9fb2b-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9fb2b-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9fb2b-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="9fb2b-123">Vertex</span></span> | <span data-ttu-id="9fb2b-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9fb2b-124">Hull</span></span> | <span data-ttu-id="9fb2b-125">Домен</span><span class="sxs-lookup"><span data-stu-id="9fb2b-125">Domain</span></span> | <span data-ttu-id="9fb2b-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9fb2b-126">Geometry</span></span> | <span data-ttu-id="9fb2b-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9fb2b-127">Pixel</span></span> | <span data-ttu-id="9fb2b-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9fb2b-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9fb2b-129">x</span><span class="sxs-lookup"><span data-stu-id="9fb2b-129">x</span></span>      | <span data-ttu-id="9fb2b-130">x</span><span class="sxs-lookup"><span data-stu-id="9fb2b-130">x</span></span>    | <span data-ttu-id="9fb2b-131">x</span><span class="sxs-lookup"><span data-stu-id="9fb2b-131">x</span></span>      | <span data-ttu-id="9fb2b-132">x</span><span class="sxs-lookup"><span data-stu-id="9fb2b-132">x</span></span>        | <span data-ttu-id="9fb2b-133">x</span><span class="sxs-lookup"><span data-stu-id="9fb2b-133">x</span></span>     | <span data-ttu-id="9fb2b-134">x</span><span class="sxs-lookup"><span data-stu-id="9fb2b-134">x</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="9fb2b-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="9fb2b-135">Examples</span></span>

<span data-ttu-id="9fb2b-136">В этом примере показано, как использовать **Load**:</span><span class="sxs-lookup"><span data-stu-id="9fb2b-136">This example shows how to use **Load**:</span></span>

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a><span data-ttu-id="9fb2b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fb2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb2b-138">Методы Load</span><span class="sxs-lookup"><span data-stu-id="9fb2b-138">Load methods</span></span>](buffer-load.md)
</dt> </dl>

 

 
