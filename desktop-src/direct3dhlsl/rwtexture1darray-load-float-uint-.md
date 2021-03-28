---
title: 'Функция RWTexture1DArray:: Load (int, uint)'
description: 'Считывает данные текстуры и возвращает сведения о состоянии операции. | Функция RWTexture1DArray:: Load (int, uint)'
ms.assetid: EF1D51CC-E037-4E04-9DD6-6A9C5950E5B5
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
ms.openlocfilehash: 5a46dde9b75d3194cc081409fe2b450c5453d7c1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986280"
---
# <a name="rwtexture1darrayloadintuint-function"></a><span data-ttu-id="6ca4a-105">Функция RWTexture1DArray:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="6ca4a-105">RWTexture1DArray::Load(int,uint) function</span></span>

<span data-ttu-id="6ca4a-106">Считывает данные текстуры и возвращает сведения о состоянии операции.</span><span class="sxs-lookup"><span data-stu-id="6ca4a-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca4a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ca4a-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="6ca4a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ca4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca4a-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ca4a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca4a-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="6ca4a-110">Type: **int**</span></span>

<span data-ttu-id="6ca4a-111">Расположение текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ca4a-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="6ca4a-112">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ca4a-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca4a-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="6ca4a-113">Type: **uint**</span></span>

<span data-ttu-id="6ca4a-114">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="6ca4a-114">The status of the operation.</span></span> <span data-ttu-id="6ca4a-115">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca4a-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6ca4a-116">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6ca4a-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6ca4a-117">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="6ca4a-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca4a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ca4a-118">Return value</span></span>

<span data-ttu-id="6ca4a-119">Тип:</span><span class="sxs-lookup"><span data-stu-id="6ca4a-119">Type:</span></span>

<span data-ttu-id="6ca4a-120">Возвращаемый тип соответствует типу в объявлении для объекта [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca4a-120">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca4a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ca4a-121">Remarks</span></span>

<span data-ttu-id="6ca4a-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="6ca4a-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6ca4a-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="6ca4a-123">Vertex</span></span> | <span data-ttu-id="6ca4a-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="6ca4a-124">Hull</span></span> | <span data-ttu-id="6ca4a-125">Домен</span><span class="sxs-lookup"><span data-stu-id="6ca4a-125">Domain</span></span> | <span data-ttu-id="6ca4a-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="6ca4a-126">Geometry</span></span> | <span data-ttu-id="6ca4a-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="6ca4a-127">Pixel</span></span> | <span data-ttu-id="6ca4a-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="6ca4a-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6ca4a-129">x</span><span class="sxs-lookup"><span data-stu-id="6ca4a-129">x</span></span>     | <span data-ttu-id="6ca4a-130">x</span><span class="sxs-lookup"><span data-stu-id="6ca4a-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6ca4a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ca4a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca4a-132">Методы Load</span><span class="sxs-lookup"><span data-stu-id="6ca4a-132">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 
