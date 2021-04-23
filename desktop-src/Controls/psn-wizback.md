---
title: Код уведомления PSN_WIZBACK (Пршт. h)
description: Уведомляет страницу о том, что пользователь щелкнул кнопку назад в мастере. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 784f92e7-6f10-40fc-b513-bea022f13ae1
keywords:
- PSN_WIZBACK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_WIZBACK
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed1cdd742d78473266db07899796de5a5450310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891414"
---
# <a name="psn_wizback-notification-code"></a><span data-ttu-id="f8e92-105">\_Код уведомления PSN визбакк</span><span class="sxs-lookup"><span data-stu-id="f8e92-105">PSN\_WIZBACK notification code</span></span>

<span data-ttu-id="f8e92-106">Уведомляет страницу о том, что пользователь щелкнул кнопку **назад** в мастере.</span><span class="sxs-lookup"><span data-stu-id="f8e92-106">Notifies a page that the user has clicked the **Back** button in a wizard.</span></span> <span data-ttu-id="f8e92-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f8e92-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZBACK 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f8e92-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8e92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e92-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8e92-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8e92-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="f8e92-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="f8e92-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f8e92-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="f8e92-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="f8e92-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e92-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8e92-113">Return value</span></span>

<span data-ttu-id="f8e92-114">Возвращает значение 0, чтобы разрешить мастеру переходить на предыдущую страницу.</span><span class="sxs-lookup"><span data-stu-id="f8e92-114">Returns 0 to allow the wizard to go to the previous page.</span></span> <span data-ttu-id="f8e92-115">Возвращает значение-1, чтобы мастер не изменял страницы.</span><span class="sxs-lookup"><span data-stu-id="f8e92-115">Returns -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="f8e92-116">Чтобы отобразить определенную страницу, возвращается идентификатор ее ресурса диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f8e92-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="f8e92-117">Если диалоговое окно было указано с флагом [**PSP \_ длгиндирект**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , это уведомление возвращает указатель на шаблон диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f8e92-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8e92-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8e92-118">Remarks</span></span>

<span data-ttu-id="f8e92-119">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) со значением **DWL \_ Мсгресулт** и вернуть значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f8e92-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="f8e92-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="f8e92-120">For example:</span></span>

``` syntax
case PSN_WIZBACK :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZNEXT :
    ...
```

> [!Note]  
> <span data-ttu-id="f8e92-121">Страница свойств находится в процессе управления списком страниц при \_ отправке кода уведомления PSN визбакк.</span><span class="sxs-lookup"><span data-stu-id="f8e92-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZBACK notification code is sent.</span></span> <span data-ttu-id="f8e92-122">В ответ на эти коды уведомлений можно добавлять, вставлять или удалять страницы, но при вставке или удалении страниц перед текущей страницей необходимо учитывать особое внимание.</span><span class="sxs-lookup"><span data-stu-id="f8e92-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="f8e92-123">При вставке или удалении страниц перед текущей страницей необходимо вернуть (до **DWL \_ мсгресулт**) ненулевое значение, чтобы указать нужную новую страницу.</span><span class="sxs-lookup"><span data-stu-id="f8e92-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="f8e92-124">Однако обратите внимание, что при вставке или удалении страницы, расположенной перед текущей страницей (с меньшим индексом, чем текущая страница), [PSN \_ киллактиве](psn-killactive.md) может быть отправлен на неправильную страницу.</span><span class="sxs-lookup"><span data-stu-id="f8e92-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="f8e92-125">По этой причине рекомендуется, чтобы мастера, которые динамически добавляют и удаляют страницы в ответ на [PSN \_ ВИЗНЕКСТ](psn-wiznext.md) и PSN \_ визбакк, могли делать это только на страницах в конце списка.</span><span class="sxs-lookup"><span data-stu-id="f8e92-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to [PSN\_WIZNEXT](psn-wiznext.md) and PSN\_WIZBACK do so only to pages at the end of the list.</span></span> <span data-ttu-id="f8e92-126">Если вы хотите, чтобы мастер удалил страницы точно, сохраните динамические страницы в конце списка и вернитесь к постоянным страницам, прежде чем удалять их.</span><span class="sxs-lookup"><span data-stu-id="f8e92-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="f8e92-127">Например, предположим, что мастер состоит из вводной страницы, серии динамических страниц и страницы завершения, и вы хотите удалить динамические страницы, когда пользователь достигнет страницы завершения.</span><span class="sxs-lookup"><span data-stu-id="f8e92-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="f8e92-128">Мастер начнет работу с двумя страницами: «введение» и «завершение».</span><span class="sxs-lookup"><span data-stu-id="f8e92-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="f8e92-129">Пользователь начинает со страницы "Введение".</span><span class="sxs-lookup"><span data-stu-id="f8e92-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="f8e92-130">Введение (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="f8e92-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="f8e92-131">Completion</span><span class="sxs-lookup"><span data-stu-id="f8e92-131">Completion</span></span>
2.  <span data-ttu-id="f8e92-132">Когда пользователь выходит из "введения", мастер добавляет динамические страницы и помещает пользователя на первую динамическую страницу, возвращая (до **DWL \_ мсгресулт**) идентификатор диалога для страницы "Dynamic 1".</span><span class="sxs-lookup"><span data-stu-id="f8e92-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="f8e92-133">В этом примере есть три динамические страницы.</span><span class="sxs-lookup"><span data-stu-id="f8e92-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="f8e92-134">Введение</span><span class="sxs-lookup"><span data-stu-id="f8e92-134">Introduction</span></span>
    2.  <span data-ttu-id="f8e92-135">Completion</span><span class="sxs-lookup"><span data-stu-id="f8e92-135">Completion</span></span>
    3.  <span data-ttu-id="f8e92-136">Динамический 1 (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="f8e92-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="f8e92-137">Динамический 2</span><span class="sxs-lookup"><span data-stu-id="f8e92-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="f8e92-138">Динамический 3</span><span class="sxs-lookup"><span data-stu-id="f8e92-138">Dynamic 3</span></span>
3.  <span data-ttu-id="f8e92-139">После того как пользователь перейдет по динамическим страницам в "Dynamic 3", а затем перейдет к следующей странице, приложение должно поместить пользователя на страницу "завершение".</span><span class="sxs-lookup"><span data-stu-id="f8e92-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="f8e92-140">Опять же, это делается путем возврата (до **DWL \_ мсгресулт**) идентификатора диалогового окна "завершение".</span><span class="sxs-lookup"><span data-stu-id="f8e92-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="f8e92-141">Введение</span><span class="sxs-lookup"><span data-stu-id="f8e92-141">Introduction</span></span>
    2.  <span data-ttu-id="f8e92-142">Завершение (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="f8e92-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="f8e92-143">Динамический 1</span><span class="sxs-lookup"><span data-stu-id="f8e92-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="f8e92-144">Динамический 2</span><span class="sxs-lookup"><span data-stu-id="f8e92-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="f8e92-145">Динамический 3</span><span class="sxs-lookup"><span data-stu-id="f8e92-145">Dynamic 3</span></span>
4.  <span data-ttu-id="f8e92-146">Затем приложение может безопасно удалить три динамические страницы (с номерами от трех до пяти).</span><span class="sxs-lookup"><span data-stu-id="f8e92-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="f8e92-147">Введение</span><span class="sxs-lookup"><span data-stu-id="f8e92-147">Introduction</span></span>
    2.  <span data-ttu-id="f8e92-148">Завершение (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="f8e92-148">Completion (User is here)</span></span>

<span data-ttu-id="f8e92-149">Обратите внимание, что этот метод необходим только в том случае, если мастер удаляет страницы динамически.</span><span class="sxs-lookup"><span data-stu-id="f8e92-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="f8e92-150">Если мастер добавляет только страницы динамически, этот процесс не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f8e92-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e92-151">Требования</span><span class="sxs-lookup"><span data-stu-id="f8e92-151">Requirements</span></span>



| <span data-ttu-id="f8e92-152">Требование</span><span class="sxs-lookup"><span data-stu-id="f8e92-152">Requirement</span></span> | <span data-ttu-id="f8e92-153">Значение</span><span class="sxs-lookup"><span data-stu-id="f8e92-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e92-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8e92-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e92-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8e92-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8e92-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8e92-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e92-157">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8e92-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8e92-158">Header</span><span class="sxs-lookup"><span data-stu-id="f8e92-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e92-159"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e92-159"><dt>Prsht.h</dt></span></span> </dl> |



 

