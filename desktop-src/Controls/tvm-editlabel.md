---
title: Сообщение TVM_EDITLABEL (Коммктрл. h)
description: Начинает редактирование текста указанного элемента на месте, заменяя текст элемента однострочным элементом управления "поле ввода", содержащим текст.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Элементы управления Windows для TVM_EDITLABEL сообщений
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988469"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="330ff-104">\_Сообщение TVM едитлабел</span><span class="sxs-lookup"><span data-stu-id="330ff-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="330ff-105">Начинает редактирование текста указанного элемента на месте, заменяя текст элемента однострочным элементом управления "поле ввода", содержащим текст.</span><span class="sxs-lookup"><span data-stu-id="330ff-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="330ff-106">Это сообщение неявно выбирает и фокусируется на указанном элементе.</span><span class="sxs-lookup"><span data-stu-id="330ff-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="330ff-107">Это сообщение можно отправить явно или с помощью макроса [**\_ едитлабел TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="330ff-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="330ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="330ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="330ff-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="330ff-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="330ff-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="330ff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="330ff-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="330ff-112">Обрабатываемый элемент для изменения.</span><span class="sxs-lookup"><span data-stu-id="330ff-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330ff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="330ff-113">Return value</span></span>

<span data-ttu-id="330ff-114">Возвращает маркер для элемента управления "поле ввода", используемый для изменения текста элемента при его успешном выполнении, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="330ff-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="330ff-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="330ff-115">Remarks</span></span>

<span data-ttu-id="330ff-116">Это сообщение отправляет код уведомления [ТВН \_ бегинлабеледит](tvn-beginlabeledit.md) в родительский элемент элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="330ff-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="330ff-117">Когда пользователь завершает или отменяет редактирование, элемент управления "поле ввода" уничтожается и маркер становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="330ff-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="330ff-118">Можно создать подкласс элемента управления "поле ввода", но не уничтожать его.</span><span class="sxs-lookup"><span data-stu-id="330ff-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="330ff-119">Элемент управления должен иметь фокус перед отправкой этого сообщения элементу управления.</span><span class="sxs-lookup"><span data-stu-id="330ff-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="330ff-120">Фокус можно задать с помощью функции [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="330ff-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="330ff-121">Требования</span><span class="sxs-lookup"><span data-stu-id="330ff-121">Requirements</span></span>



| <span data-ttu-id="330ff-122">Требование</span><span class="sxs-lookup"><span data-stu-id="330ff-122">Requirement</span></span> | <span data-ttu-id="330ff-123">Значение</span><span class="sxs-lookup"><span data-stu-id="330ff-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="330ff-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="330ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="330ff-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="330ff-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="330ff-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="330ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="330ff-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="330ff-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="330ff-128">Header</span><span class="sxs-lookup"><span data-stu-id="330ff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="330ff-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="330ff-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="330ff-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="330ff-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="330ff-131">**TVM \_ ЕДИТЛАБЕЛВ** (Юникод) и **TVM \_ едитлабела** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="330ff-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 

