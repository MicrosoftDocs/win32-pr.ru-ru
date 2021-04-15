---
title: Сообщение PSM_INSERTPAGE (Пршт. h)
description: Вставляет новую страницу в существующую вкладку свойств. Эту страницу можно вставить либо по указанному индексу, либо после указанной страницы. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит инсертпаже.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Элементы управления Windows для PSM_INSERTPAGE сообщений
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654548"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="6b0b6-106">\_Сообщение ПСМ инсертпаже</span><span class="sxs-lookup"><span data-stu-id="6b0b6-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="6b0b6-107">Вставляет новую страницу в существующую вкладку свойств.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="6b0b6-108">Эту страницу можно вставить либо по указанному индексу, либо после указанной страницы.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="6b0b6-109">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ инсертпаже**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .</span><span class="sxs-lookup"><span data-stu-id="6b0b6-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b0b6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b0b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0b6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b0b6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0b6-112">Место вставки страницы.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-112">Where the page is to be inserted.</span></span> <span data-ttu-id="6b0b6-113">Присвойте этому параметру **значение NULL** , чтобы новая страница стала первой страницей.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="6b0b6-114">Чтобы указать место вставки новой страницы, можно передать индекс или обработчик ХПРОПШИТПАЖЕ существующей страницы.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="6b0b6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6b0b6-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="6b0b6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6b0b6-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b0b6-117"><dt></dt> <dt>index</dt></span><span class="sxs-lookup"><span data-stu-id="6b0b6-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="6b0b6-118">Если значение параметра *wParam* меньше максушорт (самое большое целое число без знака), то параметр *wParam* задает отсчитываемый от нуля индекс для новой страницы.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="6b0b6-119">Например, чтобы сделать вставленную страницу третьей страницей на странице свойств, установите параметр *wParam* в значение 2.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="6b0b6-120">Чтобы сделать его первой страницей, установите параметр *wParam* в значение 0.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="6b0b6-121">Если параметр *wParam* имеет значение больше, чем число страниц и меньше максушорт, то страница будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="6b0b6-122"><dt></dt><dt>хпажеинсертафтер</dt></span><span class="sxs-lookup"><span data-stu-id="6b0b6-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="6b0b6-123">Если задать для параметра *wParam* маркер хпропшитпаже существующей страницы, Новая страница будет вставлена после нее.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="6b0b6-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b0b6-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0b6-125">Обрабатываемый обработчик для вставляемой страницы.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="6b0b6-126">Сначала необходимо создать страницу, вызвав функцию [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="6b0b6-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0b6-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b0b6-127">Return value</span></span>

<span data-ttu-id="6b0b6-128">Возвращает ненулевое значение, если страница была успешно вставлена, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0b6-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b0b6-129">Remarks</span></span>

<span data-ttu-id="6b0b6-130">Страницы после точки вставки сдвигаются вправо, чтобы разместить новую страницу.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="6b0b6-131">Размер страницы свойств не изменяется в соответствии с новой страницей.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="6b0b6-132">Не делайте новую страницу больше, чем самая большая страница страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="6b0b6-133">Количество сообщений и один вызов функции происходят, когда страница свойств манипулирует списком страниц.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="6b0b6-134">При выполнении этого действия попытка изменить список страниц приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="6b0b6-135">Соответственно, не следует использовать \_ сообщение ПСМ инсертпаже в реализации [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) или при обработке следующих уведомлений и сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="6b0b6-136">PSN \_ Применить</span><span class="sxs-lookup"><span data-stu-id="6b0b6-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="6b0b6-137">PSN \_ киллактиве</span><span class="sxs-lookup"><span data-stu-id="6b0b6-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="6b0b6-138">\_Сброс PSN</span><span class="sxs-lookup"><span data-stu-id="6b0b6-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="6b0b6-139">PSN \_ сетактиве</span><span class="sxs-lookup"><span data-stu-id="6b0b6-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="6b0b6-140">**WM \_ destroy**</span><span class="sxs-lookup"><span data-stu-id="6b0b6-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="6b0b6-141">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="6b0b6-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="6b0b6-142">Если необходимо изменить страницу свойств во время обработки одного из этих сообщений или во время работы [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) , опубликуйте свое частное сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="6b0b6-143">Приложение не будет принимать это сообщение до тех пор, пока диспетчер страниц свойств не завершит свои задачи.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="6b0b6-144">Затем можно изменить список страниц.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="6b0b6-145">На следующие уведомления также влияют изменения страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="6b0b6-146">PSN \_ визбакк</span><span class="sxs-lookup"><span data-stu-id="6b0b6-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="6b0b6-147">PSN \_ визнекст</span><span class="sxs-lookup"><span data-stu-id="6b0b6-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="6b0b6-148">В ответ на эти уведомления можно добавлять или удалять страницы при условии, что вы возвращаете (через DWL \_ мсгресулт) ненулевое значение для указания нужной новой страницы.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="6b0b6-149">Однако обратите внимание, что при вставке страницы, расположенной перед текущей страницей (с меньшим индексом, чем текущая страница), [PSN \_ киллактиве](psn-killactive.md) может быть отправлен на неправильную страницу.</span><span class="sxs-lookup"><span data-stu-id="6b0b6-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="6b0b6-150">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="6b0b6-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b0b6-151">Требования</span><span class="sxs-lookup"><span data-stu-id="6b0b6-151">Requirements</span></span>



| <span data-ttu-id="6b0b6-152">Требование</span><span class="sxs-lookup"><span data-stu-id="6b0b6-152">Requirement</span></span> | <span data-ttu-id="6b0b6-153">Значение</span><span class="sxs-lookup"><span data-stu-id="6b0b6-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0b6-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b0b6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0b6-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b0b6-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6b0b6-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b0b6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0b6-157">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b0b6-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6b0b6-158">Header</span><span class="sxs-lookup"><span data-stu-id="6b0b6-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b0b6-159"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b0b6-159"><dt>Prsht.h</dt></span></span> </dl> |



 

