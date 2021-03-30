---
title: Код уведомления LVN_COLUMNCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что был нажат заголовок столбца, пока элемент управления "представление списка" находился в режиме отчета. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071186"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="baa61-105">\_Код уведомления ЛВН колумнкликк</span><span class="sxs-lookup"><span data-stu-id="baa61-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="baa61-106">Сообщает родительскому окну элемента управления "представление списка", что был нажат заголовок столбца, пока элемент управления "представление списка" находился в режиме отчета.</span><span class="sxs-lookup"><span data-stu-id="baa61-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="baa61-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="baa61-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="baa61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="baa61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baa61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baa61-110">Указатель на структуру [**нмлиствиев**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="baa61-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="baa61-111">Элемент **Член iItem** имеет значение-1, а член **iSubItem** определяет столбец.</span><span class="sxs-lookup"><span data-stu-id="baa61-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="baa61-112">Все остальные члены равны нулю.</span><span class="sxs-lookup"><span data-stu-id="baa61-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa61-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="baa61-113">Return value</span></span>

<span data-ttu-id="baa61-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="baa61-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa61-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="baa61-115">Remarks</span></span>

<span data-ttu-id="baa61-116">Использование форматов элементов управления заголовков, таких как ХДФ, \_ для изменения формата заголовков столбцов в элементе управления "представление списка" приводит к тому, что элемент управления отправляет код уведомления [ \_ итемстатеиконкликк ХДН](hdn-itemstateiconclick.md) , а не ЛВН \_ колумнкликк при щелчке элемента заголовка.</span><span class="sxs-lookup"><span data-stu-id="baa61-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa61-117">Требования</span><span class="sxs-lookup"><span data-stu-id="baa61-117">Requirements</span></span>



| <span data-ttu-id="baa61-118">Требование</span><span class="sxs-lookup"><span data-stu-id="baa61-118">Requirement</span></span> | <span data-ttu-id="baa61-119">Значение</span><span class="sxs-lookup"><span data-stu-id="baa61-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baa61-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="baa61-120">Minimum supported client</span></span><br/> | <span data-ttu-id="baa61-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baa61-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baa61-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="baa61-122">Minimum supported server</span></span><br/> | <span data-ttu-id="baa61-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="baa61-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="baa61-124">Header</span><span class="sxs-lookup"><span data-stu-id="baa61-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa61-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="baa61-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





