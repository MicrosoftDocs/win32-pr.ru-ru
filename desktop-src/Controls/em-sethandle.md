---
title: Сообщение EM_SETHANDLE (Winuser. h)
description: Задает маркер памяти, который будет использоваться многострочным элементом управления "поле ввода".
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Элементы управления Windows для EM_SETHANDLE сообщений
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137162"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="abdd4-104">\_Сообщение СЕСАНДЛЕ EM</span><span class="sxs-lookup"><span data-stu-id="abdd4-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="abdd4-105">Задает маркер памяти, который будет использоваться многострочным элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="abdd4-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="abdd4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="abdd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abdd4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abdd4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abdd4-108">Обработчик буфера памяти, используемый элементом управления "поле ввода" для хранения отображаемого текста вместо выделения собственной памяти.</span><span class="sxs-lookup"><span data-stu-id="abdd4-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="abdd4-109">При необходимости элемент управления перераспределяет память.</span><span class="sxs-lookup"><span data-stu-id="abdd4-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="abdd4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abdd4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abdd4-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="abdd4-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abdd4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abdd4-112">Return value</span></span>

<span data-ttu-id="abdd4-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="abdd4-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abdd4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abdd4-114">Remarks</span></span>

<span data-ttu-id="abdd4-115">Прежде чем приложение установит новый обработчик памяти, оно должно отправить сообщение [**EM- \_ Handle**](em-gethandle.md) для получения маркера текущего буфера памяти и освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="abdd4-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="abdd4-116">Элемент управления "поле ввода" автоматически перераспределяет заданный буфер каждый раз, когда ему требуется дополнительное пространство для текста, или удаляет достаточно текста, чтобы дополнительное пространство больше не нужно.</span><span class="sxs-lookup"><span data-stu-id="abdd4-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="abdd4-117">При отправке сообщения **EM \_ сесандле** очищается буфер отмены ([**EM \_ канундо**](em-canundo.md) возвращает ноль), а внутренний флаг изменения ([**EM- \_ изменения**](em-getmodify.md) возвращает ноль).</span><span class="sxs-lookup"><span data-stu-id="abdd4-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="abdd4-118">Окно элемента управления редактирования перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="abdd4-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="abdd4-119">**Расширенное редактирование:** Сообщение **EM \_ сесандле** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="abdd4-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="abdd4-120">Элементы управления Rich Edit не хранят текст как простой массив символов.</span><span class="sxs-lookup"><span data-stu-id="abdd4-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="abdd4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="abdd4-121">Requirements</span></span>



| <span data-ttu-id="abdd4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="abdd4-122">Requirement</span></span> | <span data-ttu-id="abdd4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="abdd4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abdd4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abdd4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="abdd4-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abdd4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="abdd4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abdd4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="abdd4-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="abdd4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abdd4-128">Header</span><span class="sxs-lookup"><span data-stu-id="abdd4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="abdd4-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abdd4-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abdd4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abdd4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="abdd4-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="abdd4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="abdd4-132">**EM \_ канундо**</span><span class="sxs-lookup"><span data-stu-id="abdd4-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="abdd4-133">**EM \_**</span><span class="sxs-lookup"><span data-stu-id="abdd4-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="abdd4-134">**EM, \_ изменение**</span><span class="sxs-lookup"><span data-stu-id="abdd4-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 





