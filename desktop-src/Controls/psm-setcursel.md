---
title: Сообщение PSM_SETCURSEL (Пршт. h)
description: Активирует указанную страницу на странице свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сеткурсел.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Элементы управления Windows для PSM_SETCURSEL сообщений
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135703"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="9cd59-105">\_Сообщение ПСМ сеткурсел</span><span class="sxs-lookup"><span data-stu-id="9cd59-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="9cd59-106">Активирует указанную страницу на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="9cd59-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="9cd59-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сеткурсел**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="9cd59-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9cd59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cd59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd59-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cd59-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cd59-110">Отсчитываемый от нуля индекс страницы.</span><span class="sxs-lookup"><span data-stu-id="9cd59-110">The zero-based index of the page.</span></span> <span data-ttu-id="9cd59-111">Приложение может указать индекс или маркер или оба значения.</span><span class="sxs-lookup"><span data-stu-id="9cd59-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="9cd59-112">Если указаны оба значения, приоритет имеет значение *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9cd59-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="9cd59-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cd59-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cd59-114">Маркер страницы для активации.</span><span class="sxs-lookup"><span data-stu-id="9cd59-114">The handle to the page to activate.</span></span> <span data-ttu-id="9cd59-115">Приложение может указать индекс или маркер или оба значения.</span><span class="sxs-lookup"><span data-stu-id="9cd59-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="9cd59-116">Если указаны оба значения, приоритет имеет значение *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9cd59-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd59-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cd59-117">Return value</span></span>

<span data-ttu-id="9cd59-118">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9cd59-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cd59-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cd59-119">Remarks</span></span>

<span data-ttu-id="9cd59-120">Окно, которое теряет активацию, получает код уведомления [PSN \_ киллактиве](psn-killactive.md) , а окно, получающее активацию, получает код уведомления [PSN \_ сетактиве](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd59-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd59-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9cd59-121">Requirements</span></span>



| <span data-ttu-id="9cd59-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9cd59-122">Requirement</span></span> | <span data-ttu-id="9cd59-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9cd59-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd59-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cd59-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd59-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cd59-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9cd59-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cd59-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd59-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cd59-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9cd59-128">Header</span><span class="sxs-lookup"><span data-stu-id="9cd59-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cd59-129"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cd59-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





