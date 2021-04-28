---
description: 'Метод ID3DXEffect:: Онлостдевице. Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.'
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: 'Метод ID3DXEffect:: Онлостдевице (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1aacdbae268b58a966256a99081b9943d0bfcc92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114972"
---
# <a name="id3dxeffectonlostdevice-method"></a><span data-ttu-id="72370-104">Метод ID3DXEffect:: Онлостдевице</span><span class="sxs-lookup"><span data-stu-id="72370-104">ID3DXEffect::OnLostDevice method</span></span>

<span data-ttu-id="72370-105">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="72370-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="72370-106">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="72370-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="72370-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72370-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="72370-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="72370-108">Parameters</span></span>

<span data-ttu-id="72370-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="72370-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72370-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72370-110">Return value</span></span>

<span data-ttu-id="72370-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72370-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72370-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="72370-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="72370-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="72370-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="72370-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="72370-114">Remarks</span></span>

<span data-ttu-id="72370-115">Этот метод должен вызываться при каждом потере устройства или до того, как пользователь вызывает [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="72370-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="72370-116">Даже если устройство не было потеряно, **ID3DXEffect:: онлостдевице** отвечает за освобождение статеблоккс и других ресурсов, которые, возможно, потребуется освободить перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="72370-116">Even if the device was not actually lost, **ID3DXEffect::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="72370-117">В результате объект Font не может быть использован повторно перед вызовом **IDirect3DDevice9:: Reset** , а затем [**ID3DXEffect:: онресетдевице**](id3dxeffect--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="72370-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72370-118">Требования</span><span class="sxs-lookup"><span data-stu-id="72370-118">Requirements</span></span>



| <span data-ttu-id="72370-119">Требование</span><span class="sxs-lookup"><span data-stu-id="72370-119">Requirement</span></span> | <span data-ttu-id="72370-120">Значение</span><span class="sxs-lookup"><span data-stu-id="72370-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72370-121">Header</span><span class="sxs-lookup"><span data-stu-id="72370-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72370-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="72370-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="72370-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72370-123">Library</span></span><br/> | <dl> <span data-ttu-id="72370-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72370-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="72370-125">См. также</span><span class="sxs-lookup"><span data-stu-id="72370-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72370-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="72370-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




