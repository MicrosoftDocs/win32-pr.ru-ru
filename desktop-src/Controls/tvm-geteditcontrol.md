---
title: Сообщение TVM_GETEDITCONTROL (Коммктрл. h)
description: Получает маркер элемента управления "поле ввода", используемый для изменения текста элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса Жетедитконтрол TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Элементы управления Windows для TVM_GETEDITCONTROL сообщений
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137419"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="e3910-105">\_Сообщение TVM жетедитконтрол</span><span class="sxs-lookup"><span data-stu-id="e3910-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="e3910-106">Получает маркер элемента управления "поле ввода", используемый для изменения текста элемента представления дерева.</span><span class="sxs-lookup"><span data-stu-id="e3910-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="e3910-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетедитконтрол TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="e3910-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3910-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3910-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3910-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e3910-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e3910-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e3910-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3910-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e3910-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e3910-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3910-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3910-113">Return value</span></span>

<span data-ttu-id="e3910-114">Возвращает маркер в элемент управления "поле ввода", если он успешно, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e3910-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3910-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3910-115">Remarks</span></span>

<span data-ttu-id="e3910-116">Когда начинается редактирование метки, элемент управления "Правка" создается, но не размещается или не отображается.</span><span class="sxs-lookup"><span data-stu-id="e3910-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="e3910-117">Перед отображением элемент управления иерархического представления отправляет родительскому окну код уведомления [ТВН \_ бегинлабеледит](tvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="e3910-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="e3910-118">Чтобы настроить редактирование меток, реализуйте обработчик для [ТВН \_ бегинлабеледит](tvn-beginlabeledit.md) и отправьте сообщение **TVM \_ жетедитконтрол** в элемент управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="e3910-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="e3910-119">Если метка редактируется, возвращаемое значение будет обработано элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e3910-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="e3910-120">Используйте этот маркер для настройки элемента управления "поле ввода", отправляя обычные сообщения **EM \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="e3910-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3910-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e3910-121">Requirements</span></span>



| <span data-ttu-id="e3910-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e3910-122">Requirement</span></span> | <span data-ttu-id="e3910-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e3910-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3910-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3910-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3910-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3910-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3910-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3910-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3910-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3910-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3910-128">Header</span><span class="sxs-lookup"><span data-stu-id="e3910-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3910-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3910-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





