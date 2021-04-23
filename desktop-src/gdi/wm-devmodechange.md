---
description: Сообщение WM \_ девмодечанже отправляется всем окнам верхнего уровня каждый раз, когда пользователь изменяет параметры режима устройства.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Сообщение WM_DEVMODECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985805"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="96ea4-103">\_Сообщение ДЕВМОДЕЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="96ea4-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="96ea4-104">Сообщение **WM \_ девмодечанже** отправляется всем окнам верхнего уровня каждый раз, когда пользователь изменяет параметры режима устройства.</span><span class="sxs-lookup"><span data-stu-id="96ea4-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="96ea4-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96ea4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="96ea4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96ea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ea4-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="96ea4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="96ea4-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="96ea4-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="96ea4-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="96ea4-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="96ea4-110">WM \_ девмодечанже</span><span class="sxs-lookup"><span data-stu-id="96ea4-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="96ea4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96ea4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96ea4-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="96ea4-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="96ea4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96ea4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96ea4-114">Указатель на строку, указывающую имя устройства.</span><span class="sxs-lookup"><span data-stu-id="96ea4-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ea4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96ea4-115">Return value</span></span>

<span data-ttu-id="96ea4-116">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="96ea4-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="96ea4-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="96ea4-117">Remarks</span></span>

<span data-ttu-id="96ea4-118">Это сообщение не может быть отправлено непосредственно в окно.</span><span class="sxs-lookup"><span data-stu-id="96ea4-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="96ea4-119">Чтобы отправить сообщение **WM \_ девмодечанже** всем окнам верхнего уровня, используйте функцию [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) с параметром *HWND* , имеющим значение HWND \_ Broadcast.</span><span class="sxs-lookup"><span data-stu-id="96ea4-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ea4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="96ea4-120">Requirements</span></span>



| <span data-ttu-id="96ea4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="96ea4-121">Requirement</span></span> | <span data-ttu-id="96ea4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="96ea4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ea4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96ea4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="96ea4-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96ea4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="96ea4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96ea4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="96ea4-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96ea4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96ea4-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96ea4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="96ea4-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96ea4-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ea4-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96ea4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ea4-130">Общие сведения о контекстах устройств</span><span class="sxs-lookup"><span data-stu-id="96ea4-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="96ea4-131">Сообщения контекста устройства</span><span class="sxs-lookup"><span data-stu-id="96ea4-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 
