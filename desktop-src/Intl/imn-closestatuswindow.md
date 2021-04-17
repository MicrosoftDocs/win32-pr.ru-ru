---
description: Уведомляет приложение, когда редактор IME собирается закрыть окно состояния. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: Код уведомления IMN_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650819"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="47f4c-104">\_Код уведомления ИМН клосестатусвиндов</span><span class="sxs-lookup"><span data-stu-id="47f4c-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="47f4c-105">Уведомляет приложение, когда редактор IME собирается закрыть окно состояния.</span><span class="sxs-lookup"><span data-stu-id="47f4c-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="47f4c-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="47f4c-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="47f4c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="47f4c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f4c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="47f4c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="47f4c-109">Задайте для параметра значение ИМН \_ клосестатусвиндов.</span><span class="sxs-lookup"><span data-stu-id="47f4c-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="47f4c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="47f4c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="47f4c-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="47f4c-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f4c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f4c-112">Return Value</span></span>

<span data-ttu-id="47f4c-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="47f4c-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47f4c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47f4c-114">Remarks</span></span>

<span data-ttu-id="47f4c-115">Приложение должно обработать эту команду, если в ней отображается окно состояния IME.</span><span class="sxs-lookup"><span data-stu-id="47f4c-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="47f4c-116">Окно редактора IME закрывает окно состояния при обработке этой команды.</span><span class="sxs-lookup"><span data-stu-id="47f4c-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f4c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="47f4c-117">Requirements</span></span>



| <span data-ttu-id="47f4c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="47f4c-118">Requirement</span></span> | <span data-ttu-id="47f4c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="47f4c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f4c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47f4c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="47f4c-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47f4c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47f4c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47f4c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="47f4c-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47f4c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="47f4c-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47f4c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="47f4c-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47f4c-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f4c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47f4c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f4c-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="47f4c-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="47f4c-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="47f4c-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="47f4c-129">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="47f4c-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




