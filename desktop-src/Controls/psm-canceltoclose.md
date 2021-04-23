---
title: Сообщение PSM_CANCELTOCLOSE (Пршт. h)
description: Отправляется приложением при выполнении изменений с момента последнего \_ уведомления об использовании PSN, которое не может быть отменено. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит канцелтоклосе.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- Элементы управления Windows для PSM_CANCELTOCLOSE сообщений
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136963"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="a1ea4-105">\_Сообщение ПСМ канцелтоклосе</span><span class="sxs-lookup"><span data-stu-id="a1ea4-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="a1ea4-106">Отправляется приложением при выполнении изменений с момента последнего уведомления об [ \_ использовании PSN](psn-apply.md) , которое не может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="a1ea4-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ канцелтоклосе**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .</span><span class="sxs-lookup"><span data-stu-id="a1ea4-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1ea4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1ea4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1ea4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1ea4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1ea4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a1ea4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1ea4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1ea4-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1ea4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1ea4-113">Return value</span></span>

<span data-ttu-id="a1ea4-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ea4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1ea4-115">Remarks</span></span>

<span data-ttu-id="a1ea4-116">**ПСМ \_ КАНЦЕЛТОКЛОСЕ** отключает кнопку **"Отмена** " и изменяет текст кнопки " **ОК** " на "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="a1ea4-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="a1ea4-117">Большинство страниц свойств ожидают необратимых изменений, пока не будет \_ получено уведомление о применении PSN.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="a1ea4-118">Однако в некоторых обстоятельствах страница свойств может вносить необратимые изменения за пределами стандартной \_ последовательности PSN Apply/PSN \_ Reset.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="a1ea4-119">Одним из примеров является страница свойств, содержащая кнопку « **изменить** », которая используется для вывода поддиалогового окна для редактирования свойства.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="a1ea4-120">Когда пользователь нажимает кнопку **ОК** , чтобы отправить изменение, страница вкладки свойств имеет несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="a1ea4-121">Он может записывать изменения, но дожидаться получения PSN \_ уведомления об использовании для их применения.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="a1ea4-122">Это предпочтительный подход.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="a1ea4-123">Изменения можно применить сразу после выхода из поддиалогового окна, но запомнить исходные параметры.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="a1ea4-124">Эти параметры можно использовать для восстановления исходного состояния при \_ получении уведомления о сбросе PSN.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="a1ea4-125">Он может применить изменения немедленно и не пытаться восстановить исходные параметры при получении уведомления о [ \_ сбросе PSN](psn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="a1ea4-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="a1ea4-126">Этот подход не рекомендуется, но может быть необходим, если изменения слишком далеко не позволяют сделать другие два варианта практичными.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="a1ea4-127">В третьем варианте приложения должны отправить сообщение **ПСМ \_ канцелтоклосе** на страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="a1ea4-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="a1ea4-128">Указывает пользователю, что изменения, внесенные с помощью поддиалогового окна, нельзя отменить, нажав кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="a1ea4-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="a1ea4-129">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a1ea4-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1ea4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a1ea4-130">Requirements</span></span>



| <span data-ttu-id="a1ea4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a1ea4-131">Requirement</span></span> | <span data-ttu-id="a1ea4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a1ea4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ea4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1ea4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a1ea4-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1ea4-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a1ea4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1ea4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a1ea4-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1ea4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1ea4-137">Header</span><span class="sxs-lookup"><span data-stu-id="a1ea4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1ea4-138"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1ea4-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 





