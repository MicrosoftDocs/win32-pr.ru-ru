---
description: Создает интерфейс набора анимации ID3DXCompressedAnimationSet с кадром, который хранит данные опорных кадров в сжатом формате.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Функция D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000390"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="97d65-103">Функция D3DXCreateCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="97d65-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="97d65-104">Создает интерфейс набора анимации [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) с кадром, который хранит данные опорных кадров в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="97d65-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97d65-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="97d65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97d65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d65-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97d65-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97d65-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97d65-109">Указатель на имя набора анимации.</span><span class="sxs-lookup"><span data-stu-id="97d65-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="97d65-110">*Тикксперсеконд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97d65-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-111">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97d65-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97d65-112">Число тактов опорного кадра в секунду.</span><span class="sxs-lookup"><span data-stu-id="97d65-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="97d65-113">*Воспроизведение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97d65-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-114">Тип: **[ **D3DXPLAYBACK \_ тип**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="97d65-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="97d65-115">Тип цикла воспроизведения набора анимации.</span><span class="sxs-lookup"><span data-stu-id="97d65-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="97d65-116">См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="97d65-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="97d65-117">*пкомпресседдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97d65-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-118">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="97d65-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="97d65-119">Указатель на буфер [**ID3DXBuffer**](id3dxbuffer.md) , в котором набор анимации хранится в виде сжатых данных.</span><span class="sxs-lookup"><span data-stu-id="97d65-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="97d65-120">*Нумкаллбакккэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97d65-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97d65-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97d65-122">Число ключей обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="97d65-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="97d65-123">*пкаллкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97d65-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-124">Тип: **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="97d65-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="97d65-125">Указатель на структуру [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , в которой хранятся данные обратного вызова пользователя.</span><span class="sxs-lookup"><span data-stu-id="97d65-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="97d65-126">*ппаниматионсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97d65-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97d65-127">Тип: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="97d65-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="97d65-128">Адрес указателя на интерфейс [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) , в котором хранятся данные набора анимаций с кадрами в сжатом формате.</span><span class="sxs-lookup"><span data-stu-id="97d65-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d65-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97d65-129">Return value</span></span>

<span data-ttu-id="97d65-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97d65-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97d65-131">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="97d65-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="97d65-132">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="97d65-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d65-133">Требования</span><span class="sxs-lookup"><span data-stu-id="97d65-133">Requirements</span></span>



| <span data-ttu-id="97d65-134">Требование</span><span class="sxs-lookup"><span data-stu-id="97d65-134">Requirement</span></span> | <span data-ttu-id="97d65-135">Значение</span><span class="sxs-lookup"><span data-stu-id="97d65-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d65-136">Header</span><span class="sxs-lookup"><span data-stu-id="97d65-136">Header</span></span><br/>  | <dl> <span data-ttu-id="97d65-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d65-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="97d65-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97d65-138">Library</span></span><br/> | <dl> <span data-ttu-id="97d65-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97d65-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97d65-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97d65-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d65-141">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="97d65-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
