---
title: Сообщение PSM_SHOWWIZBUTTONS (Пршт. h)
description: Показывает или скрывает кнопки в мастере. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит шоввизбуттонс.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- Элементы управления Windows для PSM_SHOWWIZBUTTONS сообщений
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654444"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="8308d-105">\_Сообщение ПСМ шоввизбуттонс</span><span class="sxs-lookup"><span data-stu-id="8308d-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="8308d-106">Показывает или скрывает кнопки в мастере.</span><span class="sxs-lookup"><span data-stu-id="8308d-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="8308d-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ шоввизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="8308d-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8308d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8308d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8308d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8308d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8308d-110">Одно или несколько из следующих значений, указывающих, какие кнопки страницы свойств должны отображаться.</span><span class="sxs-lookup"><span data-stu-id="8308d-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="8308d-111">Если значение кнопки включено в этот параметр и *lParam*, оно отображается.</span><span class="sxs-lookup"><span data-stu-id="8308d-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="8308d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8308d-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="8308d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8308d-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="8308d-114"><dt>**ПСВИЗБ \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="8308d-115">Кнопка " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="8308d-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="8308d-116"><dt>**ПСВИЗБ \_ Отмена**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="8308d-117">Кнопка **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="8308d-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="8308d-118"><dt>**ПСВИЗБ \_ дисабледфиниш**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="8308d-119">Кнопка **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="8308d-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="8308d-120"><dt>**\_Завершение псвизб**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="8308d-121">Кнопка **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="8308d-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="8308d-122"><dt>**ПСВИЗБ \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="8308d-123">Кнопка **Далее** .</span><span class="sxs-lookup"><span data-stu-id="8308d-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="8308d-124"><dt>**ПСВИЗБ \_ Показывать**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="8308d-125">Установите только этот флаг (определяется как ноль), чтобы скрыть все кнопки, указанные в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="8308d-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="8308d-126"><dt>**\_Восстановление псвизб**</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="8308d-127">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="8308d-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="8308d-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8308d-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8308d-129">Одно или несколько из тех же значений, которые используются в параметре *wParam*, указывая, какие кнопки затрагиваются этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="8308d-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="8308d-130">Если значение кнопки отображается в этом параметре, но не в *wParam*, кнопка будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="8308d-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8308d-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8308d-131">Return value</span></span>

<span data-ttu-id="8308d-132">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8308d-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8308d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8308d-133">Remarks</span></span>

<span data-ttu-id="8308d-134">В мастерах отображаются три или четыре кнопки под каждой страницей.</span><span class="sxs-lookup"><span data-stu-id="8308d-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="8308d-135">Это сообщение используется для указания того, какие кнопки видимы.</span><span class="sxs-lookup"><span data-stu-id="8308d-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="8308d-136">Обычно в мастерах отображаются кнопки **назад**, **Отмена** и кнопка « **Далее** » или « **Готово** ».</span><span class="sxs-lookup"><span data-stu-id="8308d-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="8308d-137">Кнопка **Отмена** всегда является видимой.</span><span class="sxs-lookup"><span data-stu-id="8308d-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="8308d-138">Как правило, **задайте \_ псвизб Finish** или **псвизб \_ дисабледфиниш** , чтобы заменить кнопку " **Далее** " кнопкой **"Готово** ".</span><span class="sxs-lookup"><span data-stu-id="8308d-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="8308d-139">Чтобы отобразить кнопки " **Далее** **" и "Готово"** одновременно, установите флаг **командном PSH \_ визардхасфиниш** в элементе **dwFlags** структуры [**пропшисеадер**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) при создании мастера.</span><span class="sxs-lookup"><span data-stu-id="8308d-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="8308d-140">На каждой странице будут показаны все четыре кнопки: **назад**, **Далее**, **Отмена** и **Готово**.</span><span class="sxs-lookup"><span data-stu-id="8308d-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="8308d-141">Если вы используете макрос [**пропшит \_ шоввизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) для отправки этого сообщения, он будет опубликован.</span><span class="sxs-lookup"><span data-stu-id="8308d-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="8308d-142">В любое другое время можно использовать [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) для отправки **ПСМ \_ шоввизбуттонс**.</span><span class="sxs-lookup"><span data-stu-id="8308d-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="8308d-143">Если обработчик [**уведомлений использует сообщение для отправки сообщения**](/windows/desktop/api/winuser/nf-winuser-postmessagea) **ПСМ \_ шоввизбуттонс** , ничего не повлияет на фокус окна до тех пор, пока обработчик не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="8308d-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="8308d-144">Например, если вы вызываете [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) сразу же после использования **сообщения** для отправки **ПСМ \_ шоввизбуттонс**, окно сообщения будет получать фокус.</span><span class="sxs-lookup"><span data-stu-id="8308d-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="8308d-145">Поскольку отправленные сообщения не доставляются до конца очереди сообщений, сообщение **ПСМ \_ шоввизбуттонс** не будет доставлено до тех пор, пока мастер не затеряет фокус на окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="8308d-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="8308d-146">В результате страница свойств не сможет правильно установить фокус на кнопки.</span><span class="sxs-lookup"><span data-stu-id="8308d-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="8308d-147">Требования</span><span class="sxs-lookup"><span data-stu-id="8308d-147">Requirements</span></span>



| <span data-ttu-id="8308d-148">Требование</span><span class="sxs-lookup"><span data-stu-id="8308d-148">Requirement</span></span> | <span data-ttu-id="8308d-149">Значение</span><span class="sxs-lookup"><span data-stu-id="8308d-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8308d-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8308d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8308d-151">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8308d-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8308d-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8308d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8308d-153">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8308d-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8308d-154">Header</span><span class="sxs-lookup"><span data-stu-id="8308d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="8308d-155"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="8308d-155"><dt>Prsht.h</dt></span></span> </dl> |



 

