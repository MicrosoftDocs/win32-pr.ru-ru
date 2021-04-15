---
description: Указывает окну IME для получения расположения окна состояния. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Команда IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682829"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="afa89-104">ИМК \_ жетстатусвиндовпос, команда</span><span class="sxs-lookup"><span data-stu-id="afa89-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="afa89-105">Указывает окну IME для получения расположения окна состояния.</span><span class="sxs-lookup"><span data-stu-id="afa89-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="afa89-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="afa89-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="afa89-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="afa89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afa89-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="afa89-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="afa89-109">Задайте для параметра значение ИМК \_ жетстатусвиндовпос.</span><span class="sxs-lookup"><span data-stu-id="afa89-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="afa89-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="afa89-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="afa89-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="afa89-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afa89-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afa89-112">Return Value</span></span>

<span data-ttu-id="afa89-113">Возвращает структуру [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащую координату x и координату y положения окна состояния в экранных координатах относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="afa89-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa89-114">Требования</span><span class="sxs-lookup"><span data-stu-id="afa89-114">Requirements</span></span>



| <span data-ttu-id="afa89-115">Требование</span><span class="sxs-lookup"><span data-stu-id="afa89-115">Requirement</span></span> | <span data-ttu-id="afa89-116">Значение</span><span class="sxs-lookup"><span data-stu-id="afa89-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa89-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afa89-117">Minimum supported client</span></span><br/> | <span data-ttu-id="afa89-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afa89-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="afa89-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afa89-119">Minimum supported server</span></span><br/> | <span data-ttu-id="afa89-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afa89-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="afa89-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="afa89-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa89-122"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afa89-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa89-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afa89-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa89-124">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="afa89-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="afa89-125">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="afa89-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="afa89-126">**\_ \_ элемент управления WM IME**</span><span class="sxs-lookup"><span data-stu-id="afa89-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
