---
description: Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Событие InkOverlay. Курсоринранже (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65745e93bfb7351f7e1fa6d01965ce7a271bc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999263"
---
# <a name="inkoverlaycursorinrange-event"></a><span data-ttu-id="13ddf-103">Событие InkOverlay. Курсоринранже</span><span class="sxs-lookup"><span data-stu-id="13ddf-103">InkOverlay.CursorInRange event</span></span>

<span data-ttu-id="13ddf-104">Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="13ddf-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ddf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13ddf-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="13ddf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13ddf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ddf-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13ddf-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ddf-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсоринранже**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="13ddf-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="13ddf-109">*Невкурсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13ddf-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ddf-110">Будет ли этот сборщик рукописных данных впервые подключен к объекту [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавшему событие [**курсоринранже**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="13ddf-110">Whether this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="13ddf-111">*Буттонсстате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13ddf-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ddf-112">Состояние кнопок для курсора, создавшего событие [**курсоринранже**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="13ddf-112">The state of the buttons for the cursor that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

<span data-ttu-id="13ddf-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="13ddf-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ddf-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13ddf-114">Return value</span></span>

<span data-ttu-id="13ddf-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="13ddf-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ddf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13ddf-116">Remarks</span></span>

<span data-ttu-id="13ddf-117">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсоринранже.</span><span class="sxs-lookup"><span data-stu-id="13ddf-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="13ddf-118">Событие [**курсоринранже**](inkcollector-cursorinrange.md) срабатывает даже в режиме выбора или стирания, а не только в режиме рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="13ddf-118">The [**CursorInRange**](inkcollector-cursorinrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="13ddf-119">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="13ddf-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="13ddf-120">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="13ddf-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ddf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="13ddf-121">Requirements</span></span>



| <span data-ttu-id="13ddf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="13ddf-122">Requirement</span></span> | <span data-ttu-id="13ddf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="13ddf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ddf-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13ddf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="13ddf-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="13ddf-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="13ddf-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13ddf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="13ddf-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13ddf-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="13ddf-128">Header</span><span class="sxs-lookup"><span data-stu-id="13ddf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ddf-129"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="13ddf-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="13ddf-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13ddf-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="13ddf-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ddf-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="13ddf-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13ddf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ddf-133">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="13ddf-133">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="13ddf-134">**Событие Курсораутофранже**</span><span class="sxs-lookup"><span data-stu-id="13ddf-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="13ddf-135">**Перечисление Инккурсорбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="13ddf-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="13ddf-136">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="13ddf-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




