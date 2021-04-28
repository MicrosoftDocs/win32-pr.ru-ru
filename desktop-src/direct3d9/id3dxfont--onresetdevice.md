---
description: 'Метод ID3DXFont:: Онресетдевице. Используйте этот метод для повторного получения ресурсов и сохранения начального состояния.'
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: 'Метод ID3DXFont:: Онресетдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d976c29d370887362e46899c7fb2a654d6e2cc7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093742"
---
# <a name="id3dxfontonresetdevice-method"></a><span data-ttu-id="ecea1-103">Метод ID3DXFont:: Онресетдевице</span><span class="sxs-lookup"><span data-stu-id="ecea1-103">ID3DXFont::OnResetDevice method</span></span>

<span data-ttu-id="ecea1-104">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="ecea1-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecea1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecea1-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="ecea1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecea1-106">Parameters</span></span>

<span data-ttu-id="ecea1-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ecea1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecea1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecea1-108">Return value</span></span>

<span data-ttu-id="ecea1-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ecea1-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ecea1-110">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ecea1-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ecea1-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ecea1-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecea1-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="ecea1-112">Remarks</span></span>

<span data-ttu-id="ecea1-113">**Онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью функции [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов.</span><span class="sxs-lookup"><span data-stu-id="ecea1-113">**OnResetDevice** should be called each time the device is reset (using [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="ecea1-114">Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.</span><span class="sxs-lookup"><span data-stu-id="ecea1-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecea1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ecea1-115">Requirements</span></span>



| <span data-ttu-id="ecea1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ecea1-116">Requirement</span></span> | <span data-ttu-id="ecea1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ecea1-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecea1-118">Header</span><span class="sxs-lookup"><span data-stu-id="ecea1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ecea1-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecea1-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ecea1-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ecea1-120">Library</span></span><br/> | <dl> <span data-ttu-id="ecea1-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecea1-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ecea1-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ecea1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecea1-123">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="ecea1-123">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
