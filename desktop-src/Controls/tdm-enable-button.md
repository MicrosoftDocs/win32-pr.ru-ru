---
title: Сообщение TDM_ENABLE_BUTTON (Коммктрл. h)
description: Включает или отключает кнопку отправки в диалоговом окне задачи.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Элементы управления Windows для TDM_ENABLE_BUTTON сообщений
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654683"
---
# <a name="tdm_enable_button-message"></a><span data-ttu-id="651e4-104">\_ \_ Сообщение кнопки "включить TDM"</span><span class="sxs-lookup"><span data-stu-id="651e4-104">TDM\_ENABLE\_BUTTON message</span></span>

<span data-ttu-id="651e4-105">Включает или отключает кнопку отправки в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="651e4-105">Enables or disables a push button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="651e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="651e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="651e4-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="651e4-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="651e4-108">Значение **типа int** , указывающее идентификатор кнопки, которая должна быть включена или отключена.</span><span class="sxs-lookup"><span data-stu-id="651e4-108">An **int** value that specifies the ID of the push button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="651e4-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="651e4-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="651e4-110">Указывает состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="651e4-110">Specifies button state.</span></span> <span data-ttu-id="651e4-111">Задайте значение 0, чтобы отключить кнопку. Задайте для параметра значение ненулевой, чтобы включить кнопку.</span><span class="sxs-lookup"><span data-stu-id="651e4-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="651e4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="651e4-112">Return value</span></span>

<span data-ttu-id="651e4-113">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="651e4-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="651e4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="651e4-114">Requirements</span></span>



| <span data-ttu-id="651e4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="651e4-115">Requirement</span></span> | <span data-ttu-id="651e4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="651e4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="651e4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="651e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="651e4-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="651e4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="651e4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="651e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="651e4-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="651e4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="651e4-121">Header</span><span class="sxs-lookup"><span data-stu-id="651e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="651e4-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="651e4-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





