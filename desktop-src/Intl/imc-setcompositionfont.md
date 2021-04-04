---
description: Указывает окну IME указать логический шрифт, используемый для отображения промежуточных символов в окне композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Команда IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897690"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="1de25-104">ИМК \_ сеткомпоситионфонт, команда</span><span class="sxs-lookup"><span data-stu-id="1de25-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="1de25-105">Указывает окну IME указать логический шрифт, используемый для отображения промежуточных символов в окне композиции.</span><span class="sxs-lookup"><span data-stu-id="1de25-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="1de25-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="1de25-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="1de25-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1de25-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de25-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1de25-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1de25-109">Задайте для параметра значение ИМК \_ сеткомпоситионфонт.</span><span class="sxs-lookup"><span data-stu-id="1de25-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="1de25-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1de25-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1de25-111">Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , содержащую сведения о логическом шрифте.</span><span class="sxs-lookup"><span data-stu-id="1de25-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de25-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1de25-112">Return Value</span></span>

<span data-ttu-id="1de25-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1de25-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1de25-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1de25-114">Remarks</span></span>

<span data-ttu-id="1de25-115">При обработке этой команды окно IME изменяет текущий выбранный шрифт во входном контексте.</span><span class="sxs-lookup"><span data-stu-id="1de25-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de25-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1de25-116">Requirements</span></span>



| <span data-ttu-id="1de25-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1de25-117">Requirement</span></span> | <span data-ttu-id="1de25-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1de25-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de25-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1de25-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1de25-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1de25-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1de25-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1de25-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1de25-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1de25-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1de25-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1de25-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1de25-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1de25-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1de25-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1de25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de25-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="1de25-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1de25-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="1de25-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1de25-128">**\_ \_ элемент управления WM IME**</span><span class="sxs-lookup"><span data-stu-id="1de25-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
