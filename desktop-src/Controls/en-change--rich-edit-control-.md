---
title: Код уведомления EN_CHANGE (с расширенными возможностями редактирования) (Winuser. h)
description: Уведомляет окно главного окна элемента управления Rich Edit, что произошло изменение. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- Элементы управления Windows для кода уведомления EN_CHANGE (Rich Edit)
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988484"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="23ff7-105">\_Код уведомления о смене EN (Rich Edit)</span><span class="sxs-lookup"><span data-stu-id="23ff7-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="23ff7-106">Уведомляет окно главного окна элемента управления Rich Edit, что произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="23ff7-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="23ff7-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="23ff7-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="23ff7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23ff7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ff7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23ff7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23ff7-110">Структура [**чанженотифи**](/windows/desktop/api/Textserv/ns-textserv-changenotify) , указывающая произведенное изменение.</span><span class="sxs-lookup"><span data-stu-id="23ff7-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23ff7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23ff7-111">Return value</span></span>

<span data-ttu-id="23ff7-112">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="23ff7-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23ff7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23ff7-113">Remarks</span></span>

<span data-ttu-id="23ff7-114">Чтобы получить \_ коды уведомлений о смене, укажите [**енм \_ изменения**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**\_ SETEVENTMASK EM**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="23ff7-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ff7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="23ff7-115">Requirements</span></span>



| <span data-ttu-id="23ff7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="23ff7-116">Requirement</span></span> | <span data-ttu-id="23ff7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="23ff7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23ff7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23ff7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23ff7-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23ff7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="23ff7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23ff7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23ff7-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23ff7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23ff7-122">Header</span><span class="sxs-lookup"><span data-stu-id="23ff7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="23ff7-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ff7-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ff7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23ff7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ff7-125">**ткснотифи**</span><span class="sxs-lookup"><span data-stu-id="23ff7-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





