---
description: Событие InkOverlay. Курсоринранже возникает, когда курсор попадает в диапазон физического обнаружения (близость) контекста планшета.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Событие InkOverlay. Курсоринранже (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1b48cba731720072aae88aa59b80c569a4aa07b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086842"
---
# <a name="inkoverlaycursorinrange-event"></a><span data-ttu-id="ecb1a-103">Событие InkOverlay. Курсоринранже</span><span class="sxs-lookup"><span data-stu-id="ecb1a-103">InkOverlay.CursorInRange event</span></span>

<span data-ttu-id="ecb1a-104">Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="ecb1a-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecb1a-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="ecb1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecb1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb1a-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecb1a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb1a-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсоринранже**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb1a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="ecb1a-109">*Невкурсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecb1a-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb1a-110">Будет ли этот сборщик рукописных данных впервые подключен к объекту [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавшему событие [**курсоринранже**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb1a-110">Whether this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="ecb1a-111">*Буттонсстате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecb1a-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb1a-112">Состояние кнопок для курсора, создавшего событие [**курсоринранже**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb1a-112">The state of the buttons for the cursor that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

<span data-ttu-id="ecb1a-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="ecb1a-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb1a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecb1a-114">Return value</span></span>

<span data-ttu-id="ecb1a-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ecb1a-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecb1a-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="ecb1a-116">Remarks</span></span>

<span data-ttu-id="ecb1a-117">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсоринранже.</span><span class="sxs-lookup"><span data-stu-id="ecb1a-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="ecb1a-118">Событие [**курсоринранже**](inkcollector-cursorinrange.md) срабатывает даже в режиме выбора или стирания, а не только в режиме рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ecb1a-118">The [**CursorInRange**](inkcollector-cursorinrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="ecb1a-119">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="ecb1a-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ecb1a-120">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="ecb1a-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb1a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb1a-121">Requirements</span></span>



| <span data-ttu-id="ecb1a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb1a-122">Requirement</span></span> | <span data-ttu-id="ecb1a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb1a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb1a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecb1a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb1a-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ecb1a-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ecb1a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecb1a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb1a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ecb1a-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ecb1a-128">Header</span><span class="sxs-lookup"><span data-stu-id="ecb1a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb1a-129"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ecb1a-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ecb1a-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ecb1a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecb1a-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb1a-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ecb1a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ecb1a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb1a-133">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ecb1a-133">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ecb1a-134">**Событие Курсораутофранже**</span><span class="sxs-lookup"><span data-stu-id="ecb1a-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="ecb1a-135">**Перечисление Инккурсорбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="ecb1a-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="ecb1a-136">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="ecb1a-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




