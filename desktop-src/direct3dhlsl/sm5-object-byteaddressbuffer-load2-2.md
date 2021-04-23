---
title: 'Функция Битеаддрессбуффер:: Load2 (uint, uint)'
description: Возвращает два значения и состояние операции.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
keywords:
- Функция Load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070390"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="75d35-104">Load2 (uint, uint), функция</span><span class="sxs-lookup"><span data-stu-id="75d35-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="75d35-105">Возвращает два значения и состояние операции.</span><span class="sxs-lookup"><span data-stu-id="75d35-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d35-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75d35-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="75d35-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="75d35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d35-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75d35-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d35-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="75d35-109">Type: **uint**</span></span>

<span data-ttu-id="75d35-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="75d35-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="75d35-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75d35-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75d35-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="75d35-112">Type: **uint**</span></span>

<span data-ttu-id="75d35-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="75d35-113">The status of the operation.</span></span> <span data-ttu-id="75d35-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="75d35-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="75d35-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="75d35-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="75d35-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="75d35-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d35-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75d35-117">Return value</span></span>

<span data-ttu-id="75d35-118">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="75d35-118">Type: **uint2**</span></span>

<span data-ttu-id="75d35-119">Два значения.</span><span class="sxs-lookup"><span data-stu-id="75d35-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d35-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="75d35-120">Remarks</span></span>

<span data-ttu-id="75d35-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="75d35-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="75d35-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="75d35-122">Vertex</span></span> | <span data-ttu-id="75d35-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="75d35-123">Hull</span></span> | <span data-ttu-id="75d35-124">Домен</span><span class="sxs-lookup"><span data-stu-id="75d35-124">Domain</span></span> | <span data-ttu-id="75d35-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="75d35-125">Geometry</span></span> | <span data-ttu-id="75d35-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="75d35-126">Pixel</span></span> | <span data-ttu-id="75d35-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="75d35-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="75d35-128">x</span><span class="sxs-lookup"><span data-stu-id="75d35-128">x</span></span>      | <span data-ttu-id="75d35-129">x</span><span class="sxs-lookup"><span data-stu-id="75d35-129">x</span></span>    | <span data-ttu-id="75d35-130">x</span><span class="sxs-lookup"><span data-stu-id="75d35-130">x</span></span>      | <span data-ttu-id="75d35-131">x</span><span class="sxs-lookup"><span data-stu-id="75d35-131">x</span></span>        | <span data-ttu-id="75d35-132">x</span><span class="sxs-lookup"><span data-stu-id="75d35-132">x</span></span>     | <span data-ttu-id="75d35-133">x</span><span class="sxs-lookup"><span data-stu-id="75d35-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="75d35-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75d35-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d35-135">Методы Load2</span><span class="sxs-lookup"><span data-stu-id="75d35-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="75d35-136">**битеаддрессбуффер**</span><span class="sxs-lookup"><span data-stu-id="75d35-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 