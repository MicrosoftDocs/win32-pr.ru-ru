---
description: Отправляется перед \_ сообщением о создании WM при первом создании окна.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Сообщение WM_NCCREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711949"
---
# <a name="wm_nccreate-message"></a><span data-ttu-id="938e4-103">\_Сообщение НККРЕАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="938e4-103">WM\_NCCREATE message</span></span>

<span data-ttu-id="938e4-104">Отправляется перед сообщением о [**\_ создании WM**](wm-create.md) при первом создании окна.</span><span class="sxs-lookup"><span data-stu-id="938e4-104">Sent prior to the [**WM\_CREATE**](wm-create.md) message when a window is first created.</span></span>

<span data-ttu-id="938e4-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="938e4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a><span data-ttu-id="938e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="938e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="938e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="938e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="938e4-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="938e4-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="938e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="938e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="938e4-110">Указатель на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , содержащую сведения о создаваемом окне.</span><span class="sxs-lookup"><span data-stu-id="938e4-110">A pointer to the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span> <span data-ttu-id="938e4-111">Элементы **CREATESTRUCT** идентичны параметрам функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="938e4-111">The members of **CREATESTRUCT** are identical to the parameters of the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="938e4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="938e4-112">Return value</span></span>

<span data-ttu-id="938e4-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="938e4-113">Type: **LRESULT**</span></span>

<span data-ttu-id="938e4-114">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true** , чтобы продолжить создание окна.</span><span class="sxs-lookup"><span data-stu-id="938e4-114">If an application processes this message, it should return **TRUE** to continue creation of the window.</span></span> <span data-ttu-id="938e4-115">Если приложение возвращает **значение false**, функция [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) вернет **нулевой** маркер.</span><span class="sxs-lookup"><span data-stu-id="938e4-115">If the application returns **FALSE**, the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function will return a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="938e4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="938e4-116">Requirements</span></span>



| <span data-ttu-id="938e4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="938e4-117">Requirement</span></span> | <span data-ttu-id="938e4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="938e4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="938e4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="938e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="938e4-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="938e4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="938e4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="938e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="938e4-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="938e4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="938e4-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="938e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="938e4-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="938e4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="938e4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="938e4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="938e4-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="938e4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="938e4-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="938e4-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="938e4-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="938e4-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="938e4-129">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="938e4-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="938e4-130">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="938e4-130">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="938e4-131">**\_Создание WM**</span><span class="sxs-lookup"><span data-stu-id="938e4-131">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

<span data-ttu-id="938e4-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="938e4-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="938e4-133">Windows</span><span class="sxs-lookup"><span data-stu-id="938e4-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
