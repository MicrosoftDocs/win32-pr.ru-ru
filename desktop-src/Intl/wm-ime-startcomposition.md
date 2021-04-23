---
description: Отправляется непосредственно перед тем, как редактор IME создает строку композиции в результате нажатия клавиши. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Сообщение WM_IME_STARTCOMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897414"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="d0e97-104">\_Сообщение старткомпоситион редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="d0e97-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="d0e97-105">Отправляется непосредственно перед тем, как редактор IME создает строку композиции в результате нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="d0e97-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="d0e97-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d0e97-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="d0e97-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0e97-107">Parameters</span></span>

<span data-ttu-id="d0e97-108">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="d0e97-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="d0e97-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0e97-109">Return value</span></span>

<span data-ttu-id="d0e97-110">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d0e97-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e97-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0e97-111">Remarks</span></span>

<span data-ttu-id="d0e97-112">Это сообщение является уведомлением для окна редактора IME, чтобы открыть его окно композиции.</span><span class="sxs-lookup"><span data-stu-id="d0e97-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="d0e97-113">Приложение должно обработать это сообщение, если оно отображает сами символы композиции.</span><span class="sxs-lookup"><span data-stu-id="d0e97-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="d0e97-114">Если приложение создало окно IME, оно должно передать это сообщение в это окно.</span><span class="sxs-lookup"><span data-stu-id="d0e97-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="d0e97-115">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обрабатывает сообщение, передавая его в окно IME по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d0e97-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e97-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d0e97-116">Requirements</span></span>



| <span data-ttu-id="d0e97-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d0e97-117">Requirement</span></span> | <span data-ttu-id="d0e97-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d0e97-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e97-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0e97-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e97-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0e97-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d0e97-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0e97-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e97-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0e97-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0e97-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d0e97-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0e97-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0e97-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e97-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0e97-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e97-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="d0e97-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d0e97-127">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="d0e97-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
