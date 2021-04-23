---
title: Сообщение PSM_GETCURRENTPAGEHWND (Пршт. h)
description: Извлекает маркер окна текущей страницы на странице свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит жеткуррентпажехвнд.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Элементы управления Windows для PSM_GETCURRENTPAGEHWND сообщений
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654631"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="a1621-105">\_Сообщение ПСМ жеткуррентпажехвнд</span><span class="sxs-lookup"><span data-stu-id="a1621-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="a1621-106">Извлекает маркер окна текущей страницы на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="a1621-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="a1621-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ жеткуррентпажехвнд**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .</span><span class="sxs-lookup"><span data-stu-id="a1621-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1621-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1621-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1621-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1621-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1621-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a1621-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a1621-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1621-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1621-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a1621-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1621-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1621-113">Return value</span></span>

<span data-ttu-id="a1621-114">Возвращает маркер окна текущей страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a1621-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1621-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1621-115">Remarks</span></span>

<span data-ttu-id="a1621-116">Используйте сообщение **ПСМ \_ жеткуррентпажехвнд** с немодальными страницами свойств, чтобы определить, когда следует уничтожить диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a1621-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="a1621-117">Когда пользователь нажимает кнопку **ОК** или **Отмена** , **ПСМ \_ жеткуррентпажехвнд** возвращает **значение NULL**, а затем можно использовать функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) для уничтожения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a1621-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="a1621-118">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a1621-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1621-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a1621-119">Requirements</span></span>



| <span data-ttu-id="a1621-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a1621-120">Requirement</span></span> | <span data-ttu-id="a1621-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a1621-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1621-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1621-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1621-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1621-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a1621-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1621-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1621-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1621-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1621-126">Header</span><span class="sxs-lookup"><span data-stu-id="a1621-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1621-127"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1621-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1621-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1621-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1621-129">**Страница свойств**</span><span class="sxs-lookup"><span data-stu-id="a1621-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

