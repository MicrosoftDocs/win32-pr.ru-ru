---
description: Создает интерфейс набора анимации с ID3DXKeyframedAnimationSet ключом в рамке.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Функция D3DXCreateKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694253"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="3c7d5-103">Функция D3DXCreateKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="3c7d5-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="3c7d5-104">Создает интерфейс набора анимации с [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) ключом в рамке.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c7d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c7d5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="3c7d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c7d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c7d5-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c7d5-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c7d5-109">Указатель на имя набора анимации.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="3c7d5-110">*Тикксперсеконд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-111">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c7d5-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c7d5-112">Число тактов опорного кадра в секунду.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="3c7d5-113">*Воспроизведение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-114">Тип: **[ **D3DXPLAYBACK \_ тип**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="3c7d5-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="3c7d5-115">Тип цикла воспроизведения набора анимации.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="3c7d5-116">См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="3c7d5-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c7d5-117">*Нуманиматионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c7d5-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c7d5-119">Количество наборов анимации Scale, вращение и сдвига (SRT).</span><span class="sxs-lookup"><span data-stu-id="3c7d5-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="3c7d5-120">*Нумкаллбакккэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c7d5-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c7d5-122">Число ключей обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="3c7d5-123">*пкаллкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-124">Тип: **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c7d5-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="3c7d5-125">Указатель на структуру [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , в которой хранятся данные обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="3c7d5-126">*ппаниматионсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3c7d5-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7d5-127">Тип: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c7d5-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="3c7d5-128">Адрес указателя на интерфейсный набор эффектов анимации [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) Key.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c7d5-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c7d5-129">Return value</span></span>

<span data-ttu-id="3c7d5-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c7d5-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c7d5-131">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3c7d5-132">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3c7d5-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c7d5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3c7d5-133">Requirements</span></span>



| <span data-ttu-id="3c7d5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3c7d5-134">Requirement</span></span> | <span data-ttu-id="3c7d5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3c7d5-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7d5-136">Header</span><span class="sxs-lookup"><span data-stu-id="3c7d5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3c7d5-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d5-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3c7d5-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c7d5-138">Library</span></span><br/> | <dl> <span data-ttu-id="3c7d5-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c7d5-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c7d5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c7d5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c7d5-141">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="3c7d5-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
