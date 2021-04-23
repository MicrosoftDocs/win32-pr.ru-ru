---
title: Сообщение TDM_NAVIGATE_PAGE (Коммктрл. h)
description: Повторно создает диалоговое окно задачи с новым содержимым, имитируя функциональные возможности многостраничного мастера.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- Элементы управления Windows для TDM_NAVIGATE_PAGE сообщений
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989284"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="f2253-104">TDM \_ переходить к \_ сообщению страницы</span><span class="sxs-lookup"><span data-stu-id="f2253-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="f2253-105">Повторно создает диалоговое окно задачи с новым содержимым, имитируя функциональные возможности многостраничного мастера.</span><span class="sxs-lookup"><span data-stu-id="f2253-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2253-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2253-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2253-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2253-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2253-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f2253-108">Not used.</span></span> <span data-ttu-id="f2253-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f2253-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2253-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2253-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2253-111">Указатель на структуру [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , описывающую создаваемое диалоговое окно задачи.</span><span class="sxs-lookup"><span data-stu-id="f2253-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="f2253-112">Вызывающее приложение должно выделить эту структуру и задать ее члены.</span><span class="sxs-lookup"><span data-stu-id="f2253-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="f2253-113">Значения элементов зависят от типа страницы, к которой осуществляется переход.</span><span class="sxs-lookup"><span data-stu-id="f2253-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2253-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2253-114">Return value</span></span>

<span data-ttu-id="f2253-115">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f2253-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2253-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2253-116">Remarks</span></span>

<span data-ttu-id="f2253-117">Чтобы запустить диалоговое окно задачи мастера, используйте функцию [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="f2253-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="f2253-118">По мере того, как пользователь переходит с помощью мастера, отправьте это сообщение в диалоговое окно задачи, чтобы отобразить следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="f2253-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="f2253-119">Создается новое диалоговое окно задачи (выглядит как новая страница) с элементами, указанными в структуре, на которую указывает *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f2253-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="f2253-120">При создании все содержимое диалогового окна уничтожается и реконструируется.</span><span class="sxs-lookup"><span data-stu-id="f2253-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="f2253-121">В результате теряются все сведения о состоянии, удерживаемые элементами управления (например, индикатор выполнения, кнопка "expando" или "Проверка") в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f2253-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="f2253-122">Макет диалогового окна задачи может завершиться ошибкой, и это может не отражаться в возвращаемом значении.</span><span class="sxs-lookup"><span data-stu-id="f2253-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="f2253-123">Возвращаемое значение S " \_ ОК" отражает только то, что диалоговое окно задачи получило сообщение и попыталось обработать его.</span><span class="sxs-lookup"><span data-stu-id="f2253-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="f2253-124">Если происходит сбой макета диалогового окна задачи (диалоговое окно задачи не может быть отображено), диалоговое окно закроется и в зарегистрированной функции обратного вызова будет возвращен код **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2253-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="f2253-125">Дополнительные сведения о синтаксисе функции обратного вызова см. в разделе [*таскдиалогкаллбаккпрок*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="f2253-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2253-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f2253-126">Requirements</span></span>



| <span data-ttu-id="f2253-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f2253-127">Requirement</span></span> | <span data-ttu-id="f2253-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f2253-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2253-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2253-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2253-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2253-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2253-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2253-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2253-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2253-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2253-133">Header</span><span class="sxs-lookup"><span data-stu-id="f2253-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2253-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2253-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

