---
title: Код уведомления HDN_ITEMDBLCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь дважды щелкнул элемент управления. Этот код уведомления отправляется в виде \_ сообщения WM notify. Только элементы управления "заголовок", для которых задан \_ стиль кнопки HDS, отправляют этот код уведомления.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262220"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="f55f9-106">\_Код уведомления ХДН итемдблкликк</span><span class="sxs-lookup"><span data-stu-id="f55f9-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="f55f9-107">Сообщает родительскому окну элемента управления заголовка, что пользователь дважды щелкнул элемент управления.</span><span class="sxs-lookup"><span data-stu-id="f55f9-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="f55f9-108">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f55f9-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="f55f9-109">Только элементы управления "заголовок", для которых задан стиль [**\_ кнопки HDS**](header-control-styles.md) , отправляют этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f55f9-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f55f9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f55f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f55f9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f55f9-112">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="f55f9-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55f9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f55f9-113">Return value</span></span>

<span data-ttu-id="f55f9-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f55f9-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55f9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f55f9-115">Requirements</span></span>



| <span data-ttu-id="f55f9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f55f9-116">Requirement</span></span> | <span data-ttu-id="f55f9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f55f9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f55f9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f55f9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f55f9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f55f9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f55f9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f55f9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f55f9-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f55f9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f55f9-122">Header</span><span class="sxs-lookup"><span data-stu-id="f55f9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55f9-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55f9-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f55f9-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f55f9-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f55f9-125">**ХДН \_ ИТЕМДБЛКЛИККВ** (Юникод) и **ХДН \_ итемдблкликка** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f55f9-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 





