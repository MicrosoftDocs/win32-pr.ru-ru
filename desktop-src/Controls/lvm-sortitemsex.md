---
title: Сообщение LVM_SORTITEMSEX (Коммктрл. h)
description: Использует определяемую приложением функцию сравнения для сортировки элементов элемента управления "представление списка". Индекс каждого элемента изменяется в соответствии с новой последовательностью. Это сообщение можно отправить явно или с помощью \_ макроса Сортитемсекс ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Элементы управления Windows для LVM_SORTITEMSEX сообщений
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071191"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="9c3e4-106">\_Сообщение LVM сортитемсекс</span><span class="sxs-lookup"><span data-stu-id="9c3e4-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="9c3e4-107">Использует определяемую приложением функцию сравнения для сортировки элементов элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="9c3e4-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="9c3e4-108">Индекс каждого элемента изменяется в соответствии с новой последовательностью.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="9c3e4-109">Это сообщение можно отправить явно или с помощью макроса [**\_ сортитемсекс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .</span><span class="sxs-lookup"><span data-stu-id="9c3e4-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c3e4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c3e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c3e4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c3e4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c3e4-112">Определяемое приложением значение, которое передается в функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="9c3e4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c3e4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c3e4-114">Указатель на определяемую приложением функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="9c3e4-115">Он вызывается во время операции сортировки каждый раз, когда необходимо сравнить относительный порядок двух элементов списка.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c3e4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c3e4-116">Return value</span></span>

<span data-ttu-id="9c3e4-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c3e4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c3e4-118">Remarks</span></span>

<span data-ttu-id="9c3e4-119">Функция сравнения имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="9c3e4-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="9c3e4-120">Это сообщение похоже на [**LVM \_ сортитемс**](lvm-sortitems.md), за исключением типа данных, передаваемых в функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="9c3e4-121">При использовании **LVM \_ сортитемсекс** *lParam1* является текущим индексом первого элемента, а *lParam2* — текущим индексом второго элемента.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="9c3e4-122">Вы можете отправить сообщение [**LVM \_ жетитемтекст**](lvm-getitemtext.md) , чтобы получить дополнительные сведения об элементе, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="9c3e4-123">Функция сравнения должна возвращать отрицательное значение, если первый элемент должен предшествовать второму, положительное значение, если первый элемент должен следовать за вторым, или нуль, если два элемента эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="9c3e4-124">В процессе сортировки содержимое представления списка нестабильно.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="9c3e4-125">Если функция обратного вызова отправляет все сообщения в элемент управления "список", не считая [**LVM \_**](lvm-getitem.md) -Item ([**ListView- \_ элемент**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), результаты могут оказаться непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="9c3e4-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c3e4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9c3e4-126">Requirements</span></span>



| <span data-ttu-id="9c3e4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9c3e4-127">Requirement</span></span> | <span data-ttu-id="9c3e4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9c3e4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c3e4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c3e4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9c3e4-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c3e4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c3e4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c3e4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9c3e4-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c3e4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c3e4-133">Header</span><span class="sxs-lookup"><span data-stu-id="9c3e4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c3e4-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c3e4-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





