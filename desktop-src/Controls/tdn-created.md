---
title: Код уведомления TDN_CREATED (Коммктрл. h)
description: Отправляется диалоговым окном задачи после создания диалогового окна и до его отображения. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- TDN_CREATED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989370"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="075ec-105">ТДН \_ созданный код уведомления</span><span class="sxs-lookup"><span data-stu-id="075ec-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="075ec-106">Отправляется диалоговым окном задачи после создания диалогового окна и до его отображения.</span><span class="sxs-lookup"><span data-stu-id="075ec-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="075ec-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="075ec-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="075ec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="075ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="075ec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="075ec-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="075ec-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="075ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="075ec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="075ec-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="075ec-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="075ec-113">Return value</span></span>

<span data-ttu-id="075ec-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="075ec-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="075ec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="075ec-115">Requirements</span></span>



| <span data-ttu-id="075ec-116">Требование</span><span class="sxs-lookup"><span data-stu-id="075ec-116">Requirement</span></span> | <span data-ttu-id="075ec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="075ec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="075ec-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="075ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="075ec-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="075ec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="075ec-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="075ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="075ec-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="075ec-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="075ec-122">Header</span><span class="sxs-lookup"><span data-stu-id="075ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="075ec-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="075ec-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





