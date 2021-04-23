---
description: Уведомляет приложение, когда редактор IME собирается создать окно состояния. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: Код уведомления IMN_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683521"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="0d7da-104">\_Код уведомления ИМН опенстатусвиндов</span><span class="sxs-lookup"><span data-stu-id="0d7da-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="0d7da-105">Уведомляет приложение, когда редактор IME собирается создать окно состояния.</span><span class="sxs-lookup"><span data-stu-id="0d7da-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="0d7da-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0d7da-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="0d7da-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d7da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d7da-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d7da-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="0d7da-109">Задайте для параметра значение ИМН \_ опенстатусвиндов.</span><span class="sxs-lookup"><span data-stu-id="0d7da-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="0d7da-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d7da-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0d7da-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d7da-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d7da-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d7da-112">Return Value</span></span>

<span data-ttu-id="0d7da-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0d7da-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d7da-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d7da-114">Remarks</span></span>

<span data-ttu-id="0d7da-115">Приложение обрабатывает эту команду, чтобы отобразить окно состояния IME отдельно.</span><span class="sxs-lookup"><span data-stu-id="0d7da-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="0d7da-116">Окно редактора IME создает окно состояния при обработке этой команды и задает строки, отображаемые в окне во входном контексте.</span><span class="sxs-lookup"><span data-stu-id="0d7da-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="0d7da-117">Приложения могут получать сведения о окне состояния с помощью функции [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="0d7da-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d7da-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0d7da-118">Requirements</span></span>



| <span data-ttu-id="0d7da-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0d7da-119">Requirement</span></span> | <span data-ttu-id="0d7da-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0d7da-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7da-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d7da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d7da-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d7da-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0d7da-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d7da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d7da-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d7da-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0d7da-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0d7da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d7da-126"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d7da-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d7da-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d7da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7da-128">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="0d7da-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="0d7da-129">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="0d7da-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="0d7da-130">**иммжетконверсионстатус**</span><span class="sxs-lookup"><span data-stu-id="0d7da-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="0d7da-131">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="0d7da-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




