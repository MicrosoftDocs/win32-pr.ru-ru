---
title: Код уведомления TBN_DRAGOVER (Коммктрл. h)
description: Определяет, \_ следует ли отправлять маркбуттон-ТБ сообщение для кнопки, для которой выполняется перетаскивание. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489795"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="9dd69-105">\_Код уведомления ТБН DRAGOVER</span><span class="sxs-lookup"><span data-stu-id="9dd69-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="9dd69-106">Определяет, следует ли [**отправлять \_ Маркбуттон-ТБ**](tb-markbutton.md) сообщение для кнопки, для которой выполняется перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="9dd69-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="9dd69-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9dd69-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9dd69-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dd69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd69-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9dd69-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9dd69-110">Указатель на структуру [**нмтбхотитем**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) , указывающую, к какому элементу выполняется перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="9dd69-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd69-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dd69-111">Return value</span></span>

<span data-ttu-id="9dd69-112">**Значение false** , если панель инструментов должна отправить \_ сообщение маркбуттон ТБ; в противном случае — **значение true**.</span><span class="sxs-lookup"><span data-stu-id="9dd69-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd69-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9dd69-113">Requirements</span></span>



| <span data-ttu-id="9dd69-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9dd69-114">Requirement</span></span> | <span data-ttu-id="9dd69-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9dd69-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd69-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9dd69-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd69-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9dd69-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9dd69-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9dd69-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd69-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9dd69-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9dd69-120">Header</span><span class="sxs-lookup"><span data-stu-id="9dd69-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dd69-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd69-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





