---
title: Сообщение LVM_SORTITEMS (Коммктрл. h)
description: Использует определяемую приложением функцию сравнения для сортировки элементов элемента управления "представление списка". Индекс каждого элемента изменяется в соответствии с новой последовательностью. Это сообщение можно отправить явно или с помощью \_ макроса Сортитемс ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- Элементы управления Windows для LVM_SORTITEMS сообщений
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989452"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="8a3c6-106">\_Сообщение LVM сортитемс</span><span class="sxs-lookup"><span data-stu-id="8a3c6-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="8a3c6-107">Использует определяемую приложением функцию сравнения для сортировки элементов элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="8a3c6-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="8a3c6-108">Индекс каждого элемента изменяется в соответствии с новой последовательностью.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="8a3c6-109">Это сообщение можно отправить явно или с помощью макроса [**\_ сортитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .</span><span class="sxs-lookup"><span data-stu-id="8a3c6-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a3c6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a3c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a3c6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a3c6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a3c6-112">Определяемое приложением значение, которое передается в функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="8a3c6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a3c6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a3c6-114">Указатель на определяемую приложением функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="8a3c6-115">Функция сравнения вызывается во время операции сортировки каждый раз, когда необходимо сравнить относительный порядок двух элементов списка.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a3c6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a3c6-116">Return value</span></span>

<span data-ttu-id="8a3c6-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3c6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a3c6-118">Remarks</span></span>

<span data-ttu-id="8a3c6-119">Функция сравнения имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="8a3c6-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="8a3c6-120">Параметр *lParam1* — это значение, связанное с первым сравниваемым элементом, а параметр *lParam2* — значение, связанное со вторым элементом.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="8a3c6-121">Это значения, указанные в элементе **lParam** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) элементов, когда они вставляются в список.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="8a3c6-122">Параметр *wParam* [**\_ сортитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)передается в функцию обратного вызова в качестве третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="8a3c6-123">Функция сравнения должна возвращать отрицательное значение, если первый элемент должен предшествовать второму, положительное значение, если первый элемент должен следовать за вторым, или нуль, если два элемента эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="8a3c6-124">В процессе сортировки содержимое представления списка нестабильно.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="8a3c6-125">Если функция обратного вызова отправляет все сообщения в элемент управления "список", не считая [**LVM \_**](lvm-getitem.md) -Item ([**ListView- \_ элемент**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), результаты могут оказаться непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="8a3c6-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a3c6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8a3c6-126">Requirements</span></span>



| <span data-ttu-id="8a3c6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8a3c6-127">Requirement</span></span> | <span data-ttu-id="8a3c6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3c6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3c6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a3c6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a3c6-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a3c6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a3c6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a3c6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a3c6-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a3c6-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a3c6-133">Header</span><span class="sxs-lookup"><span data-stu-id="8a3c6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a3c6-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a3c6-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





