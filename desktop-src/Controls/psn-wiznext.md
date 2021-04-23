---
title: Код уведомления PSN_WIZNEXT (Пршт. h)
description: Уведомляет страницу о нажатии пользователем кнопки "Далее" в мастере. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654570"
---
# <a name="psn_wiznext-notification-code"></a><span data-ttu-id="328d0-105">\_Код уведомления PSN визнекст</span><span class="sxs-lookup"><span data-stu-id="328d0-105">PSN\_WIZNEXT notification code</span></span>

<span data-ttu-id="328d0-106">Уведомляет страницу о нажатии пользователем кнопки " **Далее** " в мастере.</span><span class="sxs-lookup"><span data-stu-id="328d0-106">Notifies a page that the user has clicked the **Next** button in a wizard.</span></span> <span data-ttu-id="328d0-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="328d0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="328d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="328d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="328d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="328d0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="328d0-110">Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="328d0-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="328d0-111">Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="328d0-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="328d0-112">Член **lParam** структуры **пшнотифи** не содержит никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="328d0-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="328d0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="328d0-113">Return value</span></span>

<span data-ttu-id="328d0-114">Возвращает значение 0, чтобы разрешить мастеру переходить на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="328d0-114">Return 0 to allow the wizard to go to the next page.</span></span> <span data-ttu-id="328d0-115">Возвращает значение-1, чтобы мастер не изменял страницы.</span><span class="sxs-lookup"><span data-stu-id="328d0-115">Return -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="328d0-116">Чтобы отобразить определенную страницу, возвращается идентификатор ее ресурса диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="328d0-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="328d0-117">Если диалоговое окно было указано с флагом [**PSP \_ длгиндирект**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , это уведомление возвращает указатель на шаблон диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="328d0-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="328d0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="328d0-118">Remarks</span></span>

<span data-ttu-id="328d0-119">Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) со значением **DWL \_ Мсгресулт** и вернуть значение **true**.</span><span class="sxs-lookup"><span data-stu-id="328d0-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="328d0-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="328d0-120">For example:</span></span>

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> <span data-ttu-id="328d0-121">Страница свойств находится в процессе управления списком страниц при \_ отправке кода уведомления PSN визнекст.</span><span class="sxs-lookup"><span data-stu-id="328d0-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZNEXT notification code is sent.</span></span> <span data-ttu-id="328d0-122">В ответ на эти коды уведомлений можно добавлять, вставлять или удалять страницы, но при вставке или удалении страниц перед текущей страницей необходимо учитывать особое внимание.</span><span class="sxs-lookup"><span data-stu-id="328d0-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="328d0-123">При вставке или удалении страниц перед текущей страницей необходимо вернуть (до **DWL \_ мсгресулт**) ненулевое значение, чтобы указать нужную новую страницу.</span><span class="sxs-lookup"><span data-stu-id="328d0-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="328d0-124">Однако обратите внимание, что при вставке или удалении страницы, расположенной перед текущей страницей (с меньшим индексом, чем текущая страница), [PSN \_ киллактиве](psn-killactive.md) может быть отправлен на неправильную страницу.</span><span class="sxs-lookup"><span data-stu-id="328d0-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="328d0-125">По этой причине рекомендуется, чтобы мастера, которые динамически добавляют и удаляют страницы в ответ на PSN \_ визнекст и [PSN \_ визбакк](psn-wizback.md) , могли делать это только на страницах в конце списка.</span><span class="sxs-lookup"><span data-stu-id="328d0-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to PSN\_WIZNEXT and [PSN\_WIZBACK](psn-wizback.md) do so only to pages at the end of the list.</span></span> <span data-ttu-id="328d0-126">Если вы хотите, чтобы мастер удалил страницы точно, сохраните динамические страницы в конце списка и вернитесь к постоянным страницам, прежде чем удалять их.</span><span class="sxs-lookup"><span data-stu-id="328d0-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="328d0-127">Например, предположим, что мастер состоит из вводной страницы, серии динамических страниц и страницы завершения, и вы хотите удалить динамические страницы, когда пользователь достигнет страницы завершения.</span><span class="sxs-lookup"><span data-stu-id="328d0-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="328d0-128">Мастер начнет работу с двумя страницами: «введение» и «завершение».</span><span class="sxs-lookup"><span data-stu-id="328d0-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="328d0-129">Пользователь начинает со страницы "Введение".</span><span class="sxs-lookup"><span data-stu-id="328d0-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="328d0-130">Введение (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="328d0-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="328d0-131">Completion</span><span class="sxs-lookup"><span data-stu-id="328d0-131">Completion</span></span>
2.  <span data-ttu-id="328d0-132">Когда пользователь выходит из "введения", мастер добавляет динамические страницы и помещает пользователя на первую динамическую страницу, возвращая (до **DWL \_ мсгресулт**) идентификатор диалога для страницы "Dynamic 1".</span><span class="sxs-lookup"><span data-stu-id="328d0-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="328d0-133">В этом примере есть три динамические страницы.</span><span class="sxs-lookup"><span data-stu-id="328d0-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="328d0-134">Введение</span><span class="sxs-lookup"><span data-stu-id="328d0-134">Introduction</span></span>
    2.  <span data-ttu-id="328d0-135">Completion</span><span class="sxs-lookup"><span data-stu-id="328d0-135">Completion</span></span>
    3.  <span data-ttu-id="328d0-136">Динамический 1 (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="328d0-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="328d0-137">Динамический 2</span><span class="sxs-lookup"><span data-stu-id="328d0-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="328d0-138">Динамический 3</span><span class="sxs-lookup"><span data-stu-id="328d0-138">Dynamic 3</span></span>
3.  <span data-ttu-id="328d0-139">После того как пользователь перейдет по динамическим страницам в "Dynamic 3", а затем перейдет к следующей странице, приложение должно поместить пользователя на страницу "завершение".</span><span class="sxs-lookup"><span data-stu-id="328d0-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="328d0-140">Опять же, это делается путем возврата (до **DWL \_ мсгресулт**) идентификатора диалогового окна "завершение".</span><span class="sxs-lookup"><span data-stu-id="328d0-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="328d0-141">Введение</span><span class="sxs-lookup"><span data-stu-id="328d0-141">Introduction</span></span>
    2.  <span data-ttu-id="328d0-142">Завершение (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="328d0-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="328d0-143">Динамический 1</span><span class="sxs-lookup"><span data-stu-id="328d0-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="328d0-144">Динамический 2</span><span class="sxs-lookup"><span data-stu-id="328d0-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="328d0-145">Динамический 3</span><span class="sxs-lookup"><span data-stu-id="328d0-145">Dynamic 3</span></span>
4.  <span data-ttu-id="328d0-146">Затем приложение может безопасно удалить три динамические страницы (с номерами от трех до пяти).</span><span class="sxs-lookup"><span data-stu-id="328d0-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="328d0-147">Введение</span><span class="sxs-lookup"><span data-stu-id="328d0-147">Introduction</span></span>
    2.  <span data-ttu-id="328d0-148">Завершение (пользователь здесь)</span><span class="sxs-lookup"><span data-stu-id="328d0-148">Completion (User is here)</span></span>

<span data-ttu-id="328d0-149">Обратите внимание, что этот метод необходим только в том случае, если мастер удаляет страницы динамически.</span><span class="sxs-lookup"><span data-stu-id="328d0-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="328d0-150">Если мастер добавляет только страницы динамически, этот процесс не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="328d0-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="328d0-151">Требования</span><span class="sxs-lookup"><span data-stu-id="328d0-151">Requirements</span></span>



| <span data-ttu-id="328d0-152">Требование</span><span class="sxs-lookup"><span data-stu-id="328d0-152">Requirement</span></span> | <span data-ttu-id="328d0-153">Значение</span><span class="sxs-lookup"><span data-stu-id="328d0-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="328d0-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="328d0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="328d0-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="328d0-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="328d0-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="328d0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="328d0-157">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="328d0-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="328d0-158">Header</span><span class="sxs-lookup"><span data-stu-id="328d0-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="328d0-159"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="328d0-159"><dt>Prsht.h</dt></span></span> </dl> |



 

