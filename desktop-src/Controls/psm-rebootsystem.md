---
title: Сообщение PSM_REBOOTSYSTEM (Пршт. h)
description: Указывает, что необходимо перезапустить систему, чтобы изменения вступили в силу. Сообщение ПСМ ребутсистем можно отправить \_ явным образом или с помощью \_ макроса пропшит ребутсистем.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Элементы управления Windows для PSM_REBOOTSYSTEM сообщений
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489951"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="68918-105">\_Сообщение ПСМ ребутсистем</span><span class="sxs-lookup"><span data-stu-id="68918-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="68918-106">Указывает, что необходимо перезапустить систему, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="68918-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="68918-107">Сообщение **ПСМ \_ ребутсистем** можно отправить явным образом или с помощью макроса [**пропшит \_ ребутсистем**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .</span><span class="sxs-lookup"><span data-stu-id="68918-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68918-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68918-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68918-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68918-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68918-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="68918-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="68918-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68918-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68918-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="68918-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68918-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68918-113">Return value</span></span>

<span data-ttu-id="68918-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="68918-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68918-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68918-115">Remarks</span></span>

<span data-ttu-id="68918-116">Приложение должно отправить это сообщение только в ответ на сообщение [PSN \_ Apply](psn-apply.md) или [PSN \_ киллактиве](psn-killactive.md) Notification.</span><span class="sxs-lookup"><span data-stu-id="68918-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="68918-117">Это сообщение приводит к тому, что функция [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) ВОЗВРАЩАЕТ \_ значение ID псребутсистем, но только в том случае, если пользователь нажмет кнопку **ОК** , чтобы закрыть страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="68918-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="68918-118">Ответственность за перезагрузку системы, которую можно выполнить с помощью функции [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) , несет приложение.</span><span class="sxs-lookup"><span data-stu-id="68918-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="68918-119">Это сообщение заменяет все сообщения [**ПСМ \_ рестартвиндовс**](psm-restartwindows.md) , которые предшествуют или следуют за ним.</span><span class="sxs-lookup"><span data-stu-id="68918-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="68918-120">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="68918-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68918-121">Требования</span><span class="sxs-lookup"><span data-stu-id="68918-121">Requirements</span></span>



| <span data-ttu-id="68918-122">Требование</span><span class="sxs-lookup"><span data-stu-id="68918-122">Requirement</span></span> | <span data-ttu-id="68918-123">Значение</span><span class="sxs-lookup"><span data-stu-id="68918-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68918-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68918-124">Minimum supported client</span></span><br/> | <span data-ttu-id="68918-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68918-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68918-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68918-126">Minimum supported server</span></span><br/> | <span data-ttu-id="68918-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68918-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68918-128">Header</span><span class="sxs-lookup"><span data-stu-id="68918-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="68918-129"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="68918-129"><dt>Prsht.h</dt></span></span> </dl> |



 

