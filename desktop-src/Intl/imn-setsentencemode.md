---
description: Уведомляет приложение при обновлении режима предложения входного контекста. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 72455193-cd17-45f8-b19c-a1f735ff81bf
title: Код уведомления IMN_SETSENTENCEMODE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0130c5b3d7284112e64cca698b358650f51f3642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663064"
---
# <a name="imn_setsentencemode-notification-code"></a><span data-ttu-id="4d107-104">\_Код уведомления ИМН сетсентенцемоде</span><span class="sxs-lookup"><span data-stu-id="4d107-104">IMN\_SETSENTENCEMODE notification code</span></span>

<span data-ttu-id="4d107-105">Уведомляет приложение при обновлении режима предложения входного контекста.</span><span class="sxs-lookup"><span data-stu-id="4d107-105">Notifies an application when the sentence mode of the input context is updated.</span></span> <span data-ttu-id="4d107-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4d107-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETSENTENCEMODE
```



## <a name="parameters"></a><span data-ttu-id="4d107-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d107-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d107-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d107-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4d107-109">Задайте для параметра значение ИМН \_ сетсентенцемоде.</span><span class="sxs-lookup"><span data-stu-id="4d107-109">Set to IMN\_SETSENTENCEMODE.</span></span>

</dd> <dt>

<span data-ttu-id="4d107-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d107-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4d107-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4d107-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d107-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d107-112">Return Value</span></span>

<span data-ttu-id="4d107-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4d107-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d107-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d107-114">Remarks</span></span>

<span data-ttu-id="4d107-115">Приложение может получать сведения о режиме предложений с помощью функции [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="4d107-115">The application can get information about the sentence mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d107-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4d107-116">Requirements</span></span>



| <span data-ttu-id="4d107-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4d107-117">Requirement</span></span> | <span data-ttu-id="4d107-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4d107-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d107-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d107-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d107-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d107-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4d107-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d107-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d107-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d107-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d107-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4d107-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d107-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d107-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d107-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d107-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d107-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="4d107-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4d107-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="4d107-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4d107-128">**иммжетконверсионстатус**</span><span class="sxs-lookup"><span data-stu-id="4d107-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="4d107-129">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="4d107-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




