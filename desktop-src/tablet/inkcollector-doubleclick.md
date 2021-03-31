---
description: Происходит при двойном щелчке объекта InkCollector или InkOverlay.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Событие InkCollector. DoubleClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896862"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="b8f29-103">Событие InkCollector. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="b8f29-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="b8f29-104">Происходит при двойном щелчке объекта [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b8f29-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8f29-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="b8f29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8f29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f29-107">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b8f29-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f29-108">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="b8f29-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f29-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8f29-109">Return value</span></span>

<span data-ttu-id="b8f29-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8f29-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f29-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8f29-111">Remarks</span></span>

<span data-ttu-id="b8f29-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипедблкликк.</span><span class="sxs-lookup"><span data-stu-id="b8f29-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f29-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b8f29-113">Requirements</span></span>



| <span data-ttu-id="b8f29-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b8f29-114">Requirement</span></span> | <span data-ttu-id="b8f29-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f29-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f29-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8f29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f29-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b8f29-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b8f29-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8f29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f29-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b8f29-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b8f29-120">Header</span><span class="sxs-lookup"><span data-stu-id="b8f29-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f29-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8f29-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8f29-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8f29-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8f29-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f29-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b8f29-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8f29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f29-125">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="b8f29-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




