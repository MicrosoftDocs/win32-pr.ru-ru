---
title: Код уведомления NM_TVSTATEIMAGECHANGING (Коммктрл. h)
description: Посылается элементом управления иерархического представления в родительское окно, которое изменяется изображением состояния. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- NM_TVSTATEIMAGECHANGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135578"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="76d21-105">\_Код уведомления твстатеимажечангинг (NM)</span><span class="sxs-lookup"><span data-stu-id="76d21-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="76d21-106">Посылается элементом управления иерархического представления в родительское окно, которое изменяется изображением состояния.</span><span class="sxs-lookup"><span data-stu-id="76d21-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="76d21-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="76d21-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="76d21-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76d21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76d21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d21-110">Указатель на структуру [**нмтвстатеимажечангинг**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="76d21-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d21-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76d21-111">Return value</span></span>

<span data-ttu-id="76d21-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="76d21-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d21-113">Требования</span><span class="sxs-lookup"><span data-stu-id="76d21-113">Requirements</span></span>



| <span data-ttu-id="76d21-114">Требование</span><span class="sxs-lookup"><span data-stu-id="76d21-114">Requirement</span></span> | <span data-ttu-id="76d21-115">Значение</span><span class="sxs-lookup"><span data-stu-id="76d21-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76d21-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76d21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="76d21-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76d21-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76d21-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76d21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="76d21-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76d21-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76d21-120">Header</span><span class="sxs-lookup"><span data-stu-id="76d21-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d21-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d21-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





