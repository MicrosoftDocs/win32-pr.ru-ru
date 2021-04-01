---
title: Код уведомления HDN_BEGINFILTEREDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что началось изменение фильтра. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- HDN_BEGINFILTEREDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989457"
---
# <a name="hdn_beginfilteredit-notification-code"></a><span data-ttu-id="315c1-105">\_Код уведомления ХДН бегинфилтередит</span><span class="sxs-lookup"><span data-stu-id="315c1-105">HDN\_BEGINFILTEREDIT notification code</span></span>

<span data-ttu-id="315c1-106">Сообщает родительскому окну элемента управления заголовка, что началось изменение фильтра.</span><span class="sxs-lookup"><span data-stu-id="315c1-106">Notifies a header control's parent window that a filter edit has begun.</span></span> <span data-ttu-id="315c1-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="315c1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="315c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="315c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="315c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="315c1-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую дополнительные сведения о редактируемом фильтре.</span><span class="sxs-lookup"><span data-stu-id="315c1-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315c1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="315c1-111">Return value</span></span>

<span data-ttu-id="315c1-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="315c1-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="315c1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="315c1-113">Requirements</span></span>



| <span data-ttu-id="315c1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="315c1-114">Requirement</span></span> | <span data-ttu-id="315c1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="315c1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="315c1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="315c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="315c1-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="315c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="315c1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="315c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="315c1-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="315c1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="315c1-120">Header</span><span class="sxs-lookup"><span data-stu-id="315c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="315c1-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="315c1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





