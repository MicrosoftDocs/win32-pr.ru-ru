---
title: Код уведомления HDN_ITEMKEYDOWN (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что нажата клавиша с выбранным элементом. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072009"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="06347-105">\_Код уведомления ХДН итемкэйдовн</span><span class="sxs-lookup"><span data-stu-id="06347-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="06347-106">Сообщает родительскому окну элемента управления заголовка, что нажата клавиша с выбранным элементом.</span><span class="sxs-lookup"><span data-stu-id="06347-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="06347-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="06347-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="06347-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="06347-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06347-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06347-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06347-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , которая содержит дополнительные сведения о нажатом ключе.</span><span class="sxs-lookup"><span data-stu-id="06347-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06347-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06347-111">Return value</span></span>

<span data-ttu-id="06347-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="06347-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06347-113">Требования</span><span class="sxs-lookup"><span data-stu-id="06347-113">Requirements</span></span>



| <span data-ttu-id="06347-114">Требование</span><span class="sxs-lookup"><span data-stu-id="06347-114">Requirement</span></span> | <span data-ttu-id="06347-115">Значение</span><span class="sxs-lookup"><span data-stu-id="06347-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06347-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06347-116">Minimum supported client</span></span><br/> | <span data-ttu-id="06347-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06347-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06347-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06347-118">Minimum supported server</span></span><br/> | <span data-ttu-id="06347-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06347-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06347-120">Header</span><span class="sxs-lookup"><span data-stu-id="06347-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="06347-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="06347-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





