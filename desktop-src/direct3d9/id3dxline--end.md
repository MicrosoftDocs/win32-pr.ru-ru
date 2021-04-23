---
description: 'Восстанавливает состояние устройства в том виде, в котором оно было при вызове ID3DXLine:: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'Метод ID3DXLine:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694282"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="9ce2e-103">Метод ID3DXLine:: end</span><span class="sxs-lookup"><span data-stu-id="9ce2e-103">ID3DXLine::End method</span></span>

<span data-ttu-id="9ce2e-104">Восстанавливает состояние устройства в том виде, в котором оно было при вызове [**ID3DXLine:: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce2e-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ce2e-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="9ce2e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ce2e-106">Parameters</span></span>

<span data-ttu-id="9ce2e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9ce2e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ce2e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ce2e-108">Return value</span></span>

<span data-ttu-id="9ce2e-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ce2e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ce2e-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9ce2e-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9ce2e-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9ce2e-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ce2e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ce2e-112">Remarks</span></span>

<span data-ttu-id="9ce2e-113">**ID3DXLine:: end** нельзя использовать в качестве замены для [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: ендсцене**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="9ce2e-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce2e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce2e-114">Requirements</span></span>



| <span data-ttu-id="9ce2e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce2e-115">Requirement</span></span> | <span data-ttu-id="9ce2e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce2e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce2e-117">Header</span><span class="sxs-lookup"><span data-stu-id="9ce2e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9ce2e-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce2e-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9ce2e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ce2e-119">Library</span></span><br/> | <dl> <span data-ttu-id="9ce2e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ce2e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ce2e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ce2e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce2e-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="9ce2e-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="9ce2e-123">**ID3DXLine:: Begin**</span><span class="sxs-lookup"><span data-stu-id="9ce2e-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 




