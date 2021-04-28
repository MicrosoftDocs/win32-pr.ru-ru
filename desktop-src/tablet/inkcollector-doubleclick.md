---
description: Событие InkCollector. DoubleClick — происходит при двойном щелчке объекта InkCollector или InkOverlay.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Событие InkCollector. DoubleClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51c3fef9ee999bbe2701da64e09a360f07db345
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110212"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="c5d55-103">Событие InkCollector. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="c5d55-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="c5d55-104">Происходит при двойном щелчке объекта [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d55-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5d55-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="c5d55-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5d55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d55-107">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c5d55-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d55-108">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5d55-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d55-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5d55-109">Return value</span></span>

<span data-ttu-id="c5d55-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c5d55-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5d55-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="c5d55-111">Remarks</span></span>

<span data-ttu-id="c5d55-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипедблкликк.</span><span class="sxs-lookup"><span data-stu-id="c5d55-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d55-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c5d55-113">Requirements</span></span>



| <span data-ttu-id="c5d55-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c5d55-114">Requirement</span></span> | <span data-ttu-id="c5d55-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c5d55-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d55-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5d55-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d55-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c5d55-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c5d55-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5d55-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d55-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c5d55-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c5d55-120">Header</span><span class="sxs-lookup"><span data-stu-id="c5d55-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d55-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c5d55-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c5d55-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5d55-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="c5d55-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5d55-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c5d55-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c5d55-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d55-125">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="c5d55-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




