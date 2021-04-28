---
description: Событие InkOverlay. DoubleClick — происходит при двойном щелчке объекта InkCollector или InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Событие InkOverlay. DoubleClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086832"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="85926-103">Событие InkOverlay. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="85926-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="85926-104">Происходит при двойном щелчке объекта [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="85926-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="85926-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85926-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="85926-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85926-107">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="85926-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85926-108">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85926-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85926-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85926-109">Return value</span></span>

<span data-ttu-id="85926-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="85926-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85926-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="85926-111">Remarks</span></span>

<span data-ttu-id="85926-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипедблкликк.</span><span class="sxs-lookup"><span data-stu-id="85926-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="85926-113">Требования</span><span class="sxs-lookup"><span data-stu-id="85926-113">Requirements</span></span>



| <span data-ttu-id="85926-114">Требование</span><span class="sxs-lookup"><span data-stu-id="85926-114">Requirement</span></span> | <span data-ttu-id="85926-115">Значение</span><span class="sxs-lookup"><span data-stu-id="85926-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85926-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85926-116">Minimum supported client</span></span><br/> | <span data-ttu-id="85926-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85926-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="85926-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85926-118">Minimum supported server</span></span><br/> | <span data-ttu-id="85926-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85926-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="85926-120">Header</span><span class="sxs-lookup"><span data-stu-id="85926-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="85926-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85926-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85926-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85926-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="85926-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85926-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="85926-124">См. также</span><span class="sxs-lookup"><span data-stu-id="85926-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85926-125">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="85926-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




