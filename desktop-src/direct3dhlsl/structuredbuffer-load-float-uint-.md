---
title: 'Функция Структуредбуффер:: Load (int, uint)'
description: 'Считывает данные буфера и возвращает сведения о состоянии операции. | Функция Структуредбуффер:: Load (int, uint)'
ms.assetid: d71c6057-6651-4b70-91cf-892fde6d0188
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
ms.openlocfilehash: 957b85631bbd19742cb7afe52f6bf061de323614
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273490"
---
# <a name="structuredbufferloadintuint-function"></a><span data-ttu-id="6c0c7-105">Функция Структуредбуффер:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="6c0c7-105">StructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="6c0c7-106">Считывает данные буфера и возвращает сведения о состоянии операции.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c0c7-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="6c0c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c0c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0c7-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c0c7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0c7-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-110">Type: **int**</span></span>

<span data-ttu-id="6c0c7-111">Расположение буфера.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6c0c7-112">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6c0c7-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0c7-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-113">Type: **uint**</span></span>

<span data-ttu-id="6c0c7-114">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-114">The status of the operation.</span></span> <span data-ttu-id="6c0c7-115">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0c7-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6c0c7-116">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6c0c7-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6c0c7-117">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c0c7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c0c7-118">Return value</span></span>

<span data-ttu-id="6c0c7-119">Тип:</span><span class="sxs-lookup"><span data-stu-id="6c0c7-119">Type:</span></span>

<span data-ttu-id="6c0c7-120">Возвращаемый тип соответствует типу в объявлении для объекта [**структуредбуффер**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0c7-120">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c0c7-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c0c7-121">Remarks</span></span>

<span data-ttu-id="6c0c7-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="6c0c7-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6c0c7-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="6c0c7-123">Vertex</span></span> | <span data-ttu-id="6c0c7-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="6c0c7-124">Hull</span></span> | <span data-ttu-id="6c0c7-125">Домен</span><span class="sxs-lookup"><span data-stu-id="6c0c7-125">Domain</span></span> | <span data-ttu-id="6c0c7-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="6c0c7-126">Geometry</span></span> | <span data-ttu-id="6c0c7-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="6c0c7-127">Pixel</span></span> | <span data-ttu-id="6c0c7-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="6c0c7-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6c0c7-129">x</span><span class="sxs-lookup"><span data-stu-id="6c0c7-129">x</span></span>     | <span data-ttu-id="6c0c7-130">x</span><span class="sxs-lookup"><span data-stu-id="6c0c7-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6c0c7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c0c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0c7-132">Методы Load</span><span class="sxs-lookup"><span data-stu-id="6c0c7-132">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 
