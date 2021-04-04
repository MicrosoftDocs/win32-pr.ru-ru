---
title: Каунтеритем. Color, свойство
description: Возвращает или задает цвет, используемый для отображения значения счетчика.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Свойство Color Сисмон
- Свойство Color Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, свойство Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802590"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="3a8fa-106">Каунтеритем. Color, свойство</span><span class="sxs-lookup"><span data-stu-id="3a8fa-106">CounterItem.Color property</span></span>

<span data-ttu-id="3a8fa-107">Возвращает или задает цвет, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="3a8fa-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8fa-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a8fa-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="3a8fa-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a8fa-110">Property value</span></span>

<span data-ttu-id="3a8fa-111">Цвет, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a8fa-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a8fa-112">Remarks</span></span>

<span data-ttu-id="3a8fa-113">Если не указать используемый цвет, СИСМОН выбирает цвета для первых шестнадцати счетчиков.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="3a8fa-114">Если указать более шестнадцати счетчиков, СИСМОН будет использовать те же цвета, что и первые шестнадцати счетчиков.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="3a8fa-115">Чтобы отличать счетчики друг от друга, СИСМОН изменяет [**стиль линии**](counteritem-linestyle.md) , используемый для каждой кратности 16 счетчиков до первых счетчиков 80.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="3a8fa-116">Например, первые шестнадцати счетчиков используют сплошной стиль линии, следующие шестнадцать используют тип штриховой линии и т. д.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="3a8fa-117">Затем СИСМОН устанавливает [**толщину линии**](counteritem-width.md) равным 2 для счетчиков 81-96 и 3 для счетчиков 96-112.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="3a8fa-118">Если коллекция содержит более 112 счетчиков, счетчики будут содержать одинаковые значения цвета, стиля линии и ширины.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="3a8fa-119">**До Windows Vista:** Если не указать используемый цвет, СИСМОН выбирает цвета для первых шестнадцати счетчиков.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="3a8fa-120">Если указать более шестнадцати счетчиков, СИСМОН будет использовать те же цвета, что и первые шестнадцати счетчиков.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="3a8fa-121">Чтобы отличать счетчики друг от друга, СИСМОН увеличивает [**ширину линии**](counteritem-width.md) первых трех счетчиков, которые получают одно и то же назначение цвета.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="3a8fa-122">Если более трех счетчиков используют один и тот же цвет, СИСМОН случайным образом выбирает толщину линии, используемую для счетчика.</span><span class="sxs-lookup"><span data-stu-id="3a8fa-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8fa-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3a8fa-123">Requirements</span></span>



| <span data-ttu-id="3a8fa-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3a8fa-124">Requirement</span></span> | <span data-ttu-id="3a8fa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3a8fa-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8fa-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a8fa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3a8fa-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3a8fa-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3a8fa-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a8fa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3a8fa-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3a8fa-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a8fa-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3a8fa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a8fa-131"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3a8fa-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a8fa-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a8fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8fa-133">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="3a8fa-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





