---
description: Уведомляет приложение, когда редактор IME собирается закрыть окно кандидатов. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: Код уведомления IMN_CLOSECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683524"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="405ac-104">\_Код уведомления ИМН клосекандидате</span><span class="sxs-lookup"><span data-stu-id="405ac-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="405ac-105">Уведомляет приложение, когда редактор IME собирается закрыть окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="405ac-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="405ac-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="405ac-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="405ac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="405ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="405ac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="405ac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="405ac-109">Задайте для параметра значение ИМН \_ клосекандидате.</span><span class="sxs-lookup"><span data-stu-id="405ac-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="405ac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="405ac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="405ac-111">Флаг списка кандидатов.</span><span class="sxs-lookup"><span data-stu-id="405ac-111">Candidate list flag.</span></span> <span data-ttu-id="405ac-112">Каждый бит соответствует списку кандидатов: бит 0 в первый список, бит 1 – второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="405ac-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="405ac-113">Если указан бит 1, соответствующее окно кандидатов будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="405ac-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="405ac-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="405ac-114">Return Value</span></span>

<span data-ttu-id="405ac-115">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="405ac-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="405ac-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="405ac-116">Remarks</span></span>

<span data-ttu-id="405ac-117">Приложение должно обработать эту команду, если на ней отображаются сами кандидаты.</span><span class="sxs-lookup"><span data-stu-id="405ac-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="405ac-118">По умолчанию окно IME уничтожает окно-кандидат при обработке этой команды.</span><span class="sxs-lookup"><span data-stu-id="405ac-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="405ac-119">Требования</span><span class="sxs-lookup"><span data-stu-id="405ac-119">Requirements</span></span>



| <span data-ttu-id="405ac-120">Требование</span><span class="sxs-lookup"><span data-stu-id="405ac-120">Requirement</span></span> | <span data-ttu-id="405ac-121">Значение</span><span class="sxs-lookup"><span data-stu-id="405ac-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="405ac-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="405ac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="405ac-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="405ac-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="405ac-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="405ac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="405ac-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="405ac-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="405ac-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="405ac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="405ac-127"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="405ac-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="405ac-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="405ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405ac-129">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="405ac-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="405ac-130">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="405ac-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="405ac-131">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="405ac-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




