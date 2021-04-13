---
title: Сообщение TDM_SET_PROGRESS_BAR_STATE (Коммктрл. h)
description: Задает состояние индикатора выполнения в диалоговом окне задачи.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- Элементы управления Windows для TDM_SET_PROGRESS_BAR_STATE сообщений
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "104352035"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="e4787-104">TDM \_ задать \_ \_ сообщение о \_ состоянии индикатора выполнения</span><span class="sxs-lookup"><span data-stu-id="e4787-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="e4787-105">Задает состояние индикатора выполнения в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="e4787-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4787-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4787-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4787-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4787-108">Значение **типа int** , указывающее состояние индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="e4787-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="e4787-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e4787-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e4787-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e4787-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="e4787-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e4787-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="e4787-112"><dt>**ПБСТ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="e4787-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="e4787-113">Задает для индикатора выполнения нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="e4787-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="e4787-114"><dt>**ПБСТ \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="e4787-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="e4787-115">Задает состояние "приостановлено" для индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="e4787-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="e4787-116"><dt>**ПБСТ, \_ Ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="e4787-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="e4787-117">Задайте для индикатора выполнения состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="e4787-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e4787-118">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4787-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4787-119">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e4787-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4787-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4787-120">Return value</span></span>

<span data-ttu-id="e4787-121">Если функция выполнена, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e4787-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="e4787-122">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e4787-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="e4787-123">Для получения расширенной информации об ошибке вызова GetLastError.</span><span class="sxs-lookup"><span data-stu-id="e4787-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4787-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e4787-124">Requirements</span></span>



| <span data-ttu-id="e4787-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e4787-125">Requirement</span></span> | <span data-ttu-id="e4787-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e4787-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4787-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4787-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4787-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4787-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4787-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4787-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4787-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4787-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4787-131">Header</span><span class="sxs-lookup"><span data-stu-id="e4787-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4787-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4787-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





