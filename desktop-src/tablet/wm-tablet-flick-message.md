---
description: Посылается, когда пользователь выполняет многофункциональное перо. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Сообщение WM_TABLET_FLICK (Тпкшрд. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263031"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="d0c1c-104">\_Сообщение пера планшета WM \_</span><span class="sxs-lookup"><span data-stu-id="d0c1c-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="d0c1c-105">Посылается, когда пользователь выполняет многофункциональное перо.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="d0c1c-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d0c1c-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="d0c1c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0c1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c1c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0c1c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c1c-109">[**\_ Структура данных о жестах**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) , содержащая сведения о произошедшем жесте пера.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d0c1c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0c1c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c1c-111">[**Структура многофункциональных \_ точек**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) , указывающая, где произошло перо.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0c1c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0c1c-112">Remarks</span></span>

<span data-ttu-id="d0c1c-113">Многофункциональное перо — это однонаправленный жест пера, который требует, чтобы пользователь связывался с дигитайзером в быстром и прямолинейном движении.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="d0c1c-114">Жесты характеризуются высокой скоростью и высокой степенью равномерности.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="d0c1c-115">Жест определяется по направлению.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-115">A flick is identified by its direction.</span></span> <span data-ttu-id="d0c1c-116">Жесты можно создавать в восьми направлениях, соответствующих количеством элементов и вспомогательных компасов.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="d0c1c-117">При возникновении многофункционального пера система Windows сначала уведомляет приложение, отправляя сообщение **\_ \_ пера планшета WM** , которое окно получает через свою функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d0c1c-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="d0c1c-118">Возвращает переменную **\_ \_ \_ маски, обработанную** с помощью пера, описанную в разделе " [жесты жестов](flicks-constants.md)", чтобы указать, что приложение ответило на сообщение с **\_ \_ пером планшета WM** .</span><span class="sxs-lookup"><span data-stu-id="d0c1c-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="d0c1c-119">Если приложение не возвращает **\_ \_ \_ маску, обработанную** функцией жестов WM, Windows выполняет действие по умолчанию, указанное на панели управления "жесты", отправляя уведомление о дальнейших действиях, например [**WM \_ аппкомманд**](../inputdev/wm-appcommand.md), [**WM \_ VSCROLL**](../controls/wm-vscroll.md)или [**WM \_ KeyDown**](../inputdev/wm-keydown.md), в зависимости от того, какое действие связано с пером.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="d0c1c-120">Будьте внимательны при обработке **сообщения \_ \_ пера планшета WM** .</span><span class="sxs-lookup"><span data-stu-id="d0c1c-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="d0c1c-121">**WM \_ \_ЖЕСТ планшета** передается через функцию [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="d0c1c-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="d0c1c-122">При вызове методов для COM-интерфейса этот объект должен находиться в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="d0c1c-123">В противном случае COM создает исключение.</span><span class="sxs-lookup"><span data-stu-id="d0c1c-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c1c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d0c1c-124">Requirements</span></span>



| <span data-ttu-id="d0c1c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d0c1c-125">Requirement</span></span> | <span data-ttu-id="d0c1c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c1c-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c1c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0c1c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c1c-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0c1c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d0c1c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0c1c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c1c-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0c1c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0c1c-131">Header</span><span class="sxs-lookup"><span data-stu-id="d0c1c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c1c-132"><dt>Тпкшрд. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1c-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c1c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0c1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c1c-134">**Структура данных многофункционального пера \_**</span><span class="sxs-lookup"><span data-stu-id="d0c1c-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="d0c1c-135">**\_сообщение пера планшета WM \_**</span><span class="sxs-lookup"><span data-stu-id="d0c1c-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="d0c1c-136">жесты жестов</span><span class="sxs-lookup"><span data-stu-id="d0c1c-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="d0c1c-137">[реагирование на жесты пером](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0c1c-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 
