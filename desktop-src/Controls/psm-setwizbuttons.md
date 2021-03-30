---
title: Сообщение PSM_SETWIZBUTTONS (Пршт. h)
description: Включает или отключает кнопки "назад", "Далее" и "Готово" в мастере. Можно также использовать \_ макрос пропшит сетвизбуттонс для публикации сообщения.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Элементы управления Windows для PSM_SETWIZBUTTONS сообщений
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136242"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="40c3d-105">\_Сообщение ПСМ сетвизбуттонс</span><span class="sxs-lookup"><span data-stu-id="40c3d-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="40c3d-106">Включает или отключает кнопки " **назад**", " **Далее** **" и "Готово"** в мастере.</span><span class="sxs-lookup"><span data-stu-id="40c3d-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="40c3d-107">Можно также использовать макрос [**пропшит \_ сетвизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) для публикации сообщения.</span><span class="sxs-lookup"><span data-stu-id="40c3d-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="40c3d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="40c3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c3d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40c3d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40c3d-110">Задайте для этого параметра значение ПСВИЗБФ \_ елеватионрекуиред, чтобы отобразить значок с повышенными привилегиями на кнопках, указанных в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="40c3d-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="40c3d-111">Значок с повышенными привилегиями (или значок щита экранирования UAC) указывает, что запрос на повышение прав будет использоваться для запроса пользователя на утверждение или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="40c3d-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="40c3d-112">Дополнительные сведения см. в статье [Разработка приложений UAC для Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="40c3d-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="40c3d-113">Отображение значка щита контроля учетных записей поддерживается только в Аеровизардс (КОМАНДНОМ PSH \_ аеровизард).</span><span class="sxs-lookup"><span data-stu-id="40c3d-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="40c3d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40c3d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40c3d-115">Значение, указывающее, какие кнопки страницы свойств включены.</span><span class="sxs-lookup"><span data-stu-id="40c3d-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="40c3d-116">Можно сочетать один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="40c3d-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="40c3d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="40c3d-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="40c3d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="40c3d-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="40c3d-119"><dt>**ПСВИЗБ \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="40c3d-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="40c3d-120">Включает кнопку " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="40c3d-120">Enables the **Back** button.</span></span> <span data-ttu-id="40c3d-121">Если этот флаг не установлен, кнопка **назад** отображается как отключенная.</span><span class="sxs-lookup"><span data-stu-id="40c3d-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="40c3d-122"><dt>**ПСВИЗБ \_ дисабледфиниш**</dt></span><span class="sxs-lookup"><span data-stu-id="40c3d-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="40c3d-123">Отображает отключенную кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="40c3d-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="40c3d-124"><dt>**\_Завершение псвизб**</dt></span><span class="sxs-lookup"><span data-stu-id="40c3d-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="40c3d-125">Отображает включенную кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="40c3d-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="40c3d-126"><dt>**ПСВИЗБ \_ Далее**</dt></span><span class="sxs-lookup"><span data-stu-id="40c3d-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="40c3d-127">Становится активной кнопка **Далее**.</span><span class="sxs-lookup"><span data-stu-id="40c3d-127">Enables the **Next** button.</span></span> <span data-ttu-id="40c3d-128">Если этот флаг не установлен, кнопка **Далее** отображается как отключенная.</span><span class="sxs-lookup"><span data-stu-id="40c3d-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c3d-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40c3d-129">Return value</span></span>

<span data-ttu-id="40c3d-130">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="40c3d-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40c3d-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40c3d-131">Remarks</span></span>

<span data-ttu-id="40c3d-132">Если обработчик [**уведомлений использует сообщение для отправки сообщения**](/windows/desktop/api/winuser/nf-winuser-postmessagea) **ПСМ \_ сетвизбуттонс** , ничего не повлияет на фокус окна до тех пор, пока обработчик не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="40c3d-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="40c3d-133">Например, если вы вызываете [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) сразу же после использования **сообщения** для отправки **ПСМ \_ сетвизбуттонс**, окно сообщения будет получать фокус.</span><span class="sxs-lookup"><span data-stu-id="40c3d-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="40c3d-134">Поскольку отправленные сообщения не доставляются до конца очереди сообщений, сообщение **ПСМ \_ сетвизбуттонс** не будет доставлено до тех пор, пока мастер не затеряет фокус на окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="40c3d-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="40c3d-135">В результате страница свойств не сможет правильно установить фокус на кнопки.</span><span class="sxs-lookup"><span data-stu-id="40c3d-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="40c3d-136">При отправке сообщения ПСМ \_ сетвизбуттонс во время обработки уведомления [PSN \_ сетактиве](psn-setactive.md) используйте функцию посылки [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , а не функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="40c3d-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="40c3d-137">В противном случае система не будет правильно обновлять кнопки.</span><span class="sxs-lookup"><span data-stu-id="40c3d-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="40c3d-138">Если вы используете макрос [**пропшит \_ сетвизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) для отправки этого сообщения, он будет опубликован.</span><span class="sxs-lookup"><span data-stu-id="40c3d-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="40c3d-139">В любое другое время можно использовать **SendMessage** для отправки **ПСМ \_ сетвизбуттонс**.</span><span class="sxs-lookup"><span data-stu-id="40c3d-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="40c3d-140">В мастерах отображаются три или четыре кнопки под каждой страницей.</span><span class="sxs-lookup"><span data-stu-id="40c3d-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="40c3d-141">Это сообщение используется для указания того, какие кнопки включены.</span><span class="sxs-lookup"><span data-stu-id="40c3d-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="40c3d-142">Обычно в мастерах отображаются кнопки **назад**, **Отмена** и кнопка « **Далее** » или « **Готово** ».</span><span class="sxs-lookup"><span data-stu-id="40c3d-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="40c3d-143">Обычно включается только кнопка **Далее** для страницы приветствия, **Далее** и **обратно** для внутренних страниц, а также **назад** и **Готово** для страницы Завершение.</span><span class="sxs-lookup"><span data-stu-id="40c3d-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="40c3d-144">Кнопка **Отмена** всегда включена.</span><span class="sxs-lookup"><span data-stu-id="40c3d-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="40c3d-145">Как правило, установка ПСВИЗБ \_ Finish или псвизб \_ дисабледфиниш заменяет кнопку " **Далее** " кнопкой **"Готово** ".</span><span class="sxs-lookup"><span data-stu-id="40c3d-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="40c3d-146">Чтобы отобразить кнопки " **вперед** **" и "Готово"** одновременно, установите \_ флаг командном PSH Визардхасфиниш в элементе **dwFlags** структуры [**пропшисеадер**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) мастера при создании мастера.</span><span class="sxs-lookup"><span data-stu-id="40c3d-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="40c3d-147">На каждой странице будут показаны все четыре кнопки.</span><span class="sxs-lookup"><span data-stu-id="40c3d-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c3d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="40c3d-148">Requirements</span></span>



| <span data-ttu-id="40c3d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="40c3d-149">Requirement</span></span> | <span data-ttu-id="40c3d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="40c3d-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40c3d-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40c3d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="40c3d-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40c3d-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="40c3d-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40c3d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="40c3d-154">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="40c3d-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="40c3d-155">Header</span><span class="sxs-lookup"><span data-stu-id="40c3d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c3d-156"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="40c3d-156"><dt>Prsht.h</dt></span></span> </dl> |



 

