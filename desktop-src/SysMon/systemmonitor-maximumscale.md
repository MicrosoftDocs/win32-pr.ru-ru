---
title: Системмонитор. Максимумскале, свойство
description: Возвращает или задает максимальное значение вертикальной оси (Y) диаграммы.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Сисмон свойство Максимумскале
- Максимумскале Property Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Максимумскале
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988522"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="4a041-106">Системмонитор. Максимумскале, свойство</span><span class="sxs-lookup"><span data-stu-id="4a041-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="4a041-107">Возвращает или задает максимальное значение вертикальной оси (Y) диаграммы.</span><span class="sxs-lookup"><span data-stu-id="4a041-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="4a041-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a041-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a041-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a041-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="4a041-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4a041-110">Property value</span></span>

<span data-ttu-id="4a041-111">Положительное максимальное значение вертикальной оси графа.</span><span class="sxs-lookup"><span data-stu-id="4a041-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="4a041-112">По умолчанию максимальное значение вертикального масштаба равно 100.</span><span class="sxs-lookup"><span data-stu-id="4a041-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="4a041-113">Наименьшее значение, для которого можно задать максимальное значение, — это значение, которое больше значения [**минимумскале**](systemmonitor-minimumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="4a041-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="4a041-114">Наибольшее значение, которое можно задать для максимального значения, равно 999 999 999.</span><span class="sxs-lookup"><span data-stu-id="4a041-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a041-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a041-115">Remarks</span></span>

<span data-ttu-id="4a041-116">Элемент управления автоматически корректирует расположение чисел шкалы, отображаемых на вертикальном масштабировании, в соответствии с размером отображаемого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4a041-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a041-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4a041-117">Requirements</span></span>



| <span data-ttu-id="4a041-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4a041-118">Requirement</span></span> | <span data-ttu-id="4a041-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4a041-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a041-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a041-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a041-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a041-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4a041-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a041-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a041-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a041-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a041-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4a041-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a041-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4a041-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a041-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a041-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a041-127">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="4a041-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="4a041-128">**Системмонитор. Минимумскале**</span><span class="sxs-lookup"><span data-stu-id="4a041-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="4a041-129">**Системмонитор. Шовскалелабелс**</span><span class="sxs-lookup"><span data-stu-id="4a041-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





