---
title: Сообщение EM_GETHANDLE (Winuser. h)
description: Возвращает маркер памяти, выделенной в данный момент для текста элемента управления многострочного редактирования.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- Элементы управления Windows для EM_GETHANDLE сообщений
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534685"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="7d09c-104">\_Сообщение EM</span><span class="sxs-lookup"><span data-stu-id="7d09c-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="7d09c-105">Возвращает маркер памяти, выделенной в данный момент для текста элемента управления многострочного редактирования.</span><span class="sxs-lookup"><span data-stu-id="7d09c-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d09c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d09c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d09c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d09c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d09c-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d09c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d09c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d09c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d09c-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d09c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d09c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d09c-111">Return value</span></span>

<span data-ttu-id="7d09c-112">Возвращаемое значение — это маркер памяти, идентифицирующий буфер, в котором содержится содержимое элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="7d09c-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="7d09c-113">Если возникает ошибка, например Отправка сообщения в однострочный элемент управления Edit, то возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d09c-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d09c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d09c-114">Remarks</span></span>

<span data-ttu-id="7d09c-115">Если функция завершается успешно, приложение может получить доступ к содержимому элемента управления "поле ввода" путем приведения возвращаемого значения к [**хлокал**](/windows/desktop/WinProg/windows-data-types) и передачи его в [**локаллокк**](/windows/desktop/api/winbase/nf-winbase-locallock).</span><span class="sxs-lookup"><span data-stu-id="7d09c-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="7d09c-116">**Локаллокк** возвращает указатель на буфер, который является массивом **char** s или **WCHAR**, завершающимся нулем, в зависимости от того, создал ли элемент управления функцию ANSI или Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d09c-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="7d09c-117">Например, если используется [**креатевиндовекса**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , буфер является массивом **символов** s, но если **креатевиндовексв** использовался, буфер является массивом типа **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="7d09c-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="7d09c-118">Приложение может не изменять содержимое буфера.</span><span class="sxs-lookup"><span data-stu-id="7d09c-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="7d09c-119">Чтобы разблокировать буфер, приложение вызывает [**локалунлокк**](/windows/desktop/api/winbase/nf-winbase-localunlock) , прежде чем разрешить элементу управления "поле ввода" получать новые сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d09c-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="7d09c-120">Для Comctl32.dll версии 6 буфер всегда содержит массив типа **WCHAR**, независимо от того, создал ли элемент управления "поле ввода" функцию ANSI или Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d09c-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="7d09c-121">Дополнительные сведения о версиях DLL см. в разделе [общие версии элементов управления](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7d09c-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="7d09c-122">Если приложение не может соблюдать ограничения, накладываемые методом EM, используйте функции [**жетвиндовтекстленгс**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) и [**жетвиндовтекст**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) , чтобы скопировать содержимое элемента управления "поле ввода" в буфер, предоставленный приложением. **\_**</span><span class="sxs-lookup"><span data-stu-id="7d09c-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="7d09c-123">**Расширенное редактирование:** Сообщение **EM- \_ Handle** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d09c-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="7d09c-124">Элементы управления Rich Edit не хранят текст как простой массив символов.</span><span class="sxs-lookup"><span data-stu-id="7d09c-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d09c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7d09c-125">Requirements</span></span>



| <span data-ttu-id="7d09c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7d09c-126">Requirement</span></span> | <span data-ttu-id="7d09c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7d09c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d09c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d09c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d09c-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d09c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d09c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d09c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d09c-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d09c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d09c-132">Header</span><span class="sxs-lookup"><span data-stu-id="7d09c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d09c-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d09c-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d09c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d09c-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d09c-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7d09c-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d09c-136">**EM \_ сесандле**</span><span class="sxs-lookup"><span data-stu-id="7d09c-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="7d09c-137">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="7d09c-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7d09c-138">**жетвиндовтекст**</span><span class="sxs-lookup"><span data-stu-id="7d09c-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="7d09c-139">**жетвиндовтекстленгс**</span><span class="sxs-lookup"><span data-stu-id="7d09c-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="7d09c-140">**локаллокк**</span><span class="sxs-lookup"><span data-stu-id="7d09c-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="7d09c-141">**локалунлокк**</span><span class="sxs-lookup"><span data-stu-id="7d09c-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

