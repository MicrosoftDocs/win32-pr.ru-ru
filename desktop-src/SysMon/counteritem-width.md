---
title: Каунтеритем. Width, свойство
description: Возвращает или задает толщину линии, используемую для отображения значения счетчика.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Свойство Width Сисмон
- Свойство Width Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, свойство Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802489"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="61786-106">Каунтеритем. Width, свойство</span><span class="sxs-lookup"><span data-stu-id="61786-106">CounterItem.Width property</span></span>

<span data-ttu-id="61786-107">Возвращает или задает толщину линии, используемую для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="61786-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="61786-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="61786-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="61786-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61786-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="61786-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="61786-110">Property value</span></span>

<span data-ttu-id="61786-111">Толщина линии, используемой в линейном графике.</span><span class="sxs-lookup"><span data-stu-id="61786-111">Line width used in a line graph.</span></span> <span data-ttu-id="61786-112">Допустимые значения находятся в диапазоне от 1 до 3, где 1 (значение по умолчанию) является самой короткой шириной.</span><span class="sxs-lookup"><span data-stu-id="61786-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="61786-113">**До Windows Vista:** Допустимы значения в диапазоне от 1 до 9.</span><span class="sxs-lookup"><span data-stu-id="61786-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="61786-114">Если приложение будет выполняться в Windows Vista, не используйте значение ширины больше 3.</span><span class="sxs-lookup"><span data-stu-id="61786-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="61786-115">Исключения</span><span class="sxs-lookup"><span data-stu-id="61786-115">Exceptions</span></span>



| <span data-ttu-id="61786-116">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="61786-116">Exception type</span></span>               | <span data-ttu-id="61786-117">Условие</span><span class="sxs-lookup"><span data-stu-id="61786-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="61786-118">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="61786-118">**System.ArgumentException**</span></span> | <span data-ttu-id="61786-119">Указана недопустимая толщина линии.</span><span class="sxs-lookup"><span data-stu-id="61786-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="61786-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61786-120">Remarks</span></span>

<span data-ttu-id="61786-121">Ширина линии по умолчанию для первых 16 добавляемых счетчиков — 1.</span><span class="sxs-lookup"><span data-stu-id="61786-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="61786-122">Ширина линии по умолчанию для следующих 16 счетчиков (счетчиков 17-32), которые вы добавили, равна 2.</span><span class="sxs-lookup"><span data-stu-id="61786-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="61786-123">Ширина линии по умолчанию для следующих 16 счетчиков (счетчики 33 – 48), которые вы добавили, равна 3.</span><span class="sxs-lookup"><span data-stu-id="61786-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="61786-124">После этого СИСМОН случайным образом выбирает толщину линии.</span><span class="sxs-lookup"><span data-stu-id="61786-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="61786-125">Дополнительные сведения см. в разделе [**каунтеритем. Color**](counteritem-color.md).</span><span class="sxs-lookup"><span data-stu-id="61786-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="61786-126">Чтобы задать [**стиль линии**](counteritem-linestyle.md) , отличный от сплошной, ширина должна быть равна 1.</span><span class="sxs-lookup"><span data-stu-id="61786-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="61786-127">Если указать значение больше 1 и указать несплошной стиль линии, СИСМОН игнорирует указанную толщину линии.</span><span class="sxs-lookup"><span data-stu-id="61786-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="61786-128">Требования</span><span class="sxs-lookup"><span data-stu-id="61786-128">Requirements</span></span>



| <span data-ttu-id="61786-129">Требование</span><span class="sxs-lookup"><span data-stu-id="61786-129">Requirement</span></span> | <span data-ttu-id="61786-130">Значение</span><span class="sxs-lookup"><span data-stu-id="61786-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61786-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61786-131">Minimum supported client</span></span><br/> | <span data-ttu-id="61786-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61786-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="61786-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61786-133">Minimum supported server</span></span><br/> | <span data-ttu-id="61786-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61786-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61786-135">DLL</span><span class="sxs-lookup"><span data-stu-id="61786-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61786-136"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="61786-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61786-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61786-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61786-138">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="61786-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





