---
title: Код уведомления TDN_BUTTON_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь выбирает кнопку или ссылку на команду в диалоговом окне задачи. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989369"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="93a5f-105">\_ \_ Код уведомления при нажатии кнопки ТДН</span><span class="sxs-lookup"><span data-stu-id="93a5f-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="93a5f-106">Отправляется диалоговым окном задачи, когда пользователь выбирает кнопку или ссылку на команду в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="93a5f-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="93a5f-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="93a5f-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="93a5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="93a5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93a5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93a5f-110">Значение **типа int** , указывающее идентификатор выбранной кнопки или ссылки командную.</span><span class="sxs-lookup"><span data-stu-id="93a5f-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="93a5f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93a5f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93a5f-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="93a5f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a5f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93a5f-113">Return value</span></span>

<span data-ttu-id="93a5f-114">Чтобы предотвратить закрытие диалогового окна задачи, приложение должно вернуть **\_ значение false**, в противном случае диалоговое окно задачи закрывается, а идентификатор кнопки возвращается с помощью исходного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="93a5f-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a5f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="93a5f-115">Requirements</span></span>



| <span data-ttu-id="93a5f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="93a5f-116">Requirement</span></span> | <span data-ttu-id="93a5f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="93a5f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93a5f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93a5f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93a5f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93a5f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93a5f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93a5f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93a5f-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93a5f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93a5f-122">Header</span><span class="sxs-lookup"><span data-stu-id="93a5f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a5f-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="93a5f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





