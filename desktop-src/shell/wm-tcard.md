---
description: Отправляется в приложение, которое инициировало обучение с помощью справки Windows.
title: Сообщение WM_TCARD (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264407"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="ff38a-103">\_Сообщение ТКАРД WM</span><span class="sxs-lookup"><span data-stu-id="ff38a-103">WM\_TCARD message</span></span>

<span data-ttu-id="ff38a-104">Отправляется в приложение, которое инициировало обучение с помощью справки Windows.</span><span class="sxs-lookup"><span data-stu-id="ff38a-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="ff38a-105">Сообщение информирует приложение, когда пользователь щелкает настраиваемую кнопку.</span><span class="sxs-lookup"><span data-stu-id="ff38a-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="ff38a-106">Приложение инициирует учебную карточку, указывая \_ команду Help ткард в вызове функции [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .</span><span class="sxs-lookup"><span data-stu-id="ff38a-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff38a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff38a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff38a-108">*идактион*</span><span class="sxs-lookup"><span data-stu-id="ff38a-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="ff38a-109">Значение, указывающее действие, выполненное пользователем.</span><span class="sxs-lookup"><span data-stu-id="ff38a-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="ff38a-110">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ff38a-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="ff38a-111"><span id="IDABORT"></span><span id="idabort"></span>**идаборт**</span><span class="sxs-lookup"><span data-stu-id="ff38a-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-112">Пользователь щелкнул настраиваемую кнопку **прерывания** .</span><span class="sxs-lookup"><span data-stu-id="ff38a-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="ff38a-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**идканцел**</span><span class="sxs-lookup"><span data-stu-id="ff38a-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-114">Пользователь щелкнул настраиваемую кнопку **отмены** .</span><span class="sxs-lookup"><span data-stu-id="ff38a-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="ff38a-115"><span id="IDCLOSE"></span><span id="idclose"></span>**идклосе**</span><span class="sxs-lookup"><span data-stu-id="ff38a-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-116">Пользователь закрыл карточку обучения.</span><span class="sxs-lookup"><span data-stu-id="ff38a-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="ff38a-117"><span id="IDHELP"></span><span id="idhelp"></span>**идхелп**</span><span class="sxs-lookup"><span data-stu-id="ff38a-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-118">Пользователь щелкнул настраиваемую кнопку **справки** Windows.</span><span class="sxs-lookup"><span data-stu-id="ff38a-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="ff38a-119"><span id="IDIGNORE"></span><span id="idignore"></span>**идигноре**</span><span class="sxs-lookup"><span data-stu-id="ff38a-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-120">Пользователь щелкнул кнопку " **пропустить** ", которая является автором.</span><span class="sxs-lookup"><span data-stu-id="ff38a-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="ff38a-121"><span id="IDOK"></span><span id="idok"></span>**идок**</span><span class="sxs-lookup"><span data-stu-id="ff38a-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-122">Пользователь щелкнул настраиваемую кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="ff38a-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="ff38a-123"><span id="IDNO"></span><span id="idno"></span>**идно**</span><span class="sxs-lookup"><span data-stu-id="ff38a-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-124">Пользователь щелкнул элемент "Автор" **без** кнопки.</span><span class="sxs-lookup"><span data-stu-id="ff38a-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="ff38a-125"><span id="IDRETRY"></span><span id="idretry"></span>**идретри**</span><span class="sxs-lookup"><span data-stu-id="ff38a-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-126">Пользователь щелкнул настраиваемую кнопку **повтора** .</span><span class="sxs-lookup"><span data-stu-id="ff38a-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="ff38a-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**Справка \_ ткард \_ данных**</span><span class="sxs-lookup"><span data-stu-id="ff38a-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-128">Пользователь щелкнул настраиваемую кнопку.</span><span class="sxs-lookup"><span data-stu-id="ff38a-128">The user clicked an authorable button.</span></span> <span data-ttu-id="ff38a-129">Параметр *двактиондата* содержит длинное целое число, заданное автором справки.</span><span class="sxs-lookup"><span data-stu-id="ff38a-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="ff38a-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**Помогите \_ ткард \_ другим \_ вызывающим**</span><span class="sxs-lookup"><span data-stu-id="ff38a-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-131">Другое приложение запросило карточки обучения.</span><span class="sxs-lookup"><span data-stu-id="ff38a-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="ff38a-132"><span id="IDYES"></span><span id="idyes"></span>**идес**</span><span class="sxs-lookup"><span data-stu-id="ff38a-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="ff38a-133">Пользователь щелкнул настраиваемую кнопку **Да** .</span><span class="sxs-lookup"><span data-stu-id="ff38a-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ff38a-134">*двактиондата*</span><span class="sxs-lookup"><span data-stu-id="ff38a-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="ff38a-135">Если *идактион* указывает Help \_ ткард \_ Data, этот параметр является **длинным** , заданным автором справки.</span><span class="sxs-lookup"><span data-stu-id="ff38a-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="ff38a-136">В противном случае этот параметр равен нулю.</span><span class="sxs-lookup"><span data-stu-id="ff38a-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff38a-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff38a-137">Return value</span></span>

<span data-ttu-id="ff38a-138">Возвращаемое значение игнорируется; Используйте нуль.</span><span class="sxs-lookup"><span data-stu-id="ff38a-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff38a-139">Требования</span><span class="sxs-lookup"><span data-stu-id="ff38a-139">Requirements</span></span>



| <span data-ttu-id="ff38a-140">Требование</span><span class="sxs-lookup"><span data-stu-id="ff38a-140">Requirement</span></span> | <span data-ttu-id="ff38a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="ff38a-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff38a-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff38a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ff38a-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ff38a-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ff38a-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff38a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ff38a-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff38a-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff38a-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff38a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff38a-147"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff38a-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 




