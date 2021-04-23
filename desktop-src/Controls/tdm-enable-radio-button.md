---
title: Сообщение TDM_ENABLE_RADIO_BUTTON (Коммктрл. h)
description: Включает или отключает переключатель в диалоговом окне задачи.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- Элементы управления Windows для TDM_ENABLE_RADIO_BUTTON сообщений
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989285"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="d206e-104">TDM \_ включить \_ сообщение переключателя \_</span><span class="sxs-lookup"><span data-stu-id="d206e-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="d206e-105">Включает или отключает переключатель в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="d206e-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="d206e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d206e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d206e-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d206e-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d206e-108">Значение **типа int** , указывающее идентификатор переключателя, который должен быть включен или отключен.</span><span class="sxs-lookup"><span data-stu-id="d206e-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="d206e-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d206e-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d206e-110">Указывает состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="d206e-110">Specifies button state.</span></span> <span data-ttu-id="d206e-111">Задайте значение 0, чтобы отключить кнопку. Задайте для параметра значение ненулевой, чтобы включить кнопку.</span><span class="sxs-lookup"><span data-stu-id="d206e-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d206e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d206e-112">Return value</span></span>

<span data-ttu-id="d206e-113">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d206e-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d206e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d206e-114">Requirements</span></span>



| <span data-ttu-id="d206e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d206e-115">Requirement</span></span> | <span data-ttu-id="d206e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d206e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d206e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d206e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d206e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d206e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d206e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d206e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d206e-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d206e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d206e-121">Header</span><span class="sxs-lookup"><span data-stu-id="d206e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d206e-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d206e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





