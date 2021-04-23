---
description: Происходит при завершении перерисовки объекта InkOverlay или элемента управления InkPicture.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Событие InkOverlay. окрашено (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498075"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="37518-103">Событие InkOverlay. окрашено</span><span class="sxs-lookup"><span data-stu-id="37518-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="37518-104">Происходит при завершении перерисовки объекта [**InkOverlay**](inkoverlay-class.md) или элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="37518-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="37518-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37518-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="37518-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37518-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37518-107">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37518-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37518-108">Контекст устройства, в котором произошло событие.</span><span class="sxs-lookup"><span data-stu-id="37518-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="37518-109">*Rect* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="37518-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37518-110">Перерисовка [**инкректангле**](inkrectangle-class.md) .</span><span class="sxs-lookup"><span data-stu-id="37518-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37518-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37518-111">Return value</span></span>

<span data-ttu-id="37518-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="37518-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37518-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37518-113">Remarks</span></span>

<span data-ttu-id="37518-114">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоепаинтед.</span><span class="sxs-lookup"><span data-stu-id="37518-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="37518-115">Требования</span><span class="sxs-lookup"><span data-stu-id="37518-115">Requirements</span></span>



| <span data-ttu-id="37518-116">Требование</span><span class="sxs-lookup"><span data-stu-id="37518-116">Requirement</span></span> | <span data-ttu-id="37518-117">Значение</span><span class="sxs-lookup"><span data-stu-id="37518-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37518-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37518-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37518-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="37518-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="37518-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37518-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37518-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="37518-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="37518-122">Header</span><span class="sxs-lookup"><span data-stu-id="37518-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37518-123"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="37518-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37518-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37518-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="37518-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37518-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="37518-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37518-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37518-127">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="37518-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




