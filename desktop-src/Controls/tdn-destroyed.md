---
title: Код уведомления TDN_DESTROYED (Коммктрл. h)
description: Отправляется диалоговым окном задачи при его уничтожении, а его маркер окна становится недействительным. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- TDN_DESTROYED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892686"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="40c8b-105">ТДН \_ разрушенный код уведомления</span><span class="sxs-lookup"><span data-stu-id="40c8b-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="40c8b-106">Отправляется диалоговым окном задачи при его уничтожении, а его маркер окна становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="40c8b-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="40c8b-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="40c8b-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="40c8b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="40c8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c8b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40c8b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40c8b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="40c8b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="40c8b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40c8b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40c8b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="40c8b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c8b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40c8b-113">Return value</span></span>

<span data-ttu-id="40c8b-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="40c8b-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c8b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="40c8b-115">Requirements</span></span>



| <span data-ttu-id="40c8b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="40c8b-116">Requirement</span></span> | <span data-ttu-id="40c8b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="40c8b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40c8b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40c8b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40c8b-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40c8b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40c8b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40c8b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40c8b-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40c8b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40c8b-122">Header</span><span class="sxs-lookup"><span data-stu-id="40c8b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c8b-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="40c8b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





