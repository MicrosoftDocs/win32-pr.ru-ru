---
description: Указывает окну редактора IME отображать окно состояния. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: Команда IMC_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897693"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="8ea5a-104">ИМК \_ опенстатусвиндов, команда</span><span class="sxs-lookup"><span data-stu-id="8ea5a-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="8ea5a-105">Указывает окну редактора IME отображать окно состояния.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="8ea5a-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="8ea5a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ea5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea5a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ea5a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="8ea5a-109">Задайте для параметра значение ИМК \_ опенстатусвиндов.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="8ea5a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ea5a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8ea5a-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea5a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ea5a-112">Return Value</span></span>

<span data-ttu-id="8ea5a-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea5a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ea5a-114">Remarks</span></span>

<span data-ttu-id="8ea5a-115">Эта команда пропускается, если операционная система не находится в режиме отображения состояния IME.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="8ea5a-116">Пользователь может установить или снять режим отображения состояния IME на панели задач.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="8ea5a-117">Если окно состояния уже отображается, команда не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="8ea5a-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="8ea5a-118">Несмотря на то, что приложение может отправить эту команду в окно IME, приложение не получает соответствующую команду [**ИМН \_ опенстатусвиндов**](imn-openstatuswindow.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea5a-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea5a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8ea5a-119">Requirements</span></span>



| <span data-ttu-id="8ea5a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8ea5a-120">Requirement</span></span> | <span data-ttu-id="8ea5a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8ea5a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea5a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ea5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea5a-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ea5a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8ea5a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ea5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea5a-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ea5a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ea5a-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ea5a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea5a-127"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea5a-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea5a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ea5a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea5a-129">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="8ea5a-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8ea5a-130">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="8ea5a-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="8ea5a-131">**\_ \_ элемент управления WM IME**</span><span class="sxs-lookup"><span data-stu-id="8ea5a-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




