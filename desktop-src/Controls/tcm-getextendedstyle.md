---
title: Сообщение TCM_GETEXTENDEDSTYLE (Коммктрл. h)
description: Извлекает расширенные стили, используемые в данный момент для элемента управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл жетекстендедстиле.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Элементы управления Windows для TCM_GETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989226"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="03ef4-105">\_Сообщение ЖЕТЕКСТЕНДЕДСТИЛЕ TCM</span><span class="sxs-lookup"><span data-stu-id="03ef4-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="03ef4-106">Извлекает расширенные стили, используемые в данный момент для элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="03ef4-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="03ef4-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ жетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="03ef4-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="03ef4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="03ef4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ef4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03ef4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="03ef4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="03ef4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="03ef4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03ef4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="03ef4-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="03ef4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ef4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03ef4-113">Return value</span></span>

<span data-ttu-id="03ef4-114">Возвращает значение **типа DWORD** , представляющее расширенные стили, используемые в данный момент для элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="03ef4-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="03ef4-115">Это значение представляет собой сочетание [расширенных стилей](tab-control-extended-styles.md)элемента управления Tab.</span><span class="sxs-lookup"><span data-stu-id="03ef4-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ef4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="03ef4-116">Requirements</span></span>



| <span data-ttu-id="03ef4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="03ef4-117">Requirement</span></span> | <span data-ttu-id="03ef4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="03ef4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03ef4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03ef4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="03ef4-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03ef4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03ef4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03ef4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="03ef4-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03ef4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03ef4-123">Header</span><span class="sxs-lookup"><span data-stu-id="03ef4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ef4-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="03ef4-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ef4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03ef4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ef4-126">**\_СЕТЕКСТЕНДЕДСТИЛЕ TCM**</span><span class="sxs-lookup"><span data-stu-id="03ef4-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 





