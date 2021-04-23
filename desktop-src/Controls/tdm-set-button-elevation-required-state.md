---
title: Сообщение TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (Коммктрл. h)
description: Указывает, должен ли данная кнопка диалогового окна задачи или ссылка на команду иметь значок щита контроля учетных записей (UAC). то есть, требуется ли повышение прав для действия, вызываемого кнопкой.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Элементы управления Windows для TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE сообщений
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137427"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="bea06-104">\_Сообщение о \_ \_ состоянии "требуется повышение прав" для кнопки TDM \_ \_</span><span class="sxs-lookup"><span data-stu-id="bea06-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="bea06-105">Указывает, должен ли данная кнопка диалогового окна задачи или ссылка на команду иметь значок щита контроля учетных записей (UAC). то есть, требуется ли повышение прав для действия, вызываемого кнопкой.</span><span class="sxs-lookup"><span data-stu-id="bea06-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="bea06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bea06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea06-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bea06-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea06-108">Идентификатор обновляемой кнопки или ссылки на команду.</span><span class="sxs-lookup"><span data-stu-id="bea06-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="bea06-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bea06-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea06-110">Задайте значение 0, чтобы указать, что действие, вызываемое кнопкой, не требует повышения прав.</span><span class="sxs-lookup"><span data-stu-id="bea06-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="bea06-111">Задайте значение ненулевой, чтобы обозначить, что действие требует повышения прав.</span><span class="sxs-lookup"><span data-stu-id="bea06-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea06-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bea06-112">Return value</span></span>

<span data-ttu-id="bea06-113">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bea06-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea06-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bea06-114">Requirements</span></span>



| <span data-ttu-id="bea06-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bea06-115">Requirement</span></span> | <span data-ttu-id="bea06-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bea06-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bea06-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bea06-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bea06-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bea06-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bea06-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bea06-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bea06-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bea06-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bea06-121">Header</span><span class="sxs-lookup"><span data-stu-id="bea06-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea06-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bea06-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





