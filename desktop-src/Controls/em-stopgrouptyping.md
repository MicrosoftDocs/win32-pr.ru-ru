---
title: Сообщение EM_STOPGROUPTYPING (RichEdit. h)
description: Останавливает расширенный элемент управления "Правка" для сбора дополнительных действий ввода в текущем действии отмены. Элемент управления сохраняет следующее действие ввода, если оно есть, в новое действие в очереди отмены.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Элементы управления Windows для EM_STOPGROUPTYPING сообщений
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802075"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="8d68e-105">\_Сообщение СТОПГРАУПТИПИНГ EM</span><span class="sxs-lookup"><span data-stu-id="8d68e-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="8d68e-106">Останавливает расширенный элемент управления "Правка" для сбора дополнительных действий ввода в текущем действии отмены.</span><span class="sxs-lookup"><span data-stu-id="8d68e-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="8d68e-107">Элемент управления сохраняет следующее действие ввода, если оно есть, в новое действие в очереди отмены.</span><span class="sxs-lookup"><span data-stu-id="8d68e-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d68e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d68e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d68e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d68e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d68e-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8d68e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8d68e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d68e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d68e-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8d68e-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d68e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d68e-113">Return value</span></span>

<span data-ttu-id="8d68e-114">Возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8d68e-114">The return value is zero.</span></span> <span data-ttu-id="8d68e-115">Это сообщение не может быть выполнено.</span><span class="sxs-lookup"><span data-stu-id="8d68e-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d68e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d68e-116">Remarks</span></span>

<span data-ttu-id="8d68e-117">Форматированный элемент управления "поле ввода" группирует последовательные действия ввода, включая символы, удаленные с помощью клавиши **Backspace** , в одно действие отмены до тех пор, пока не произойдет одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="8d68e-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="8d68e-118">Элемент управления получает сообщение **EM \_ стопграуптипинг** .</span><span class="sxs-lookup"><span data-stu-id="8d68e-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="8d68e-119">Элемент управления теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="8d68e-119">The control loses focus.</span></span>
-   <span data-ttu-id="8d68e-120">Пользователь перемещает выделенный фрагмент с помощью клавиш со стрелками или щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="8d68e-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="8d68e-121">Пользователь нажимает клавишу **Delete** .</span><span class="sxs-lookup"><span data-stu-id="8d68e-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="8d68e-122">Пользователь выполняет любое другое действие, например операцию вставки, в которой **не** участвует ввод.</span><span class="sxs-lookup"><span data-stu-id="8d68e-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="8d68e-123">Сообщение **EM \_ стопграуптипинг** можно отправить для разбиения последовательных действий ввода на меньшие группы отмены.</span><span class="sxs-lookup"><span data-stu-id="8d68e-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="8d68e-124">Например, можно отправить **EM \_ стопграуптипинг** после каждого символа или при каждом разрыве слова.</span><span class="sxs-lookup"><span data-stu-id="8d68e-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d68e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8d68e-125">Requirements</span></span>



| <span data-ttu-id="8d68e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8d68e-126">Requirement</span></span> | <span data-ttu-id="8d68e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8d68e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d68e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d68e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d68e-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d68e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d68e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d68e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d68e-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d68e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d68e-132">Header</span><span class="sxs-lookup"><span data-stu-id="8d68e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d68e-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d68e-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d68e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d68e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d68e-135">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="8d68e-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





