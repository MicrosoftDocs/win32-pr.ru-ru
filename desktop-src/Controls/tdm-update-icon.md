---
title: Сообщение TDM_UPDATE_ICON (Коммктрл. h)
description: Обновляет значок диалогового окна задачи.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- Элементы управления Windows для TDM_UPDATE_ICON сообщений
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989371"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="63992-104">\_ \_ Сообщение значка обновления TDM</span><span class="sxs-lookup"><span data-stu-id="63992-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="63992-105">Обновляет значок диалогового окна задачи.</span><span class="sxs-lookup"><span data-stu-id="63992-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="63992-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63992-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63992-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63992-108">Указывает, какой элемент Icon обновить.</span><span class="sxs-lookup"><span data-stu-id="63992-108">Indicates which icon element to update.</span></span> <span data-ttu-id="63992-109">Этот параметр должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="63992-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="63992-110">Значение</span><span class="sxs-lookup"><span data-stu-id="63992-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="63992-111">Значение</span><span class="sxs-lookup"><span data-stu-id="63992-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="63992-112"><dt>**\_значок тдие \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63992-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="63992-113">Основной значок.</span><span class="sxs-lookup"><span data-stu-id="63992-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="63992-114"><dt>**\_Нижний колонтитул значка тдие \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63992-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="63992-115">Значок нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="63992-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="63992-116">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63992-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63992-117">Указатель на строку (ПКВСТР) или обработчик для отображаемого значка (ХИКОН).</span><span class="sxs-lookup"><span data-stu-id="63992-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="63992-118">Если параметр *lParam* имеет **значение NULL**, значок не отображается, независимо от значения параметра *wParam*.</span><span class="sxs-lookup"><span data-stu-id="63992-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="63992-119">Если значение *wParam* равно тдие \_ Icon \_ Main и для \_ \_ \_ элемента **dwFlags** в структуре [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , используемой для создания диалогового окна задачи, установлен флаг TDF use Хикон Main, то параметр *lParam* должен содержать маркер для отображаемого значка (Хикон).</span><span class="sxs-lookup"><span data-stu-id="63992-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="63992-120">Если для параметра *wParam* задано значение тдие, \_ а для \_ \_ \_ \_ элемента **dwFlags** структуры [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , использованной для создания диалогового окна задачи, установлен флаг TDF use Хикон Footer, то параметр *lParam* должен содержать маркер для отображаемого значка (Хикон).</span><span class="sxs-lookup"><span data-stu-id="63992-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="63992-121">Если TDF \_ использовать \_ Хикон \_ Main или TDF \_ USE \_ Хикон \_ footer flags **не** задано для элемента **dwFlags** , параметр *lParam* должен указывать на заканчивающуюся нулем строку Юникода (пквстр), которая содержит допустимый идентификатор ресурса, передаваемый через макрос [**макеинтресаурце**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="63992-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="63992-122">Значок отображается на основе значения *wParam*: Если значение равно тдие \_ Icon \_ Main (основной значок), значок отображается в заголовке; если значение равно тдие \_ значка \_ , значок отображается в нижнем колонтитуле.</span><span class="sxs-lookup"><span data-stu-id="63992-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="63992-123">Ресурс должен быть либо из модуля ресурсов приложения (указанный в элементе **HINSTANCE** структуры [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ), либо если значение **HINSTANCE** равно **NULL**, из модуля ресурсов системы (imageres.dll).</span><span class="sxs-lookup"><span data-stu-id="63992-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="63992-124">Чтобы определить системный ресурс, используйте допустимый идентификатор системы, переданный в макросе **макеинтресаурце** , или одно из следующих предопределенных значений из коммктрл. h:</span><span class="sxs-lookup"><span data-stu-id="63992-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="63992-125">Значение</span><span class="sxs-lookup"><span data-stu-id="63992-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="63992-126">Значение</span><span class="sxs-lookup"><span data-stu-id="63992-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="63992-127"><dt>**\_значок ошибки \_ TD**</dt></span><span class="sxs-lookup"><span data-stu-id="63992-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="63992-128">Значок "отключить знак".</span><span class="sxs-lookup"><span data-stu-id="63992-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="63992-129"><dt>**\_значок предупреждения \_ TD**</dt></span><span class="sxs-lookup"><span data-stu-id="63992-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="63992-130">Значок восклицательного знака.</span><span class="sxs-lookup"><span data-stu-id="63992-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="63992-131"><dt>**\_значок сведений \_ TD**</dt></span><span class="sxs-lookup"><span data-stu-id="63992-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="63992-132">Строчная буква i в значке круга.</span><span class="sxs-lookup"><span data-stu-id="63992-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="63992-133"><dt>**\_значок щита \_ TD**</dt></span><span class="sxs-lookup"><span data-stu-id="63992-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="63992-134">Значок щита безопасности.</span><span class="sxs-lookup"><span data-stu-id="63992-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63992-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63992-135">Return value</span></span>

<span data-ttu-id="63992-136">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="63992-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="63992-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63992-137">Remarks</span></span>

<span data-ttu-id="63992-138">Макет диалогового окна задачи со значком может завершиться ошибкой, и это может не отражаться в возвращаемом значении.</span><span class="sxs-lookup"><span data-stu-id="63992-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="63992-139">Возвращаемое значение S " \_ ОК" отражает только то, что диалоговое окно задачи получило сообщение и попыталось обработать его.</span><span class="sxs-lookup"><span data-stu-id="63992-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="63992-140">Если происходит сбой макета диалогового окна задачи, диалоговое окно закроется, а в зарегистрированной функции обратного вызова будет возвращен код **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63992-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="63992-141">Дополнительные сведения о синтаксисе функции обратного вызова см. в разделе [*таскдиалогкаллбаккпрок*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="63992-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="63992-142">Если диалоговое окно задачи создается без нижнего колонтитула (то есть соответствующие элементы в структуре [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , используемой для создания диалогового окна задачи имеют **значение NULL**) и сообщение отправляется, нижний колонтитул не добавляется динамически в диалоговое окно задачи.</span><span class="sxs-lookup"><span data-stu-id="63992-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="63992-143">То же самое справедливо для отправки этого сообщения для обновления значка заголовка при создании диалогового окна задачи без заголовка.</span><span class="sxs-lookup"><span data-stu-id="63992-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="63992-144">Чтобы добавить верхний или нижний колонтитул во время выполнения, используйте функцию [**TDM \_ навигации \_ Page**](tdm-navigate-page.md) .</span><span class="sxs-lookup"><span data-stu-id="63992-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="63992-145">Требования</span><span class="sxs-lookup"><span data-stu-id="63992-145">Requirements</span></span>



| <span data-ttu-id="63992-146">Требование</span><span class="sxs-lookup"><span data-stu-id="63992-146">Requirement</span></span> | <span data-ttu-id="63992-147">Значение</span><span class="sxs-lookup"><span data-stu-id="63992-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63992-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63992-148">Minimum supported client</span></span><br/> | <span data-ttu-id="63992-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63992-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63992-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63992-150">Minimum supported server</span></span><br/> | <span data-ttu-id="63992-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63992-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63992-152">Header</span><span class="sxs-lookup"><span data-stu-id="63992-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="63992-153"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="63992-153"><dt>Commctrl.h</dt></span></span> </dl> |



 

