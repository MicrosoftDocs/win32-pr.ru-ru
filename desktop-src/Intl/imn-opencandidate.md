---
description: Уведомляет приложение, когда редактор IME готов открыть окно кандидатов. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Событие IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910111"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="2f41c-104">\_Событие ИМН опенкандидате</span><span class="sxs-lookup"><span data-stu-id="2f41c-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="2f41c-105">Уведомляет приложение, когда редактор IME готов открыть окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="2f41c-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="2f41c-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="2f41c-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="2f41c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f41c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f41c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f41c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2f41c-109">Задайте для параметра значение ИМН \_ опенкандидате.</span><span class="sxs-lookup"><span data-stu-id="2f41c-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="2f41c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f41c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2f41c-111">Флаг списка кандидатов.</span><span class="sxs-lookup"><span data-stu-id="2f41c-111">Candidate list flag.</span></span> <span data-ttu-id="2f41c-112">Каждый бит соответствует списку кандидатов: бит 0 в первый список, бит 1 – второй и т. д.</span><span class="sxs-lookup"><span data-stu-id="2f41c-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="2f41c-113">Если указан бит 1, откроется соответствующее окно с кандидатом.</span><span class="sxs-lookup"><span data-stu-id="2f41c-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f41c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f41c-114">Return Value</span></span>

<span data-ttu-id="2f41c-115">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2f41c-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f41c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f41c-116">Remarks</span></span>

<span data-ttu-id="2f41c-117">Приложение должно обработать эту команду, если на ней отображаются сами кандидаты.</span><span class="sxs-lookup"><span data-stu-id="2f41c-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="2f41c-118">Приложение может получить список кандидатов для вывода с помощью функции [**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="2f41c-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="2f41c-119">По умолчанию при обработке этой команды в окне редактора IME создается окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="2f41c-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f41c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2f41c-120">Requirements</span></span>



| <span data-ttu-id="2f41c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2f41c-121">Requirement</span></span> | <span data-ttu-id="2f41c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2f41c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f41c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f41c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2f41c-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f41c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f41c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f41c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2f41c-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f41c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2f41c-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2f41c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f41c-128"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f41c-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f41c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f41c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f41c-130">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="2f41c-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2f41c-131">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="2f41c-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2f41c-132">**иммжеткандидателист**</span><span class="sxs-lookup"><span data-stu-id="2f41c-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="2f41c-133">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="2f41c-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




