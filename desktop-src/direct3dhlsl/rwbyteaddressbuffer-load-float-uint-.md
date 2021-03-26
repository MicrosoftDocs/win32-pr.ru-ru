---
title: 'Функция Рвбитеаддрессбуффер:: Load (int, uint)'
description: Возвращает одно значение и возвращает состояние операции.
ms.assetid: E3FD0FFA-6A9B-4B44-A90D-47270326F9BA
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
ms.openlocfilehash: 71f142d35ae8be3800ccf85b5e8114d5e85c44ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891285"
---
# <a name="rwbyteaddressbufferloadintuint-function"></a><span data-ttu-id="0c5bf-104">Функция Рвбитеаддрессбуффер:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="0c5bf-104">RWByteAddressBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="0c5bf-105">Возвращает одно значение и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="0c5bf-105">Gets one value and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5bf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c5bf-106">Syntax</span></span>


``` syntax
uint Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="0c5bf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c5bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c5bf-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c5bf-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5bf-109">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="0c5bf-109">Type: **int**</span></span>

<span data-ttu-id="0c5bf-110">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="0c5bf-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0c5bf-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0c5bf-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5bf-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="0c5bf-112">Type: **uint**</span></span>

<span data-ttu-id="0c5bf-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="0c5bf-113">The status of the operation.</span></span> <span data-ttu-id="0c5bf-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0c5bf-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0c5bf-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0c5bf-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0c5bf-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0c5bf-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c5bf-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c5bf-117">Return value</span></span>

<span data-ttu-id="0c5bf-118">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="0c5bf-118">Type: **uint**</span></span>

<span data-ttu-id="0c5bf-119">Одно значение.</span><span class="sxs-lookup"><span data-stu-id="0c5bf-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c5bf-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c5bf-120">Remarks</span></span>

<span data-ttu-id="0c5bf-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0c5bf-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0c5bf-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="0c5bf-122">Vertex</span></span> | <span data-ttu-id="0c5bf-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0c5bf-123">Hull</span></span> | <span data-ttu-id="0c5bf-124">Домен</span><span class="sxs-lookup"><span data-stu-id="0c5bf-124">Domain</span></span> | <span data-ttu-id="0c5bf-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0c5bf-125">Geometry</span></span> | <span data-ttu-id="0c5bf-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0c5bf-126">Pixel</span></span> | <span data-ttu-id="0c5bf-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0c5bf-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0c5bf-128">x</span><span class="sxs-lookup"><span data-stu-id="0c5bf-128">x</span></span>     | <span data-ttu-id="0c5bf-129">x</span><span class="sxs-lookup"><span data-stu-id="0c5bf-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0c5bf-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c5bf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5bf-131">Методы Load</span><span class="sxs-lookup"><span data-stu-id="0c5bf-131">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 
