---
description: Создает объект Sprite, связанный с определенным устройством. Объекты Sprite используются для рисования 2D-изображений на экране.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Функция D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713695"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="f8f47-104">Функция D3DXCreateSprite</span><span class="sxs-lookup"><span data-stu-id="f8f47-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="f8f47-105">Создает объект Sprite, связанный с определенным устройством.</span><span class="sxs-lookup"><span data-stu-id="f8f47-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="f8f47-106">Объекты Sprite используются для рисования 2D-изображений на экране.</span><span class="sxs-lookup"><span data-stu-id="f8f47-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f47-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8f47-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="f8f47-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8f47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f47-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8f47-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f47-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f8f47-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f8f47-111">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, связываемое с спрайтом.</span><span class="sxs-lookup"><span data-stu-id="f8f47-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="f8f47-112">*ппсприте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8f47-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f47-113">Тип: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8f47-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="f8f47-114">Адрес указателя на интерфейс [**ID3DXSprite**](id3dxsprite.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f47-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="f8f47-115">Этот интерфейс позволяет пользователю получить доступ к функциям спрайта.</span><span class="sxs-lookup"><span data-stu-id="f8f47-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f47-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8f47-116">Return value</span></span>

<span data-ttu-id="f8f47-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8f47-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8f47-118">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f8f47-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f8f47-119">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f8f47-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f47-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8f47-120">Remarks</span></span>

<span data-ttu-id="f8f47-121">Этот интерфейс можно использовать для рисования двух трехмерных изображений в пространстве экрана связанного устройства.</span><span class="sxs-lookup"><span data-stu-id="f8f47-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f47-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f8f47-122">Requirements</span></span>



| <span data-ttu-id="f8f47-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f8f47-123">Requirement</span></span> | <span data-ttu-id="f8f47-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f8f47-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f47-125">Header</span><span class="sxs-lookup"><span data-stu-id="f8f47-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f8f47-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f47-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f8f47-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8f47-127">Library</span></span><br/> | <dl> <span data-ttu-id="f8f47-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8f47-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8f47-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8f47-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f47-130">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="f8f47-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
