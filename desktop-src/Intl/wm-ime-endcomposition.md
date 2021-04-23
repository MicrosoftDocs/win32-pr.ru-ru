---
description: Отправляется в приложение, когда редактор IME завершает композицию. Окно получает это сообщение через функцию WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Сообщение WM_IME_ENDCOMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343632"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="75b31-104">\_Сообщение ендкомпоситион редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="75b31-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="75b31-105">Отправляется в приложение, когда редактор IME завершает композицию.</span><span class="sxs-lookup"><span data-stu-id="75b31-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="75b31-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75b31-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="75b31-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="75b31-107">Parameters</span></span>

<span data-ttu-id="75b31-108">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="75b31-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="75b31-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75b31-109">Return value</span></span>

<span data-ttu-id="75b31-110">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="75b31-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b31-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75b31-111">Remarks</span></span>

<span data-ttu-id="75b31-112">Приложение должно обработать это сообщение, если оно отображает сами символы композиции.</span><span class="sxs-lookup"><span data-stu-id="75b31-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="75b31-113">Если приложение создало окно IME, оно должно передать это сообщение в это окно.</span><span class="sxs-lookup"><span data-stu-id="75b31-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="75b31-114">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  обрабатывает это сообщение, передавая его в окно IME по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75b31-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b31-115">Требования</span><span class="sxs-lookup"><span data-stu-id="75b31-115">Requirements</span></span>



| <span data-ttu-id="75b31-116">Требование</span><span class="sxs-lookup"><span data-stu-id="75b31-116">Requirement</span></span> | <span data-ttu-id="75b31-117">Значение</span><span class="sxs-lookup"><span data-stu-id="75b31-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b31-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75b31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75b31-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="75b31-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="75b31-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75b31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75b31-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="75b31-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75b31-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="75b31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b31-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75b31-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b31-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75b31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b31-125">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="75b31-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="75b31-126">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="75b31-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
