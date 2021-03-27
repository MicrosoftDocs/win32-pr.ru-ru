---
title: 'Функция Битеаддрессбуффер:: Load4 (uint, uint)'
description: Возвращает четыре значения и состояние операции.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Функция Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070028"
---
# <a name="load4uint-uint-function"></a><span data-ttu-id="3cb39-104">Load4 (uint, uint), функция</span><span class="sxs-lookup"><span data-stu-id="3cb39-104">Load4(uint, uint) function</span></span>

<span data-ttu-id="3cb39-105">Возвращает четыре значения и состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3cb39-105">Gets four values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb39-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cb39-106">Syntax</span></span>

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="3cb39-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cb39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb39-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cb39-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb39-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3cb39-109">Type: **uint**</span></span>

<span data-ttu-id="3cb39-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="3cb39-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="3cb39-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3cb39-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb39-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3cb39-112">Type: **uint**</span></span>

<span data-ttu-id="3cb39-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3cb39-113">The status of the operation.</span></span> <span data-ttu-id="3cb39-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb39-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3cb39-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3cb39-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3cb39-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3cb39-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb39-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cb39-117">Return value</span></span>

<span data-ttu-id="3cb39-118">Тип: **uint4**</span><span class="sxs-lookup"><span data-stu-id="3cb39-118">Type: **uint4**</span></span>

<span data-ttu-id="3cb39-119">Четыре значения.</span><span class="sxs-lookup"><span data-stu-id="3cb39-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb39-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cb39-120">Remarks</span></span>

<span data-ttu-id="3cb39-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3cb39-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3cb39-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="3cb39-122">Vertex</span></span> | <span data-ttu-id="3cb39-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3cb39-123">Hull</span></span> | <span data-ttu-id="3cb39-124">Домен</span><span class="sxs-lookup"><span data-stu-id="3cb39-124">Domain</span></span> | <span data-ttu-id="3cb39-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3cb39-125">Geometry</span></span> | <span data-ttu-id="3cb39-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3cb39-126">Pixel</span></span> | <span data-ttu-id="3cb39-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3cb39-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3cb39-128">x</span><span class="sxs-lookup"><span data-stu-id="3cb39-128">x</span></span>      | <span data-ttu-id="3cb39-129">x</span><span class="sxs-lookup"><span data-stu-id="3cb39-129">x</span></span>    | <span data-ttu-id="3cb39-130">x</span><span class="sxs-lookup"><span data-stu-id="3cb39-130">x</span></span>      | <span data-ttu-id="3cb39-131">x</span><span class="sxs-lookup"><span data-stu-id="3cb39-131">x</span></span>        | <span data-ttu-id="3cb39-132">x</span><span class="sxs-lookup"><span data-stu-id="3cb39-132">x</span></span>     | <span data-ttu-id="3cb39-133">x</span><span class="sxs-lookup"><span data-stu-id="3cb39-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3cb39-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cb39-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb39-135">Методы Load4</span><span class="sxs-lookup"><span data-stu-id="3cb39-135">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="3cb39-136">**битеаддрессбуффер**</span><span class="sxs-lookup"><span data-stu-id="3cb39-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 