---
description: Указывает окну редактора IME задать стиль окна композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Команда IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682828"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="e04e1-104">ИМК \_ сеткомпоситионвиндов, команда</span><span class="sxs-lookup"><span data-stu-id="e04e1-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="e04e1-105">Указывает окну редактора IME задать стиль окна композиции.</span><span class="sxs-lookup"><span data-stu-id="e04e1-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="e04e1-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="e04e1-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="e04e1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e04e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e04e1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e04e1-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e04e1-109">Задайте для параметра значение ИМК \_ сеткомпоситионвиндов.</span><span class="sxs-lookup"><span data-stu-id="e04e1-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="e04e1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e04e1-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e04e1-111">Указатель на структуру [**компоситионформ**](/windows/win32/api/imm/ns-imm-compositionform) , содержащую сведения о стиле.</span><span class="sxs-lookup"><span data-stu-id="e04e1-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e04e1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e04e1-112">Return Value</span></span>

<span data-ttu-id="e04e1-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e04e1-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04e1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e04e1-114">Remarks</span></span>

<span data-ttu-id="e04e1-115">Эта команда задает стиль в текущем контексте ввода, и стиль затем применяется к каждому окну IME, которое получает этот контекст ввода.</span><span class="sxs-lookup"><span data-stu-id="e04e1-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="e04e1-116">По умолчанию окно IME имеет \_ стиль CFS Point.</span><span class="sxs-lookup"><span data-stu-id="e04e1-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="e04e1-117">В этом стиле окно IME использует текущую точку курсора и клиентскую область окна при открытии любого окна композиции.</span><span class="sxs-lookup"><span data-stu-id="e04e1-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e04e1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e04e1-118">Requirements</span></span>



| <span data-ttu-id="e04e1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e04e1-119">Requirement</span></span> | <span data-ttu-id="e04e1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e04e1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04e1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e04e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e04e1-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e04e1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e04e1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e04e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e04e1-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e04e1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e04e1-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e04e1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e04e1-126"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e04e1-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04e1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e04e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04e1-128">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="e04e1-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e04e1-129">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="e04e1-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e04e1-130">**компоситионформ**</span><span class="sxs-lookup"><span data-stu-id="e04e1-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="e04e1-131">**\_ \_ элемент управления WM IME**</span><span class="sxs-lookup"><span data-stu-id="e04e1-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




