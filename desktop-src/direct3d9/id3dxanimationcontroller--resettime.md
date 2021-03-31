---
description: Сбрасывает глобальное время анимации в ноль. Все события, ожидающие обработки, сохраняют свои исходные расписания, но в новом периоде времени.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'Метод ID3DXAnimationController:: Ресеттиме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821301"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="eccfd-104">Метод ID3DXAnimationController:: Ресеттиме</span><span class="sxs-lookup"><span data-stu-id="eccfd-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="eccfd-105">Сбрасывает глобальное время анимации в ноль.</span><span class="sxs-lookup"><span data-stu-id="eccfd-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="eccfd-106">Все события, ожидающие обработки, сохраняют свои исходные расписания, но в новом периоде времени.</span><span class="sxs-lookup"><span data-stu-id="eccfd-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccfd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eccfd-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="eccfd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eccfd-108">Parameters</span></span>

<span data-ttu-id="eccfd-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="eccfd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eccfd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eccfd-110">Return value</span></span>

<span data-ttu-id="eccfd-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eccfd-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eccfd-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="eccfd-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eccfd-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="eccfd-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="eccfd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eccfd-114">Remarks</span></span>

<span data-ttu-id="eccfd-115">Этот метод обычно используется, когда значение глобального времени анимации приближается к максимальной точности ДВОЙНого хранилища или 2 ⁶ ⁴-1.</span><span class="sxs-lookup"><span data-stu-id="eccfd-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccfd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="eccfd-116">Requirements</span></span>



| <span data-ttu-id="eccfd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="eccfd-117">Requirement</span></span> | <span data-ttu-id="eccfd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="eccfd-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eccfd-119">Header</span><span class="sxs-lookup"><span data-stu-id="eccfd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="eccfd-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="eccfd-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="eccfd-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eccfd-121">Library</span></span><br/> | <dl> <span data-ttu-id="eccfd-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eccfd-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eccfd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eccfd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccfd-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="eccfd-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




