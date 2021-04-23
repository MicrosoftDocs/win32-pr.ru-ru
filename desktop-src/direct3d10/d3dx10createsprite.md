---
description: Создайте спрайт для рисования двухмерной текстуры. Примечание. вместо использования этой функции рекомендуется использовать Direct2D и библиотеку Директкстк, класс SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Функция D3DX10CreateSprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703713"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="47c67-103">Функция D3DX10CreateSprite</span><span class="sxs-lookup"><span data-stu-id="47c67-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="47c67-104">Создайте спрайт для рисования двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="47c67-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="47c67-105">Вместо использования этой функции рекомендуется использовать [Direct2D](../direct2d/direct2d-portal.md) и библиотеку [Директкстк](https://github.com/Microsoft/DirectXTK) , класс **SpriteBatch** .</span><span class="sxs-lookup"><span data-stu-id="47c67-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="47c67-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47c67-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="47c67-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="47c67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c67-108">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47c67-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c67-109">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="47c67-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="47c67-110">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет рисовать спрайт.</span><span class="sxs-lookup"><span data-stu-id="47c67-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="47c67-111">*кдевицебуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47c67-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c67-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47c67-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47c67-113">Размер буфера вершин в числе спрайтов, который будет отправлен на устройство при вызове [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) или [**ID3DX10Sprite::D равспритесиммедиате**](id3dx10sprite-drawspritesimmediate.md) .</span><span class="sxs-lookup"><span data-stu-id="47c67-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="47c67-114">Это должно быть небольшое число, если известно, что вы будете отображать небольшое количество спрайтов за раз (чтобы сэкономить память) и большое число, если известно, что в каждый момент времени будет отображено большое количество спрайтов.</span><span class="sxs-lookup"><span data-stu-id="47c67-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="47c67-115">Максимальное значение — 4096.</span><span class="sxs-lookup"><span data-stu-id="47c67-115">The maximum value is 4096.</span></span> <span data-ttu-id="47c67-116">Если задано значение 0, размер буфера вершин будет автоматически установлен в 4096.</span><span class="sxs-lookup"><span data-stu-id="47c67-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="47c67-117">*ппсприте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="47c67-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c67-118">Тип: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="47c67-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="47c67-119">Адрес указателя на интерфейс Sprite (см. [**интерфейс ID3DX10Sprite**](id3dx10sprite.md)).</span><span class="sxs-lookup"><span data-stu-id="47c67-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c67-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47c67-120">Return value</span></span>

<span data-ttu-id="47c67-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47c67-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47c67-122">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="47c67-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="47c67-123">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="47c67-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c67-124">Требования</span><span class="sxs-lookup"><span data-stu-id="47c67-124">Requirements</span></span>



| <span data-ttu-id="47c67-125">Требование</span><span class="sxs-lookup"><span data-stu-id="47c67-125">Requirement</span></span> | <span data-ttu-id="47c67-126">Значение</span><span class="sxs-lookup"><span data-stu-id="47c67-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47c67-127">Header</span><span class="sxs-lookup"><span data-stu-id="47c67-127">Header</span></span><br/>  | <dl> <span data-ttu-id="47c67-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c67-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="47c67-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47c67-129">Library</span></span><br/> | <dl> <span data-ttu-id="47c67-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47c67-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c67-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47c67-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c67-132">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="47c67-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
