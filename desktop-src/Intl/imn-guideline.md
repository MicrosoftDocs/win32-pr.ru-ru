---
description: Уведомляет приложение, когда редактор IME собирается отобразить сообщение об ошибке или другую информацию. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: Код уведомления IMN_GUIDELINE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345765"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="4f4b0-104">\_Код уведомления об рекомендации ИМН</span><span class="sxs-lookup"><span data-stu-id="4f4b0-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="4f4b0-105">Уведомляет приложение, когда редактор IME собирается отобразить сообщение об ошибке или другую информацию.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="4f4b0-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="4f4b0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f4b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f4b0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f4b0-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4f4b0-109">Задайте для параметра ИМН \_ Рекомендация.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="4f4b0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f4b0-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4f4b0-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f4b0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f4b0-112">Return Value</span></span>

<span data-ttu-id="4f4b0-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f4b0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f4b0-114">Remarks</span></span>

<span data-ttu-id="4f4b0-115">Приложение обрабатывает эту команду, вызывая функцию [**иммжетгуиделине**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) для получения сообщения об ошибке или сведений из IME.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="4f4b0-116">В окне редактора IME отображается сообщение об ошибке или информационная строка в информационном окне.</span><span class="sxs-lookup"><span data-stu-id="4f4b0-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4b0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4f4b0-117">Requirements</span></span>



| <span data-ttu-id="4f4b0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4f4b0-118">Requirement</span></span> | <span data-ttu-id="4f4b0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4f4b0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4b0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f4b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4b0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f4b0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4f4b0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f4b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4b0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f4b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f4b0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f4b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f4b0-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f4b0-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4b0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f4b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4b0-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="4f4b0-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4f4b0-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="4f4b0-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4f4b0-129">**иммжетгуиделине**</span><span class="sxs-lookup"><span data-stu-id="4f4b0-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="4f4b0-130">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="4f4b0-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




