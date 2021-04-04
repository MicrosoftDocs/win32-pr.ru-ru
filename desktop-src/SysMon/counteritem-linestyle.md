---
title: Каунтеритем. Линестиле, свойство
description: Возвращает или задает стиль линии, используемый для отображения значения счетчика.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Сисмон свойство Линестиле
- Линестиле Property Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, свойство Линестиле
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988616"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="677a3-106">Каунтеритем. Линестиле, свойство</span><span class="sxs-lookup"><span data-stu-id="677a3-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="677a3-107">Возвращает или задает стиль линии, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="677a3-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="677a3-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="677a3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="677a3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="677a3-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="677a3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="677a3-110">Property value</span></span>

<span data-ttu-id="677a3-111">Стиль линии, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="677a3-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="677a3-112">Значения соответствуют системным константам, приведенным в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="677a3-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="677a3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="677a3-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="677a3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="677a3-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="677a3-115"><dt>**System. Drawing. Drawing2D. DashStyle. твердое**</dt> значение <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="677a3-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="677a3-116">Сплошная линия.</span><span class="sxs-lookup"><span data-stu-id="677a3-116">Solid line.</span></span> <span data-ttu-id="677a3-117">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="677a3-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="677a3-118"><dt>**System. Drawing. Drawing2D. DashStyle. тире**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="677a3-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="677a3-119">Пунктирная линия с длинными сегментами и узкими пробелами.</span><span class="sxs-lookup"><span data-stu-id="677a3-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="677a3-120"><dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="677a3-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="677a3-121">Пунктирная линия с равномерными сегментами и пробелами.</span><span class="sxs-lookup"><span data-stu-id="677a3-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="677a3-122"><dt>**System. Drawing. Drawing2D. DashStyle. дашдот**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="677a3-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="677a3-123">Пунктирная линия с чередованием коротких и длинных сегментов.</span><span class="sxs-lookup"><span data-stu-id="677a3-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="677a3-124"><dt>**System. Drawing. Drawing2D. DashStyle. дашдотдот**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="677a3-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="677a3-125">Пунктирная линия с чередованием штрихов и двойными точками.</span><span class="sxs-lookup"><span data-stu-id="677a3-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="677a3-126">Исключения</span><span class="sxs-lookup"><span data-stu-id="677a3-126">Exceptions</span></span>



| <span data-ttu-id="677a3-127">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="677a3-127">Exception type</span></span>               | <span data-ttu-id="677a3-128">Условие</span><span class="sxs-lookup"><span data-stu-id="677a3-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="677a3-129">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="677a3-129">**System.ArgumentException**</span></span> | <span data-ttu-id="677a3-130">Указан недопустимый стиль линии.</span><span class="sxs-lookup"><span data-stu-id="677a3-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="677a3-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="677a3-131">Remarks</span></span>

<span data-ttu-id="677a3-132">Чтобы указать значение, отличное от DashStyle. сплошной, [**каунтеритем. Width**](counteritem-width.md) должно иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="677a3-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="677a3-133">Если ширина больше 1, СИСМОН игнорирует указанный стиль линии и использует DashStyle. сплошной.</span><span class="sxs-lookup"><span data-stu-id="677a3-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="677a3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="677a3-134">Requirements</span></span>



| <span data-ttu-id="677a3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="677a3-135">Requirement</span></span> | <span data-ttu-id="677a3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="677a3-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="677a3-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="677a3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="677a3-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="677a3-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="677a3-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="677a3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="677a3-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="677a3-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="677a3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="677a3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="677a3-142"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="677a3-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677a3-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="677a3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677a3-144">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="677a3-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





