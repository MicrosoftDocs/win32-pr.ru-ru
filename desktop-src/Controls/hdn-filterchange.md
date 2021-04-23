---
title: Код уведомления HDN_FILTERCHANGE (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что атрибуты фильтра элемента управления заголовков изменяются или редактируются. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489270"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="66e1e-105">\_Код уведомления ХДН филтерчанже</span><span class="sxs-lookup"><span data-stu-id="66e1e-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="66e1e-106">Сообщает родительскому окну элемента управления заголовка, что атрибуты фильтра элемента управления заголовков изменяются или редактируются.</span><span class="sxs-lookup"><span data-stu-id="66e1e-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="66e1e-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="66e1e-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="66e1e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="66e1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66e1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66e1e-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления заголовка и элементе заголовка, включая атрибуты, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="66e1e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e1e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66e1e-111">Return value</span></span>

<span data-ttu-id="66e1e-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="66e1e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e1e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="66e1e-113">Requirements</span></span>



| <span data-ttu-id="66e1e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="66e1e-114">Requirement</span></span> | <span data-ttu-id="66e1e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="66e1e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66e1e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66e1e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66e1e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66e1e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66e1e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66e1e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66e1e-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66e1e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66e1e-120">Header</span><span class="sxs-lookup"><span data-stu-id="66e1e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e1e-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="66e1e-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e1e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66e1e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e1e-123">**\_СЕТФИЛТЕРЧАНЖЕТИМЕАУТ HDM**</span><span class="sxs-lookup"><span data-stu-id="66e1e-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





