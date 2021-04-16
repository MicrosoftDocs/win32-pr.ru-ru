---
description: Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о окне композиции. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с набором параметров, как показано ниже.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: Код уведомления IMR_COMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650790"
---
# <a name="imr_compositionwindow-notification-code"></a><span data-ttu-id="aa79e-104">\_Код уведомления КОМПОСИТИОНВИНДОВ IMR</span><span class="sxs-lookup"><span data-stu-id="aa79e-104">IMR\_COMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="aa79e-105">Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о окне композиции.</span><span class="sxs-lookup"><span data-stu-id="aa79e-105">Notifies an application when a selected IME needs information about the composition window.</span></span> <span data-ttu-id="aa79e-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с набором параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="aa79e-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="aa79e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa79e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa79e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa79e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="aa79e-109">Задайте значение IMR \_ компоситионвиндов.</span><span class="sxs-lookup"><span data-stu-id="aa79e-109">Set to IMR\_COMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="aa79e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa79e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="aa79e-111">Указатель на буфер, содержащий структуру [**компоситионформ**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="aa79e-111">Pointer to a buffer containing a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa79e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa79e-112">Return Value</span></span>

<span data-ttu-id="aa79e-113">Функция возвращает ненулевое значение, если приложение заполняет структуру [**компоситионформ**](/windows/win32/api/imm/ns-imm-compositionform) .</span><span class="sxs-lookup"><span data-stu-id="aa79e-113">Returns a nonzero value if the application fills in the [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure.</span></span> <span data-ttu-id="aa79e-114">В противном случае команда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="aa79e-114">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa79e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa79e-115">Remarks</span></span>

<span data-ttu-id="aa79e-116">Эта команда может быть отправлена редактором IME в окно, которое очистило \_ флаг ISC шовуикомпоситионвиндов в обработчике сообщений [**\_ \_ SETCONTEXT редактора IME**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="aa79e-116">This command can be sent by the IME to a window that has cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa79e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aa79e-117">Requirements</span></span>



| <span data-ttu-id="aa79e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aa79e-118">Requirement</span></span> | <span data-ttu-id="aa79e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aa79e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa79e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa79e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa79e-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa79e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa79e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa79e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa79e-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aa79e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aa79e-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aa79e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa79e-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa79e-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa79e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa79e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa79e-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="aa79e-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="aa79e-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="aa79e-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="aa79e-129">**компоситионформ**</span><span class="sxs-lookup"><span data-stu-id="aa79e-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="aa79e-130">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="aa79e-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="aa79e-131">**\_SETCONTEXT IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="aa79e-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 




