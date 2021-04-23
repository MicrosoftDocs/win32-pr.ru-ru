---
title: Сообщение PSM_ISDIALOGMESSAGE (Пршт. h)
description: Передает сообщение в диалоговое окно страницы свойств и указывает, обрабатывало ли это сообщение диалоговое окно. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит исдиалогмессаже.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Элементы управления Windows для PSM_ISDIALOGMESSAGE сообщений
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892013"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="14329-105">\_Сообщение ПСМ исдиалогмессаже</span><span class="sxs-lookup"><span data-stu-id="14329-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="14329-106">Передает сообщение в диалоговое окно страницы свойств и указывает, обрабатывало ли это сообщение диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="14329-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="14329-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ исдиалогмессаже**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .</span><span class="sxs-lookup"><span data-stu-id="14329-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="14329-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14329-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14329-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14329-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14329-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="14329-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="14329-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14329-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14329-112">Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение для проверки.</span><span class="sxs-lookup"><span data-stu-id="14329-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14329-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14329-113">Return value</span></span>

<span data-ttu-id="14329-114">Возвращает **значение true** , если сообщение было обработано, или **значение false** , если сообщение не было обработано.</span><span class="sxs-lookup"><span data-stu-id="14329-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="14329-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14329-115">Remarks</span></span>

<span data-ttu-id="14329-116">Для передачи сообщений в диалоговое окно страницы свойств в цикле сообщений следует использовать сообщение **ПСМ \_ исдиалогмессаже** с немодальными страницами свойств.</span><span class="sxs-lookup"><span data-stu-id="14329-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="14329-117">В системах, поддерживающих Юникод, для получения сообщений используйте версии [](/windows/desktop/api/winuser/nf-winuser-getmessage) Юникода для функций [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**Жетмессажев** и **пикмессажев**) в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="14329-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="14329-118">Если возвращаемое значение указывает, что сообщение было обработано, оно не должно передаваться в функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) или [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="14329-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="14329-119">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="14329-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14329-120">Требования</span><span class="sxs-lookup"><span data-stu-id="14329-120">Requirements</span></span>



| <span data-ttu-id="14329-121">Требование</span><span class="sxs-lookup"><span data-stu-id="14329-121">Requirement</span></span> | <span data-ttu-id="14329-122">Значение</span><span class="sxs-lookup"><span data-stu-id="14329-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14329-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14329-123">Minimum supported client</span></span><br/> | <span data-ttu-id="14329-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14329-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="14329-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14329-125">Minimum supported server</span></span><br/> | <span data-ttu-id="14329-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14329-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14329-127">Header</span><span class="sxs-lookup"><span data-stu-id="14329-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="14329-128"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="14329-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14329-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14329-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14329-130">**Страница свойств**</span><span class="sxs-lookup"><span data-stu-id="14329-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

