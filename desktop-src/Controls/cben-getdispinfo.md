---
title: Код уведомления CBEN_GETDISPINFO (Коммктрл. h)
description: Отправлено, чтобы получить отображаемые сведения о элементе обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533770"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="167da-105">\_Код уведомления кбен жетдиспинфо</span><span class="sxs-lookup"><span data-stu-id="167da-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="167da-106">Отправлено, чтобы получить отображаемые сведения о элементе обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="167da-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="167da-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="167da-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="167da-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="167da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="167da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="167da-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="167da-110">Указатель на структуру [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="167da-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="167da-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="167da-111">Return value</span></span>

<span data-ttu-id="167da-112">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="167da-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="167da-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="167da-113">Remarks</span></span>

<span data-ttu-id="167da-114">Структура [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) содержит структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="167da-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="167da-115">Элемент **Mask** задает сведения, запрашиваемые элементом управления.</span><span class="sxs-lookup"><span data-stu-id="167da-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="167da-116">Заполните соответствующие члены структуры, чтобы вернуть запрошенные сведения в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="167da-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="167da-117">Если обработчик сообщений устанавливает для элемента **маски** структуры [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) значение кбеиф \_ di \_ сетитем, элемент управления сохраняет информацию и не запрашивает их снова.</span><span class="sxs-lookup"><span data-stu-id="167da-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="167da-118">Требования</span><span class="sxs-lookup"><span data-stu-id="167da-118">Requirements</span></span>



| <span data-ttu-id="167da-119">Требование</span><span class="sxs-lookup"><span data-stu-id="167da-119">Requirement</span></span> | <span data-ttu-id="167da-120">Значение</span><span class="sxs-lookup"><span data-stu-id="167da-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="167da-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="167da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="167da-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="167da-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="167da-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="167da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="167da-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="167da-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="167da-125">Header</span><span class="sxs-lookup"><span data-stu-id="167da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="167da-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="167da-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="167da-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="167da-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="167da-128">**Кбен \_ ЖЕТДИСПИНФОВ** (Юникод) и **кбен \_ жетдиспинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="167da-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





