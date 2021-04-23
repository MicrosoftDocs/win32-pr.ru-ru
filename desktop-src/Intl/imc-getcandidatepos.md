---
description: Указывает окну IME для получения расположения окна кандидатов. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Команда IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651224"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="87241-104">ИМК \_ жеткандидатепос, команда</span><span class="sxs-lookup"><span data-stu-id="87241-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="87241-105">Указывает окну IME для получения расположения окна кандидатов.</span><span class="sxs-lookup"><span data-stu-id="87241-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="87241-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="87241-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="87241-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="87241-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87241-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="87241-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="87241-109">Задайте для параметра значение ИМК \_ жеткандидатепос.</span><span class="sxs-lookup"><span data-stu-id="87241-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="87241-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="87241-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="87241-111">Указатель на структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) , содержащую расположение окна кандидатов.</span><span class="sxs-lookup"><span data-stu-id="87241-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87241-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87241-112">Return Value</span></span>

<span data-ttu-id="87241-113">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="87241-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87241-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87241-114">Remarks</span></span>

<span data-ttu-id="87241-115">Так как редактор IME может скорректировать расположение окна кандидатов, приложение использует эту команду для получения фактического расположения, чтобы решить, следует ли изменить расположение окна.</span><span class="sxs-lookup"><span data-stu-id="87241-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="87241-116">Полученное расположение находится в координатах окна относительно окна, имеющего текущий фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="87241-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="87241-117">Требования</span><span class="sxs-lookup"><span data-stu-id="87241-117">Requirements</span></span>



| <span data-ttu-id="87241-118">Требование</span><span class="sxs-lookup"><span data-stu-id="87241-118">Requirement</span></span> | <span data-ttu-id="87241-119">Значение</span><span class="sxs-lookup"><span data-stu-id="87241-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87241-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87241-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87241-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87241-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87241-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87241-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87241-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87241-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="87241-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="87241-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87241-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87241-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87241-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87241-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87241-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="87241-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="87241-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="87241-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="87241-129">**кандидатеформ**</span><span class="sxs-lookup"><span data-stu-id="87241-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




