---
description: Проверяет, является ли указанный обработчик событий допустимым, а событие анимации еще не завершено.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'Метод ID3DXAnimationController:: ValidateEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647895"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="73dcb-103">Метод ID3DXAnimationController:: ValidateEvent</span><span class="sxs-lookup"><span data-stu-id="73dcb-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="73dcb-104">Проверяет, является ли указанный обработчик событий допустимым, а событие анимации еще не завершено.</span><span class="sxs-lookup"><span data-stu-id="73dcb-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="73dcb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73dcb-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="73dcb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73dcb-107">*Хевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73dcb-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73dcb-108">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="73dcb-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="73dcb-109">Обработчик события анимации.</span><span class="sxs-lookup"><span data-stu-id="73dcb-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73dcb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73dcb-110">Return value</span></span>

<span data-ttu-id="73dcb-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73dcb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73dcb-112">Возвращает значение \_ ОК, если маркер события является допустимым и событие еще не завершено.</span><span class="sxs-lookup"><span data-stu-id="73dcb-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="73dcb-113">Возвращает значение E \_ Fail, если недопустимый маркер события и (или) событие завершено.</span><span class="sxs-lookup"><span data-stu-id="73dcb-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="73dcb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73dcb-114">Remarks</span></span>

<span data-ttu-id="73dcb-115">Метод будет указывать, что обработчик событий допустим, даже если событие выполняется, но еще не завершено.</span><span class="sxs-lookup"><span data-stu-id="73dcb-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="73dcb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="73dcb-116">Requirements</span></span>



| <span data-ttu-id="73dcb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="73dcb-117">Requirement</span></span> | <span data-ttu-id="73dcb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="73dcb-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73dcb-119">Header</span><span class="sxs-lookup"><span data-stu-id="73dcb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="73dcb-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="73dcb-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="73dcb-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73dcb-121">Library</span></span><br/> | <dl> <span data-ttu-id="73dcb-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73dcb-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73dcb-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73dcb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73dcb-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="73dcb-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




