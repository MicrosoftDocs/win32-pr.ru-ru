---
title: Код уведомления NM_RELEASEDCAPTURE (Toolbar) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления ToolBar, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- Элементы управления Windows для кода уведомления NM_RELEASEDCAPTURE (панель инструментов)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d915b3af073ba0c6b5c74a7b13317f7b2d4ab8a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136051"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a><span data-ttu-id="677a5-105">\_Код уведомления "NM релеаседкаптуре (панель инструментов)"</span><span class="sxs-lookup"><span data-stu-id="677a5-105">NM\_RELEASEDCAPTURE (toolbar) notification code</span></span>

<span data-ttu-id="677a5-106">Сообщает родительскому окну элемента управления ToolBar, что элемент управления освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="677a5-106">Notifies a toolbar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="677a5-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="677a5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="677a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="677a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="677a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="677a5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="677a5-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="677a5-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="677a5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="677a5-111">Return value</span></span>

<span data-ttu-id="677a5-112">Элемент управления игнорирует возвращаемое значение из этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="677a5-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="677a5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="677a5-113">Requirements</span></span>



| <span data-ttu-id="677a5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="677a5-114">Requirement</span></span> | <span data-ttu-id="677a5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="677a5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="677a5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="677a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="677a5-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="677a5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="677a5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="677a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="677a5-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="677a5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="677a5-120">Header</span><span class="sxs-lookup"><span data-stu-id="677a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="677a5-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="677a5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





