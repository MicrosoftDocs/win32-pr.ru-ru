---
title: Сообщение PSM_SETCURSELID (Пршт. h)
description: Активирует заданную страницу в таблице свойств на основе идентификатора ресурса страницы. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сеткурселбид.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Элементы управления Windows для PSM_SETCURSELID сообщений
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136835"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="e4855-105">\_Сообщение ПСМ сеткурселид</span><span class="sxs-lookup"><span data-stu-id="e4855-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="e4855-106">Активирует заданную страницу в таблице свойств на основе идентификатора ресурса страницы.</span><span class="sxs-lookup"><span data-stu-id="e4855-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="e4855-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сеткурселбид**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .</span><span class="sxs-lookup"><span data-stu-id="e4855-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4855-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4855-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4855-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4855-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4855-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e4855-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e4855-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4855-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4855-112">Идентификатор ресурса страницы для активации.</span><span class="sxs-lookup"><span data-stu-id="e4855-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4855-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4855-113">Return value</span></span>

<span data-ttu-id="e4855-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e4855-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4855-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4855-115">Remarks</span></span>

<span data-ttu-id="e4855-116">Окно, которое теряет активацию, получает код уведомления [PSN \_ киллактиве](psn-killactive.md) , а окно, получающее активацию, получает код уведомления [PSN \_ сетактиве](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="e4855-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4855-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e4855-117">Requirements</span></span>



| <span data-ttu-id="e4855-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e4855-118">Requirement</span></span> | <span data-ttu-id="e4855-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e4855-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4855-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4855-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4855-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4855-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e4855-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4855-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4855-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4855-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e4855-124">Header</span><span class="sxs-lookup"><span data-stu-id="e4855-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4855-125"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4855-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





