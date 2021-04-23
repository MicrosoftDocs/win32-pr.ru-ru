---
description: Отправляется в самое верхнее окно после изменения языка ввода приложения. Необходимо внести все зависящие от приложения параметры и передать сообщение функции Дефвиндовпрок, которая передает сообщение всем дочерним окнам первого уровня.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Сообщение WM_INPUTLANGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144719"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="36ef5-104">\_Сообщение ИНПУТЛАНГЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="36ef5-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="36ef5-105">Отправляется в самое верхнее окно после изменения языка ввода приложения.</span><span class="sxs-lookup"><span data-stu-id="36ef5-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="36ef5-106">Необходимо внести все зависящие от приложения параметры и передать сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , которая передает сообщение всем дочерним окнам первого уровня.</span><span class="sxs-lookup"><span data-stu-id="36ef5-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="36ef5-107">Эти дочерние окна могут передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы оно передавало сообщение дочерним окнам и так далее.</span><span class="sxs-lookup"><span data-stu-id="36ef5-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="36ef5-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="36ef5-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="36ef5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="36ef5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ef5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36ef5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36ef5-111">Кодировка нового языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="36ef5-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="36ef5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36ef5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36ef5-113">Идентификатор локали ввода.</span><span class="sxs-lookup"><span data-stu-id="36ef5-113">The input locale identifier.</span></span> <span data-ttu-id="36ef5-114">Дополнительные сведения см. в разделе [языки, языковые стандарты и раскладки клавиатуры](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="36ef5-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ef5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36ef5-115">Return value</span></span>

<span data-ttu-id="36ef5-116">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="36ef5-116">Type: **LRESULT**</span></span>

<span data-ttu-id="36ef5-117">Приложение должно вернуть ненулевое значение, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="36ef5-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ef5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="36ef5-118">Requirements</span></span>



| <span data-ttu-id="36ef5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="36ef5-119">Requirement</span></span> | <span data-ttu-id="36ef5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="36ef5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ef5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36ef5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36ef5-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36ef5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="36ef5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36ef5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36ef5-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36ef5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36ef5-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36ef5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ef5-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36ef5-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ef5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36ef5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="36ef5-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="36ef5-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36ef5-129">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="36ef5-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="36ef5-130">**WM \_ инпутлангчанжерекуест**</span><span class="sxs-lookup"><span data-stu-id="36ef5-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="36ef5-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="36ef5-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="36ef5-132">Windows</span><span class="sxs-lookup"><span data-stu-id="36ef5-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
