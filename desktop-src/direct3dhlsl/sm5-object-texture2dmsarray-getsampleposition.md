---
title: 'Функция Texture2DMSArray:: Жетсамплепоситион'
description: 'Возвращает расположение указанного образца. | Функция Texture2DMSArray:: Жетсамплепоситион'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- Функция Жетсамплепоситион HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273644"
---
# <a name="texture2dmsarraygetsampleposition-function"></a><span data-ttu-id="d4044-105">Функция Texture2DMSArray:: Жетсамплепоситион</span><span class="sxs-lookup"><span data-stu-id="d4044-105">Texture2DMSArray::GetSamplePosition function</span></span>

<span data-ttu-id="d4044-106">Возвращает расположение указанного образца.</span><span class="sxs-lookup"><span data-stu-id="d4044-106">Gets the position of the specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4044-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4044-107">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="d4044-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4044-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4044-109">*sampleindex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4044-109">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4044-110">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d4044-110">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d4044-111">Отсчитываемый от нуля индекс образца расположения.</span><span class="sxs-lookup"><span data-stu-id="d4044-111">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4044-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4044-112">Return value</span></span>

<span data-ttu-id="d4044-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="d4044-113">Type: **float2**</span></span>

<span data-ttu-id="d4044-114">Пример расположения.</span><span class="sxs-lookup"><span data-stu-id="d4044-114">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4044-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4044-115">Remarks</span></span>

<span data-ttu-id="d4044-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d4044-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d4044-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="d4044-117">Vertex</span></span> | <span data-ttu-id="d4044-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d4044-118">Hull</span></span> | <span data-ttu-id="d4044-119">Домен</span><span class="sxs-lookup"><span data-stu-id="d4044-119">Domain</span></span> | <span data-ttu-id="d4044-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d4044-120">Geometry</span></span> | <span data-ttu-id="d4044-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d4044-121">Pixel</span></span> | <span data-ttu-id="d4044-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d4044-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d4044-123">x</span><span class="sxs-lookup"><span data-stu-id="d4044-123">x</span></span>      | <span data-ttu-id="d4044-124">x</span><span class="sxs-lookup"><span data-stu-id="d4044-124">x</span></span>    | <span data-ttu-id="d4044-125">x</span><span class="sxs-lookup"><span data-stu-id="d4044-125">x</span></span>      | <span data-ttu-id="d4044-126">x</span><span class="sxs-lookup"><span data-stu-id="d4044-126">x</span></span>        | <span data-ttu-id="d4044-127">x</span><span class="sxs-lookup"><span data-stu-id="d4044-127">x</span></span>     | <span data-ttu-id="d4044-128">x</span><span class="sxs-lookup"><span data-stu-id="d4044-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d4044-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4044-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4044-130">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d4044-130">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="d4044-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d4044-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
