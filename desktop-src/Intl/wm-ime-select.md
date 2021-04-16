---
description: Отправляется в приложение, когда операционная система собирается изменить текущий редактор IME. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Сообщение WM_IME_SELECT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682723"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="29d32-104">\_Выбор сообщения для редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="29d32-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="29d32-105">Отправляется в приложение, когда операционная система собирается изменить текущий редактор IME.</span><span class="sxs-lookup"><span data-stu-id="29d32-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="29d32-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="29d32-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="29d32-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="29d32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d32-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="29d32-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="29d32-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="29d32-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="29d32-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29d32-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29d32-111">Индикатор выделения.</span><span class="sxs-lookup"><span data-stu-id="29d32-111">Selection indicator.</span></span> <span data-ttu-id="29d32-112">Этот параметр указывает **значение true** , если выбран указанный редактор IME.</span><span class="sxs-lookup"><span data-stu-id="29d32-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="29d32-113">Параметр имеет значение **false** , если указанный редактор IME больше не выбран.</span><span class="sxs-lookup"><span data-stu-id="29d32-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="29d32-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29d32-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29d32-115">Идентификатор языка ввода, связанный с редактором IME.</span><span class="sxs-lookup"><span data-stu-id="29d32-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d32-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29d32-116">Return value</span></span>

<span data-ttu-id="29d32-117">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="29d32-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29d32-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29d32-118">Remarks</span></span>

<span data-ttu-id="29d32-119">Приложение, создавшее окно IME, должно передать это сообщение в это окно, чтобы он мог получить маркер раскладки клавиатуры для вновь выбранного редактора IME.</span><span class="sxs-lookup"><span data-stu-id="29d32-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="29d32-120">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  обрабатывает это сообщение, передавая сведения в окно IME по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="29d32-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="29d32-121">Требования</span><span class="sxs-lookup"><span data-stu-id="29d32-121">Requirements</span></span>



| <span data-ttu-id="29d32-122">Требование</span><span class="sxs-lookup"><span data-stu-id="29d32-122">Requirement</span></span> | <span data-ttu-id="29d32-123">Значение</span><span class="sxs-lookup"><span data-stu-id="29d32-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d32-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29d32-124">Minimum supported client</span></span><br/> | <span data-ttu-id="29d32-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29d32-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="29d32-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29d32-126">Minimum supported server</span></span><br/> | <span data-ttu-id="29d32-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29d32-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29d32-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29d32-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d32-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29d32-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d32-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29d32-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d32-131">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="29d32-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="29d32-132">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="29d32-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
