---
title: Код уведомления RBN_AUTOSIZE (Коммктрл. h)
description: Посылается элементом управления главной панели, созданным с помощью стиля автомасштабирования RBS, \_ когда Главная панель автоматически изменяет размер. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654702"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="483c3-105">\_Код уведомления РБН AUTOSIZE</span><span class="sxs-lookup"><span data-stu-id="483c3-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="483c3-106">Посылается элементом управления главной панели, созданным с помощью стиля автомасштабирования [**RBS \_**](rebar-control-styles.md) , когда Главная панель автоматически изменяет размер.</span><span class="sxs-lookup"><span data-stu-id="483c3-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="483c3-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="483c3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="483c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="483c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="483c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="483c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="483c3-110">Указатель на структуру [**нмрбаутосизе**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) , содержащую сведения об операции изменения размера.</span><span class="sxs-lookup"><span data-stu-id="483c3-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="483c3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="483c3-111">Return value</span></span>

<span data-ttu-id="483c3-112">Возвращаемое значение для этого уведомления не используется.</span><span class="sxs-lookup"><span data-stu-id="483c3-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="483c3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="483c3-113">Requirements</span></span>



| <span data-ttu-id="483c3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="483c3-114">Requirement</span></span> | <span data-ttu-id="483c3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="483c3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="483c3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="483c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="483c3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="483c3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="483c3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="483c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="483c3-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="483c3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="483c3-120">Header</span><span class="sxs-lookup"><span data-stu-id="483c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="483c3-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="483c3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





