---
title: Код уведомления TBN_BEGINDRAG (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь начал перетаскивать кнопку на панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- TBN_BEGINDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135451"
---
# <a name="tbn_begindrag-notification-code"></a><span data-ttu-id="6a4f9-105">\_Код уведомления ТБН бегиндраг</span><span class="sxs-lookup"><span data-stu-id="6a4f9-105">TBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="6a4f9-106">Сообщает родительскому окну панели инструментов, что пользователь начал перетаскивать кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="6a4f9-106">Notifies a toolbar's parent window that the user has begun dragging a button in a toolbar.</span></span> <span data-ttu-id="6a4f9-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6a4f9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6a4f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a4f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a4f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a4f9-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="6a4f9-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="6a4f9-111">Элемент **Член iItem** содержит идентификатор команды для перетаскивания кнопки.</span><span class="sxs-lookup"><span data-stu-id="6a4f9-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4f9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a4f9-112">Return value</span></span>

<span data-ttu-id="6a4f9-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6a4f9-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4f9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6a4f9-114">Requirements</span></span>



| <span data-ttu-id="6a4f9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6a4f9-115">Requirement</span></span> | <span data-ttu-id="6a4f9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6a4f9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4f9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a4f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4f9-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a4f9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a4f9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a4f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4f9-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a4f9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a4f9-121">Header</span><span class="sxs-lookup"><span data-stu-id="6a4f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a4f9-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4f9-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





