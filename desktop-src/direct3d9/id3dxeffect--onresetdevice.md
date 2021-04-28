---
description: 'Метод ID3DXEffect:: Онресетдевице. Используйте этот метод для повторного получения ресурсов и сохранения начального состояния.'
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'Метод ID3DXEffect:: Онресетдевице (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a10d9d0a9092bf7a0fdd345cde8220675503acd0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114932"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="7af50-103">Метод ID3DXEffect:: Онресетдевице</span><span class="sxs-lookup"><span data-stu-id="7af50-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="7af50-104">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="7af50-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7af50-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="7af50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7af50-106">Parameters</span></span>

<span data-ttu-id="7af50-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7af50-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7af50-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7af50-108">Return value</span></span>

<span data-ttu-id="7af50-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7af50-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7af50-110">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="7af50-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7af50-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="7af50-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af50-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="7af50-112">Remarks</span></span>

<span data-ttu-id="7af50-113">**ID3DXEffect:: онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов.</span><span class="sxs-lookup"><span data-stu-id="7af50-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="7af50-114">Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.</span><span class="sxs-lookup"><span data-stu-id="7af50-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af50-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7af50-115">Requirements</span></span>



| <span data-ttu-id="7af50-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7af50-116">Requirement</span></span> | <span data-ttu-id="7af50-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7af50-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af50-118">Header</span><span class="sxs-lookup"><span data-stu-id="7af50-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7af50-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7af50-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7af50-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7af50-120">Library</span></span><br/> | <dl> <span data-ttu-id="7af50-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7af50-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7af50-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7af50-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af50-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="7af50-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
