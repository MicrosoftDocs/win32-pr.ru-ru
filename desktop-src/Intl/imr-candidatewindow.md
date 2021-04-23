---
description: Нотфиес приложение, когда для выбранного редактора IME требуются сведения о окне кандидатов. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами параметров, как показано ниже.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: Код уведомления IMR_CANDIDATEWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663063"
---
# <a name="imr_candidatewindow-notification-code"></a><span data-ttu-id="3da68-104">\_Код уведомления КАНДИДАТЕВИНДОВ IMR</span><span class="sxs-lookup"><span data-stu-id="3da68-104">IMR\_CANDIDATEWINDOW notification code</span></span>

<span data-ttu-id="3da68-105">Нотфиес приложение, когда для выбранного редактора IME требуются сведения о окне кандидатов.</span><span class="sxs-lookup"><span data-stu-id="3da68-105">Notfies an application when a selected IME needs information about the candidate window.</span></span> <span data-ttu-id="3da68-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="3da68-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a><span data-ttu-id="3da68-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3da68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da68-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3da68-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3da68-109">Задайте значение IMR \_ кандидатевиндов.</span><span class="sxs-lookup"><span data-stu-id="3da68-109">Set to IMR\_CANDIDATEWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="3da68-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3da68-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3da68-111">Указатель на буфер, содержащий структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="3da68-111">Pointer to a buffer containing a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="3da68-112">Его член **двиндекс** содержит индекс к окну кандидатов, на которое есть ссылка.</span><span class="sxs-lookup"><span data-stu-id="3da68-112">Its **dwIndex** member contains the index to the candidate window referenced.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da68-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3da68-113">Return Value</span></span>

<span data-ttu-id="3da68-114">Функция возвращает ненулевое значение, если приложение заполняет структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) .</span><span class="sxs-lookup"><span data-stu-id="3da68-114">Returns a nonzero value if the application fills in the [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure.</span></span> <span data-ttu-id="3da68-115">В противном случае команда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="3da68-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da68-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3da68-116">Remarks</span></span>

<span data-ttu-id="3da68-117">Эта команда может быть отправлена редактором IME в окно, которое очистило \_ флаг ISC шовуикандидатевиндов в обработчике сообщений [**\_ \_ SETCONTEXT редактора IME**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="3da68-117">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICANDIDATEWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da68-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3da68-118">Requirements</span></span>



| <span data-ttu-id="3da68-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3da68-119">Requirement</span></span> | <span data-ttu-id="3da68-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3da68-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da68-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3da68-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3da68-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3da68-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3da68-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3da68-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3da68-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3da68-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3da68-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3da68-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da68-126"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3da68-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da68-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3da68-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da68-128">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="3da68-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3da68-129">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="3da68-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3da68-130">**кандидатеформ**</span><span class="sxs-lookup"><span data-stu-id="3da68-130">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="3da68-131">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="3da68-131">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="3da68-132">**\_SETCONTEXT IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="3da68-132">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




