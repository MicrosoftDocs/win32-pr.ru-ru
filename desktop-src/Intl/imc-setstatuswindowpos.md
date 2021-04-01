---
description: Указывает окну редактора IME задать расположение окна состояния. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, как показано ниже.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Команда IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072821"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="2c0c5-104">ИМК \_ сетстатусвиндовпос, команда</span><span class="sxs-lookup"><span data-stu-id="2c0c5-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="2c0c5-105">Указывает окну редактора IME задать расположение окна состояния.</span><span class="sxs-lookup"><span data-stu-id="2c0c5-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="2c0c5-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="2c0c5-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="2c0c5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c0c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c0c5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c0c5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2c0c5-109">Задайте для параметра значение ИМК \_ сетстатусвиндовпос.</span><span class="sxs-lookup"><span data-stu-id="2c0c5-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="2c0c5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c0c5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2c0c5-111">Указатель на структуру [**точек**](/previous-versions//dd162808(v=vs.85)) , которая содержит координату x и координату y позиции окна состояния.</span><span class="sxs-lookup"><span data-stu-id="2c0c5-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="2c0c5-112">Координаты расположены в экранных координатах относительно левого верхнего угла отображения.</span><span class="sxs-lookup"><span data-stu-id="2c0c5-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c0c5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c0c5-113">Return Value</span></span>

<span data-ttu-id="2c0c5-114">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2c0c5-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0c5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2c0c5-115">Requirements</span></span>



| <span data-ttu-id="2c0c5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2c0c5-116">Requirement</span></span> | <span data-ttu-id="2c0c5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2c0c5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0c5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c0c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c0c5-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c0c5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2c0c5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c0c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c0c5-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c0c5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c0c5-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c0c5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c0c5-123"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c0c5-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0c5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c0c5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0c5-125">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="2c0c5-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2c0c5-126">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="2c0c5-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2c0c5-127">**\_ \_ элемент управления WM IME**</span><span class="sxs-lookup"><span data-stu-id="2c0c5-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
