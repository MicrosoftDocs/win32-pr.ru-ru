---
description: Указывает окну редактора IME скрыть окно состояния. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: Команда IMC_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913880"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="01fea-104">ИМК \_ клосестатусвиндов, команда</span><span class="sxs-lookup"><span data-stu-id="01fea-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="01fea-105">Указывает окну редактора IME скрыть окно состояния.</span><span class="sxs-lookup"><span data-stu-id="01fea-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="01fea-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="01fea-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="01fea-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01fea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fea-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="01fea-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="01fea-109">Задайте для параметра значение ИМК \_ клосестатусвиндов.</span><span class="sxs-lookup"><span data-stu-id="01fea-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="01fea-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="01fea-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="01fea-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="01fea-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fea-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01fea-112">Return Value</span></span>

<span data-ttu-id="01fea-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="01fea-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01fea-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01fea-114">Remarks</span></span>

<span data-ttu-id="01fea-115">Если окно состояния IME уже скрыто, команда не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="01fea-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="01fea-116">Хотя приложение может отправлять эту команду в окно IME, приложение не получает соответствующую команду [ИМН \_ клосестатусвиндов](imn-closestatuswindow.md) .</span><span class="sxs-lookup"><span data-stu-id="01fea-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fea-117">Требования</span><span class="sxs-lookup"><span data-stu-id="01fea-117">Requirements</span></span>



| <span data-ttu-id="01fea-118">Требование</span><span class="sxs-lookup"><span data-stu-id="01fea-118">Requirement</span></span> | <span data-ttu-id="01fea-119">Значение</span><span class="sxs-lookup"><span data-stu-id="01fea-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01fea-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01fea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01fea-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01fea-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="01fea-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01fea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01fea-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01fea-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="01fea-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="01fea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01fea-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01fea-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fea-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01fea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fea-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="01fea-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="01fea-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="01fea-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 




