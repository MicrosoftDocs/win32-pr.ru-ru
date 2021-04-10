---
description: Уведомляет приложение, когда редактор IME собирается изменить содержимое окна-кандидата. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: Код уведомления IMN_CHANGECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156586"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="cdabe-104">\_Код уведомления ИМН чанжекандидате</span><span class="sxs-lookup"><span data-stu-id="cdabe-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="cdabe-105">Уведомляет приложение, когда редактор IME собирается изменить содержимое окна-кандидата.</span><span class="sxs-lookup"><span data-stu-id="cdabe-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="cdabe-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="cdabe-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="cdabe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdabe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdabe-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdabe-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="cdabe-109">Задайте для параметра значение ИМН \_ чанжекандидате.</span><span class="sxs-lookup"><span data-stu-id="cdabe-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="cdabe-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdabe-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="cdabe-111">Флаг списка кандидатов.</span><span class="sxs-lookup"><span data-stu-id="cdabe-111">Candidate list flag.</span></span> <span data-ttu-id="cdabe-112">Каждый бит соответствует списку кандидатов: бит 0 — первому списку, бит 1 — второму списку и т. д.</span><span class="sxs-lookup"><span data-stu-id="cdabe-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="cdabe-113">Если указан бит 1, соответствующее окно-кандидата будет изменено.</span><span class="sxs-lookup"><span data-stu-id="cdabe-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdabe-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdabe-114">Return Value</span></span>

<span data-ttu-id="cdabe-115">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="cdabe-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdabe-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdabe-116">Remarks</span></span>

<span data-ttu-id="cdabe-117">Приложение должно обработать эту команду, если на ней отображаются сами кандидаты.</span><span class="sxs-lookup"><span data-stu-id="cdabe-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="cdabe-118">Окно IME изменяет внешний вид окна кандидатов при обработке этой команды.</span><span class="sxs-lookup"><span data-stu-id="cdabe-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="cdabe-119">Приложение может получать сведения о системном окне с помощью [**иммжеткандидателисткаунт**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) и [**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="cdabe-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="cdabe-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cdabe-120">Requirements</span></span>



| <span data-ttu-id="cdabe-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cdabe-121">Requirement</span></span> | <span data-ttu-id="cdabe-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cdabe-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdabe-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdabe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cdabe-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdabe-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cdabe-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdabe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cdabe-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdabe-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cdabe-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cdabe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdabe-128"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdabe-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdabe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdabe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdabe-130">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="cdabe-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cdabe-131">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="cdabe-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="cdabe-132">**иммжеткандидателист**</span><span class="sxs-lookup"><span data-stu-id="cdabe-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="cdabe-133">**иммжеткандидателисткаунт**</span><span class="sxs-lookup"><span data-stu-id="cdabe-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="cdabe-134">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="cdabe-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




