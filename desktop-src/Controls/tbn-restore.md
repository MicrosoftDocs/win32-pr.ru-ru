---
title: Код уведомления TBN_RESTORE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что панель инструментов находится в процессе восстановления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491976"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="6492f-105">\_Код уведомления о восстановлении ТБН</span><span class="sxs-lookup"><span data-stu-id="6492f-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="6492f-106">Сообщает родительскому окну панели инструментов, что панель инструментов находится в процессе восстановления.</span><span class="sxs-lookup"><span data-stu-id="6492f-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="6492f-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6492f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6492f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6492f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6492f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6492f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6492f-110">Указатель на структуру [**нмтбресторе**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .</span><span class="sxs-lookup"><span data-stu-id="6492f-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6492f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6492f-111">Return value</span></span>

<span data-ttu-id="6492f-112">Приложение должно вернуть ноль в ответ на первый ТБН код уведомления о **\_ восстановлении** , полученный в начале процесса восстановления, чтобы продолжить восстановление сведений о кнопке.</span><span class="sxs-lookup"><span data-stu-id="6492f-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="6492f-113">Если приложение возвращает ненулевое значение, процесс восстановления отменяется.</span><span class="sxs-lookup"><span data-stu-id="6492f-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="6492f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6492f-114">Remarks</span></span>

<span data-ttu-id="6492f-115">Приложение получит этот код уведомления один раз в начале процесса восстановления и один раз для каждой кнопки.</span><span class="sxs-lookup"><span data-stu-id="6492f-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="6492f-116">Этот код уведомления позволяет извлекать сведения из потока данных, сохраненного ранее.</span><span class="sxs-lookup"><span data-stu-id="6492f-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="6492f-117">Если вы не сохранили какую бы то ни было информации, пропустите код уведомления.</span><span class="sxs-lookup"><span data-stu-id="6492f-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="6492f-118">Дополнительные сведения об обработке **ТБН \_ RESTORE** см. в статье [Настройка панелей инструментов](toolbar-controls-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="6492f-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6492f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6492f-119">Requirements</span></span>



| <span data-ttu-id="6492f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6492f-120">Requirement</span></span> | <span data-ttu-id="6492f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6492f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6492f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6492f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6492f-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6492f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6492f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6492f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6492f-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6492f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6492f-126">Header</span><span class="sxs-lookup"><span data-stu-id="6492f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6492f-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6492f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





