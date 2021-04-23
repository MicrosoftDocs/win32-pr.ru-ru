---
title: Сообщение BCM_SETSHIELD (Коммктрл. h)
description: Задает состояние, необходимое для повышения прав доступа к указанной кнопке или ссылке на команду для отображения значка с повышенными привилегиями. Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки сетелеватионрекуиредстате.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Элементы управления Windows для BCM_SETSHIELD сообщений
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135723"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="b259f-105">\_Сообщение СЕТШИЕЛД BCM</span><span class="sxs-lookup"><span data-stu-id="b259f-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="b259f-106">Задает состояние, необходимое для повышения прав доступа к указанной кнопке или ссылке на команду для отображения значка с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="b259f-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="b259f-107">Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ сетелеватионрекуиредстате**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) .</span><span class="sxs-lookup"><span data-stu-id="b259f-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b259f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b259f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b259f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b259f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b259f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b259f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b259f-111">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b259f-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b259f-112">**Логическое** значение, равное **true** для рисования значка с повышенными привилегиями, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b259f-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b259f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b259f-113">Return value</span></span>

<span data-ttu-id="b259f-114">Возвращает 1 в случае успеха или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b259f-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b259f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b259f-115">Remarks</span></span>

<span data-ttu-id="b259f-116">Приложение должно быть манифестом для использования comctl32.dll версии 6 для получения этой функции.</span><span class="sxs-lookup"><span data-stu-id="b259f-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="b259f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b259f-117">Requirements</span></span>



| <span data-ttu-id="b259f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b259f-118">Requirement</span></span> | <span data-ttu-id="b259f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b259f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b259f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b259f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b259f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b259f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b259f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b259f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b259f-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b259f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b259f-124">Header</span><span class="sxs-lookup"><span data-stu-id="b259f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b259f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b259f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





