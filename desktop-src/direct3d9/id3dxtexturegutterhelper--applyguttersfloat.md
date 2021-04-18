---
description: Применяет переплет к буферу текстуры с плавающей запятой.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'Метод ID3DXTextureGutterHelper:: Апплигуттерсфлоат (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713765"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="c3acf-103">Метод ID3DXTextureGutterHelper:: Апплигуттерсфлоат</span><span class="sxs-lookup"><span data-stu-id="c3acf-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="c3acf-104">Применяет переплет к буферу текстуры с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="c3acf-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3acf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3acf-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="c3acf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3acf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3acf-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3acf-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3acf-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3acf-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3acf-109">Указатель на буфер данных текстуры с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="c3acf-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="c3acf-110">*Нумкоеффс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3acf-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3acf-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3acf-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3acf-112">Число скаляров на цветовой канал, используемое в памяти для хранения образцов.</span><span class="sxs-lookup"><span data-stu-id="c3acf-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="c3acf-113">Каждый шаг текселя содержит значения Нумкоеффс FLOAT.</span><span class="sxs-lookup"><span data-stu-id="c3acf-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="c3acf-114">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3acf-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3acf-115">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3acf-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3acf-116">Ширина текстуры в пикселях, полученная из [**ID3DXTextureGutterHelper:: полуширинные**](id3dxtexturegutterhelper--getwidth.md).</span><span class="sxs-lookup"><span data-stu-id="c3acf-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3acf-117">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3acf-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3acf-118">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3acf-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3acf-119">Высота текстуры (в пикселях), полученная из [**ID3DXTextureGutterHelper:: Height**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="c3acf-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3acf-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3acf-120">Return value</span></span>

<span data-ttu-id="c3acf-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3acf-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3acf-122">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c3acf-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c3acf-123">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="c3acf-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c3acf-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3acf-124">Remarks</span></span>

<span data-ttu-id="c3acf-125">[**Класс 2 пикселей текстуры**](id3dxtexturegutterhelper.md) создается путем повторной выборки класса 1 и 4 пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="c3acf-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3acf-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c3acf-126">Requirements</span></span>



| <span data-ttu-id="c3acf-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c3acf-127">Requirement</span></span> | <span data-ttu-id="c3acf-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c3acf-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3acf-129">Header</span><span class="sxs-lookup"><span data-stu-id="c3acf-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c3acf-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3acf-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c3acf-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3acf-131">Library</span></span><br/> | <dl> <span data-ttu-id="c3acf-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3acf-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3acf-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3acf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3acf-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="c3acf-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
