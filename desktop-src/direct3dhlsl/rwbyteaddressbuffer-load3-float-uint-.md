---
title: 'Функция Рвбитеаддрессбуффер:: Load3 (uint, uint)'
description: Возвращает три значения и возвращает состояние операции.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
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
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338593"
---
# <a name="load3uintuint-function"></a><span data-ttu-id="7714e-104">Load3 (uint, uint), функция</span><span class="sxs-lookup"><span data-stu-id="7714e-104">Load3(uint,uint) function</span></span>

<span data-ttu-id="7714e-105">Возвращает три значения и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="7714e-105">Gets three values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7714e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7714e-106">Syntax</span></span>


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="7714e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7714e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7714e-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7714e-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7714e-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7714e-109">Type: **uint**</span></span>

<span data-ttu-id="7714e-110">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="7714e-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7714e-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7714e-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7714e-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7714e-112">Type: **uint**</span></span>

<span data-ttu-id="7714e-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="7714e-113">The status of the operation.</span></span> <span data-ttu-id="7714e-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7714e-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7714e-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7714e-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7714e-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7714e-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7714e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7714e-117">Return value</span></span>

<span data-ttu-id="7714e-118">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="7714e-118">Type: **uint3**</span></span>

<span data-ttu-id="7714e-119">Три значения.</span><span class="sxs-lookup"><span data-stu-id="7714e-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7714e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7714e-120">Remarks</span></span>

<span data-ttu-id="7714e-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7714e-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7714e-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="7714e-122">Vertex</span></span> | <span data-ttu-id="7714e-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7714e-123">Hull</span></span> | <span data-ttu-id="7714e-124">Домен</span><span class="sxs-lookup"><span data-stu-id="7714e-124">Domain</span></span> | <span data-ttu-id="7714e-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7714e-125">Geometry</span></span> | <span data-ttu-id="7714e-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7714e-126">Pixel</span></span> | <span data-ttu-id="7714e-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7714e-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7714e-128">x</span><span class="sxs-lookup"><span data-stu-id="7714e-128">x</span></span>     | <span data-ttu-id="7714e-129">x</span><span class="sxs-lookup"><span data-stu-id="7714e-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7714e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7714e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7714e-131">Методы Load3</span><span class="sxs-lookup"><span data-stu-id="7714e-131">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 