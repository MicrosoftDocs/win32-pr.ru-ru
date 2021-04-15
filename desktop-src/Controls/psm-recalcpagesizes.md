---
title: Сообщение PSM_RECALCPAGESIZES (Пршт. h)
description: Повторно вычисляет размер страницы на странице свойств стандартного или мастера после добавления или удаления страниц. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ рекалкпажесизес.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Элементы управления Windows для PSM_RECALCPAGESIZES сообщений
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654629"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="2ad42-105">\_Сообщение ПСМ рекалкпажесизес</span><span class="sxs-lookup"><span data-stu-id="2ad42-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="2ad42-106">Повторно вычисляет размер страницы на странице свойств стандартного или мастера после добавления или удаления страниц.</span><span class="sxs-lookup"><span data-stu-id="2ad42-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="2ad42-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ рекалкпажесизес**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .</span><span class="sxs-lookup"><span data-stu-id="2ad42-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ad42-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ad42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ad42-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad42-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2ad42-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2ad42-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ad42-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad42-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2ad42-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad42-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ad42-113">Return value</span></span>

<span data-ttu-id="2ad42-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2ad42-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad42-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ad42-115">Remarks</span></span>

<span data-ttu-id="2ad42-116">При создании страницы свойств ее размер изменяется по размеру исходной коллекции страниц.</span><span class="sxs-lookup"><span data-stu-id="2ad42-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="2ad42-117">Чтобы обеспечить совместимость с предыдущими версиями стандартных элементов управления, страницы свойств и мастера не изменяют размер автоматически при последующем добавлении или удалении страниц.</span><span class="sxs-lookup"><span data-stu-id="2ad42-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="2ad42-118">При использовании стандартных элементов управления [версии 5,80](common-control-versions.md)приложения должны отправить **сообщение \_ ПСМ рекалкпажесизес** после добавления или удаления страниц с помощью [**ПСМ \_ ADDPAGE**](psm-addpage.md), [**ПСМ \_ инсертпаже**](psm-insertpage.md), [**ПСМ \_ REMOVEPAGE**](psm-removepage.md)или их эквивалентных макросов.</span><span class="sxs-lookup"><span data-stu-id="2ad42-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="2ad42-119">Это гарантирует, что лист свойств будет иметь правильный размер для текущей коллекции страниц.</span><span class="sxs-lookup"><span data-stu-id="2ad42-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="2ad42-120">Если это сообщение не отправлено, некоторые страницы листа свойств могут быть усечены или слишком велики.</span><span class="sxs-lookup"><span data-stu-id="2ad42-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="2ad42-121">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="2ad42-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ad42-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2ad42-122">Requirements</span></span>



| <span data-ttu-id="2ad42-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2ad42-123">Requirement</span></span> | <span data-ttu-id="2ad42-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2ad42-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad42-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ad42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad42-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ad42-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2ad42-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ad42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad42-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ad42-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2ad42-129">Header</span><span class="sxs-lookup"><span data-stu-id="2ad42-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ad42-130"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ad42-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 





