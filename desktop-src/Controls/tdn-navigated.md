---
title: Код уведомления TDN_NAVIGATED (Коммктрл. h)
description: Отправляется диалоговым окном задачи при переходе. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- TDN_NAVIGATED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535435"
---
# <a name="tdn_navigated-notification-code"></a><span data-ttu-id="b8572-105">\_Код уведомления ТДН с навигацией</span><span class="sxs-lookup"><span data-stu-id="b8572-105">TDN\_NAVIGATED notification code</span></span>

<span data-ttu-id="b8572-106">Отправляется диалоговым окном задачи при переходе.</span><span class="sxs-lookup"><span data-stu-id="b8572-106">Sent by a task dialog when navigation has occurred.</span></span> <span data-ttu-id="b8572-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="b8572-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b8572-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8572-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8572-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8572-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8572-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b8572-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b8572-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8572-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8572-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b8572-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8572-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8572-113">Return value</span></span>

<span data-ttu-id="b8572-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b8572-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8572-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b8572-115">Requirements</span></span>



| <span data-ttu-id="b8572-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b8572-116">Requirement</span></span> | <span data-ttu-id="b8572-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b8572-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8572-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8572-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8572-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8572-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8572-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8572-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8572-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8572-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8572-122">Header</span><span class="sxs-lookup"><span data-stu-id="b8572-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8572-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8572-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





