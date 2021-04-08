---
title: Сообщение PSM_REMOVEPAGE (Пршт. h)
description: Удаляет страницу из листа свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Элементы управления Windows для PSM_REMOVEPAGE сообщений
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892377"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="fa0fc-105">\_Сообщение ПСМ REMOVEPAGE</span><span class="sxs-lookup"><span data-stu-id="fa0fc-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="fa0fc-106">Удаляет страницу из листа свойств.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="fa0fc-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .</span><span class="sxs-lookup"><span data-stu-id="fa0fc-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa0fc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa0fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa0fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa0fc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0fc-110">Отсчитываемый от нуля индекс страницы, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="fa0fc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa0fc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0fc-112">ХПРОПШИТПАЖЕ-маркер страницы для удаления.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa0fc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa0fc-113">Return value</span></span>

<span data-ttu-id="fa0fc-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa0fc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa0fc-115">Remarks</span></span>

<span data-ttu-id="fa0fc-116">Приложение может указывать индекс или обработчик, либо и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="fa0fc-117">Если указаны оба значения, приоритет имеет значение *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fa0fc-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="fa0fc-118">При отправке **ПСМ \_ REMOVEPAGE** удаляется Удаляемая страница страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="fa0fc-119">Количество сообщений и один вызов функции происходят, когда страница свойств манипулирует списком страниц.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="fa0fc-120">При выполнении этого действия попытка изменить список страниц приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="fa0fc-121">Соответственно, не следует использовать сообщение **ПСМ \_ REMOVEPAGE** в реализации [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) или при обработке следующих уведомлений и сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="fa0fc-122">PSN \_ Применить</span><span class="sxs-lookup"><span data-stu-id="fa0fc-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="fa0fc-123">PSN \_ киллактиве</span><span class="sxs-lookup"><span data-stu-id="fa0fc-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="fa0fc-124">\_Сброс PSN</span><span class="sxs-lookup"><span data-stu-id="fa0fc-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="fa0fc-125">PSN \_ сетактиве</span><span class="sxs-lookup"><span data-stu-id="fa0fc-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="fa0fc-126">**WM \_ destroy**</span><span class="sxs-lookup"><span data-stu-id="fa0fc-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="fa0fc-127">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="fa0fc-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="fa0fc-128">Если необходимо изменить страницу свойств во время обработки одного из этих сообщений или во время работы [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) , опубликуйте свое частное сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="fa0fc-129">Приложение не будет принимать это сообщение до тех пор, пока диспетчер страниц свойств не завершит свои задачи.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="fa0fc-130">Затем можно изменить список страниц.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="fa0fc-131">На следующие уведомления также влияют изменения страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="fa0fc-132">PSN \_ визбакк</span><span class="sxs-lookup"><span data-stu-id="fa0fc-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="fa0fc-133">PSN \_ визнекст</span><span class="sxs-lookup"><span data-stu-id="fa0fc-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="fa0fc-134">В ответ на эти уведомления можно добавлять или удалять страницы при условии, что вы возвращаете (через DWL \_ мсгресулт) ненулевое значение для указания нужной новой страницы.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="fa0fc-135">Однако обратите внимание, что при удалении страницы, расположенной перед текущей страницей (с меньшим индексом, чем текущая страница), [PSN \_ киллактиве](psn-killactive.md) может быть отправлен на неправильную страницу.</span><span class="sxs-lookup"><span data-stu-id="fa0fc-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0fc-136">Требования</span><span class="sxs-lookup"><span data-stu-id="fa0fc-136">Requirements</span></span>



| <span data-ttu-id="fa0fc-137">Требование</span><span class="sxs-lookup"><span data-stu-id="fa0fc-137">Requirement</span></span> | <span data-ttu-id="fa0fc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="fa0fc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0fc-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa0fc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0fc-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa0fc-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fa0fc-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa0fc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0fc-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa0fc-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fa0fc-143">Header</span><span class="sxs-lookup"><span data-stu-id="fa0fc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa0fc-144"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa0fc-144"><dt>Prsht.h</dt></span></span> </dl> |



 

