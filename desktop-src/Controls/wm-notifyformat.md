---
title: Сообщение WM_NOTIFYFORMAT (Winuser. h)
description: Определяет, принимает ли окно структуры ANSI или Unicode в \_ сообщении уведомления WM notify. \_Сообщения WM нотифиформат отправляются из общего элемента управления в родительское окно и из родительского окна в общий элемент управления.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Элементы управления Windows для WM_NOTIFYFORMAT сообщений
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988897"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="c8dfd-105">\_Сообщение НОТИФИФОРМАТ WM</span><span class="sxs-lookup"><span data-stu-id="c8dfd-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="c8dfd-106">Определяет, принимает ли окно структуры ANSI или Unicode в сообщении уведомления [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="c8dfd-107">**WM \_ Сообщения НОТИФИФОРМАТ** отправляются из общего элемента управления в его родительское окно и из родительского окна в общий элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8dfd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8dfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8dfd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8dfd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8dfd-110">Маркер окна, отправляющего сообщение **WM \_ нотифиформат** .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="c8dfd-111">Если аргумент *lParam* имеет значение NF \_ Query, этот параметр является маркером элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="c8dfd-112">Если аргумент *lParam* имеет значение NF \_ Requery, этот параметр является маркером родительского окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="c8dfd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8dfd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8dfd-114">Значение команды, указывающее природу сообщения **WM \_ нотифиформат** .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="c8dfd-115">Это может быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c8dfd-115">This will be one of the following values:</span></span>



| <span data-ttu-id="c8dfd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c8dfd-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="c8dfd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c8dfd-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="c8dfd-118"><dt>**\_запрос NF**</dt></span><span class="sxs-lookup"><span data-stu-id="c8dfd-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="c8dfd-119">Сообщение — это запрос, позволяющий определить, следует ли использовать структуры ANSI или Unicode в сообщениях [**\_ уведомления WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c8dfd-120">Эта команда отправляется из элемента управления в родительское окно во время создания элемента управления и в ответ на \_ команду NF Requery.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="c8dfd-121"><dt>**NF \_ Requery**</dt></span><span class="sxs-lookup"><span data-stu-id="c8dfd-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="c8dfd-122">Сообщение является запросом элемента управления на отправку \_ формы запроса NF этого сообщения родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="c8dfd-123">Эта команда отправляется из родительского окна.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-123">This command is sent from the parent window.</span></span> <span data-ttu-id="c8dfd-124">Родительское окно запрашивает у элемента управления, чтобы запросить тип структур для использования в сообщениях [**\_ уведомления WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c8dfd-125">Если параметр *lParam* — NF \_ Requery, возвращаемое значение является результатом операции Requery.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8dfd-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8dfd-126">Return value</span></span>

<span data-ttu-id="c8dfd-127">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-127">Returns one of the following values.</span></span>



| <span data-ttu-id="c8dfd-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c8dfd-128">Return code</span></span>                                                                                 | <span data-ttu-id="c8dfd-129">Описание</span><span class="sxs-lookup"><span data-stu-id="c8dfd-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8dfd-130"><dt>**NFR \_ ANSI**</dt></span><span class="sxs-lookup"><span data-stu-id="c8dfd-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="c8dfd-131">Структуры ANSI следует использовать в сообщениях [**WM \_ Notify**](wm-notify.md) , отправленных элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="c8dfd-132"><dt>**NFR \_ Юникод**</dt></span><span class="sxs-lookup"><span data-stu-id="c8dfd-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="c8dfd-133">Структуры Юникода следует использовать в сообщениях [**WM \_ Notify**](wm-notify.md) , отправленных элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="c8dfd-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c8dfd-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="c8dfd-135">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="c8dfd-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8dfd-136">Remarks</span></span>

<span data-ttu-id="c8dfd-137">При создании общего элемента управления элемент управления отправляет сообщение **WM \_ нотифиформат** в свое родительское окно, чтобы определить тип структур, используемых в сообщениях [**\_ уведомления WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c8dfd-138">Если родительское окно не обрабатывает это сообщение, функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) реагирует в соответствии с типом родительского окна.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="c8dfd-139">То есть, если родительское окно является окном Юникода, **дефвиндовпрок** ВОЗВРАЩАЕТ значение NFR \_ Unicode, а если родительское окно является окном ANSI, **дефвиндовпрок** возвращает значение NFR \_ ANSI.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="c8dfd-140">Если родительское окно является диалоговым и не обрабатывает это сообщение, функция [**дефдлгпрок**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) будет реагировать в соответствии с типом диалогового окна (Юникод или ANSI).</span><span class="sxs-lookup"><span data-stu-id="c8dfd-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="c8dfd-141">Родительское окно может изменить тип структур, используемых стандартным элементом управления в сообщениях [**WM \_ Notify**](wm-notify.md) , установив параметр *lParam* в NF \_ Requery и отправив сообщение **WM \_ нотифиформат** в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="c8dfd-142">Это приводит к тому, что элемент управления отправляет \_ форму запроса NF формы **WM \_ нотифиформат** в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="c8dfd-143">Все стандартные элементы управления отправляют сообщения **WM \_ нотифиформат** .</span><span class="sxs-lookup"><span data-stu-id="c8dfd-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="c8dfd-144">Однако стандартные элементы управления Windows (элементы управления "поле ввода", поля со списком, списки, кнопки, полосы прокрутки и статические элементы управления) не имеют.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8dfd-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c8dfd-145">Requirements</span></span>



| <span data-ttu-id="c8dfd-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c8dfd-146">Requirement</span></span> | <span data-ttu-id="c8dfd-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c8dfd-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8dfd-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8dfd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c8dfd-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8dfd-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c8dfd-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8dfd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c8dfd-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8dfd-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c8dfd-152">Header</span><span class="sxs-lookup"><span data-stu-id="c8dfd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8dfd-153"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8dfd-153"><dt>Winuser.h</dt></span></span> </dl> |



 

