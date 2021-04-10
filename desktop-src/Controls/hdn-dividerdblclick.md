---
title: Код уведомления HDN_DIVIDERDBLCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь дважды щелкнул область разделителя элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072036"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="799bf-105">\_Код уведомления ХДН дивидердблкликк</span><span class="sxs-lookup"><span data-stu-id="799bf-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="799bf-106">Сообщает родительскому окну элемента управления заголовка, что пользователь дважды щелкнул область разделителя элемента управления.</span><span class="sxs-lookup"><span data-stu-id="799bf-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="799bf-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="799bf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="799bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="799bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="799bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="799bf-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления "заголовок", и элемент, разделитель которого был двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="799bf-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="799bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="799bf-111">Return value</span></span>

<span data-ttu-id="799bf-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="799bf-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="799bf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="799bf-113">Requirements</span></span>



| <span data-ttu-id="799bf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="799bf-114">Requirement</span></span> | <span data-ttu-id="799bf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="799bf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="799bf-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="799bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="799bf-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="799bf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="799bf-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="799bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="799bf-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="799bf-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="799bf-120">Header</span><span class="sxs-lookup"><span data-stu-id="799bf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="799bf-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="799bf-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="799bf-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="799bf-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="799bf-123">**ХДН \_ ДИВИДЕРДБЛКЛИККВ** (Юникод) и **ХДН \_ дивидердблкликка** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="799bf-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 





