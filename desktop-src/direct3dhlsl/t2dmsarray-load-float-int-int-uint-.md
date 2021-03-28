---
title: 'Функция Texture2DMSArray:: Load (int, int, int, uint)'
description: 'Считывает данные текстуры и возвращает состояние операции. | Функция Texture2DMSArray:: Load (int, int, int, uint)'
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: 0065ee5e420c67876b87c67be1f5e5c8ff10e65b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998042"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a><span data-ttu-id="3f997-105">Функция Texture2DMSArray:: Load (int, int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="3f997-105">Texture2DMSArray::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="3f997-106">Считывает данные текстуры и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3f997-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f997-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f997-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="3f997-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f997-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f997-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f997-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="3f997-110">Type: **int**</span></span>

<span data-ttu-id="3f997-111">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="3f997-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="3f997-112">*sampleindex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f997-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f997-113">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3f997-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3f997-114">Пример индекса.</span><span class="sxs-lookup"><span data-stu-id="3f997-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="3f997-115">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f997-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f997-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="3f997-116">Type: **int**</span></span>

<span data-ttu-id="3f997-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="3f997-117">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3f997-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f997-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f997-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f997-119">Type: **uint**</span></span>

<span data-ttu-id="3f997-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3f997-120">The status of the operation.</span></span> <span data-ttu-id="3f997-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3f997-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3f997-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3f997-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3f997-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3f997-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f997-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f997-124">Return value</span></span>

<span data-ttu-id="3f997-125">Тип:</span><span class="sxs-lookup"><span data-stu-id="3f997-125">Type:</span></span>

<span data-ttu-id="3f997-126">Возвращаемый тип соответствует типу в объявлении для объекта [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) .</span><span class="sxs-lookup"><span data-stu-id="3f997-126">The return type matches the type in the declaration for the [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f997-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f997-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f997-128">Методы Load</span><span class="sxs-lookup"><span data-stu-id="3f997-128">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="3f997-129">**Texture2DMSArray**</span><span class="sxs-lookup"><span data-stu-id="3f997-129">**Texture2DMSArray**</span></span>](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
