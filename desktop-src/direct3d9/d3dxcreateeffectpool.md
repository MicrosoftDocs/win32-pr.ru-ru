---
description: Создайте пул эффектов. Пул используется для совместного использования параметров различными эффектами.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Функция D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273932"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="7abe4-104">Функция D3DXCreateEffectPool</span><span class="sxs-lookup"><span data-stu-id="7abe4-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="7abe4-105">Создайте пул эффектов.</span><span class="sxs-lookup"><span data-stu-id="7abe4-105">Create an effect pool.</span></span> <span data-ttu-id="7abe4-106">Пул используется для совместного использования параметров различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="7abe4-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abe4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7abe4-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="7abe4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7abe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abe4-109">*пппул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7abe4-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7abe4-110">Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="7abe4-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="7abe4-111">Возвращает указатель на созданный пул.</span><span class="sxs-lookup"><span data-stu-id="7abe4-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abe4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7abe4-112">Return value</span></span>

<span data-ttu-id="7abe4-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7abe4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7abe4-114">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="7abe4-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="7abe4-115">Если аргументы недопустимы, метод возвратит D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="7abe4-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="7abe4-116">Если метод завершается с ошибкой, возвращается значение E \_ Failed.</span><span class="sxs-lookup"><span data-stu-id="7abe4-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7abe4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7abe4-117">Remarks</span></span>

<span data-ttu-id="7abe4-118">Для эффектов в пуле общие параметры с одинаковыми общими значениями имен.</span><span class="sxs-lookup"><span data-stu-id="7abe4-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abe4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7abe4-119">Requirements</span></span>



| <span data-ttu-id="7abe4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7abe4-120">Requirement</span></span> | <span data-ttu-id="7abe4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7abe4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abe4-122">Header</span><span class="sxs-lookup"><span data-stu-id="7abe4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7abe4-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7abe4-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7abe4-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7abe4-124">Library</span></span><br/> | <dl> <span data-ttu-id="7abe4-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7abe4-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7abe4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7abe4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abe4-127">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="7abe4-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




