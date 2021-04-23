---
title: Сообщение PSM_APPLY (Пршт. h)
description: Имитирует выбор кнопки Применить, указывающей на то, что одна или несколько страниц изменились, а изменения должны быть проверены и записаны.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Элементы управления Windows для PSM_APPLY сообщений
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892381"
---
# <a name="psm_apply-message"></a><span data-ttu-id="9df83-104">ПСМ \_ Применить сообщение</span><span class="sxs-lookup"><span data-stu-id="9df83-104">PSM\_APPLY message</span></span>

<span data-ttu-id="9df83-105">Имитирует выбор кнопки **Применить** , указывающей на то, что одна или несколько страниц изменились, а изменения должны быть проверены и записаны.</span><span class="sxs-lookup"><span data-stu-id="9df83-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="9df83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9df83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df83-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9df83-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9df83-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9df83-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9df83-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9df83-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9df83-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9df83-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df83-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9df83-111">Return value</span></span>

<span data-ttu-id="9df83-112">Возвращает **значение true** , если изменения успешно применены ко всем страницам, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9df83-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9df83-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9df83-113">Remarks</span></span>

<span data-ttu-id="9df83-114">Страница свойств отправляет код уведомления [PSN \_ киллактиве](psn-killactive.md) на текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="9df83-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="9df83-115">Если текущая страница возвращает **значение false**, страница свойств отправляет [PSN \_ Применить](psn-apply.md) код уведомления ко всем активным страницам.</span><span class="sxs-lookup"><span data-stu-id="9df83-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="9df83-116">Сообщение ПСМ Apply можно отправить \_ явным образом или с помощью макроса [**пропшит \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .</span><span class="sxs-lookup"><span data-stu-id="9df83-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="9df83-117">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="9df83-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9df83-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9df83-118">Requirements</span></span>



| <span data-ttu-id="9df83-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9df83-119">Requirement</span></span> | <span data-ttu-id="9df83-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9df83-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9df83-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9df83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9df83-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9df83-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9df83-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9df83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9df83-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9df83-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9df83-125">Header</span><span class="sxs-lookup"><span data-stu-id="9df83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9df83-126"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df83-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





