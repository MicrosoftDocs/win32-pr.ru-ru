---
title: 'Функция Рвбитеаддрессбуффер:: Load4 (uint, uint)'
description: Возвращает четыре значения и возвращает состояние операции.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
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
ms.openlocfilehash: 14cb5354c21935c22833ea6f4b54b20fedc696f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793741"
---
# <a name="load4uintuint-function"></a><span data-ttu-id="3cf89-104">Load4 (uint, uint), функция</span><span class="sxs-lookup"><span data-stu-id="3cf89-104">Load4(uint,uint) function</span></span>

<span data-ttu-id="3cf89-105">Возвращает четыре значения и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3cf89-105">Gets four values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf89-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cf89-106">Syntax</span></span>


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="3cf89-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cf89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf89-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cf89-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf89-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3cf89-109">Type: **uint**</span></span>

<span data-ttu-id="3cf89-110">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="3cf89-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3cf89-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3cf89-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf89-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3cf89-112">Type: **uint**</span></span>

<span data-ttu-id="3cf89-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3cf89-113">The status of the operation.</span></span> <span data-ttu-id="3cf89-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3cf89-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3cf89-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3cf89-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3cf89-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3cf89-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf89-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cf89-117">Return value</span></span>

<span data-ttu-id="3cf89-118">Тип: **uint4**</span><span class="sxs-lookup"><span data-stu-id="3cf89-118">Type: **uint4**</span></span>

<span data-ttu-id="3cf89-119">Четыре значения.</span><span class="sxs-lookup"><span data-stu-id="3cf89-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf89-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cf89-120">Remarks</span></span>

<span data-ttu-id="3cf89-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3cf89-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3cf89-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="3cf89-122">Vertex</span></span> | <span data-ttu-id="3cf89-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3cf89-123">Hull</span></span> | <span data-ttu-id="3cf89-124">Домен</span><span class="sxs-lookup"><span data-stu-id="3cf89-124">Domain</span></span> | <span data-ttu-id="3cf89-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3cf89-125">Geometry</span></span> | <span data-ttu-id="3cf89-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3cf89-126">Pixel</span></span> | <span data-ttu-id="3cf89-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3cf89-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3cf89-128">x</span><span class="sxs-lookup"><span data-stu-id="3cf89-128">x</span></span>     | <span data-ttu-id="3cf89-129">x</span><span class="sxs-lookup"><span data-stu-id="3cf89-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3cf89-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cf89-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf89-131">Методы Load4</span><span class="sxs-lookup"><span data-stu-id="3cf89-131">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 