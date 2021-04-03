---
title: Сообщение TCM_DESELECTALL (Коммктрл. h)
description: Сбрасывает элементы в элементе управления "Вкладка", удаляя все, которые были установлены в \_ состояние тЦис буттонпрессед. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл деселекталл.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Элементы управления Windows для TCM_DESELECTALL сообщений
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137278"
---
# <a name="tcm_deselectall-message"></a><span data-ttu-id="edb72-105">\_Сообщение ДЕСЕЛЕКТАЛЛ TCM</span><span class="sxs-lookup"><span data-stu-id="edb72-105">TCM\_DESELECTALL message</span></span>

<span data-ttu-id="edb72-106">Сбрасывает элементы в элементе управления "Вкладка", удаляя все, которые были установлены в состояние [**тЦис \_ буттонпрессед**](tab-control-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="edb72-106">Resets items in a tab control, clearing any that were set to the [**TCIS\_BUTTONPRESSED**](tab-control-item-states.md) state.</span></span> <span data-ttu-id="edb72-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ деселекталл**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .</span><span class="sxs-lookup"><span data-stu-id="edb72-107">You can send this message explicitly or by using the [**TabCtrl\_DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="edb72-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="edb72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edb72-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edb72-110">Флаг, указывающий область девыделения элемента.</span><span class="sxs-lookup"><span data-stu-id="edb72-110">Flag that specifies the scope of the item deselection.</span></span> <span data-ttu-id="edb72-111">Если этот параметр имеет значение **false**, все элементы вкладки будут сброшены.</span><span class="sxs-lookup"><span data-stu-id="edb72-111">If this parameter is set to **FALSE**, all tab items will be reset.</span></span> <span data-ttu-id="edb72-112">Если задано **значение true**, все элементы вкладки, кроме выбранного в данный момент, будут сброшены.</span><span class="sxs-lookup"><span data-stu-id="edb72-112">If it is set to **TRUE**, then all tab items except for the one currently selected will be reset.</span></span>

</dd> <dt>

<span data-ttu-id="edb72-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edb72-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="edb72-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="edb72-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb72-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edb72-115">Return value</span></span>

<span data-ttu-id="edb72-116">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="edb72-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb72-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edb72-117">Remarks</span></span>

<span data-ttu-id="edb72-118">Это сообщение имеет смысл только в том случае, если установлен флаг стиля [**TCS \_ Buttons**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="edb72-118">This message is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb72-119">Требования</span><span class="sxs-lookup"><span data-stu-id="edb72-119">Requirements</span></span>



| <span data-ttu-id="edb72-120">Требование</span><span class="sxs-lookup"><span data-stu-id="edb72-120">Requirement</span></span> | <span data-ttu-id="edb72-121">Значение</span><span class="sxs-lookup"><span data-stu-id="edb72-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edb72-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edb72-122">Minimum supported client</span></span><br/> | <span data-ttu-id="edb72-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edb72-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edb72-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edb72-124">Minimum supported server</span></span><br/> | <span data-ttu-id="edb72-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edb72-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edb72-126">Header</span><span class="sxs-lookup"><span data-stu-id="edb72-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb72-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb72-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





