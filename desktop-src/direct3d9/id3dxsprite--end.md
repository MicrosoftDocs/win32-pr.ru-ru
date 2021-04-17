---
description: 'Вызывает ID3DXSprite:: Flush и восстанавливает состояние устройства до вызова ID3DXSprite:: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'Метод ID3DXSprite:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424453"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="376b6-103">Метод ID3DXSprite:: end</span><span class="sxs-lookup"><span data-stu-id="376b6-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="376b6-104">Вызывает [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) и восстанавливает состояние устройства до вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="376b6-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="376b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="376b6-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="376b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="376b6-106">Parameters</span></span>

<span data-ttu-id="376b6-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="376b6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="376b6-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="376b6-108">Return value</span></span>

<span data-ttu-id="376b6-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="376b6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="376b6-110">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="376b6-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="376b6-111">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="376b6-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="376b6-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="376b6-112">Remarks</span></span>

<span data-ttu-id="376b6-113">**ID3DXSprite:: end** нельзя использовать в качестве замены для [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: ендсцене**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="376b6-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="376b6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="376b6-114">Requirements</span></span>



| <span data-ttu-id="376b6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="376b6-115">Requirement</span></span> | <span data-ttu-id="376b6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="376b6-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="376b6-117">Header</span><span class="sxs-lookup"><span data-stu-id="376b6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="376b6-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="376b6-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="376b6-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="376b6-119">Library</span></span><br/> | <dl> <span data-ttu-id="376b6-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="376b6-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="376b6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="376b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376b6-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="376b6-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="376b6-123">**ID3DXSprite:: Begin**</span><span class="sxs-lookup"><span data-stu-id="376b6-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 




