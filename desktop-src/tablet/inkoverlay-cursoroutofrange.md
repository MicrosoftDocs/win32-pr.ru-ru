---
description: Происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: Событие InkOverlay. Курсораутофранже (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1510013d24bf092a08ba7d57b54c0f94bf7c2dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703059"
---
# <a name="inkoverlaycursoroutofrange-event"></a><span data-ttu-id="11e0c-103">Событие InkOverlay. Курсораутофранже</span><span class="sxs-lookup"><span data-stu-id="11e0c-103">InkOverlay.CursorOutOfRange event</span></span>

<span data-ttu-id="11e0c-104">Происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="11e0c-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11e0c-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="11e0c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11e0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e0c-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11e0c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e0c-108">Объект [**интерфейса иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсораутофранже**](inkcollector-cursoroutofrange.md) .</span><span class="sxs-lookup"><span data-stu-id="11e0c-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e0c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11e0c-109">Return value</span></span>

<span data-ttu-id="11e0c-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11e0c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11e0c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11e0c-111">Remarks</span></span>

<span data-ttu-id="11e0c-112">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсораутофранже.</span><span class="sxs-lookup"><span data-stu-id="11e0c-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="11e0c-113">Событие [**курсораутофранже**](inkcollector-cursoroutofrange.md) срабатывает даже в режиме выбора или стирания, а не только в режиме рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="11e0c-113">The [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="11e0c-114">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="11e0c-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="11e0c-115">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="11e0c-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e0c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="11e0c-116">Requirements</span></span>



| <span data-ttu-id="11e0c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="11e0c-117">Requirement</span></span> | <span data-ttu-id="11e0c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="11e0c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e0c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11e0c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="11e0c-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="11e0c-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="11e0c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11e0c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="11e0c-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="11e0c-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="11e0c-123">Header</span><span class="sxs-lookup"><span data-stu-id="11e0c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e0c-124"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="11e0c-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11e0c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11e0c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="11e0c-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e0c-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="11e0c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11e0c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e0c-128">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="11e0c-128">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="11e0c-129">**Событие Курсоринранже**</span><span class="sxs-lookup"><span data-stu-id="11e0c-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="11e0c-130">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="11e0c-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




