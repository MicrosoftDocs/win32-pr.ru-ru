---
description: Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о шрифте, используемом окном композиции. Приложение получает эту команду через \_ сообщение запроса WM IME \_ с параметрами, как показано ниже.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: Код уведомления IMR_COMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683363"
---
# <a name="imr_compositionfont-notification-code"></a><span data-ttu-id="d9acf-104">\_Код уведомления КОМПОСИТИОНФОНТ IMR</span><span class="sxs-lookup"><span data-stu-id="d9acf-104">IMR\_COMPOSITIONFONT notification code</span></span>

<span data-ttu-id="d9acf-105">Уведомляет приложение, когда выбранному РЕДАКТОРу требуется информация о шрифте, используемом окном композиции.</span><span class="sxs-lookup"><span data-stu-id="d9acf-105">Notifies an application when a selected IME needs information about the font used by the composition window.</span></span> <span data-ttu-id="d9acf-106">Приложение получает эту команду через сообщение [**запроса WM \_ IME \_**](wm-ime-request.md) с параметрами, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d9acf-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters as shown below.</span></span>


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="d9acf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9acf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9acf-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9acf-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d9acf-109">Задайте значение IMR \_ компоситионфонт.</span><span class="sxs-lookup"><span data-stu-id="d9acf-109">Set to IMR\_COMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="d9acf-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9acf-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d9acf-111">Указатель на буфер, содержащий структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="d9acf-111">Pointer to a buffer containing a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="d9acf-112">Приложение заполняет значения для текущего окна композиции.</span><span class="sxs-lookup"><span data-stu-id="d9acf-112">The application fills in the values for the current composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9acf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9acf-113">Return Value</span></span>

<span data-ttu-id="d9acf-114">Функция возвращает ненулевое значение, если приложение заполняет структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="d9acf-114">Returns a nonzero value if the application fills in the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="d9acf-115">В противном случае команда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="d9acf-115">Otherwise, the command returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9acf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9acf-116">Remarks</span></span>

<span data-ttu-id="d9acf-117">Эта команда может быть отправлена редактором IME в окно, которое очистило \_ флаг ШОВУИКОМПОСИТИОНВИНДОВ ISC в обработчике сообщений [**\_ \_ SETCONTEXT редактора IME**](wm-ime-setcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="d9acf-117">This command can be sent by the IME to a window that cleared the ISC\_SHOWUICOMPOSITIONWINDOW flag in the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9acf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d9acf-118">Requirements</span></span>



| <span data-ttu-id="d9acf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d9acf-119">Requirement</span></span> | <span data-ttu-id="d9acf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d9acf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9acf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9acf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9acf-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9acf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d9acf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9acf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9acf-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9acf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d9acf-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9acf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9acf-126"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9acf-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9acf-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9acf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9acf-128">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="d9acf-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d9acf-129">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="d9acf-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d9acf-130">**\_запрос IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d9acf-130">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> <dt>

[<span data-ttu-id="d9acf-131">**\_SETCONTEXT IME \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d9acf-131">**WM\_IME\_SETCONTEXT**</span></span>](wm-ime-setcontext.md)
</dt> </dl>

 

 
