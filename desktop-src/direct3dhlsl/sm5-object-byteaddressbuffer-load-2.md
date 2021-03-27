---
title: 'Функция Битеаддрессбуффер:: Load (int, uint)'
description: Возвращает одно значение и состояние операции.
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 319daad35da0256a4d36ef4580df62fd4d295854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134882"
---
# <a name="byteaddressbufferloadint-uint-function"></a><span data-ttu-id="7af79-104">Функция Битеаддрессбуффер:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="7af79-104">ByteAddressBuffer::Load(int, uint) function</span></span>

<span data-ttu-id="7af79-105">Возвращает одно значение и состояние операции.</span><span class="sxs-lookup"><span data-stu-id="7af79-105">Gets one value and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af79-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7af79-106">Syntax</span></span>

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="7af79-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7af79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af79-108">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7af79-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af79-109">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="7af79-109">Type: **int**</span></span>

<span data-ttu-id="7af79-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="7af79-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="7af79-111">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7af79-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7af79-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7af79-112">Type: **uint**</span></span>

<span data-ttu-id="7af79-113">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="7af79-113">The status of the operation.</span></span> <span data-ttu-id="7af79-114">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7af79-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7af79-115">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7af79-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7af79-116">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7af79-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af79-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7af79-117">Return value</span></span>

<span data-ttu-id="7af79-118">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7af79-118">Type: **uint**</span></span>

<span data-ttu-id="7af79-119">Одно значение.</span><span class="sxs-lookup"><span data-stu-id="7af79-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af79-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7af79-120">Remarks</span></span>

<span data-ttu-id="7af79-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7af79-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7af79-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="7af79-122">Vertex</span></span> | <span data-ttu-id="7af79-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7af79-123">Hull</span></span> | <span data-ttu-id="7af79-124">Домен</span><span class="sxs-lookup"><span data-stu-id="7af79-124">Domain</span></span> | <span data-ttu-id="7af79-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7af79-125">Geometry</span></span> | <span data-ttu-id="7af79-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7af79-126">Pixel</span></span> | <span data-ttu-id="7af79-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7af79-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7af79-128">x</span><span class="sxs-lookup"><span data-stu-id="7af79-128">x</span></span>      | <span data-ttu-id="7af79-129">x</span><span class="sxs-lookup"><span data-stu-id="7af79-129">x</span></span>    | <span data-ttu-id="7af79-130">x</span><span class="sxs-lookup"><span data-stu-id="7af79-130">x</span></span>      | <span data-ttu-id="7af79-131">x</span><span class="sxs-lookup"><span data-stu-id="7af79-131">x</span></span>        | <span data-ttu-id="7af79-132">x</span><span class="sxs-lookup"><span data-stu-id="7af79-132">x</span></span>     | <span data-ttu-id="7af79-133">x</span><span class="sxs-lookup"><span data-stu-id="7af79-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7af79-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7af79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af79-135">Методы Load</span><span class="sxs-lookup"><span data-stu-id="7af79-135">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="7af79-136">**битеаддрессбуффер**</span><span class="sxs-lookup"><span data-stu-id="7af79-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
