---
title: Сообщение HDN_ITEMSTATEICONCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул значок состояния элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- Элементы управления Windows для HDN_ITEMSTATEICONCLICK сообщений
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493053"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="498bf-105">\_Сообщение ХДН итемстатеиконкликк</span><span class="sxs-lookup"><span data-stu-id="498bf-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="498bf-106">Сообщает родительскому окну элемента управления заголовка, что пользователь щелкнул значок состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="498bf-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="498bf-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="498bf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="498bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="498bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="498bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="498bf-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую дополнительные сведения о значке состояния, в котором была нажата кнопка.</span><span class="sxs-lookup"><span data-stu-id="498bf-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="498bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="498bf-111">Return value</span></span>

<span data-ttu-id="498bf-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="498bf-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="498bf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="498bf-113">Requirements</span></span>



| <span data-ttu-id="498bf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="498bf-114">Requirement</span></span> | <span data-ttu-id="498bf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="498bf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="498bf-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="498bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="498bf-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="498bf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="498bf-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="498bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="498bf-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="498bf-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="498bf-120">Header</span><span class="sxs-lookup"><span data-stu-id="498bf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="498bf-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="498bf-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





