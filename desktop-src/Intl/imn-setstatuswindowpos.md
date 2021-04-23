---
description: Уведомляет приложение при обновлении расположения окна состояния во входном контексте. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров следующим образом.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: Код уведомления IMN_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683365"
---
# <a name="imn_setstatuswindowpos-notification-code"></a><span data-ttu-id="57b04-104">\_Код уведомления ИМН сетстатусвиндовпос</span><span class="sxs-lookup"><span data-stu-id="57b04-104">IMN\_SETSTATUSWINDOWPOS notification code</span></span>

<span data-ttu-id="57b04-105">Уведомляет приложение при обновлении расположения окна состояния во входном контексте.</span><span class="sxs-lookup"><span data-stu-id="57b04-105">Notifies an application when the status window position in the input context is updated.</span></span> <span data-ttu-id="57b04-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров следующим образом.</span><span class="sxs-lookup"><span data-stu-id="57b04-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as follows.</span></span>


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="57b04-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="57b04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b04-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="57b04-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="57b04-109">Задайте для параметра значение ИМН \_ сетстатусвиндовпос.</span><span class="sxs-lookup"><span data-stu-id="57b04-109">Set to IMN\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="57b04-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="57b04-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="57b04-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="57b04-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b04-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57b04-112">Return Value</span></span>

<span data-ttu-id="57b04-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="57b04-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b04-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57b04-114">Remarks</span></span>

<span data-ttu-id="57b04-115">Приложение может получить сведения о положении окна состояния с помощью команды [**ИМК \_ жетстатусвиндовпос**](imc-getstatuswindowpos.md) .</span><span class="sxs-lookup"><span data-stu-id="57b04-115">The application can get information about the status window position by using the [**IMC\_GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b04-116">Требования</span><span class="sxs-lookup"><span data-stu-id="57b04-116">Requirements</span></span>



| <span data-ttu-id="57b04-117">Требование</span><span class="sxs-lookup"><span data-stu-id="57b04-117">Requirement</span></span> | <span data-ttu-id="57b04-118">Значение</span><span class="sxs-lookup"><span data-stu-id="57b04-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b04-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57b04-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57b04-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57b04-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57b04-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57b04-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57b04-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57b04-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="57b04-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57b04-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b04-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57b04-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b04-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57b04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b04-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="57b04-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="57b04-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="57b04-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="57b04-128">**ИМК \_ жетстатусвиндовпос**</span><span class="sxs-lookup"><span data-stu-id="57b04-128">**IMC\_GETSTATUSWINDOWPOS**</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="57b04-129">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="57b04-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




