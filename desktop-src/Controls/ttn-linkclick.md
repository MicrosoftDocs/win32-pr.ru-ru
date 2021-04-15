---
title: Код уведомления TTN_LINKCLICK (Коммктрл. h)
description: Посылается при щелчке по текстовой ссылке внутри всплывающей подсказки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654545"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="0a2e7-105">\_Код уведомления ТТН линккликк</span><span class="sxs-lookup"><span data-stu-id="0a2e7-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="0a2e7-106">Посылается при щелчке по текстовой ссылке внутри всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="0a2e7-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="0a2e7-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0a2e7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="0a2e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a2e7-108">Parameters</span></span>

<span data-ttu-id="0a2e7-109">Этот код уведомления не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="0a2e7-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a2e7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a2e7-110">Return value</span></span>

<span data-ttu-id="0a2e7-111">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="0a2e7-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a2e7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a2e7-112">Remarks</span></span>

<span data-ttu-id="0a2e7-113">Ниже приведен пример того, когда будет отправлено это уведомление.</span><span class="sxs-lookup"><span data-stu-id="0a2e7-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="0a2e7-114">Предположим, что всплывающая подсказка содержит следующий текст: "это <A>ссылка</A>".</span><span class="sxs-lookup"><span data-stu-id="0a2e7-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="0a2e7-115">При нажатии ссылки элемент управления ToolTip отправляет \_ код уведомления ТТН линккликк.</span><span class="sxs-lookup"><span data-stu-id="0a2e7-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="0a2e7-116">Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="0a2e7-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0a2e7-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a2e7-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a2e7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0a2e7-118">Requirements</span></span>



| <span data-ttu-id="0a2e7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0a2e7-119">Requirement</span></span> | <span data-ttu-id="0a2e7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0a2e7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2e7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a2e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0a2e7-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a2e7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a2e7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a2e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0a2e7-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a2e7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a2e7-125">Header</span><span class="sxs-lookup"><span data-stu-id="0a2e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a2e7-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a2e7-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





