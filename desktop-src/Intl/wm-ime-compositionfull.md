---
description: Отправляется в приложение, когда окно IME не находит место для расширения области окна композиции. Окно получает это сообщение через функцию WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Сообщение WM_IME_COMPOSITIONFULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272947"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="0925b-104">\_Сообщение компоситионфулл редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="0925b-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="0925b-105">Отправляется в приложение, когда окно IME не находит место для расширения области окна композиции.</span><span class="sxs-lookup"><span data-stu-id="0925b-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="0925b-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0925b-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="0925b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0925b-107">Parameters</span></span>

<span data-ttu-id="0925b-108">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="0925b-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="0925b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0925b-109">Return value</span></span>

<span data-ttu-id="0925b-110">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0925b-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0925b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0925b-111">Remarks</span></span>

<span data-ttu-id="0925b-112">Для указания способа отображения окна приложение должно использовать команду [ИМК \_ сеткомпоситионвиндов](imc-setcompositionwindow.md) .</span><span class="sxs-lookup"><span data-stu-id="0925b-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="0925b-113">Окно IME, а не редактор IME, отправляет это сообщение уведомления функцией [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="0925b-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0925b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0925b-114">Requirements</span></span>



| <span data-ttu-id="0925b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0925b-115">Requirement</span></span> | <span data-ttu-id="0925b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0925b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0925b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0925b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0925b-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0925b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0925b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0925b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0925b-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0925b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0925b-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0925b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0925b-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0925b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0925b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0925b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0925b-124">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="0925b-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="0925b-125">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="0925b-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="0925b-126">ИМК \_ сеткомпоситионвиндов</span><span class="sxs-lookup"><span data-stu-id="0925b-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
