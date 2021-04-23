---
description: Уведомляет приложение при обновлении шрифта входного контекста. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: Код уведомления IMN_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684244"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="a3953-104">\_Код уведомления ИМН сеткомпоситионфонт</span><span class="sxs-lookup"><span data-stu-id="a3953-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="a3953-105">Уведомляет приложение при обновлении шрифта входного контекста.</span><span class="sxs-lookup"><span data-stu-id="a3953-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="a3953-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a3953-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="a3953-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3953-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3953-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3953-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a3953-109">Задайте для параметра значение ИМН \_ сеткомпоситионфонт.</span><span class="sxs-lookup"><span data-stu-id="a3953-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="a3953-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3953-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a3953-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="a3953-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3953-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3953-112">Return Value</span></span>

<span data-ttu-id="a3953-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a3953-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3953-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3953-114">Remarks</span></span>

<span data-ttu-id="a3953-115">Приложение может получить сведения о шрифте с помощью функции [**иммжеткомпоситионфонт**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) .</span><span class="sxs-lookup"><span data-stu-id="a3953-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="a3953-116">Затем окно IME использует шрифт для рисования строки композиции.</span><span class="sxs-lookup"><span data-stu-id="a3953-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3953-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a3953-117">Requirements</span></span>



| <span data-ttu-id="a3953-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a3953-118">Requirement</span></span> | <span data-ttu-id="a3953-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a3953-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3953-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3953-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a3953-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3953-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a3953-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3953-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a3953-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3953-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3953-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3953-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3953-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3953-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3953-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3953-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3953-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="a3953-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a3953-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="a3953-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a3953-129">**иммжеткомпоситионфонт**</span><span class="sxs-lookup"><span data-stu-id="a3953-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="a3953-130">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="a3953-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




