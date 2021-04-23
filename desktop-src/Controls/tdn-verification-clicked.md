---
title: Код уведомления TDN_VERIFICATION_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь нажимает флажок "Проверка диалогового окна задачи". Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989364"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="092bf-105">\_ \_ Код уведомления о нажатии ТДН проверки</span><span class="sxs-lookup"><span data-stu-id="092bf-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="092bf-106">Отправляется диалоговым окном задачи, когда пользователь нажимает флажок "Проверка диалогового окна задачи".</span><span class="sxs-lookup"><span data-stu-id="092bf-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="092bf-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="092bf-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="092bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="092bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="092bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="092bf-110">**Логическое** значение, указывающее состояние флажка проверки.</span><span class="sxs-lookup"><span data-stu-id="092bf-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="092bf-111">**Значение true** , если флажок проверки установлен, или **значение false** , если флажок снят.</span><span class="sxs-lookup"><span data-stu-id="092bf-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="092bf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="092bf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="092bf-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="092bf-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092bf-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="092bf-114">Return value</span></span>

<span data-ttu-id="092bf-115">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="092bf-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="092bf-116">Требования</span><span class="sxs-lookup"><span data-stu-id="092bf-116">Requirements</span></span>



| <span data-ttu-id="092bf-117">Требование</span><span class="sxs-lookup"><span data-stu-id="092bf-117">Requirement</span></span> | <span data-ttu-id="092bf-118">Значение</span><span class="sxs-lookup"><span data-stu-id="092bf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="092bf-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="092bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="092bf-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="092bf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="092bf-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="092bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="092bf-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="092bf-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="092bf-123">Header</span><span class="sxs-lookup"><span data-stu-id="092bf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="092bf-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="092bf-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="092bf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="092bf-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="092bf-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="092bf-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="092bf-127">*таскдиалогкаллбаккпрок*</span><span class="sxs-lookup"><span data-stu-id="092bf-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

