---
title: Код уведомления TBN_SAVE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что панель инструментов находится в процессе сохранения. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804001"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="0ad85-105">ТБН \_ сохранить код уведомления</span><span class="sxs-lookup"><span data-stu-id="0ad85-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="0ad85-106">Сообщает родительскому окну панели инструментов, что панель инструментов находится в процессе сохранения.</span><span class="sxs-lookup"><span data-stu-id="0ad85-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="0ad85-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad85-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0ad85-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ad85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ad85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad85-110">Указатель на структуру [**нмтбсаве**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .</span><span class="sxs-lookup"><span data-stu-id="0ad85-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad85-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ad85-111">Return value</span></span>

<span data-ttu-id="0ad85-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0ad85-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ad85-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ad85-113">Remarks</span></span>

<span data-ttu-id="0ad85-114">Приложение получит этот код уведомления один раз в начале процесса сохранения и один раз для каждой кнопки.</span><span class="sxs-lookup"><span data-stu-id="0ad85-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="0ad85-115">Этот код уведомления позволяет добавлять в оболочку собственные сведения, сохраненные с помощью оболочки.</span><span class="sxs-lookup"><span data-stu-id="0ad85-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="0ad85-116">Если вы не хотите добавлять сведения, пропустите код уведомления.</span><span class="sxs-lookup"><span data-stu-id="0ad85-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="0ad85-117">Дополнительные сведения об обработке ТБН Save см. в статье [Настройка панелей инструментов](toolbar-controls-overview.md) \_ .</span><span class="sxs-lookup"><span data-stu-id="0ad85-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad85-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0ad85-118">Requirements</span></span>



| <span data-ttu-id="0ad85-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0ad85-119">Requirement</span></span> | <span data-ttu-id="0ad85-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad85-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad85-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ad85-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad85-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ad85-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ad85-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ad85-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad85-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ad85-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ad85-125">Header</span><span class="sxs-lookup"><span data-stu-id="0ad85-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ad85-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ad85-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ad85-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ad85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad85-128">\_Восстановление ТБН</span><span class="sxs-lookup"><span data-stu-id="0ad85-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





