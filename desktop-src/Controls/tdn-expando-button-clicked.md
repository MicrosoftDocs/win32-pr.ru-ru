---
title: Код уведомления TDN_EXPANDO_BUTTON_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь нажимает кнопку "expando" диалогового окна. Это уведомление получено только с помощью функции обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654699"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="70709-105">\_ \_ \_ Код уведомления при нажатии кнопки expando ТДН</span><span class="sxs-lookup"><span data-stu-id="70709-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="70709-106">Отправляется диалоговым окном задачи, когда пользователь нажимает кнопку "expando" диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="70709-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="70709-107">Это уведомление получено только с помощью функции обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="70709-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="70709-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="70709-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70709-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70709-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70709-110">**Логическое** значение, равное **true** , если диалоговое окно развернуто, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="70709-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="70709-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70709-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70709-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="70709-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70709-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70709-113">Return value</span></span>

<span data-ttu-id="70709-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="70709-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="70709-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70709-115">Remarks</span></span>

<span data-ttu-id="70709-116">Пример в разделе синтаксиса показывает приведение к wParam перед отправкой уведомления.</span><span class="sxs-lookup"><span data-stu-id="70709-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="70709-117">**LParam** не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="70709-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="70709-118">Требования</span><span class="sxs-lookup"><span data-stu-id="70709-118">Requirements</span></span>



| <span data-ttu-id="70709-119">Требование</span><span class="sxs-lookup"><span data-stu-id="70709-119">Requirement</span></span> | <span data-ttu-id="70709-120">Значение</span><span class="sxs-lookup"><span data-stu-id="70709-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70709-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70709-121">Minimum supported client</span></span><br/> | <span data-ttu-id="70709-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70709-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70709-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70709-123">Minimum supported server</span></span><br/> | <span data-ttu-id="70709-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70709-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70709-125">Header</span><span class="sxs-lookup"><span data-stu-id="70709-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="70709-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="70709-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





