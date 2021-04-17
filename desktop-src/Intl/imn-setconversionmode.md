---
description: Уведомляет приложение при обновлении режима преобразования входного контекста. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: Код уведомления IMN_SETCONVERSIONMODE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684243"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="d57e1-104">\_Код уведомления ИМН сетконверсионмоде</span><span class="sxs-lookup"><span data-stu-id="d57e1-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="d57e1-105">Уведомляет приложение при обновлении режима преобразования входного контекста.</span><span class="sxs-lookup"><span data-stu-id="d57e1-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="d57e1-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d57e1-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="d57e1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d57e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57e1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d57e1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d57e1-109">Задайте для параметра значение ИМН \_ сетконверсионмоде.</span><span class="sxs-lookup"><span data-stu-id="d57e1-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="d57e1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d57e1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d57e1-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d57e1-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57e1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d57e1-112">Return Value</span></span>

<span data-ttu-id="d57e1-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d57e1-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57e1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d57e1-114">Remarks</span></span>

<span data-ttu-id="d57e1-115">Приложение может получать сведения о режиме преобразования с помощью функции [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="d57e1-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57e1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d57e1-116">Requirements</span></span>



| <span data-ttu-id="d57e1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d57e1-117">Requirement</span></span> | <span data-ttu-id="d57e1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d57e1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57e1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d57e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d57e1-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d57e1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d57e1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d57e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d57e1-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d57e1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d57e1-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d57e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57e1-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d57e1-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57e1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d57e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57e1-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="d57e1-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d57e1-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="d57e1-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d57e1-128">**иммжетконверсионстатус**</span><span class="sxs-lookup"><span data-stu-id="d57e1-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="d57e1-129">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="d57e1-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




