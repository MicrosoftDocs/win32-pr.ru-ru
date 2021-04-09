---
title: Код уведомления NM_FONTCHANGED (Коммктрл. h)
description: Посылается элементом управления "представление списка", когда элемент управления изменил шрифт. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891430"
---
# <a name="nm_fontchanged-notification-code"></a><span data-ttu-id="09c87-105">\_Код уведомления фонтчанжед (NM)</span><span class="sxs-lookup"><span data-stu-id="09c87-105">NM\_FONTCHANGED notification code</span></span>

<span data-ttu-id="09c87-106">Посылается элементом управления "представление списка", когда элемент управления изменил шрифт.</span><span class="sxs-lookup"><span data-stu-id="09c87-106">Sent by a list-view control when the control has changed a font.</span></span> <span data-ttu-id="09c87-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="09c87-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="09c87-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="09c87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09c87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09c87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09c87-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="09c87-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09c87-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09c87-111">Return value</span></span>

<span data-ttu-id="09c87-112">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="09c87-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="09c87-113">Требования</span><span class="sxs-lookup"><span data-stu-id="09c87-113">Requirements</span></span>



| <span data-ttu-id="09c87-114">Требование</span><span class="sxs-lookup"><span data-stu-id="09c87-114">Requirement</span></span> | <span data-ttu-id="09c87-115">Значение</span><span class="sxs-lookup"><span data-stu-id="09c87-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09c87-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09c87-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09c87-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09c87-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09c87-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09c87-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09c87-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09c87-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09c87-120">Header</span><span class="sxs-lookup"><span data-stu-id="09c87-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="09c87-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="09c87-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





