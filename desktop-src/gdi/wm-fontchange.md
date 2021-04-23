---
description: Приложение отправляет \_ сообщение WM фонтчанже всем окнам верхнего уровня в системе после изменения пула ресурсов шрифтов.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Сообщение WM_FONTCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985804"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="c4781-103">\_Сообщение ФОНТЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="c4781-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="c4781-104">Приложение отправляет сообщение **WM \_ фонтчанже** всем окнам верхнего уровня в системе после изменения пула ресурсов шрифтов.</span><span class="sxs-lookup"><span data-stu-id="c4781-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="c4781-105">Чтобы отправить это сообщение, вызовите функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c4781-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="c4781-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4781-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4781-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4781-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c4781-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4781-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4781-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4781-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c4781-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4781-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4781-111">Remarks</span></span>

<span data-ttu-id="c4781-112">Приложение, добавляющее или удаляющее шрифты из системы (например, с помощью функции [**аддфонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) или [**ремовефонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ), должно отправить это сообщение всем окнам верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="c4781-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="c4781-113">Чтобы отправить сообщение **WM \_ фонтчанже** всем окнам верхнего уровня, приложение может вызвать функцию **SendMessage** с параметром *HWND* , для которого установлено значение HWND \_ Broadcast.</span><span class="sxs-lookup"><span data-stu-id="c4781-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4781-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c4781-114">Requirements</span></span>



| <span data-ttu-id="c4781-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c4781-115">Requirement</span></span> | <span data-ttu-id="c4781-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c4781-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4781-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4781-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c4781-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4781-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c4781-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4781-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c4781-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4781-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4781-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c4781-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4781-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4781-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4781-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4781-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4781-124">Общие сведения о шрифтах и тексте</span><span class="sxs-lookup"><span data-stu-id="c4781-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="c4781-125">Шрифт и текстовые сообщения</span><span class="sxs-lookup"><span data-stu-id="c4781-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="c4781-126">**аддфонтресаурце**</span><span class="sxs-lookup"><span data-stu-id="c4781-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="c4781-127">**ремовефонтресаурце**</span><span class="sxs-lookup"><span data-stu-id="c4781-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
