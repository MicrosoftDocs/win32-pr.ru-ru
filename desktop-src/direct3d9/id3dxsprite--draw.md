---
description: Добавляет спрайт в список пакетных спрайтов.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D необработанный метод (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713957"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="45e24-103">ID3DXSprite::D необработанный метод</span><span class="sxs-lookup"><span data-stu-id="45e24-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="45e24-104">Добавляет спрайт в список пакетных спрайтов.</span><span class="sxs-lookup"><span data-stu-id="45e24-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="45e24-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45e24-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="45e24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45e24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45e24-107">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45e24-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e24-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="45e24-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="45e24-109">Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру спрайта.</span><span class="sxs-lookup"><span data-stu-id="45e24-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="45e24-110">*псркрект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45e24-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e24-111">Тип: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="45e24-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="45e24-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую часть текстуры источника, используемую для спрайта.</span><span class="sxs-lookup"><span data-stu-id="45e24-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="45e24-113">Если этот параметр имеет **значение NULL**, то для спрайта используется все исходное изображение.</span><span class="sxs-lookup"><span data-stu-id="45e24-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="45e24-114">*пцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45e24-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e24-115">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="45e24-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="45e24-116">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , определяющий центр спрайта.</span><span class="sxs-lookup"><span data-stu-id="45e24-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="45e24-117">Если этот аргумент имеет **значение NULL**, то используется точка (0, 0, 0), которая является верхним левым углом.</span><span class="sxs-lookup"><span data-stu-id="45e24-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="45e24-118">*ппоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45e24-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e24-119">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="45e24-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="45e24-120">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , определяющий расположение спрайта.</span><span class="sxs-lookup"><span data-stu-id="45e24-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="45e24-121">Если этот аргумент имеет **значение NULL**, то используется точка (0, 0, 0), которая является верхним левым углом.</span><span class="sxs-lookup"><span data-stu-id="45e24-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="45e24-122">*Цветовая палитра* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45e24-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45e24-123">Тип: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="45e24-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="45e24-124">Тип [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="45e24-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="45e24-125">Этот параметр используется для связи цвета и альфа-каналов.</span><span class="sxs-lookup"><span data-stu-id="45e24-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="45e24-126">Значение 0xFFFFFFFF сохраняет исходный цвет и альфа-данные.</span><span class="sxs-lookup"><span data-stu-id="45e24-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="45e24-127">Чтобы создать этот цвет, используйте макрос [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) .</span><span class="sxs-lookup"><span data-stu-id="45e24-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45e24-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45e24-128">Return value</span></span>

<span data-ttu-id="45e24-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45e24-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45e24-130">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="45e24-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="45e24-131">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="45e24-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="45e24-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45e24-132">Remarks</span></span>

<span data-ttu-id="45e24-133">Для масштабирования, вращения или перевода спрайта вызовите [**ID3DXSprite:: сеттрансформ**](id3dxsprite--settransform.md) с матрицей, которая содержит значения Scale, поверните и сдвига (SRT) перед вызовом ID3DXSprite::D RAW.</span><span class="sxs-lookup"><span data-stu-id="45e24-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="45e24-134">Сведения о настройке значений SRT в матрице см. в разделе [преобразования матрицы](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="45e24-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45e24-135">Требования</span><span class="sxs-lookup"><span data-stu-id="45e24-135">Requirements</span></span>



| <span data-ttu-id="45e24-136">Требование</span><span class="sxs-lookup"><span data-stu-id="45e24-136">Requirement</span></span> | <span data-ttu-id="45e24-137">Значение</span><span class="sxs-lookup"><span data-stu-id="45e24-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45e24-138">Header</span><span class="sxs-lookup"><span data-stu-id="45e24-138">Header</span></span><br/>  | <dl> <span data-ttu-id="45e24-139"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="45e24-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="45e24-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45e24-140">Library</span></span><br/> | <dl> <span data-ttu-id="45e24-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45e24-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45e24-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45e24-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45e24-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="45e24-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="45e24-144">**ID3DXSprite:: Transform**</span><span class="sxs-lookup"><span data-stu-id="45e24-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
