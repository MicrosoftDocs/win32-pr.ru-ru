---
title: Код уведомления NM_RELEASEDCAPTURE (Главная панель) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления главной панели, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- Элементы управления Windows для кода уведомления NM_RELEASEDCAPTURE (Главная панель)
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
ms.openlocfilehash: 3c2f5367a0a5d5fac0948493ef70e4be1140013c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988724"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a><span data-ttu-id="d1f49-105">\_Код уведомления "NM релеаседкаптуре" (Главная панель)</span><span class="sxs-lookup"><span data-stu-id="d1f49-105">NM\_RELEASEDCAPTURE (rebar) notification code</span></span>

<span data-ttu-id="d1f49-106">Сообщает родительскому окну элемента управления главной панели, что элемент управления освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="d1f49-106">Notifies a rebar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="d1f49-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f49-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d1f49-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1f49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1f49-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1f49-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1f49-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="d1f49-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1f49-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1f49-111">Return value</span></span>

<span data-ttu-id="d1f49-112">Элемент управления игнорирует возвращаемое значение из этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="d1f49-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f49-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d1f49-113">Requirements</span></span>



| <span data-ttu-id="d1f49-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d1f49-114">Requirement</span></span> | <span data-ttu-id="d1f49-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d1f49-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f49-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1f49-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d1f49-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1f49-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1f49-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1f49-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d1f49-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1f49-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1f49-120">Header</span><span class="sxs-lookup"><span data-stu-id="d1f49-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1f49-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1f49-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





