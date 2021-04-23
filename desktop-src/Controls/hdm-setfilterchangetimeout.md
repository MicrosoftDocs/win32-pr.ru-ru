---
title: Сообщение HDM_SETFILTERCHANGETIMEOUT (Коммктрл. h)
description: Устанавливает интервал времени ожидания между временем изменения атрибутов фильтра и разноски \_ уведомления ХДН филтерчанже. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетфилтерчанжетимеаут.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Элементы управления Windows для HDM_SETFILTERCHANGETIMEOUT сообщений
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071873"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="e41de-105">\_Сообщение СЕТФИЛТЕРЧАНЖЕТИМЕАУТ HDM</span><span class="sxs-lookup"><span data-stu-id="e41de-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="e41de-106">Устанавливает интервал времени ожидания между временем изменения атрибутов фильтра и разноски уведомления [ХДН \_ филтерчанже](hdn-filterchange.md) .</span><span class="sxs-lookup"><span data-stu-id="e41de-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="e41de-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетфилтерчанжетимеаут**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .</span><span class="sxs-lookup"><span data-stu-id="e41de-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e41de-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e41de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e41de-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e41de-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e41de-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e41de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e41de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e41de-112">Значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="e41de-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41de-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e41de-113">Return value</span></span>

<span data-ttu-id="e41de-114">Возвращает индекс изменяемого элемента управления фильтра.</span><span class="sxs-lookup"><span data-stu-id="e41de-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41de-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e41de-115">Requirements</span></span>



| <span data-ttu-id="e41de-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e41de-116">Requirement</span></span> | <span data-ttu-id="e41de-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e41de-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e41de-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e41de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e41de-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e41de-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e41de-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e41de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e41de-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e41de-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e41de-122">Header</span><span class="sxs-lookup"><span data-stu-id="e41de-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e41de-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e41de-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41de-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e41de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41de-125">ХДН \_ филтерчанже</span><span class="sxs-lookup"><span data-stu-id="e41de-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





