---
title: Код уведомления TVN_DELETEITEM (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что элемент удаляется. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490839"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="c75fa-105">\_Код уведомления ТВН DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="c75fa-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="c75fa-106">Сообщает родительскому окну элемента управления древовидного представления о том, что элемент удаляется.</span><span class="sxs-lookup"><span data-stu-id="c75fa-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="c75fa-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c75fa-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="c75fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c75fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c75fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c75fa-110">Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="c75fa-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="c75fa-111">Элемент **итемолд** — это структура [**Твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , элементы **хитем** и **lParam** которой содержат действительные сведения об удаляемом элементе.</span><span class="sxs-lookup"><span data-stu-id="c75fa-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75fa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c75fa-112">Return value</span></span>

<span data-ttu-id="c75fa-113">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c75fa-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75fa-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c75fa-114">Remarks</span></span>

<span data-ttu-id="c75fa-115">Если член **lParam** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) указывает на память, выделенную приложением, вы можете освободить его при получении \_ кода уведомления ТВН DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="c75fa-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75fa-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c75fa-116">Requirements</span></span>



| <span data-ttu-id="c75fa-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c75fa-117">Requirement</span></span> | <span data-ttu-id="c75fa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c75fa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c75fa-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c75fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c75fa-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c75fa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c75fa-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c75fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c75fa-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c75fa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c75fa-123">Header</span><span class="sxs-lookup"><span data-stu-id="c75fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75fa-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c75fa-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c75fa-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c75fa-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c75fa-126">**ТВН \_ ДЕЛЕТЕИТЕМВ** (Юникод) и **ТВН \_ делетеитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c75fa-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 





