---
description: Извлекает устройство Direct3D, связанное с картой среды.
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: Метод ID3DXRenderToEnvMap::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b5adc045beeefa220a849a6da752a8d3efc82ff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703717"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a><span data-ttu-id="4b6ae-103">Метод ID3DXRenderToEnvMap:: of Device</span><span class="sxs-lookup"><span data-stu-id="4b6ae-103">ID3DXRenderToEnvMap::GetDevice method</span></span>

<span data-ttu-id="4b6ae-104">Извлекает устройство Direct3D, связанное с картой среды.</span><span class="sxs-lookup"><span data-stu-id="4b6ae-104">Retrieves the Direct3D device associated with the environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b6ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b6ae-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="4b6ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b6ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b6ae-107">*ппдевице* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4b6ae-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4b6ae-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="4b6ae-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="4b6ae-109">Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с картой среды.</span><span class="sxs-lookup"><span data-stu-id="4b6ae-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface that represents the Direct3D device object associated with the environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b6ae-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b6ae-110">Return value</span></span>

<span data-ttu-id="4b6ae-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b6ae-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b6ae-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4b6ae-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4b6ae-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4b6ae-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="4b6ae-114">Вызов этого метода увеличивает внутренний счетчик ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="4b6ae-114">Calling this method increases the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="4b6ae-115">Не забудьте вызвать [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , когда вы завершите работу с этим интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="4b6ae-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6ae-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4b6ae-116">Requirements</span></span>



| <span data-ttu-id="4b6ae-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4b6ae-117">Requirement</span></span> | <span data-ttu-id="4b6ae-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ae-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6ae-119">Header</span><span class="sxs-lookup"><span data-stu-id="4b6ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4b6ae-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b6ae-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4b6ae-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b6ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="4b6ae-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b6ae-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b6ae-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b6ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b6ae-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="4b6ae-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
