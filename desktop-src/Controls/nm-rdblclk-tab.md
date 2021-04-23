---
title: Код уведомления NM_RDBLCLK (TAB) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул правой кнопкой мыши в элементе управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- Элементы управления Windows для кода уведомления NM_RDBLCLK (TAB)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071107"
---
# <a name="nm_rdblclk-tab-notification-code"></a><span data-ttu-id="c5b4b-105">\_Код уведомления "NM рдблклк (вкладка)"</span><span class="sxs-lookup"><span data-stu-id="c5b4b-105">NM\_RDBLCLK (tab) notification code</span></span>

<span data-ttu-id="c5b4b-106">Сообщает родительскому окну элемента управления "Вкладка", что пользователь дважды щелкнул правой кнопкой мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-106">Notifies the parent window of a tab control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="c5b4b-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c5b4b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c5b4b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5b4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b4b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5b4b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b4b-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b4b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5b4b-111">Return value</span></span>

<span data-ttu-id="c5b4b-112">Возвращает ненулевое значение, чтобы не разрешать обработку по умолчанию, или нуль, чтобы разрешить обработку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-112">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b4b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c5b4b-113">Requirements</span></span>



| <span data-ttu-id="c5b4b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c5b4b-114">Requirement</span></span> | <span data-ttu-id="c5b4b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c5b4b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b4b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5b4b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b4b-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5b4b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5b4b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5b4b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b4b-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5b4b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5b4b-120">Header</span><span class="sxs-lookup"><span data-stu-id="c5b4b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b4b-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b4b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





