---
description: Уведомляет приложение при обновлении стиля или расположения окна композиции. Приложение получает эту команду через \_ \_ сообщение с уведомлением редактора IME WM с параметрами параметров, как показано ниже.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: Код уведомления IMN_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999326"
---
# <a name="imn_setcompositionwindow-notification-code"></a><span data-ttu-id="6caf7-104">\_Код уведомления ИМН сеткомпоситионвиндов</span><span class="sxs-lookup"><span data-stu-id="6caf7-104">IMN\_SETCOMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="6caf7-105">Уведомляет приложение при обновлении стиля или расположения окна композиции.</span><span class="sxs-lookup"><span data-stu-id="6caf7-105">Notifies an application when the style or position of the composition window is updated.</span></span> <span data-ttu-id="6caf7-106">Приложение получает эту команду через сообщение с [**\_ \_ уведомлением редактора IME WM**](wm-ime-notify.md) с параметрами параметров, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6caf7-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="6caf7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6caf7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6caf7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="6caf7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="6caf7-109">Задайте для параметра значение ИМН \_ сеткомпоситионвиндов.</span><span class="sxs-lookup"><span data-stu-id="6caf7-109">Set to IMN\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="6caf7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6caf7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6caf7-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6caf7-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6caf7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6caf7-112">Return Value</span></span>

<span data-ttu-id="6caf7-113">Эта команда не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6caf7-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6caf7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6caf7-114">Remarks</span></span>

<span data-ttu-id="6caf7-115">Приложение может получать сведения о форме компоновки с помощью команды [**ИМК \_ жеткомпоситионвиндов**](imc-getcompositionwindow.md) .</span><span class="sxs-lookup"><span data-stu-id="6caf7-115">The application can get information about the composition form by using the [**IMC\_GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="6caf7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6caf7-116">Requirements</span></span>



| <span data-ttu-id="6caf7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6caf7-117">Requirement</span></span> | <span data-ttu-id="6caf7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6caf7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6caf7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6caf7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6caf7-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6caf7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6caf7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6caf7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6caf7-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6caf7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6caf7-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6caf7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6caf7-124"><dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6caf7-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6caf7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6caf7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6caf7-126">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="6caf7-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6caf7-127">Команды диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="6caf7-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="6caf7-128">**ИМК \_ жеткомпоситионвиндов**</span><span class="sxs-lookup"><span data-stu-id="6caf7-128">**IMC\_GETCOMPOSITIONWINDOW**</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="6caf7-129">**\_уведомление редактора IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="6caf7-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




