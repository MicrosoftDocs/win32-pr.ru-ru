---
title: Код уведомления TTN_GETDISPINFO (Коммктрл. h)
description: Посылается элементом управления ToolTip для получения сведений, необходимых для вывода окна подсказки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892233"
---
# <a name="ttn_getdispinfo-notification-code"></a><span data-ttu-id="cee18-105">\_Код уведомления ТТН жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="cee18-105">TTN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="cee18-106">Посылается элементом управления ToolTip для получения сведений, необходимых для вывода окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="cee18-106">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="cee18-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cee18-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cee18-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cee18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cee18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cee18-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cee18-110">Указатель на структуру [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , определяющую средство, которое нуждается в тексте и получает запрошенные сведения.</span><span class="sxs-lookup"><span data-stu-id="cee18-110">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cee18-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cee18-111">Return value</span></span>

<span data-ttu-id="cee18-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="cee18-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee18-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cee18-113">Remarks</span></span>

<span data-ttu-id="cee18-114">Заполните соответствующие элементы структуры, чтобы вернуть запрошенные сведения в элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="cee18-114">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="cee18-115">Если обработчик сообщений задает для элемента **уфлагс** структуры [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) значение TTF \_ di \_ сетитем, элемент управления ToolTip сохраняет информацию и не запрашивает их снова.</span><span class="sxs-lookup"><span data-stu-id="cee18-115">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee18-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cee18-116">Requirements</span></span>



| <span data-ttu-id="cee18-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cee18-117">Requirement</span></span> | <span data-ttu-id="cee18-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cee18-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cee18-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cee18-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cee18-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cee18-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cee18-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cee18-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cee18-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cee18-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cee18-123">Header</span><span class="sxs-lookup"><span data-stu-id="cee18-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cee18-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cee18-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cee18-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="cee18-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cee18-126">**ТТН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ТТН \_ жетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cee18-126">**TTN\_GETDISPINFOW** (Unicode) and **TTN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





