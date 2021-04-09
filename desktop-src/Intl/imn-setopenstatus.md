---
description: Уведомляет приложение при обновлении состояния открытия входного контекста. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: Код уведомления IMN_SETOPENSTATUS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3598d7415cf415de3279e016d81a6d14b767d5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080766"
---
# <a name="imn_setopenstatus-notification-code"></a><span data-ttu-id="fe7ed-104">\_Код уведомления ИМН сетопенстатус</span><span class="sxs-lookup"><span data-stu-id="fe7ed-104">IMN\_SETOPENSTATUS notification code</span></span>

<span data-ttu-id="fe7ed-105">Уведомляет приложение при обновлении состояния открытия входного контекста.</span><span class="sxs-lookup"><span data-stu-id="fe7ed-105">Notifies an application when the open status of the input context is updated.</span></span> <span data-ttu-id="fe7ed-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fe7ed-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a><span data-ttu-id="fe7ed-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe7ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe7ed-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe7ed-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="fe7ed-109">Задайте для параметра значение ИМН \_ сетопенстатус.</span><span class="sxs-lookup"><span data-stu-id="fe7ed-109">Set to IMN\_SETOPENSTATUS.</span></span>

</dd> <dt>

<span data-ttu-id="fe7ed-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe7ed-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="fe7ed-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fe7ed-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe7ed-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe7ed-112">Return Value</span></span>

<span data-ttu-id="fe7ed-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fe7ed-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe7ed-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe7ed-114">Remarks</span></span>

<span data-ttu-id="fe7ed-115">Приложение может получить сведения о состоянии Open с помощью функции [**иммжетопенстатус**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) .</span><span class="sxs-lookup"><span data-stu-id="fe7ed-115">The application can get information about the open status by using the [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe7ed-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fe7ed-116">Requirements</span></span>



| <span data-ttu-id="fe7ed-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fe7ed-117">Requirement</span></span> | <span data-ttu-id="fe7ed-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fe7ed-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe7ed-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe7ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe7ed-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe7ed-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe7ed-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe7ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe7ed-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe7ed-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fe7ed-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fe7ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe7ed-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ed-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe7ed-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe7ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe7ed-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="fe7ed-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="fe7ed-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="fe7ed-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="fe7ed-128">**иммжетопенстатус**</span><span class="sxs-lookup"><span data-stu-id="fe7ed-128">**ImmGetOpenStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[<span data-ttu-id="fe7ed-129">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="fe7ed-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




