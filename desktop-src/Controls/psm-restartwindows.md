---
title: Сообщение PSM_RESTARTWINDOWS (Пршт. h)
description: Указывает, что необходимо перезапустить Windows, чтобы изменения вступили в силу.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Элементы управления Windows для PSM_RESTARTWINDOWS сообщений
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891777"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="134f7-104">\_Сообщение ПСМ рестартвиндовс</span><span class="sxs-lookup"><span data-stu-id="134f7-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="134f7-105">Указывает, что необходимо перезапустить Windows, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="134f7-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="134f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="134f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="134f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="134f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="134f7-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="134f7-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="134f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="134f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="134f7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="134f7-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="134f7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="134f7-111">Return value</span></span>

<span data-ttu-id="134f7-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="134f7-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="134f7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="134f7-113">Remarks</span></span>

<span data-ttu-id="134f7-114">Приложение должно отправить это сообщение только в ответ на код уведомления [PSN \_ Apply](psn-apply.md) или [PSN \_ киллактиве](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="134f7-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="134f7-115">Сообщение **ПСМ \_ рестартвиндовс** можно отправить явным образом или с помощью макроса [**пропшит \_ рестартвиндовс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .</span><span class="sxs-lookup"><span data-stu-id="134f7-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="134f7-116">Это сообщение приводит к тому, что функция [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) ВОЗВРАЩАЕТ \_ значение ID псрестартвиндовс, но только в том случае, если пользователь нажмет кнопку **ОК** , чтобы закрыть страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="134f7-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="134f7-117">Это обязанность приложения перезапускать Windows, что можно сделать с помощью функции [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="134f7-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="134f7-118">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="134f7-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="134f7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="134f7-119">Requirements</span></span>



| <span data-ttu-id="134f7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="134f7-120">Requirement</span></span> | <span data-ttu-id="134f7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="134f7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="134f7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="134f7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="134f7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="134f7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="134f7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="134f7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="134f7-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="134f7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="134f7-126">Header</span><span class="sxs-lookup"><span data-stu-id="134f7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="134f7-127"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="134f7-127"><dt>Prsht.h</dt></span></span> </dl> |



 

