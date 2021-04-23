---
description: Удаляет указанное событие из записи анимации, предотвращая выполнение события.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'Метод ID3DXAnimationController:: Ункэйевент (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355943"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="e196c-103">Метод ID3DXAnimationController:: Ункэйевент</span><span class="sxs-lookup"><span data-stu-id="e196c-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="e196c-104">Удаляет указанное событие из записи анимации, предотвращая выполнение события.</span><span class="sxs-lookup"><span data-stu-id="e196c-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="e196c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e196c-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="e196c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e196c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e196c-107">*Хевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e196c-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e196c-108">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="e196c-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="e196c-109">Обработчик события, удаляемый из контрольной анимации.</span><span class="sxs-lookup"><span data-stu-id="e196c-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e196c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e196c-110">Return value</span></span>

<span data-ttu-id="e196c-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e196c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e196c-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="e196c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e196c-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e196c-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e196c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e196c-114">Requirements</span></span>



| <span data-ttu-id="e196c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e196c-115">Requirement</span></span> | <span data-ttu-id="e196c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e196c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e196c-117">Header</span><span class="sxs-lookup"><span data-stu-id="e196c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e196c-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e196c-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e196c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e196c-119">Library</span></span><br/> | <dl> <span data-ttu-id="e196c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e196c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e196c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e196c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e196c-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e196c-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




