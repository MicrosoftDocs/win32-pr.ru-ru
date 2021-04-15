---
title: Код уведомления CBEN_BEGINEDIT (Коммктрл. h)
description: Посылается, когда пользователь активирует раскрывающийся список или щелкает поле ввода элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- CBEN_BEGINEDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654675"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="66420-105">\_Код уведомления кбен BEGINEDIT</span><span class="sxs-lookup"><span data-stu-id="66420-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="66420-106">Посылается, когда пользователь активирует раскрывающийся список или щелкает поле ввода элемента управления.</span><span class="sxs-lookup"><span data-stu-id="66420-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="66420-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="66420-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="66420-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="66420-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66420-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66420-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66420-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="66420-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66420-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66420-111">Return value</span></span>

<span data-ttu-id="66420-112">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="66420-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="66420-113">Требования</span><span class="sxs-lookup"><span data-stu-id="66420-113">Requirements</span></span>



| <span data-ttu-id="66420-114">Требование</span><span class="sxs-lookup"><span data-stu-id="66420-114">Requirement</span></span> | <span data-ttu-id="66420-115">Значение</span><span class="sxs-lookup"><span data-stu-id="66420-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66420-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66420-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66420-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66420-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66420-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66420-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66420-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66420-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66420-120">Header</span><span class="sxs-lookup"><span data-stu-id="66420-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66420-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="66420-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





