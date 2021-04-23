---
title: 'Функция Texture2DArray:: Load (int, int, uint)'
description: 'Считывает данные текстуры и возвращает состояние операции. | Функция Texture2DArray:: Load (int, int, uint)'
ms.assetid: 551EA931-6D24-478B-B741-3DD5B1E030E2
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
ms.openlocfilehash: 0a1dd61506eba7ea6e334f2b3e3f89dd6bca5873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998122"
---
# <a name="texture2darrayloadintintuint-function"></a><span data-ttu-id="8fece-105">Функция Texture2DArray:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="8fece-105">Texture2DArray::Load(int,int,uint) function</span></span>

<span data-ttu-id="8fece-106">Считывает данные текстуры и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="8fece-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fece-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fece-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="8fece-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fece-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fece-109">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fece-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fece-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="8fece-110">Type: **int**</span></span>

<span data-ttu-id="8fece-111">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="8fece-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8fece-112">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fece-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fece-113">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="8fece-113">Type: **int**</span></span>

<span data-ttu-id="8fece-114">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="8fece-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="8fece-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fece-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fece-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="8fece-116">Type: **uint**</span></span>

<span data-ttu-id="8fece-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="8fece-117">The status of the operation.</span></span> <span data-ttu-id="8fece-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8fece-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8fece-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8fece-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8fece-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8fece-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fece-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fece-121">Return value</span></span>

<span data-ttu-id="8fece-122">Тип:</span><span class="sxs-lookup"><span data-stu-id="8fece-122">Type:</span></span>

<span data-ttu-id="8fece-123">Возвращаемый тип соответствует типу в объявлении для объекта [**Texture2DArray**](sm5-object-texture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="8fece-123">The return type matches the type in the declaration for the [**Texture2DArray**](sm5-object-texture2darray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fece-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fece-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fece-125">Методы Load</span><span class="sxs-lookup"><span data-stu-id="8fece-125">Load methods</span></span>](texture2darray-load.md)
</dt> </dl>

 

 
