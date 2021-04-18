---
description: Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'Метод ID3DXFont:: Онлостдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685006"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="0a5eb-104">Метод ID3DXFont:: Онлостдевице</span><span class="sxs-lookup"><span data-stu-id="0a5eb-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="0a5eb-105">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="0a5eb-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="0a5eb-106">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="0a5eb-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a5eb-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="0a5eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a5eb-108">Parameters</span></span>

<span data-ttu-id="0a5eb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0a5eb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a5eb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a5eb-110">Return value</span></span>

<span data-ttu-id="0a5eb-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a5eb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a5eb-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="0a5eb-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0a5eb-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0a5eb-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a5eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a5eb-114">Remarks</span></span>

<span data-ttu-id="0a5eb-115">Этот метод должен вызываться при каждом потере устройства или до того, как пользователь вызывает [**Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="0a5eb-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="0a5eb-116">Даже если устройство не было потеряно, **онлостдевице** отвечает за освобождение статеблоккс и других ресурсов, которые, возможно, потребуется освободить перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="0a5eb-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="0a5eb-117">В результате объект Font не может быть использован повторно перед вызовом **Reset** , а затем [**онресетдевице**](id3dxfont--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0a5eb-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5eb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0a5eb-118">Requirements</span></span>



| <span data-ttu-id="0a5eb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0a5eb-119">Requirement</span></span> | <span data-ttu-id="0a5eb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0a5eb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5eb-121">Header</span><span class="sxs-lookup"><span data-stu-id="0a5eb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0a5eb-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a5eb-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0a5eb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a5eb-123">Library</span></span><br/> | <dl> <span data-ttu-id="0a5eb-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a5eb-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a5eb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a5eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a5eb-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="0a5eb-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




