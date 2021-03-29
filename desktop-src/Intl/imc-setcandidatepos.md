---
description: Указывает окну IME задать расположение окна кандидатов. Чтобы отправить эту команду, приложение использует \_ \_ управляющее сообщение WM IME с параметрами параметров, приведенными ниже.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Команда IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810409"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="808e7-104">ИМК \_ сеткандидатепос, команда</span><span class="sxs-lookup"><span data-stu-id="808e7-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="808e7-105">Указывает окну IME задать расположение окна кандидатов.</span><span class="sxs-lookup"><span data-stu-id="808e7-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="808e7-106">Чтобы отправить эту команду, приложение использует [**\_ \_ управляющее сообщение WM IME**](wm-ime-control.md) с параметрами параметров, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="808e7-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="808e7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="808e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="808e7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="808e7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="808e7-109">Задайте для параметра значение ИМК \_ сеткандидатепос.</span><span class="sxs-lookup"><span data-stu-id="808e7-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="808e7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="808e7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="808e7-111">Указатель на структуру [**кандидатеформ**](/windows/win32/api/imm/ns-imm-candidateform) , которая содержит координату x и координату y для окна кандидатов.</span><span class="sxs-lookup"><span data-stu-id="808e7-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="808e7-112">Приложение должно установить элемент **двиндекс** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="808e7-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="808e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="808e7-113">Return Value</span></span>

<span data-ttu-id="808e7-114">Возвращает 0 в случае успеха или ненулевое значение в противном случае.</span><span class="sxs-lookup"><span data-stu-id="808e7-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="808e7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="808e7-115">Remarks</span></span>

<span data-ttu-id="808e7-116">Эта команда предназначена для приложений, которые отображают собственные символы композиции, но используют окно IME для вывода кандидатов.</span><span class="sxs-lookup"><span data-stu-id="808e7-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="808e7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="808e7-117">Requirements</span></span>



| <span data-ttu-id="808e7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="808e7-118">Requirement</span></span> | <span data-ttu-id="808e7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="808e7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="808e7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="808e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="808e7-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="808e7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="808e7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="808e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="808e7-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="808e7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="808e7-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="808e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="808e7-125"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="808e7-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="808e7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="808e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808e7-127">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="808e7-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="808e7-128">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="808e7-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="808e7-129">**кандидатеформ**</span><span class="sxs-lookup"><span data-stu-id="808e7-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="808e7-130">**\_ \_ элемент управления WM IME**</span><span class="sxs-lookup"><span data-stu-id="808e7-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




