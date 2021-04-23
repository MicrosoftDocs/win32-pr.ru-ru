---
description: Подготавливает устройство для рисования линий.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'Метод ID3DXLine:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694285"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="f31fe-103">Метод ID3DXLine:: Begin</span><span class="sxs-lookup"><span data-stu-id="f31fe-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="f31fe-104">Подготавливает устройство для рисования линий.</span><span class="sxs-lookup"><span data-stu-id="f31fe-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f31fe-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="f31fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f31fe-106">Parameters</span></span>

<span data-ttu-id="f31fe-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f31fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f31fe-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f31fe-108">Return value</span></span>

<span data-ttu-id="f31fe-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f31fe-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f31fe-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f31fe-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f31fe-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f31fe-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f31fe-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f31fe-112">Remarks</span></span>

<span data-ttu-id="f31fe-113">Вызов **ID3DXLine:: Begin** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f31fe-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="f31fe-114">Если вызывается за пределами последовательности ID3DXLine:: Begin/ID3DXLine:: end, функции рисования будут внутренним вызовом ID3DXLine:: Begin и ID3DXLine:: end.</span><span class="sxs-lookup"><span data-stu-id="f31fe-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="f31fe-115">Чтобы избежать дополнительных издержек, следует использовать этот метод, если несколько функций рисования будут вызываться последовательно.</span><span class="sxs-lookup"><span data-stu-id="f31fe-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="f31fe-116">Этот метод должен вызываться из последовательности [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) и [**IDirect3DDevice9:: ендсцене**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="f31fe-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="f31fe-117">ID3DXLine:: Begin не может использоваться в качестве замены для [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="f31fe-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f31fe-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f31fe-118">Requirements</span></span>



| <span data-ttu-id="f31fe-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f31fe-119">Requirement</span></span> | <span data-ttu-id="f31fe-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f31fe-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31fe-121">Header</span><span class="sxs-lookup"><span data-stu-id="f31fe-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f31fe-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f31fe-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f31fe-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f31fe-123">Library</span></span><br/> | <dl> <span data-ttu-id="f31fe-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f31fe-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f31fe-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f31fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31fe-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="f31fe-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
