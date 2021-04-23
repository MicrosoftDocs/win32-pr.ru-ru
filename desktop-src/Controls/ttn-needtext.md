---
title: Код уведомления TTN_NEEDTEXT (Коммктрл. h)
description: Посылается элементом управления ToolTip для получения сведений, необходимых для вывода окна подсказки. Этот код уведомления идентичен ТТН \_ жетдиспинфо. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136395"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="7dc97-106">\_Код уведомления ТТН нидтекст</span><span class="sxs-lookup"><span data-stu-id="7dc97-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="7dc97-107">Посылается элементом управления ToolTip для получения сведений, необходимых для вывода окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="7dc97-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="7dc97-108">Этот код уведомления идентичен [ТТН \_ жетдиспинфо](ttn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="7dc97-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="7dc97-109">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc97-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7dc97-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dc97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc97-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dc97-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc97-112">Указатель на структуру [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , определяющую средство, которое нуждается в тексте и получает запрошенные сведения.</span><span class="sxs-lookup"><span data-stu-id="7dc97-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc97-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dc97-113">Return value</span></span>

<span data-ttu-id="7dc97-114">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="7dc97-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc97-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7dc97-115">Remarks</span></span>

<span data-ttu-id="7dc97-116">Заполните соответствующие элементы структуры, чтобы вернуть запрошенные сведения в элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="7dc97-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="7dc97-117">Если обработчик сообщений задает для элемента **уфлагс** структуры [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) значение TTF \_ di \_ сетитем, элемент управления ToolTip сохраняет информацию и не запрашивает их снова.</span><span class="sxs-lookup"><span data-stu-id="7dc97-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc97-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7dc97-118">Requirements</span></span>



| <span data-ttu-id="7dc97-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7dc97-119">Requirement</span></span> | <span data-ttu-id="7dc97-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7dc97-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc97-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dc97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc97-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dc97-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dc97-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dc97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc97-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7dc97-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dc97-125">Header</span><span class="sxs-lookup"><span data-stu-id="7dc97-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc97-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc97-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7dc97-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7dc97-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7dc97-128">**ТТН \_ НИДТЕКСТВ** (Юникод) и **ТТН \_ нидтекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7dc97-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 





