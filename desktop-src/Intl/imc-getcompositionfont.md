---
description: Указывает окну редактора IME получить логический шрифт, используемый для отображения промежуточных символов в окне композиции. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Команда IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263241"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="69077-104">ИМК \_ жеткомпоситионфонт, команда</span><span class="sxs-lookup"><span data-stu-id="69077-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="69077-105">Указывает окну редактора IME получить логический шрифт, используемый для отображения промежуточных символов в окне композиции.</span><span class="sxs-lookup"><span data-stu-id="69077-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="69077-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="69077-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="69077-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="69077-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69077-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="69077-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="69077-109">Задайте для параметра значение ИМК \_ жеткомпоситионфонт.</span><span class="sxs-lookup"><span data-stu-id="69077-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="69077-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="69077-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="69077-111">Указатель на структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , которая получает сведения о логическом шрифте.</span><span class="sxs-lookup"><span data-stu-id="69077-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69077-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69077-112">Return Value</span></span>

<span data-ttu-id="69077-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="69077-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="69077-114">Требования</span><span class="sxs-lookup"><span data-stu-id="69077-114">Requirements</span></span>



| <span data-ttu-id="69077-115">Требование</span><span class="sxs-lookup"><span data-stu-id="69077-115">Requirement</span></span> | <span data-ttu-id="69077-116">Значение</span><span class="sxs-lookup"><span data-stu-id="69077-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69077-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69077-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69077-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69077-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69077-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69077-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69077-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69077-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69077-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="69077-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69077-122"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69077-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69077-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69077-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69077-124">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="69077-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="69077-125">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="69077-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 
