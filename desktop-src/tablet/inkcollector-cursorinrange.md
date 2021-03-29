---
description: Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: Событие InkCollector. Курсоринранже (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c1d59927f9ed0a932fe28a2c5243f328a223c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540391"
---
# <a name="inkcollectorcursorinrange-event"></a><span data-ttu-id="85c82-103">Событие InkCollector. Курсоринранже</span><span class="sxs-lookup"><span data-stu-id="85c82-103">InkCollector.CursorInRange event</span></span>

<span data-ttu-id="85c82-104">Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="85c82-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c82-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85c82-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="85c82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85c82-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85c82-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c82-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **курсоринранже** .</span><span class="sxs-lookup"><span data-stu-id="85c82-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="85c82-109">*Невкурсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85c82-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c82-110">**Вариант \_ Значение TRUE** указывает, что это первый раз, когда сборщик рукописных данных приступает к работе с объектом [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавшим событие **курсоринранже** . в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="85c82-110">**VARIANT\_TRUE** to indicate that this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="85c82-111">*Буттонсстате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85c82-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c82-112">Состояние кнопок для курсора, создавшего событие **курсоринранже** .</span><span class="sxs-lookup"><span data-stu-id="85c82-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="85c82-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="85c82-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85c82-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85c82-114">Return value</span></span>

<span data-ttu-id="85c82-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="85c82-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85c82-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85c82-116">Remarks</span></span>

<span data-ttu-id="85c82-117">Метод события TЭтот определен в \_ интерфейсах иинкколлекторевентс, \_ иинковерлайевентс и \_ иинкпиктуривентс (DISP) с идентификатором DISPID \_ ицекурсоринранже.</span><span class="sxs-lookup"><span data-stu-id="85c82-117">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="85c82-118">Событие **курсоринранже** срабатывает даже в режиме выбора или стирания, а не только в режиме рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="85c82-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="85c82-119">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="85c82-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="85c82-120">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="85c82-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c82-121">Требования</span><span class="sxs-lookup"><span data-stu-id="85c82-121">Requirements</span></span>



| <span data-ttu-id="85c82-122">Требование</span><span class="sxs-lookup"><span data-stu-id="85c82-122">Requirement</span></span> | <span data-ttu-id="85c82-123">Значение</span><span class="sxs-lookup"><span data-stu-id="85c82-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c82-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85c82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="85c82-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85c82-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="85c82-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85c82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="85c82-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85c82-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="85c82-128">Header</span><span class="sxs-lookup"><span data-stu-id="85c82-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c82-129"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85c82-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85c82-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85c82-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="85c82-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85c82-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="85c82-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85c82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c82-133">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="85c82-133">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="85c82-134">**Событие Курсораутофранже**</span><span class="sxs-lookup"><span data-stu-id="85c82-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="85c82-135">**Перечисление Инккурсорбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="85c82-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="85c82-136">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="85c82-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




