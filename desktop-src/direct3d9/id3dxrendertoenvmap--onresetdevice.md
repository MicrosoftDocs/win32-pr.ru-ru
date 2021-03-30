---
description: Этот метод используется для повторного получения ресурсов и сохранения начального состояния.
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: 'Метод ID3DXRenderToEnvMap:: Онресетдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d429c08d8bad23652a080998b6a4735132522ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354520"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a><span data-ttu-id="932b5-103">Метод ID3DXRenderToEnvMap:: Онресетдевице</span><span class="sxs-lookup"><span data-stu-id="932b5-103">ID3DXRenderToEnvMap::OnResetDevice method</span></span>

<span data-ttu-id="932b5-104">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="932b5-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="932b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="932b5-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="932b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="932b5-106">Parameters</span></span>

<span data-ttu-id="932b5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="932b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="932b5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="932b5-108">Return value</span></span>

<span data-ttu-id="932b5-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="932b5-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="932b5-110">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="932b5-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="932b5-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="932b5-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="932b5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="932b5-112">Remarks</span></span>

<span data-ttu-id="932b5-113">**ID3DXRenderToEnvMap:: онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов.</span><span class="sxs-lookup"><span data-stu-id="932b5-113">**ID3DXRenderToEnvMap::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="932b5-114">Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.</span><span class="sxs-lookup"><span data-stu-id="932b5-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="932b5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="932b5-115">Requirements</span></span>



| <span data-ttu-id="932b5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="932b5-116">Requirement</span></span> | <span data-ttu-id="932b5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="932b5-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="932b5-118">Header</span><span class="sxs-lookup"><span data-stu-id="932b5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="932b5-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="932b5-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="932b5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="932b5-120">Library</span></span><br/> | <dl> <span data-ttu-id="932b5-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="932b5-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="932b5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="932b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="932b5-123">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="932b5-123">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
