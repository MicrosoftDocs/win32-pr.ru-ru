---
title: Код уведомления HDN_OVERFLOWCLICK (Коммктрл. h)
description: Посылается элементом управления "заголовок" родительскому элементу при нажатии кнопки переполнения заголовка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892022"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="50d8d-105">\_Код уведомления ХДН оверфловкликк</span><span class="sxs-lookup"><span data-stu-id="50d8d-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="50d8d-106">Посылается элементом управления "заголовок" родительскому элементу при нажатии кнопки переполнения заголовка.</span><span class="sxs-lookup"><span data-stu-id="50d8d-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="50d8d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="50d8d-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="50d8d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50d8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d8d-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50d8d-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d8d-110">Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , описывающую код уведомления.</span><span class="sxs-lookup"><span data-stu-id="50d8d-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="50d8d-111">Вызывающий процесс отвечает за выделение этой структуры, включая вложенную структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="50d8d-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="50d8d-112">Задайте элементы структуры **NMHDR** , включая элемент *кода* , который должен иметь значение ХДН \_ оверфловкликк.</span><span class="sxs-lookup"><span data-stu-id="50d8d-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="50d8d-113">Задайте для элемента **Член iItem** структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) индекс первого элемента заголовка, который не является видимым, и, таким же, должен быть отображен при переполнении.</span><span class="sxs-lookup"><span data-stu-id="50d8d-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d8d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50d8d-114">Return value</span></span>

<span data-ttu-id="50d8d-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="50d8d-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d8d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50d8d-116">Remarks</span></span>

<span data-ttu-id="50d8d-117">Получатель уведомлений выполняет приведение **lParam** для получения структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="50d8d-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="50d8d-118">**WParam** содержит идентификатор элемента управления, который отправляет уведомление.</span><span class="sxs-lookup"><span data-stu-id="50d8d-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="50d8d-119">Это сообщение отправляется, только если для элемента управления "заголовок" задано [**\_ переполнение Style HDS**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="50d8d-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="50d8d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="50d8d-120">Requirements</span></span>



| <span data-ttu-id="50d8d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="50d8d-121">Requirement</span></span> | <span data-ttu-id="50d8d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="50d8d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50d8d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50d8d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="50d8d-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50d8d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50d8d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50d8d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="50d8d-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50d8d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50d8d-127">Header</span><span class="sxs-lookup"><span data-stu-id="50d8d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d8d-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d8d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





