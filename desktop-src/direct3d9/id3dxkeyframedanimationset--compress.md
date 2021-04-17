---
description: Преобразует анимации в наборе анимации в сжатый формат и возвращает указатель на буфер, в котором хранятся сжатые данные.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Метод ID3DXKeyframedAnimationSet:: сжимать (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703984"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="db11f-103">Метод ID3DXKeyframedAnimationSet:: сжимать</span><span class="sxs-lookup"><span data-stu-id="db11f-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="db11f-104">Преобразует анимации в наборе анимации в сжатый формат и возвращает указатель на буфер, в котором хранятся сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="db11f-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="db11f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db11f-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="db11f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db11f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db11f-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db11f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db11f-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db11f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db11f-109">Одно из значений [**\_ флагов D3DXCOMPRESSION**](./d3dxcompression-flags.md) , определяющих режим сжатия, используемый для хранения данных сжатого набора анимации.</span><span class="sxs-lookup"><span data-stu-id="db11f-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="db11f-110">D3DXCOMPRESS \_ по умолчанию — единственное поддерживаемое в настоящее время значение.</span><span class="sxs-lookup"><span data-stu-id="db11f-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="db11f-111">*Потери* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db11f-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db11f-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db11f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db11f-113">Отношение степени потери сжатия в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="db11f-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="db11f-114">*фиерарчи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db11f-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db11f-115">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="db11f-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="db11f-116">Указатель на иерархию фрейма преобразования [**D3DXFRAME**](d3dxframe.md) .</span><span class="sxs-lookup"><span data-stu-id="db11f-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="db11f-117">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="db11f-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="db11f-118">*ппкомпресседдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db11f-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db11f-119">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="db11f-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="db11f-120">Адрес указателя на набор сжатых данных анимации [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="db11f-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db11f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db11f-121">Return value</span></span>

<span data-ttu-id="db11f-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db11f-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db11f-123">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="db11f-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="db11f-124">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="db11f-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="db11f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="db11f-125">Requirements</span></span>



| <span data-ttu-id="db11f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="db11f-126">Requirement</span></span> | <span data-ttu-id="db11f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="db11f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db11f-128">Header</span><span class="sxs-lookup"><span data-stu-id="db11f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="db11f-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="db11f-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="db11f-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db11f-130">Library</span></span><br/> | <dl> <span data-ttu-id="db11f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db11f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db11f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db11f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db11f-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="db11f-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
