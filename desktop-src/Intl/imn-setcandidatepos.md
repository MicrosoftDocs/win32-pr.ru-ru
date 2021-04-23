---
description: Уведомляет приложение о завершении обработки кандидатов, и редактор IME собирается переместить окно кандидатов. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: Код уведомления IMN_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650818"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="4cd62-104">\_Код уведомления ИМН сеткандидатепос</span><span class="sxs-lookup"><span data-stu-id="4cd62-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="4cd62-105">Уведомляет приложение о завершении обработки кандидатов, и редактор IME собирается переместить окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="4cd62-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="4cd62-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4cd62-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="4cd62-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cd62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd62-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cd62-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="4cd62-109">Задайте для параметра значение ИМН \_ сеткандидатепос.</span><span class="sxs-lookup"><span data-stu-id="4cd62-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="4cd62-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cd62-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4cd62-111">Флаг списка кандидатов.</span><span class="sxs-lookup"><span data-stu-id="4cd62-111">Candidate list flag.</span></span> <span data-ttu-id="4cd62-112">Каждый бит соответствует списку кандидатов: бит 0 в первый список, бит 1 – второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="4cd62-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="4cd62-113">Если указан бит 1, соответствующее окно-кандидата будет перемещено.</span><span class="sxs-lookup"><span data-stu-id="4cd62-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd62-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cd62-114">Return Value</span></span>

<span data-ttu-id="4cd62-115">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4cd62-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cd62-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cd62-116">Remarks</span></span>

<span data-ttu-id="4cd62-117">Приложение должно обработать эту команду, если в ней отображается окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="4cd62-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="4cd62-118">Окно IME перемещает окно кандидатов при обработке этой команды.</span><span class="sxs-lookup"><span data-stu-id="4cd62-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd62-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4cd62-119">Requirements</span></span>



| <span data-ttu-id="4cd62-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4cd62-120">Requirement</span></span> | <span data-ttu-id="4cd62-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd62-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd62-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cd62-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd62-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cd62-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4cd62-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cd62-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd62-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4cd62-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4cd62-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4cd62-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cd62-127"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd62-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd62-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cd62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd62-129">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="4cd62-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4cd62-130">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="4cd62-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="4cd62-131">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="4cd62-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




