---
description: Указывает окну IME для получения расположения окна композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: Команда IMC_GETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810408"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="cf55e-104">ИМК \_ жеткомпоситионвиндов, команда</span><span class="sxs-lookup"><span data-stu-id="cf55e-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="cf55e-105">Указывает окну IME для получения расположения окна композиции.</span><span class="sxs-lookup"><span data-stu-id="cf55e-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="cf55e-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="cf55e-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="cf55e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf55e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf55e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf55e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="cf55e-109">Задайте для параметра значение ИМК \_ жеткомпоситионвиндов.</span><span class="sxs-lookup"><span data-stu-id="cf55e-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="cf55e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf55e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="cf55e-111">Указатель на структуру [**компоситионформ**](/windows/win32/api/imm/ns-imm-compositionform) , содержащую расположение окна композиции.</span><span class="sxs-lookup"><span data-stu-id="cf55e-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf55e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf55e-112">Return Value</span></span>

<span data-ttu-id="cf55e-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cf55e-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf55e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf55e-114">Remarks</span></span>

<span data-ttu-id="cf55e-115">Так как редактор IME может скорректировать расположение окна композиции, приложение использует эту команду для получения фактического расположения, чтобы решить, следует ли изменить расположение окна.</span><span class="sxs-lookup"><span data-stu-id="cf55e-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="cf55e-116">Полученное расположение находится в координатах окна относительно окна, имеющего текущий фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="cf55e-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf55e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cf55e-117">Requirements</span></span>



| <span data-ttu-id="cf55e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cf55e-118">Requirement</span></span> | <span data-ttu-id="cf55e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cf55e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf55e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf55e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cf55e-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf55e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cf55e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf55e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cf55e-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf55e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf55e-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf55e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf55e-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf55e-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf55e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf55e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf55e-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="cf55e-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cf55e-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="cf55e-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="cf55e-129">**компоситионформ**</span><span class="sxs-lookup"><span data-stu-id="cf55e-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




