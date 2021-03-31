---
title: Код уведомления LVN_BEGINRDRAG (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что инициируется операция перетаскивания, включающая правую кнопку мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988236"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="eb02d-105">\_Код уведомления ЛВН бегинрдраг</span><span class="sxs-lookup"><span data-stu-id="eb02d-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="eb02d-106">Сообщает родительскому окну элемента управления "представление списка", что инициируется операция перетаскивания, включающая правую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="eb02d-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="eb02d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eb02d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="eb02d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb02d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb02d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb02d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb02d-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="eb02d-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="eb02d-111">Элемент **Член iItem** определяет перетаскиваемый элемент, а остальные элементы равны нулю.</span><span class="sxs-lookup"><span data-stu-id="eb02d-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb02d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb02d-112">Return value</span></span>

<span data-ttu-id="eb02d-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="eb02d-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb02d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="eb02d-114">Requirements</span></span>



| <span data-ttu-id="eb02d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="eb02d-115">Requirement</span></span> | <span data-ttu-id="eb02d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="eb02d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb02d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb02d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb02d-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb02d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb02d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb02d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb02d-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb02d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb02d-121">Header</span><span class="sxs-lookup"><span data-stu-id="eb02d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb02d-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb02d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





