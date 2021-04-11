---
title: Код уведомления TDN_HELP (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь нажимает клавишу F1 на клавиатуре, пока диалоговое окно находится в фокусе. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- TDN_HELP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137603"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="cfe91-105">\_Код уведомления ТДН Help</span><span class="sxs-lookup"><span data-stu-id="cfe91-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="cfe91-106">Отправляется диалоговым окном задачи, когда пользователь нажимает клавишу F1 на клавиатуре, пока диалоговое окно находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="cfe91-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="cfe91-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="cfe91-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="cfe91-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfe91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfe91-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe91-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cfe91-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfe91-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfe91-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe91-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cfe91-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe91-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfe91-113">Return value</span></span>

<span data-ttu-id="cfe91-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cfe91-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe91-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cfe91-115">Requirements</span></span>



| <span data-ttu-id="cfe91-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cfe91-116">Requirement</span></span> | <span data-ttu-id="cfe91-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cfe91-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe91-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfe91-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe91-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfe91-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfe91-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfe91-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe91-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cfe91-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfe91-122">Header</span><span class="sxs-lookup"><span data-stu-id="cfe91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfe91-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe91-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





