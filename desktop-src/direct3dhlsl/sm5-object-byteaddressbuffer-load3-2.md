---
title: 'Функция Битеаддрессбуффер:: Load3 (uint, uint)'
description: Возвращает три значения и состояние операции.
ms.assetid: 6AD8E957-F646-4749-A9B4-5C0C936D90E3
keywords:
- Функция Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bf3ffda082b8d2ae9cf22db59c1c38682563136
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337532"
---
# <a name="load3uint-uint-function"></a><span data-ttu-id="bd49a-104">Load3 (uint, uint), функция</span><span class="sxs-lookup"><span data-stu-id="bd49a-104">Load3(uint, uint) function</span></span>

<span data-ttu-id="bd49a-105">Возвращает три значения и состояние операции.</span><span class="sxs-lookup"><span data-stu-id="bd49a-105">Gets three values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd49a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd49a-106">Syntax</span></span>

``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="bd49a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd49a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd49a-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bd49a-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd49a-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="bd49a-109">Type: **uint**</span></span>

<span data-ttu-id="bd49a-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="bd49a-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="bd49a-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bd49a-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd49a-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="bd49a-112">Type: **uint**</span></span>

<span data-ttu-id="bd49a-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="bd49a-113">The status of the operation.</span></span> <span data-ttu-id="bd49a-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="bd49a-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bd49a-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="bd49a-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bd49a-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="bd49a-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd49a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd49a-117">Return value</span></span>

<span data-ttu-id="bd49a-118">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="bd49a-118">Type: **uint3**</span></span>

<span data-ttu-id="bd49a-119">Три значения.</span><span class="sxs-lookup"><span data-stu-id="bd49a-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd49a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd49a-120">Remarks</span></span>

<span data-ttu-id="bd49a-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="bd49a-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bd49a-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="bd49a-122">Vertex</span></span> | <span data-ttu-id="bd49a-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="bd49a-123">Hull</span></span> | <span data-ttu-id="bd49a-124">Домен</span><span class="sxs-lookup"><span data-stu-id="bd49a-124">Domain</span></span> | <span data-ttu-id="bd49a-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="bd49a-125">Geometry</span></span> | <span data-ttu-id="bd49a-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="bd49a-126">Pixel</span></span> | <span data-ttu-id="bd49a-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="bd49a-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bd49a-128">x</span><span class="sxs-lookup"><span data-stu-id="bd49a-128">x</span></span>      | <span data-ttu-id="bd49a-129">x</span><span class="sxs-lookup"><span data-stu-id="bd49a-129">x</span></span>    | <span data-ttu-id="bd49a-130">x</span><span class="sxs-lookup"><span data-stu-id="bd49a-130">x</span></span>      | <span data-ttu-id="bd49a-131">x</span><span class="sxs-lookup"><span data-stu-id="bd49a-131">x</span></span>        | <span data-ttu-id="bd49a-132">x</span><span class="sxs-lookup"><span data-stu-id="bd49a-132">x</span></span>     | <span data-ttu-id="bd49a-133">x</span><span class="sxs-lookup"><span data-stu-id="bd49a-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bd49a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd49a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd49a-135">Методы Load3</span><span class="sxs-lookup"><span data-stu-id="bd49a-135">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="bd49a-136">**битеаддрессбуффер**</span><span class="sxs-lookup"><span data-stu-id="bd49a-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 