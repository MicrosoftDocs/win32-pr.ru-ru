---
description: Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: 'Метод ID3DXSprite:: Онлостдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f6b2b676e95b48f50b5c25a4bfc3a1bf3e7d610d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355140"
---
# <a name="id3dxspriteonlostdevice-method"></a><span data-ttu-id="89e34-104">Метод ID3DXSprite:: Онлостдевице</span><span class="sxs-lookup"><span data-stu-id="89e34-104">ID3DXSprite::OnLostDevice method</span></span>

<span data-ttu-id="89e34-105">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="89e34-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="89e34-106">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="89e34-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e34-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89e34-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="89e34-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89e34-108">Parameters</span></span>

<span data-ttu-id="89e34-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="89e34-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89e34-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89e34-110">Return value</span></span>

<span data-ttu-id="89e34-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89e34-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89e34-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="89e34-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="89e34-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="89e34-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="89e34-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89e34-114">Remarks</span></span>

<span data-ttu-id="89e34-115">Этот метод должен вызываться при каждом потере устройства или до того, как пользователь вызывает [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="89e34-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="89e34-116">Даже если устройство не было потеряно, **ID3DXSprite:: онлостдевице** отвечает за освобождение статеблоккс и других ресурсов, которые, возможно, потребуется освободить перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="89e34-116">Even if the device was not actually lost, **ID3DXSprite::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="89e34-117">В результате объект Font не может быть использован повторно перед вызовом **IDirect3DDevice9:: Reset** , а затем [**ID3DXSprite:: онресетдевице**](id3dxsprite--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="89e34-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89e34-118">Требования</span><span class="sxs-lookup"><span data-stu-id="89e34-118">Requirements</span></span>



| <span data-ttu-id="89e34-119">Требование</span><span class="sxs-lookup"><span data-stu-id="89e34-119">Requirement</span></span> | <span data-ttu-id="89e34-120">Значение</span><span class="sxs-lookup"><span data-stu-id="89e34-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89e34-121">Header</span><span class="sxs-lookup"><span data-stu-id="89e34-121">Header</span></span><br/>  | <dl> <span data-ttu-id="89e34-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e34-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="89e34-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89e34-123">Library</span></span><br/> | <dl> <span data-ttu-id="89e34-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89e34-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89e34-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89e34-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e34-126">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="89e34-126">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




