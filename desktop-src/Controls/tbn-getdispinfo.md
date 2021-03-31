---
title: Код уведомления TBN_GETDISPINFO (Коммктрл. h)
description: Извлекает отображаемые сведения об элементе панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO кода уведомления элементы управления Windows
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136798"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="01056-105">\_Код уведомления ТБН жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="01056-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="01056-106">Извлекает отображаемые сведения об элементе панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="01056-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="01056-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="01056-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="01056-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01056-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01056-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01056-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01056-110">Указатель на структуру [**нмтбдиспинфо**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="01056-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="01056-111">Элемент **идкомманд** указывает идентификатор команды элемента, член **lParam** содержит определяемые приложением данные элемента, а член **двмаск** указывает, какие сведения запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="01056-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01056-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01056-112">Return value</span></span>

<span data-ttu-id="01056-113">Возвращаемое значение игнорируется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="01056-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="01056-114">Требования</span><span class="sxs-lookup"><span data-stu-id="01056-114">Requirements</span></span>



| <span data-ttu-id="01056-115">Требование</span><span class="sxs-lookup"><span data-stu-id="01056-115">Requirement</span></span> | <span data-ttu-id="01056-116">Значение</span><span class="sxs-lookup"><span data-stu-id="01056-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01056-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01056-117">Minimum supported client</span></span><br/> | <span data-ttu-id="01056-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01056-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01056-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01056-119">Minimum supported server</span></span><br/> | <span data-ttu-id="01056-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01056-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01056-121">Header</span><span class="sxs-lookup"><span data-stu-id="01056-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="01056-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="01056-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="01056-123">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="01056-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="01056-124">**ТБН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ТБН \_ жетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="01056-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





