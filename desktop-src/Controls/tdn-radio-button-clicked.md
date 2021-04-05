---
title: Код уведомления TDN_RADIO_BUTTON_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь выбирает переключатель или ссылку на команду в диалоговом окне задачи. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c8b16f738e4807c94a060b41b3932d0f3e07ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989365"
---
# <a name="tdn_radio_button_clicked-notification-code"></a><span data-ttu-id="f458b-105">ТДНный \_ \_ \_ код уведомления при нажатии переключателя</span><span class="sxs-lookup"><span data-stu-id="f458b-105">TDN\_RADIO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="f458b-106">Отправляется диалоговым окном задачи, когда пользователь выбирает переключатель или ссылку на команду в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="f458b-106">Sent by a task dialog when the user selects a radio button or command link in the task dialog.</span></span> <span data-ttu-id="f458b-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="f458b-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f458b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f458b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f458b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f458b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f458b-110">Значение **типа int** , указывающее идентификатор, соответствующий переключателю, который был нажат.</span><span class="sxs-lookup"><span data-stu-id="f458b-110">An **int** that specifies the ID corresponding to the radio button that was clicked.</span></span>

</dd> <dt>

<span data-ttu-id="f458b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f458b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f458b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f458b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f458b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f458b-113">Return value</span></span>

<span data-ttu-id="f458b-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f458b-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f458b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f458b-115">Requirements</span></span>



| <span data-ttu-id="f458b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f458b-116">Requirement</span></span> | <span data-ttu-id="f458b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f458b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f458b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f458b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f458b-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f458b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f458b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f458b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f458b-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f458b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f458b-122">Header</span><span class="sxs-lookup"><span data-stu-id="f458b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f458b-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f458b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





