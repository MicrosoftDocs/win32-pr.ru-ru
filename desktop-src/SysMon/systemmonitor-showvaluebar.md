---
title: Системмонитор. Шоввалуебар, свойство
description: Возвращает или задает значение, определяющее, отображается ли в элементе управления Строка значений (набор статистических значений ниже диаграммы).
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Сисмон свойство Шоввалуебар
- Шоввалуебар Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Шоввалуебар
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801618"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="e8949-106">Системмонитор. Шоввалуебар, свойство</span><span class="sxs-lookup"><span data-stu-id="e8949-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="e8949-107">Возвращает или задает значение, определяющее, отображается ли в элементе управления Строка значений (набор статистических значений ниже диаграммы).</span><span class="sxs-lookup"><span data-stu-id="e8949-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="e8949-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e8949-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8949-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8949-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e8949-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e8949-110">Property value</span></span>

<span data-ttu-id="e8949-111">Значение true указывает, что панель значений отображается в элементе управления; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="e8949-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="e8949-112">Значение этого свойства по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="e8949-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8949-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8949-113">Remarks</span></span>

<span data-ttu-id="e8949-114">Отображаемая статистика включает Последнее значение, среднее значение и минимальное и максимальное значения текущего выбранного счетчика за отображаемый интервал времени.</span><span class="sxs-lookup"><span data-stu-id="e8949-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="e8949-115">Чтобы выбрать отображаемые значения счетчика, пользователь должен выбрать счетчик на панели условных обозначений элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e8949-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8949-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e8949-116">Requirements</span></span>



| <span data-ttu-id="e8949-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e8949-117">Requirement</span></span> | <span data-ttu-id="e8949-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e8949-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8949-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8949-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8949-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8949-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e8949-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8949-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8949-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8949-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8949-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e8949-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8949-124"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e8949-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8949-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8949-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8949-126">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="e8949-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





