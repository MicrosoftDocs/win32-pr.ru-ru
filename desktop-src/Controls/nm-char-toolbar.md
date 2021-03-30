---
title: Код уведомления NM_CHAR (Toolbar) (Коммктрл. h)
description: Отправляется панелью инструментов при получении сообщения WM \_ char. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Элементы управления Windows для кода уведомления NM_CHAR (панель инструментов)
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892821"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="7791f-105">\_Код уведомления (панель инструментов) NM</span><span class="sxs-lookup"><span data-stu-id="7791f-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="7791f-106">Отправляется панелью инструментов при получении сообщения [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="7791f-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="7791f-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7791f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7791f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7791f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7791f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7791f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7791f-110">Указатель на структуру [**нмчар**](/windows/win32/api/commctrl/ns-commctrl-nmchar) , которая содержит дополнительные сведения о символе, вызвавшем код уведомления.</span><span class="sxs-lookup"><span data-stu-id="7791f-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="7791f-111">Элемент **двитемпрев** этой структуры содержит идентификатор команды, которая находится в активном виде, или значение-1, если ни один элемент не является активным.</span><span class="sxs-lookup"><span data-stu-id="7791f-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="7791f-112">Элемент **двитемнекст** этой структуры содержит идентификатор команды, который будет активным, или-1, если ключ не соответствует сочетанию клавиш любого элемента.</span><span class="sxs-lookup"><span data-stu-id="7791f-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7791f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7791f-113">Return value</span></span>

<span data-ttu-id="7791f-114">Возвращает **значение true** , указывающее, что панель инструментов не должна обрабатывать символ, и **false** , чтобы панель инструментов обрабатывала символ.</span><span class="sxs-lookup"><span data-stu-id="7791f-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="7791f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7791f-115">Requirements</span></span>



| <span data-ttu-id="7791f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7791f-116">Requirement</span></span> | <span data-ttu-id="7791f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7791f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7791f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7791f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7791f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7791f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7791f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7791f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7791f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7791f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7791f-122">Header</span><span class="sxs-lookup"><span data-stu-id="7791f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7791f-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7791f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

