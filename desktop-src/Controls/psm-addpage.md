---
title: Сообщение PSM_ADDPAGE (Пршт. h)
description: Добавляет новую страницу в конец существующей страницы свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит addPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Элементы управления Windows для PSM_ADDPAGE сообщений
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892382"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="6c597-105">\_Сообщение ПСМ ADDPAGE</span><span class="sxs-lookup"><span data-stu-id="6c597-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="6c597-106">Добавляет новую страницу в конец существующей страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="6c597-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="6c597-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ addPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .</span><span class="sxs-lookup"><span data-stu-id="6c597-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c597-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c597-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c597-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c597-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c597-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6c597-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c597-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c597-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c597-112">Обрабатываемый обработчик для добавляемой страницы.</span><span class="sxs-lookup"><span data-stu-id="6c597-112">Handle to the page to add.</span></span> <span data-ttu-id="6c597-113">Страница должна быть создана с помощью предыдущего вызова функции [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="6c597-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c597-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c597-114">Return value</span></span>

<span data-ttu-id="6c597-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c597-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c597-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c597-116">Remarks</span></span>

<span data-ttu-id="6c597-117">Новая страница не должна быть больше самой большой страницы, находящегося в данный момент в таблице свойств, так как размер страницы свойств не изменяется в соответствии с новой страницей.</span><span class="sxs-lookup"><span data-stu-id="6c597-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="6c597-118">Количество сообщений и один вызов функции происходят, когда страница свойств манипулирует списком страниц.</span><span class="sxs-lookup"><span data-stu-id="6c597-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="6c597-119">При выполнении этого действия попытка изменить список страниц приведет к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="6c597-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="6c597-120">Соответственно, не следует использовать \_ сообщение ПСМ ADDPAGE в реализации [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) или при обработке следующих уведомлений и сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="6c597-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="6c597-121">PSN \_ Применить</span><span class="sxs-lookup"><span data-stu-id="6c597-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="6c597-122">PSN \_ киллактиве</span><span class="sxs-lookup"><span data-stu-id="6c597-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="6c597-123">\_Сброс PSN</span><span class="sxs-lookup"><span data-stu-id="6c597-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="6c597-124">PSN \_ сетактиве</span><span class="sxs-lookup"><span data-stu-id="6c597-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="6c597-125">**WM \_ destroy**</span><span class="sxs-lookup"><span data-stu-id="6c597-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="6c597-126">**WM \_ инитдиалог**</span><span class="sxs-lookup"><span data-stu-id="6c597-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="6c597-127">Если необходимо изменить страницу свойств во время обработки одного из этих сообщений или во время работы [*пропшитпажепрок*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) , опубликуйте свое частное сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="6c597-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="6c597-128">Приложение не будет принимать это сообщение до тех пор, пока диспетчер страниц свойств не завершит свои задачи.</span><span class="sxs-lookup"><span data-stu-id="6c597-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="6c597-129">Затем можно изменить список страниц.</span><span class="sxs-lookup"><span data-stu-id="6c597-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c597-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6c597-130">Requirements</span></span>



| <span data-ttu-id="6c597-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6c597-131">Requirement</span></span> | <span data-ttu-id="6c597-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6c597-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c597-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c597-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6c597-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c597-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6c597-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c597-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6c597-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c597-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c597-137">Header</span><span class="sxs-lookup"><span data-stu-id="6c597-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c597-138"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c597-138"><dt>Prsht.h</dt></span></span> </dl> |



 

