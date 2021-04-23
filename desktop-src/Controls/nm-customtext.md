---
title: Код уведомления NM_CUSTOMTEXT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления о пользовательских операциях с текстом. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414737"
---
# <a name="nm_customtext-notification-code"></a><span data-ttu-id="ce2bd-105">\_Код уведомления кустомтекст (NM)</span><span class="sxs-lookup"><span data-stu-id="ce2bd-105">NM\_CUSTOMTEXT notification code</span></span>

<span data-ttu-id="ce2bd-106">Сообщает родительскому окну элемента управления о пользовательских операциях с текстом.</span><span class="sxs-lookup"><span data-stu-id="ce2bd-106">Notifies a control's parent window about custom text operations.</span></span> <span data-ttu-id="ce2bd-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ce2bd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ce2bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce2bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce2bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2bd-110">Указатель на структуру [**нмкустомтекст**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="ce2bd-110">A pointer to an [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce2bd-111">Return value</span></span>

<span data-ttu-id="ce2bd-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ce2bd-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2bd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ce2bd-113">Requirements</span></span>



| <span data-ttu-id="ce2bd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ce2bd-114">Requirement</span></span> | <span data-ttu-id="ce2bd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ce2bd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2bd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce2bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2bd-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce2bd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce2bd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce2bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2bd-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce2bd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce2bd-120">Header</span><span class="sxs-lookup"><span data-stu-id="ce2bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2bd-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce2bd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





