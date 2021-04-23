---
description: Извлекает устройство, связанное с объектом Sprite.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: Метод ID3DXSprite::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424461"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="37739-103">Метод ID3DXSprite:: of Device</span><span class="sxs-lookup"><span data-stu-id="37739-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="37739-104">Извлекает устройство, связанное с объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="37739-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37739-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37739-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="37739-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37739-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37739-107">*ппдевице* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="37739-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="37739-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="37739-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="37739-109">Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="37739-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37739-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37739-110">Return value</span></span>

<span data-ttu-id="37739-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37739-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37739-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="37739-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="37739-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="37739-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="37739-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37739-114">Remarks</span></span>

<span data-ttu-id="37739-115">Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="37739-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="37739-116">Требования</span><span class="sxs-lookup"><span data-stu-id="37739-116">Requirements</span></span>



| <span data-ttu-id="37739-117">Требование</span><span class="sxs-lookup"><span data-stu-id="37739-117">Requirement</span></span> | <span data-ttu-id="37739-118">Значение</span><span class="sxs-lookup"><span data-stu-id="37739-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37739-119">Header</span><span class="sxs-lookup"><span data-stu-id="37739-119">Header</span></span><br/>  | <dl> <span data-ttu-id="37739-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="37739-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="37739-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37739-121">Library</span></span><br/> | <dl> <span data-ttu-id="37739-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37739-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37739-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37739-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37739-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="37739-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
