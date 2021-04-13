---
title: Сообщение PSM_GETRESULT (Пршт. h)
description: Используется немодальными страницами свойств для получения сведений, возвращаемых в модальные страницы свойств с помощью страница свойств. Это сообщение можно отправить явным образом или воспользоваться \_ макросом пропшит.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Элементы управления Windows для PSM_GETRESULT сообщений
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534916"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="cff17-105">ПСМ, \_ сообщение о ВЫрезультате</span><span class="sxs-lookup"><span data-stu-id="cff17-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="cff17-106">Используется немодальными страницами свойств для получения сведений, возвращаемых в модальные страницы свойств с помощью [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span><span class="sxs-lookup"><span data-stu-id="cff17-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="cff17-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**пропшит \_**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .</span><span class="sxs-lookup"><span data-stu-id="cff17-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cff17-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cff17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cff17-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cff17-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cff17-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cff17-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cff17-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cff17-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cff17-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cff17-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cff17-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cff17-113">Return value</span></span>

<span data-ttu-id="cff17-114">Возвращает положительное значение в случае успеха, или-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cff17-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="cff17-115">Следующие возвращаемые значения имеют специальное значение.</span><span class="sxs-lookup"><span data-stu-id="cff17-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="cff17-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cff17-116">Return code</span></span>                                                                                         | <span data-ttu-id="cff17-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cff17-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cff17-118"><dt>**Идентификатор \_ псребутсистем**</dt></span><span class="sxs-lookup"><span data-stu-id="cff17-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="cff17-119">Страница отправила сообщение [**ПСМ \_ ребутсистем**](psm-rebootsystem.md) на страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="cff17-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="cff17-120">Чтобы изменения пользователя вступили в силу, необходимо перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="cff17-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="cff17-121"><dt>**Идентификатор \_ псрестартвиндовс**</dt></span><span class="sxs-lookup"><span data-stu-id="cff17-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="cff17-122">Страница отправила сообщение [**ПСМ \_ рестартвиндовс**](psm-restartwindows.md) на страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="cff17-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="cff17-123">Для вступления изменений пользователя в силу необходимо перезагрузить Windows.</span><span class="sxs-lookup"><span data-stu-id="cff17-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="cff17-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cff17-124">Remarks</span></span>

<span data-ttu-id="cff17-125">Чтобы получить расширенные сведения об ошибке, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cff17-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="cff17-126">Возвращаемое значение для этого сообщения идентично возвращению [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) для модальной страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="cff17-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="cff17-127">Версия 5,80.</span><span class="sxs-lookup"><span data-stu-id="cff17-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="cff17-128">Возвращаемое значение [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) содержит различные сведения для модальных и немодальных страниц свойств.</span><span class="sxs-lookup"><span data-stu-id="cff17-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="cff17-129">В некоторых случаях немодальные страницы свойств могут потребовать получения информации, полученной от **Страница свойств** , если они были модальными.</span><span class="sxs-lookup"><span data-stu-id="cff17-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="cff17-130">В частности, им может потребоваться определить, был ли \_ возвращен идентификатор псребутсистем или ID \_ псрестартвиндовс.</span><span class="sxs-lookup"><span data-stu-id="cff17-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="cff17-131">Для немодальной страницы свойств цикл обработки сообщений должен использовать [**ПСМ \_ исдиалогмессаже**](psm-isdialogmessage.md) для передачи сообщений в диалоговое окно страницы свойств, а [**ПСМ \_ жеткуррентпажехвнд**](psm-getcurrentpagehwnd.md) — для определения момента уничтожения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="cff17-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="cff17-132">Когда пользователь нажимает кнопку **ОК** или **Отмена** , **ПСМ \_ жеткуррентпажехвнд** возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cff17-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="cff17-133">Затем можно получить значение, полученное модальной страницей свойств от [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) , отправив сообщение **ПСМ- \_ result** .</span><span class="sxs-lookup"><span data-stu-id="cff17-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="cff17-134">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="cff17-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cff17-135">Требования</span><span class="sxs-lookup"><span data-stu-id="cff17-135">Requirements</span></span>



| <span data-ttu-id="cff17-136">Требование</span><span class="sxs-lookup"><span data-stu-id="cff17-136">Requirement</span></span> | <span data-ttu-id="cff17-137">Значение</span><span class="sxs-lookup"><span data-stu-id="cff17-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cff17-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cff17-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cff17-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cff17-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cff17-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cff17-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cff17-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cff17-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cff17-142">Header</span><span class="sxs-lookup"><span data-stu-id="cff17-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cff17-143"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="cff17-143"><dt>Prsht.h</dt></span></span> </dl> |



 

