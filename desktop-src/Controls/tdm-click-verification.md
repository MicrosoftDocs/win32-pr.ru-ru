---
title: Сообщение TDM_CLICK_VERIFICATION (Коммктрл. h)
description: Имитирует нажатие флажка проверки диалогового окна задачи, если оно существует.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Элементы управления Windows для TDM_CLICK_VERIFICATION сообщений
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135086"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="3f123-104">TDM \_ щелкните \_ сообщение о проверке</span><span class="sxs-lookup"><span data-stu-id="3f123-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="3f123-105">Имитирует нажатие флажка проверки диалогового окна задачи, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="3f123-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f123-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f123-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f123-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f123-108">**Значение true** , чтобы установить флажок проверять состояние флажка; **Значение false** , чтобы снять флажок для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="3f123-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="3f123-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f123-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f123-110">**Значение true** , чтобы установить флажок в фокусе клавиатуры; В противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="3f123-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f123-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f123-111">Return value</span></span>

<span data-ttu-id="3f123-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3f123-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f123-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3f123-113">Requirements</span></span>



| <span data-ttu-id="3f123-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3f123-114">Requirement</span></span> | <span data-ttu-id="3f123-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3f123-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f123-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f123-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f123-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f123-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f123-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f123-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f123-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f123-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f123-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f123-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f123-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f123-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





